I record my *experience and thoughts* here about some interesting points.

## C++

1. *Can I throw an exception from a constructor? From a destructor?*

   * For constructors, yes: You should throw an exception from a constructor whenever you cannot properly initialize (construct) an object. There is no really satisfactory alternative to exiting a constructor by a throw. For more details, see [here](https://isocpp.org/wiki/faq/exceptions#ctors-can-throw).

   * For destructors, not really: You can throw an exception in a destructor, but that exception must not leave the destructor; if a destructor exits by emitting an exception, all kinds of bad things are likely to happen because the basic rules of the standard library and the language itself will be violated. Don’t do it. For more details, see [here](https://isocpp.org/wiki/faq/exceptions#dtors-shouldnt-throw).

     

2. *What kinds of variables should be initialized in initialize list in class?*  

   Please refer [here](https://www.geeksforgeeks.org/when-do-we-use-initializer-list-in-c/).

3. When _**static**_ keyword should be used in class?

   Please refer [here](https://stackoverflow.com/questions/15235526/the-static-keyword-and-its-various-uses-in-c).











