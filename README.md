Pojo Explorer (Plain Old Java Object Explorer)
============

This class is for graphically exploring objects by calling their "get" and "is" methods that can't be seen during regular eclipse debugging. This is designed for understanding code by looking at the methods that they offer.

Some objects have their values as fields. These fields can be seen from inside the eclipse debugger. But if a get method looks up it's value in a database or analyzes files these values can't be seen during normal debugging. Pojo Explorer can let you quickly inspect the results of these getters without rerunning the program!

One thing to be aware of is that this type of examination is that these get functions can have side effects. This is most likely is the reason why it's not built into eclipse.

This is designed to be simple to insert into your code. All you do is instantiate a new PojoExplorer with the object you want to look at like this:

```
new PojoExplorer(object);
```
 
Most of the time you will want to pause the current thread so that the value isn't changed. This class has a function for that:

```
PojoExplorer.pausethread();
```
 
The point is to get this screen to explore an object. This is a view of a JFrame object


![screenshot](https://raw.githubusercontent.com/ieee8023/pojoexplorer/master/complex-objects.png)
