1. (5 Points) How is this project structure different than a Flask (or Node) application? What role are the urls.py and views.py files responsible for?
2. (5 Points) Why do we use 2 separate urls.py files? How do they interact?
3. (5 Points) When is it desirable to split our code over multiple apps? Why would we want to do so?

- There is a main project directory with an overall configuration that is created upon creating a project. Then you create "apps" which
projects can contain multiple instances of. Each app represents a different part of the web application. Url.py directs the web traffic
as needed for each app and views.py is what creates what the user sees on the web page.

- The first url.py file is the root url.py for the entire project. It is used to direct web traffic to different parts of the web application.
Each app may do something different so the first url.py file is to direct the web traffic to the desired application. The other urls.py file
is unique to each app. This urls.py file controls the different pages within this application if it has multiple.

- It is desirable to modularize the code so that if there is a problem, we can triangulate it to a single application and so that it does not
affect the rest of the web application should the specific application be needed to be taken down.