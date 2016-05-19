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

What is more commonly done is something like this:





