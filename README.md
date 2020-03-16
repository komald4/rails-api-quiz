# Rails API Quiz

**Using whatever resources you like (e.g., Google, Stack Overflow, lectures, labs, notes, etc.), answer the following questions.**

1. Write the command to create a new Rails application in API mode with a Postgresql database.

```
rails new movies-api --api -G -d=postgresql
```

2. What are 5 other options that can be passed in to the `rails new` command and what do they do?

```
rails g resource Api::V1::Movie year
rails db:create
rails db:migrate
rails db:seed
rails db:create
```

3. What one line of code can be put into `routes.rb` to get all the RESTful routes for a given resource (e.g., dogs)?

```
map.resources :photos
restular.com
localhot:3000/rails/inforoutes
```

4. In the context of API development, what is versioning? How do we implement versioning in a Rails API?
```
rails g resource Api::V1::Movie year:integer 
Nested api. will make assumptions so we will need to change in our code.
```

5. What is serialization in reference to a Rails API?

```
transforms an JSON object to a string
```

6. Imagine a dog walking domain in which a walker has many dogs. Write the `index` action from the `WalkersController`. Remember, your endpoint should return JSON.

```
def index
    @dogs = Dog.all

    respond_to do |format|
    format.html {render :index}
    format.json{ render json: @dogs}
end
```

7. Change the code from the question above so that the walkers' dogs get embedded in the JSON being returned from the `index` endpoint.

```
```

8. Again, change the code above to exclude the timestamps from the data being returned in the JSON.

```
```

9. What does CORS mean? Why do we have to think about it when making an API?

```
CORS -Cross-origin resource sharing
This occurs during an API request which will error our
```

10. What changes do we have to make in our application to allow CORS?

```
```

11. In our dog walking app, what needs to be added to the following class to allow method calls like `Dog.create(name: "Neikko", breed: "mostly rat", age: 13)` and `Dog.find_by(name: "Neikko")` to function properly?

```
class Dog < ApplicationRecord
end
```

```
```




