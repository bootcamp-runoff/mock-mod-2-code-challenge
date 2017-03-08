1. Pretend that the following is in our 'config/routes.rb' file. How would you define that making a Get request to '/dogs' should go to the index action of a controller called `CatsController`. (Yes, we know it's weird...)

```ruby
# Add Your Code Here!!
Rails.application.routes.draw do
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html

end
```

2. Given the following code in a 'config/routes.rb' file, how many HTTP requests does our application respond to and what are they?

```ruby
Rails.application.routes.draw do
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
  resources :guests, only: [:index, :show]

end
```

3. Pretend you're building Netflix. Given that we want to be RESTful, what type of HTTP Request should you make to create a new movie? What controller action will that go to?

```
# Write Your Answer Below
```

4. Given the ERB code below is in a Rails `new.html.erb` file, write out the HTML that will actually be rendered.

```erb
<%= form_form @account do |f|%>
  <%= f.label :username %>
  <%= f.text_field :username %>
  <%= f.submit %>
<% end %>
```

```html
<!-- Write Your Solution Here -->

```

5. Update the following `Dog` model to make sure that a dog can't be saved without a unique name.

```ruby
class Dog < ActiveRecord::Base

end
```

6. Pretend that we have two tables, `zorps` and `phalanges`. Below we have what our schema looks like, as well as the Ruby models. We'd like to model this out so that a zorp has_many phalanges and a phalange has many zorps. Update the code below to reflect this relationship, adding any changes to the schema as well as additional classes you might need. NOTE: Yes, we know that these are nonsense words. Do your best to follow convention with the naming.

```
Add any changes to the schema here!

zorps
id | klax

phalanges
id | tralfamadores
```


```ruby
class Zorp < ActiveRecord::Base

end

class Phalange < ActiveRecord::Base

end

## Add any other classes here
```

7. What would be the RESTful route and controller action to update a zorp?

8. Given the following routes and controller action, create a form to let a user login.

```ruby
# Add Your Code Here!!
Rails.application.routes.draw do
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html
  get '/login', to: 'sessions#new', as: 'login'
  post '/sessions', to: 'sessions#create'
  get '/users/:id', to: 'users#show', as: 'user'
end
```

```ruby
# app/controllers/sessions_controller
class SessionsController < ApplicationController

  def new
  end

  def create
    user = User.find_by(username: params[:username])
    if user && user.authenticate(params[:password])
      session[:user_id] = user.id
      redirect_to user
    else
      redirect_to login_path
    end
  end
end
```

```ERB
<!-- Create Your Login Form Here! -->

```

9. Recall that our `zorps` table has one column, `klax` of type text. Pretend below that we have three separate files - `config/routes.rb`, `app/controllers/zorps_controller.rb`,  and `app/views/zorps/new.html.erb`. Add all of the code needed for me to be able to create a new zorp with a klax.

```ruby
# config/routes.rb
Rails.application.routes.draw do
  # For details on the DSL available within this file, see http://guides.rubyonrails.org/routing.html

end
```

```ruby
# app/controllers/zorps_controller.rb
class ZorpsController < ApplicationController

end
```

```ERB
<!-- app/views/zorps/new.html.erb -->

```
