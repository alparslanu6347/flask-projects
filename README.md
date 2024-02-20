# Hands-on Flask-01-02 : Creating First Flask Application - Hello World and basic usage of Jinja Templates

Purpose of the this hands-on training is to give the students quick introductory knowledge of how to create a Flask web application on local.

## Learning Outcomes

At the end of the this hands-on training, students will be able to;

- understand client-server software architecture.

- get familiar with Python Flask framework.

- install Python and Flask framework on local

- build a simple web application with Python Flask framework.

- use git repo to manage the application versioning.

- run the web application on AWS EC2 instance using the GitHub repo as codebase (will be shown by instructor).

## Outline

- Part 1 - Getting to know the Python Flask framework

- Part 2 - Write a Simple Hello World Web Application on GitHub Repo

- Part 3 - Write a Simple Hello World Web Application with Jinja template on GitHub Repo

- Part 4 - Install Python and Flask framework on Amazon Linux 2 EC2 Instance

## Part 1 - Getting to know the Python Flask framework

![Flask](./flask.png)

Flask is a web application development framework written in Python. It is a micro-framework that provides only the essential components which makes it easier to begin with when compared to full-stack frameworks like Django which has boilerplate code and dependencies.
And yet, Flask provides libraries, tools, and modules to develop web applications with additional features like authentication, database ORM, etc.

Followings are some of features of Flask Framework;

- It provides a development server and a debugger.

- It uses Jinja2 as templating engine.

- It is compliant with WSGI 1.0.

- It provides integrated support for unit testing.

- Many extensions are available to enhance its functionalities.


## Part 2 - Write a Simple Hello World Web Application on GitHub Repo

- Create folder named `flask-01-02-hello-world-app-Jinja-Template` within your repo under `python/hands-on` folder and go under it.

- Create folder named `flask-01-hello-world-app`

- Create python file named `hello-world-app.py`

- Import Flask module.

- Create an object named `app` from imported Flask module.

- Create a function `hello` which returns a string `Hello World`.

- Assign a URL route the `hello` function with decorator `@app.route('/')`.

- Create a function `second` which returns a string `This is the second page` and assign a URL route the `second` function with decorator `@app.route('/second')`. 

- Create a function `third` which returns a string `This is the subpage of third page` and assign a URL route the `third` function with decorator `@app.route('/third/subthird')`. 

- Create a dynamic url which takes id number dynamically and return with a massage which show id of page.

- run the application in debug mode

- Connect the Hello World application from the web browser with `localhost:5000` or `127.0.0.1:5000`

- to reach application from anywhere on port 80, change debug mode

- Save the complete code as `hello-world-app.py` file under `hands-on/flask-01-02-hello-world-app-Jinja-Template/flask-01-hello-world-app` folder.

- Add and commit all changes on local repo

- Push `hello-world-app.py` to your remote repo


## Part 3 - Write a Simple Hello World Web Application with Jinja template on GitHub Repo

- Create folder named `flask-02-Jinja_Template` within your repo under `python/hands-on` and go under it

- Create python file named `jinja.py`

- Import Flask and render_template modules.

- Create an object named `app` from imported Flask module.

- Create an `index.html` file under templates folder.

- Create a function named `head` which sends number `number1` and `number2` variables to the `index.html`. Use these variables into the `index.html` file. Assign a URL route the `head` function with decorator `@app.route('/')`.

- Create an `body.html` file under templates folder.

- Create a function named `number` which sends number `num1` and `num2` and sum of them to the `index.html`. Use these variables into the `body.html` file. Assign a URL route the `number` function with decorator `@app.route('/sum')`.

- run the application in debug mode

- Connect the Hello World application from the web browser with `localhost:5000` or `127.0.0.1:5000`

- Save the complete code as `jinja.py` file under `flask-02-Jinja_Template` folder.

- Add and commit all changes on local repo

- Push all files to your remote repo on GitHub.

## Part 4 - Run the Hello World App on EC2 Instance

- Launch an Amazon EC2 instance using the Amazon Linux 2 AMI with security group allowing SSH (Port 22) and HTTP (Port 80) connections.

- Connect to your instance with SSH.

- Update the installed packages and package cache on your instance.

- install git and wget

- Download the web application file from GitHub repo.

- Run the web application

- Connect the Hello World application from the web browser

- Connect the Hello World application from the terminal with `curl` command.

###### ***** NEW PROJECTS ***** ######

# Hands-on Flask-03-04: If-For structure, Handling Routes and Get-Post Methods

Purpose of the this hands-on training is to give the students introductory knowledge of how to handle forms.

![HTTP Methods in Flask](./http-methods-flask.png)

## Learning Outcomes

At the end of the this hands-on training, students will be able to;

- build a simple web application with Flask framework.

- understand the HTTP request-response cycle and structure of URL.

- create routes (or views) with Flask.

- serve static content and files using Flask.

- serve dynamic content using the html templates.

- write html templates using Jinja Templating Engine.

- build a web application with Python Flask framework.

- create if conditions and for loops with flask.

- handle forms and GET-POST methods using the flask.

- use git repo to manage the application versioning.


## Outline

- Part 1 - Getting to know routing and HTTP URLs.

- Part 2 - Getting to know HTTP methods (GET & POST).

- Part 3 - Write a Web Application using If conditions and for loops

- Part 4 - Write a Web Application with Sample Routings and Templating on GitHub Repo

- Part 5 - Learn to use GET and POST HTTP Method

- Part 6 - Write a Sample Web Application with forms

## Part 1 - Getting to know routing and HTTP URLs.

HTTP (Hypertext Transfer Protocol) is a request-response protocol. A client on one side (web browser) asks or requests something from a server and the server on the other side sends a response to that client. When we open our browser and write down the URL (Uniform Resource Locator), we are requesting a resource from a server and the URL is the address of that resource. The structure of typical URL is as the following.

