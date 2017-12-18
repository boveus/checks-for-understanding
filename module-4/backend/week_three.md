## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?
  - Node is an interpreter that is used to run Javascript code on a server.
2. What is Express? What is Express similar to in the Ruby world?
  - Express is middleware, and it is similar to rack in the Ruby world.
3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.
  ```javascript
  let knex = require('./config');
  let express = require('express')

  app.get('/', function (req, res) {
    database.raw('SELECT * FROM foods).then(
      let someSqlQuery = data.rows
    ).catch(
      return "there was an error"
     )
    res.send(someSqlQuery)
  })
  ```
4. What do we use Knex for?
  Knex is used as an ORM to simplify SQL queries within an express application.  
5. How **could** you organize your code to follow the MVC design pattern in your Quantified Self project?
  You can create models and a controller.  The controller would handle the incoming web requests, while the models would handle operations such as quering a model's data tables.
6. How do you execute raw SQL in node?
  Knex supports raw sql queries with the .raw method that you can pass a raw SQL query to.
7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?
  An advantage to having them live in seperate applications is to have, at a high level, a clear seperation of responsibilities within your code.  It also allows work to be done concurrently by two or more developers since the two components are unrelated.  
  A disadvantage is that there may be a disconnect between what the backened is doing and what the front end is doing and what decisions are made on each application.  A good example is to consider what type of data is returned from an API.  This data can be reformatted on either the front end side or the back end side, but if a developer is working on the front end, it may be tempting to change the front end behavior to reformat the data instead of change the back end behavior to serve the data in the correct format in the frist place.

#### Review  

8. Describe DNS.
  DNS is used to resolve a host name to an IP address so that a client machine can send HTTP requests to a server.
9. What does writing clean code mean to you?
  Clean code code that follows the principles of good software design such as the single responsibility principle, the do not repeat yourself principle, and the law of demeter.  The primary consideration of what makes code clean is the ability to add to the code and the ability of other people to read and understand your code.
10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality? Hint: think about what tables you would need in the database, how those records would relate to each other, and good OOP.
  I think I would have the following classes:
    Room - The room object would belong to a guest (if this is an AR association) 
    Guest - These would be the people checking in to the hotel and paying money to stay there.
    Staff - These would have a few different classes that inherit from it such as receptionist, manager, maid etc. that have their own responsibilities, but the overall responsibility of the staff class would be to handle payments from the guest and to provide services to the guest such as responding to complaints, cleaning their room etc.
    
