# CS20-S16-Lecture-05.19-NamedTuples-Objects
Named Tuples, Objects, Jython Environment for Music


# Named Tuples

https://foo.cs.ucsb.edu/8wiki/index.php/Python:_Named_Tuples


# Objects

Some strange Python code.  This is the smallest Python class ever.

It gives you maximum flexibility, but may be confusing to work with

```Python
class Object(object):
   pass
   
```   

```Python
>>> fred = Object()
>>> fred.name = "Fred"
>>> fred.perm = 12345
>>> fred
<__main__.Object object at 0x10545ff90>
>>> fred.perm
12345
>>> fred.name
'Fred'
>>>
```

More on this crazy way of making a "class" here:  [MonkeyPatchedObjects.md](MonkeyPatchedObjects.md)

What is more commonly done is something like this. (Note: this link requires you to login with your UCSB ECI/CSIL username/password, since this is copyrighted code.)

https://github.ucsb.edu/pconrad/guttag-python-code/blob/master/codeForWebSite/Chapter%208/code.py#L48

Here, under fair use, is just the one example from p. 97 of Guttag:


```Python
import datetime

class Person(object):

    def __init__(self, name):
        """Create a person"""
        self.name = name
        try:
            lastBlank = name.rindex(' ')
            self.lastName = name[lastBlank+1:]
        except:
            self.lastName = name
        self.birthday = None
 
    def getName(self):
        """Returns self's full name"""
        return self.name

    def getLastName(self):
        """Returns self's last name"""
        return self.lastName

    def setBirthday(self, birthdate):
        """Assumes birthdate is of type datetime.date
           Sets self's birthday to birthdate"""
        self.birthday = birthdate

    def getAge(self):
        """Returns self's current age in days"""
        if self.birthday == None:
            raise ValueError
        return (datetime.date.today() - self.birthday).days

    def __lt__(self, other):
        """Returns True if self's name is lexicographically
           less than other's name, and False otherwise"""
        if self.lastName == other.lastName:
            return self.name < other.name
        return self.lastName < other.lastName

    def __str__(self):
        """Returns self's name"""
        return self.name
```


