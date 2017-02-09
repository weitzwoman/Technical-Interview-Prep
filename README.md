# Technical-Interview-Prep
## Answers to Technical Interview Questions

### Rails Week 1
#### Describe an MVC framework.
Rails follows a model-view-controller pattern. In this pattern, we use models (our classes), views (our pages) and controllers (our routing hub between external requests and internal processes and output) to manage the request-response cycle.

#### How are Ruby and Rails related?
Ruby on Rails, a framework for building web applications with Ruby. Rails is more robust than Sinatra and adheres to strict RESTful routing patterns for our CRUD processes. Rails also employs the Ruby philosophy of "convention over configuration".

#### What is the difference between routes and RESTful routes?
REST stands for Representational State Transfer which is used to design web services around HTTP methods. A good rule of thumb is that for every model in your app, you will have seven RESTful routes that will have seven corresponding controller actions. A Rails route maps a URL and HTTP method to a controller action.

It is best practice at this stage NOT to create custom controller actions outside the seven auto-generated routes. If you are considering a custom controller action, think about exactly what you are trying to accomplish. If you are wanting to show, create, update or destroy data, one of the seven actions should accomplish your task without the need for a custom action. Remember: the work of the controller is as go-between to the model and the view. Logic should always "live" in the model and be accessed by the controller.

#### Why would we want to use migrations to build our database?
Migrations are a convenient way for you to alter your database in a structured and organized manner. You could edit fragments of SQL by hand but you would then be responsible for telling other developers that they need to go and run them. You’d also have to keep track of which changes need to be run against the production machines next time you deploy.

Active Record tracks which migrations have already been run so all you have to do is update your source and run rake db:migrate. Active Record will work out which migrations should be run. It will also update your db/schema.rb file to match the structure of your database.

#### Talk about a project you created recently that you're proud of. What skills does it demonstrate? What challenges did you face during the course of development?

#### What kind of project, application, or website would be best created in the Rails framework?
Ruby on Rails will be suitable for most web startups and common web applications. 

#### What are you looking forward to learning most?

#### What does Object-relational mapping mean?
A programming technique for converting data between incompatible type systems in object-oriented programming languages. This creates, in effect, a "virtual object database" that can be used from within the programming language.

#### What object-relational mapping (ORM) frameworks do you have experience with?
PostgresSQL and MySQL, ActiveRecord

#### How do we render dynamic data in a layout? What occurs to get this data into the layout, and visible to the user?
Call render or redirect_to in a ruby tag in the layout. Rails will automatically render a view with the filename of the controller action. If you are redirecting to a file that does not have the same name as the controller action, you still must use render and then the template name.

#### Describe the appropriate time to generate new database migrations.
A migration is a Ruby file that changes your database... so any time you want to edit/update/delete parts of your database.

#### What is the difference between ActiveRecord's new(), create(), and save() methods?

#### How do we determine whether code belongs in the model or the controller?

#### How does an asset pipeline function? What benefits does it offer?
