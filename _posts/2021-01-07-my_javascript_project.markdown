---
layout: post
title:      "My JavaScript Project"
date:       2021-01-07 17:31:19 +0000
permalink:  my_javascript_project
---


One of my New Years resolutions was to get back into reading books, which inspired me to make libraries and books the center of my JavaScript project. I built *My Library* in two main parts: a Rails API backend and the JavaScript frontend.

To begin, I used a Rails scaffolding generator in order to build the vast majority of the backend, which was enormously helpful. After creating my models (Library and Book) through scaffolding, establishing their relation (Library has_many books, and Book belongs_to a Library) and running my migrations with the foreign key in place, my API was almost ready. Next, I added the gem 'active_model_serializers' in order to create serializers for each model and add all of the attributes to them, in a fashion similar to attribute accessor. I made sure to specify the models' relation in the serializer files in order to allow for nested JSON data. At this point I was ready to move on to building the frontend.

In order to allow for the communication between the backend and the frontend of my application, I used the gem 'rack-cors', which handles cross-origin resource sharing, making cross-origin (backend and frontend) AJAX possible. This gem was really great, as it let me specify which methods I want to allow to share resources for in the config/application.rb file. As I decided to only cover create, read, and delete actions of CRUD, those were the methods I allowed in my configuration. 

Next, I created an index.html file, the contents of which would be reflected by the DOM of my app. I made a very basic nav bar with links to create a library, see all libraries, and see all books. Now I was ready to move on to the JavaScript part of my project. While writing the first few needed JS functions, I decided to make a service API class which would handle all of the API data fetching in order to separate responsibilities. I tried to make it as simple as possible in order to prevent my own confusion and ended up with functions that each had a clear purpose, such as to render all books, render all libraries, show a book, show a library, etc. I did the same with my forms (create a library or create a book) and ensured the presence of necessary event listeners, as well as preventing default behavior. 

My application is quite minimal as a whole, yet it required me to be attentive and meticulous in tracking the movement of data when I was faced with errors. Very often it was one bit of code on a single line that prevented multiple functions from succeeding in their tasks. Debugging was a valuable lesson in itself, as it strengthened my understanding of what is happening at every step of the way. Similarly, restructuring or simply moving features/functionality around (e.g. from a nav link to a button inside another page) deepened my understanding of JS and increased my confidence in my own work. I am happy with this project and the experience I gained building my first JavaScript application. 