![URL anatomy](./url-structure.png)

The server responds to that request with an HTTP response message. Within the response, a status code element is a 3-digit integer defines the category of response as shown below.

- 1xx -> Informational ---> It means the request was received and the process is continuing.

- 2xx -> Success ---> It means the action was successfully received, understood, and accepted.

- 3xx -> Redirection ---> It means further action must be taken in order to complete the request.

- 4xx -> Client Error ---> It means the request contains incorrect syntax or cannot be fulfilled.

- 5xx -> Server Error ---> It means the server failed to fulfill an apparently valid request.

If you would learn those codes one by one. I can sent you a URL. You can also find different resources. 

https://www.w3schools.com/tags/ref_httpmessages.asp

## Part 2 - Getting to know HTTP methods (GET & POST)

HTTP (Hypertext Transfer Protocol) is a request-response protocol. A client on one side (web browser) asks or requests something from a server and the server on the other side sends a response to that client. 

When sending request, the client can send data with using different http methods like `GET, POST, PUT, HEAD, DELETE, PATCH, OPTIONS`, but the most common ones are `GET` and `POST`.

![Get and Post Requests](./get-post-request.jpg)

- HTTP `GET` method request;
    
    - used to request data from a specified resource.

    - can be cached.

    - remains in the browser history.

    - can be bookmarked

    - should never be used when dealing with sensitive data.

    - has length limitation.

    - only used to request data, not to modify it. 

- HTTP `POST` method request;
    
    - never cached.

    - does not remain in the browser history.

    - can not be bookmarked

    - can be used when dealing with sensitive data.

    - has no length limitation.

## Part 3 - Write a Web Application using If conditions and for loops

- Copy `flask-03-handling-routes-and-if-for` within `my-repository` repo

- Under `Flask_If_for_structure` folder within `flask-03-handling-routes-and-if-for` repo

- Create python file named `app.py`

```python
# Import Flask modules

# Create an object named app 

# Create a function named head which shows the massage as "This is my first conditions experience" in `index.html` 
# and assign to the route of ('/')

# Create a function named header which prints numbers elements of list one by one in `index.html` 
# and assign to the route of ('/')

# run this app in debug mode on your local.

```

## Part 4 - Write a Web Application with Sample Routings and Templating on GitHub Repo

- Let's head over `flask-03-handling-routes` folder within `flask-03-handling-routes-and-if-for` repo

- Create python file named `app.py`

```python
#Import Flask modules

#Create an object named app 


# Create a function named home which returns a string 'This is home page for no path, <h1> Welcome Home</h1>' 
# and assign route of no path ('/')


# Create a function named about which returns a formatted string '<h1>This is my about page </h1>' 
# and assign to the static route of ('about')


# Create a function named error which returns a formatted string '<h1>Either you encountered an error or you are not authorized.</h1>' 
# and assign to the static route of ('error')


# Create a function named admin which redirect the request to the error path 
# and assign to the route of ('/admin')


# Create a function named greet which return formatted inline html string 
# and assign to the dynamic route of ('/<name>')


# Create a function named greet_admin which redirect the request to the hello path with param of 'Master Admin!!!!' 
# and assign to the route of ('/greet-admin')


# Rewrite a function named greet which uses template file named `greet.html` under `templates` folder 
# and assign to the dynamic route of ('/<name>'). 
# Please find a template html file named `greet.html` which takes `name` as parameter under `templates` folder 


# Create a function named list10 which creates a list counting from 1 to 10 within `list10.html` 
# and assign to the route of ('/list10'). 
# Please find a template html file named `list10.html` which shows a list counting from 1 to 10 under `templates` folder 


# Create a function named evens which show the even numbers from 1 to 10 within `evens.html` 
# and assign to the route of ('/evens'). 
# Please find a template html file named `evens.html` which shows a list of even numbers from 1 to 10 under `templates` folder 


# Add a statement to run the Flask application which can be reached from any host on port 80.
```

## Part 5 - Learn to use GET and POST HTTP Method

- Go to `Flask_GET_POST_Methods` folder under the `flask-04-handling-forms-POST-GET-Methods` folder

- Create file named `app.py`  here. 

```python
# Import Flask modules


# Create an object named app


# create a function named "lcm" which calculates a least common multiple values of two numbers. 


# Create a function named `index` which uses template file named `index.html` 
# send two numbers as template variable to the app.py and assign route of no path ('/') 


# calculate sum of them using "lcm" function, then sent the result to the 
# "result.hmtl" file and assign route of path ('/calc'). 
# When the user comes directly "/calc" path, "Since this is a GET request, LCM has not been calculated" string returns to them with "result.html" file


# Add a statement to run the Flask application which can be debugged.

```

## Part 6 - Write a Sample Web Application with forms

- Go to `flask-04-handling-forms` within `flask-04-handling-forms-POST-GET-Methods` folder

- Now, we'll write an application with form handling and save the complete code as `app-form-handling.py` under `flask-04-handling-forms` folder.

```python
# Import Flask modules


# Create an object named app


# Write a function named `greet` which uses template file named `greet.html` given under 
# `templates` folder. it takes parameters from query string on URL, assign that parameter 
# to the 'user' variable and sent that user name into the html file. If it doesn't have any parameter, warning massage is raised


# Write a function named `greet` which uses template file named `greet.html` given under `templates` folder


# Write a function named `login` which uses `GET` and `POST` methods, 
# and template files named `login.html` and `secure.html` given under `templates` folder 
# and assign to the static route of ('login')


# Add a statement to run the Flask application which can be reached from any host on port 80.


# app.run(host='0.0.0.0', port=80)
```

