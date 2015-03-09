#### Deliverables for week 5 Rails MVC
##### Odin Project Routing Guide Questions:
- What is the "Root" route?<br\>The "Root" route is an instruction inside the 'config/routes.rb' file which lets Rails know how and where to set up the application when it is used. It typically takes the form of a URL (Uniform Rersource Locator) that specifies a controller and action for Rails to map the route to. The 'root' route is the simplest and most important route in the 'routes.rb' file because it defines a starting point for the application once it is in use.<br\><br\>
- What are the seven RESTful routes for a resource?<br\>The seven RESTful routes for a resource are (i) GET all the posts ("index" the posts); (ii) GET just one specific post ("show" one specific post); (iii) GET the page to create a new post (view the "new" post page); (iv) POST inputted data back to the server ("create" the post); (v) GET the page to edit an existing post (view the "edit" post page); (vi) PUT the inputted edit data back to the server so it can be updated ("update" the post); and (vii) DELETE a specific post ("destroy" the post).<br\><br\>
- Which RESTful routes share the same URL but use different verbs?<br\>There are only four different URL's for the seven RESTful routes ('GET', 'POST', 'PUT', and 'DELETE'). Of these four, 'GET' is implemented using four different verbs: "index"; "show"; "new"; and "edit". From my answer to Question 2, we see that these correspond to RESTFUL routes (i), (ii), (iii), and (v), respectively. Thus, GET->"index" corresponds to retrieving all the posts; GET->"show" corresponds to retrieving a single post; GET->"new" corresponds to creating a new post; and GET ->"edit" corresponds to editing an existing post.<br\><br\>
- How do you specify an ID or other variable in a route?<br\>To specify an ID or other variable in a route, we add a colon before it (i.e, ':id' specifies an ID and ':except' specifies the except variable).<br\><br\>
- How can you easily write all seven RESTful routes in Rails?<br\>Rather than writing out all seven RESTful routes individually, we can write all seven of them in the 'routes.rb' file using only one line of code: "resources :posts".<br\><br\>
- What is the Rails helper method that creates the HTML for links?<br\>The rails helper method that creates the HTML for links is "link_to". This helper method is truly helpful in that if you later on decide to change the URL, then the 'link_to' method will automatically update the change and it will not be necessary to go through the file and change the link manually (as would be necessary if the URL was hard coded into the file).<br\><br\>

##### Odin Project Views Guide Questions:
- What is a layout?<br\>A layout can be viewed as a 'shell' that is used to help build individual webpages. It contains code that will be common to all of the pages used, such as the docytpe declaration and html tags, in addition to instructions which load the javascript and css files where needed. A layout emphasizes the DRY (Don't Repeat Yourself) mantra used in rails programming, in that since all webpages will need the code presented in the layout file, it can be written once and implemented many times; namely by each individual webpage when needed.<br\><br\>
- What's the difference between a "view template" and a "layout"?<br\>A "view template" is a file that includes specific instructions to create an individual webpage; as such, it incorporates a "layout" which is a file that is common code for all the webpages used in the application. We can consider the "view template" as the specific instructions to build each individual webpage whereas the "layout" contains the generic instructions common to the entire collection of webpages being utilized. While an application will only have one single layout file, it generally will have many view template files.<br\><br\>
- What is a "Preprocessor"?
- Why are preprocessors useful?
- How do you make sure a preprocessor runs on your file?
- What's the outputted filetype of a preprocessed *.html.erb file? What about a *.css.scss file?
- What is the difference between the <%= and <% tags?
- What is a view partial?
- How do you insert a partial into your view?
- How can you tell that a view file is a partial?
- How do you pass a local variable to a partial?
- What's the magical Rails shortcut for rendering a User? A bunch of Users?
- What are asset tags and why are they used?

##### Link to Odin Project Basic Routes, Views and Controllers repo: [my odin repo](<linkhere>)
##### Link to Hartl's Rails Tutorial Chapter 5 repo: [my hartl's repo](<linkhere>)
