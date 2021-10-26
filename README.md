# How To Use EJS to Template Your Node Application
I have created a new project directory and then installed all the node, express, ejs in the root folder.
In the root folder i have created a .js(server.js) file which listens on port 3000
This code also sets EJS as the view engine for the Express application using:
           
           `app.set('view engine', 'ejs');`
 
 In the next step i created the views using EJS.
 I have created 3 partials (head.ejs, header.ejs, and footer.ejs) which is used on Index, About pages.
 In the head.ejs the code contains metadata it also includes Bootstrap styles.
 In header.ejs the code contains navigation for an HTML document and uses several classes from Bootstrap for styling.
 In footer.ejs the code contains copyright information and uses several classes from Bootstrap for styling.
 
 Now i have created a new pages subdirectory in views. In that directory i have created index.ejs, about.ejs files.
 I have used <%- include('RELATIVE/PATH/TO/FILE') %> to embed an EJS partial into index file.
 I have saved the changes and run the aplllication: node server.js 
 Now in the terminal we get like Server is listening on port 3000. This means our application is running without any errors.
 Now we can look at http://localhost:3000/ in a web browser, you can observe the Index page.
  ![image](https://user-images.githubusercontent.com/78608904/138869195-a92d3f32-d8a9-4029-a006-82aa7f4358a3.png)

 
In the same way using  <%- include('RELATIVE/PATH/TO/FILE') %> ejs partial embed into about file.
If you visit http://localhost:3000/about in a web browser, you can observe the About page with a sidebar
  ![image](https://user-images.githubusercontent.com/78608904/138869506-32481a31-20bb-4058-81a2-fbb76cd719b6.png)

Now we are Passing Data to Views and Partials
I have define some basic variables and a list to pass to the Index page.
Now we add those variable names  in the index.ejs code file 

Now to  loop over data, you can use .forEach.

Now after visiting http://localhost:3000/ we will see that our application is ready by how we used our template.

![image](https://user-images.githubusercontent.com/78608904/138872917-2c58058f-d79b-446c-abf5-e2eaa7d89b9a.png)


## Here are my learnings.

EJS is a template system. You define HTML pages in the EJS syntax and you specify where various data will go in the page. Then, your app combines data with the template and "renders" a complete HTML page where EJS takes your data and inserts it into the web page according to how you've defined the template. For example, you could have a table of dynamic data from a database and you want EJS to generate the table of data according to your display rules. It saves you from the drudgery of writing code to dynamically generate HTML based on data.

EJS is compatible with Express for back-end use as it hooks into the View engine architecture that Express provides and lets you render web pages to the client with res.render() in Express.

EJS was so similar to HTML so I found it easy.
EJS uses all the JS jargon and logic, so if you are proficient in JS, you can use EJS right away.
EJS is way faster than Jade and handlebars.
EJS has a really smart error handling mechanism built right into it. It points out to you, the line numbers on which an error has occurred so that you don’t end up looking through the whole template file wasting your time in searching for bugs.

