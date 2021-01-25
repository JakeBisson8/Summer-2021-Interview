## Repository: 

```
[https://github.com/JakeBisson8/OutStemBackendChallenge](https://github.com/JakeBisson8/OutStemBackendChallenge)
```

## Run Instructions

### Download Source Code

### Running the Server
1. Open a command prompt / terminal window with current directory set to the directory containing the source code
1. Run the command: ```node index```
1. Alternatively if nodemon is installed run: ```nodemon index```

The server should start and display the following:
```
Server is listening on port: 5000
Mongo DB connected!
```

### Endpoints

#### Test User Routes
**Definition:** Returns a message to test the user routes are working
**Type:** Get
**Path:** localhost:5000/api/users/test
**Accepted body parameters:**
* No parameters are required

#### Create User
**Definition:** Creates a user object
**Type:** Post
**Path:** localhost:5000/api/users/create
**Accepted body parameters:**
* firstname : String
* lastname : String
* email : String

#### Upgrade User to Premium
**Definition:** Upgrades a user to a premium user
**Type:** Post
**Path:** localhost:5000/api/users/makepremium
**Accepted body parameters:**
* id: String
**Accepted headers:**
* authentication : any passed value will suffice for the request to be authenticated.

#### Get Users
**Definition:** Returns a list of all users
**Type:** Get
**Path:** localhost:5000/api/users/getusers
**Accepted body parameters:**
* No parameters are required

#### Test Recipe Routes
**Definition:** Returns a message to test the recipe routes are working
**Type:** Get
**Path:** localhost:5000/api/recipes/test
**Accepted body parameters:**
    * No parameters are required

#### Create Recipe
**Definition:** Creates a recipe object
**Type:** Post
**Path:** localhost:5000/api/recipes/create
**Accepted body parameters:**
* author : String
* content : String
* category : String
* isPremium: Boolean (this field is optional)
* isPrivate: Boolean (this field is optional)

#### Edit Recipe
**Definition:** Edits a recipe object
**Type:** Post
**Path:** localhost:5000/api/recipes/edit
**Accepted body parameters:**
* id: String 
* author : String
* content : String
* category : String  (this field is optional)
* isPremium: Boolean (this field is optional)
* isPrivate: Boolean (this field is optional)

#### Delete Recipe
**Definition:** Deletes a recipe object 
**Type:** Post
**Path:** localhost:5000/api/recipes/delete
**Accepted body parameters:**
* id: String 
* author : String

#### Get Recipes
**Definition:** Returns a list of all public recipes. If an author is specified, returns a list of all recipes viewable by the author
**Type:** Get
**Path:** localhost:5000/api/recipes/getrecipes
**Accepted body parameters:**
* author: String (this field is optional)

#### Get Recipe
**Definition:** Returns a single recipe if it is viewable based on the parameters passed. 
**Type:** Get
**Path:** localhost:5000/api/recipes/getrecipe
**Accepted body parameters:**
* id: String 
* author: String (this field is optional)

## Additional Information

### Technology Used
* JavaScript
* NodeJS
* ExpressJS
* Mongoose
* VSCode