
Iterate names of all properties and methods of an object instance in Python:

```
>>> for i in dir(fred):
	print i

	
__class__
__delattr__
__dict__
__doc__
__format__
__getattribute__
__hash__
__init__
__module__
__new__
__reduce__
__reduce_ex__
__repr__
__setattr__
__sizeof__
__str__
__subclasshook__
__weakref__
name
perm
>>>
```

How you actually get the values of each of those:

```Python
>>> for i in dir(fred):
	print i, fred.__getattribute__(i)

	
__class__ <class '__main__.Object'>
__delattr__ <method-wrapper '__delattr__' of Object object at 0x10545ff90>
__dict__ {'name': 'Fred', 'perm': 12345}
__doc__ None
__format__ <built-in method __format__ of Object object at 0x10545ff90>
__getattribute__ <method-wrapper '__getattribute__' of Object object at 0x10545ff90>
__hash__ <method-wrapper '__hash__' of Object object at 0x10545ff90>
__init__ <method-wrapper '__init__' of Object object at 0x10545ff90>
__module__ __main__
__new__ <built-in method __new__ of type object at 0x100186aa0>
__reduce__ <built-in method __reduce__ of Object object at 0x10545ff90>
__reduce_ex__ <built-in method __reduce_ex__ of Object object at 0x10545ff90>
__repr__ <method-wrapper '__repr__' of Object object at 0x10545ff90>
__setattr__ <method-wrapper '__setattr__' of Object object at 0x10545ff90>
__sizeof__ <built-in method __sizeof__ of Object object at 0x10545ff90>
__str__ <method-wrapper '__str__' of Object object at 0x10545ff90>
__subclasshook__ <built-in method __subclasshook__ of type object at 0x10071cba0>
__weakref__ None
name Fred
perm 12345
>>> 
```
