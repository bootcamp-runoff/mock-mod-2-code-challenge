# Rails Assessment

It's time to put our Rails know-how to the test. Today, we have an basic new application.

## Objectives
+ MVC
+ REST
+ Request/Response Cycle
+ Form/Form Helpers
+ ActiveRecord
+ Validations

## Setup

Before you begin, fork and clone this repo, run `rake db:migrate` and `rake db:seed` to get started.

## The Domain

You've just been hired by 'The Late Show With Stephen Colbert' - congratulations! The production staff needs help keeping track of all of the guests that they've had on the show. To do this, we need to be able to keep track of each guest and all of their appearances on the show.

Luckily, another developer has already started the job. Visiting '/guests' shows us all of the guests in the database. Your deliverables are as follows.

## Instructions

1. On the guests index page, clicking on a guest's name should take us to a detail view about each guest. This View should include the guests name and occupation.
2. As a user, I should be able to create a new appearance for a guest. The Appearance should have a date and be associated with that guest. Remember that we can have the same guest on the show many times. The appearance should also have a rating on a 1-5 scale so we can keep track of what guests we'd like to have back on the show.
3. As a user, I should be able to view all of the guests appearances when viewing info about that particular guest. This means that on the guest show page we should also list out all of that guests appearances.
4. Build out Login Form so they'll have to use
5. Add a many to many using Episodes

### Make a Quiz Style

### Hints / Tips

+ Remember we want to be RESTful. What URL should show info about a particular guest? What URL should show a form to create an appearance? What controller actions are associated?  
+ There are probably many ways to set this up.
