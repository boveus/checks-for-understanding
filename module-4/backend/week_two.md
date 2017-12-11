## Week Two - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. What's one difference between ES5 and ES6?
  - One key difference is the keyword for variable declaration.  ES5 uses 'var', while ES6 uses 'let'.
2. What's the difference between asynchronous and synchronous JavaScript? 
  - Synchronous JS executes at a predictable time, while Aynch JS requires the use of a promise to catch when the operation completes.
3. What are the four pillars of Object Oriented programming?
  - Encapsulation
  - Inheritance 
  - Abstraction
  - Polymorphism
4. What are some tools available in JavaScript to help you write object oriented code?
  - In ES6 you can use classes with constructors that behave similarly to ruby objects.  
5. What are some key concepts to be aware of when refactoring your JavaScript?
  - A specific concept that helped us refactor our JS was that having seperate functions that did AJAX calls that returned the AJAX call helped make the code a lot more readable when dealing with promises.  Making an AJAX call and dealing with a promises immediately lead to some very verbose code.
6. What's a callback function and what are some reasons when we use/need callback functions?
  - Callback functions are used when passing a function as an argument to another function.  This is often used in event listeners.  A common pattern is to pass a function as one of the arguments and the target to be listened on (a css selector) as a second argument. 
7. What are the different scopes of variables in Javascript? When would you want to define global variables?
  - A variable can be scoped locally (within a function) or globally (outside of functions).  I tend to think of global variables as ones that will either be set once at the beginning of the code's execution and remain immutable.  Typically, I would define these as a constant.  A local variable may change a few times before the code execution completes within a function.
8. What's the difference between `==` and `===` in JavaScript?
  - '==' is loose equality and '===' is strong equality.  I have yet to find a use-case for loose equality, and it seems like it could result in some unpredictable behavior.
9. Why do front end frameworks exist?
  - Front end frameworks exist to simplify common programming patterns that are used repeatedly in vanilla JS.  A good example is jQuery - it is used to simplify selecting HTML elements and performing DOM manipulation.  What would take tens to hundreds of lines in vanilla JS can be done much more simply using jQuery.

#### Review  

10. Why do people say "HTTP is stateless"?
  - HTTP is used to communicate between a client and a server machine.  Neither the client or the server will hold any sort of state regarding the request through HTTP.  They will only send and receive requests, but not hold a state about the request.
11. Describe a RESTful API.
  - A RESTful API is used to hold the state of the client requests because HTTP is not capable of doing this by default.  This is done through create, read, update, and delete requests being sent through the client and will typically involve making a corresponding request to a database after the HTTP server receives the request.  The 
12. What are some main characteristics of a team following an agile workflow?
  - Short planning stages followed by (relatively) short execution stages called sprints.  This is done to allow the development cycle to be more responsive to change.
13. What are some advantages **and** disadvantages to using OAuth to authenticate a user?
  - The main advantage is that you are able to outsource the handling of user passwords and authentications to a third party to authenticate users within an application.  A disadvantage is that if the OAuth provider goes offline, it can affect your site.  It also makes providing granular permissions to users (such as admin access) a bit harder to implement.
