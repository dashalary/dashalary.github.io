---
layout: post
title:      "My Sinatra project"
date:       2020-10-28 19:04:54 +0000
permalink:  my_sinatra_project
---


For my second project, I wanted to create a Sinatra app that allows one to create a wishlist to keep track of desired holiday gifts. At the very beginning, after utilizing Corneal gem for my basic file structure, I created 3 models: Item, User, and Category. Users would have many items through categories, items would belong to users and categories, and categories would have many items and many users through categories. After creating appropriate tables and foreign keys, I executed my migrations and made a seeds file to allow a user access to view a few public categories. Then, I made 5 controllers to ensure separation of responsibilities: application controller (a "master" controller that the other controllers inherit from), users controller (handling signup), categories controller (handling all categories CRUD routes), items controller (handling all items CRUD routes), and sessions controller (for login/logout purposes). I also made the appropriate views for my routes and added some design elements using Bootstrap. The challenge with this project for me was taking an extra step to create a nested route that allows a user to create an item in a specific category. That was a rather emotional journey but with the support of my cohort lead and my teammates (shotout to CJ, Brock, and Leah) it all worked out at the end of the day. 
