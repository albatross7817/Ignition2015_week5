# Ignition2015_week5
Diving deeper in the MVC aspects of Rails

# Week 5: Rails MVC

#### Required 
A. Read the [Odin Project Routing Guide](http://www.theodinproject.com/ruby-on-rails/routing) and use it to <strong>answer the following questions</strong>:
  1. What is the "Root" route?<br\>The "Root" route is an instruction inside the 'config/routes.rb' file which lets Rails know how and where to set up the application when it is used.  It typically takes the form of a URL (Uniform Rersource Locator) that specifies a controller and action for Rails to map the route to.  The 'root' route is the simplest and most important route in the 'routes.rb' file because it defines a starting point for the application once it is in use.<br\><br\>
  2. What are the seven RESTful routes for a resource?<br\>The seven RESTful routes for a resource are (i) GET all the posts ("index" the posts); (ii) GET just one specific post ("show" one specific post); (iii) GET the page to create a new post (view the "new" post page); (iv) POST inputted data back to the server ("create" the post); (v) GET the page to edit an existing post (view the "edit" post page); (vi) PUT the inputted edit data back to the server so it can be updated ("update" the post); and (vii) DELETE a specific post ("destroy" the post).<br\><br\>
  3. Which RESTful routes share the same URL but use different verbs?<br\>There are only four different URL's for the seven RESTful routes ('GET', 'POST', 'PUT', and 'DELETE').  Of these four, 'GET' is implemented using four different verbs: "index"; "show"; "new"; and "edit".  From my answer to Question 2, we see that these correspond to RESTFUL routes (i), (ii), (iii), and (v), respectively.  Thus, GET->"index" corresponds to retrieving all the posts; GET->"show" corresponds to retrieving a single post; GET->"new" corresponds to creating a new post; and GET ->"edit" corresponds to editing an existing post.<br\><br\>
  4. How do you specify an ID or other variable in a route?<br\>To specify an ID or other variable in a route, we add a colon before it (i.e, ':id' specifies an ID and ':except' specifies the except variable).<br\><br\>
  5. How can you easily write all seven RESTful routes in Rails?<br\>Rather than writing out all seven RESTful routes individually, we can write all seven of them in the 'routes.rb' file using only one line of code: "resources :posts".<br\><br\>
  6. What is the Rails helper method that creates the HTML for links?<br\>The rails helper method that creates the HTML for links is "link_to".  This helper method is truly helpful in that if you later on decide to change the URL, then the 'link_to' method will automatically update the change and it will not be necessary to go through the file and change the link manually (as would be necessary if the URL was hard coded into the file).<br\><br\>
B. Read the [Odin Project Controller Guide](http://www.theodinproject.com/ruby-on-rails/controllers)<br\><br\>
C. Read the [Odin Project Views Guide](http://www.theodinproject.com/ruby-on-rails/views) and use it to <strong>answer the following questions</strong>:<br\><br\>
  7. What is a layout?<br\>A layout can be viewed as a 'shell' that is used to help build individual webpages.  It contains code that will be common to all of the pages used, such as the docytpe declaration and html tags, in addition to instructions which load the javascript and css files where needed.  A layout emphasizes the DRY (Don't Repeat Yourself) mantra used in rails programming, in that since all webpages will need the code presented in the layout file, it can be written once and implemented many times; namely by each individual webpage when needed.<br\><br\>
  8. What's the difference between a "view template" and a "layout"?<br\>A "view template" is a file that includes specific instructions to create an individual webpage; as such, it incorporates a "layout" which is a file that is common code for all the webpages used in the application.  We can consider the "view template" as the specific instructions to build each individual webpage whereas the "layout" contains the generic instructions common to the entire collection of webpages being utilized.  While an application will only have one single layout file, it generally will have many view template files.<br\><br\> 
  9. What is a "Preprocessor"?<br\>A "preprocessor" is an extension added to a file name that provides instructions to the computer about how to interpret the file it is being presented.  Common preprocessors extensions include 'erb', 'scss', and 'coffee'.  These extensions are flags that the file contains embedded code which needs to be interpreted first before the full html file is sent to the server for display.<br\><br\>    
  10. Why are preprocessors useful?<br\>Preprocessors are useful because they allow developers to add dynamic content to an html page; which by the nature of its structure, is static.  The use of preprocessors allows additional code, such as running loops and callling variables, that ordinarily could not be interpreted by a browser as html code.  Preprocessors allow us to include various types of code (i.e., Ruby, SASS, Coffescript) into an html (or css or javascript) file and have it compile in a way such that the browser will be able to interpret it correctly and display the content properly rather than generating errors and displaying garbage.<br\><br\>   
  11. How do you make sure a preprocessor runs on your file?<br\>All that is needed to make sure a preprocessor runs on a file is that the correct file extension is used and implemented properly (i.e., preceded by a '.' and 'spelled' correctly).  As long as the file extension is correctly implemented, Rails will take care of the rest!<br\><br\>
  12. What's the outputted filetype of a preprocessed *.html.erb file? What about a *.css.scss file?<\br>The outputted filetype of a '*.html.erb' file is html.  The 'erb' preprocessor indicates that the html file includes some embedded Ruby code.  The outputted filetype of a '*.css.scss' is css.  The 'scss' preprocessor indicates that the css file includes some additional Sass code.<br\><br\> 
  13. What is the difference between the <%= and <% tags?<br\>There is really only one difference between the '<%=" and "<%' tags: the equals sign is a directive to print the result of running the code within the tags to the screen.  These are ERB (Embedded RuBy) tags, and so code between them is Ruby and will be interpreted and compiled as such, provided the '.erb' preprocessor is appended to the file.  So both '<%=' and "<%' tags are indicators to interpret the code between them as Ruby, but the former prints the returned value of the code to the screen while the latter does not.<br\><br\>
  14. What is a view partial?
  15. How do you insert a partial into your view?
  16. How can you tell that a view file is a partial?
  17. How do you pass a local variable to a partial?
  18. What's the magical Rails shortcut for rendering a User? A bunch of Users?
  19. What are asset tags and why are they used?
1. (By Monday 3/9) By yourself, complete the [Odin Project: Basic Routes, Views and Controllers](http://www.theodinproject.com/ruby-on-rails/basic-routes-views-and-controllers)
  1. Skip step 1 of the Application Skeleton section.  As we did last week, you will:
    1. Create a new Rails workspace on C9
    1. Add `/.c9` to your `.gitignore` file
    1. Setup git and commit the project:
      1. `git init`
      2. `git add .`
      3. `git commit -m 'initial commit'`
    1. Create a new repo on GitHub without a `README` or `.gitignore`
    1. Add your remote and push to github (replace the `<username>` and `<repo>` with your username and repo name)
      1. `git remote add origin https://github.com/<username>/<repo>.git`
      2. `git push -u origin master`
1. (By Thursday 3/12) As a group, complete the Rails tutorial [Chapter 5](https://www.railstutorial.org/book/filling_in_the_layout#top). Make sure to trade off coding, one person should not write everything.  
  1. Pick up where you left on your week 4 assignment with your new partner.  One person should be new to the codebase, one should have been working on it the previous week.

#### Optional
- Read the [Rails Guide on Routing](http://guides.rubyonrails.org/routing.html)
- Read the [Rails Guide on Controllers](http://guides.rubyonrails.org/action_controller_overview.html)
- Read the [Rails Guide on Layouts](http://guides.rubyonrails.org/layouts_and_rendering.html)
- Read the [Odin Project Guide on Asset Pipelines](http://www.theodinproject.com/ruby-on-rails/the-asset-pipeline)
