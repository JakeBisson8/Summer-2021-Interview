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
**Definition:** Returns a message to test the user routes are working <br/>
**Type:** Get <br/>
**Path:** localhost:5000/api/users/test <br/>
**Accepted body parameters:** <br/>
* No parameters are required

#### Create User
**Definition:** Creates a user object <br/>
**Type:** Post <br/>
**Path:** localhost:5000/api/users/create <br/>
**Accepted body parameters:** <br/>
* firstname : String
* lastname : String
* email : String

#### Upgrade User to Premium
**Definition:** Upgrades a user to a premium user <br/>
**Type:** Post <br/>
**Path:** localhost:5000/api/users/makepremium <br/>
**Accepted body parameters:** <br/>
* id: String
**Accepted headers:** <br/>
* authentication : any passed value will suffice for the request to be authenticated.

#### Get Users
**Definition:** Returns a list of all users <br/>
**Type:** Get <br/>
**Path:** localhost:5000/api/users/getusers <br/>
**Accepted body parameters:** <br/>
* No parameters are required

#### Test Recipe Routes
**Definition:** Returns a message to test the recipe routes are working <br/>
**Type:** Get <br/>
**Path:** localhost:5000/api/recipes/test <br/>
**Accepted body parameters:** <br/>
    * No parameters are required

#### Create Recipe
**Definition:** Creates a recipe object <br/>
**Type:** Post <br/>
**Path:** localhost:5000/api/recipes/create <br/>
**Accepted body parameters:** <br/>
* author : String
* content : String
* category : String
* isPremium: Boolean (this field is optional)
* isPrivate: Boolean (this field is optional)

#### Edit Recipe
**Definition:** Edits a recipe object <br/>
**Type:** Post <br/>
**Path:** localhost:5000/api/recipes/edit <br/>
**Accepted body parameters:** <br/>
* id: String 
* author : String
* content : String
* category : String  (this field is optional)
* isPremium: Boolean (this field is optional)
* isPrivate: Boolean (this field is optional)

#### Delete Recipe
**Definition:** Deletes a recipe object <br/>
**Type:** Post <br/>
**Path:** localhost:5000/api/recipes/delete <br/>
**Accepted body parameters:** <br/>
* id: String 
* author : String

#### Get Recipes
**Definition:** Returns a list of all public recipes. If an author is specified, returns a list of all recipes viewable by the author <br/>
**Type:** Get <br/>
**Path:** localhost:5000/api/recipes/getrecipes <br/>
**Accepted body parameters:** <br/>
* author: String (this field is optional)

#### Get Recipe
**Definition:** Returns a single recipe if it is viewable based on the parameters passed. <br/>
**Type:** Get <br/>
**Path:** localhost:5000/api/recipes/getrecipe <br/>
**Accepted body parameters:** <br/>
* id: String 
* author: String (this field is optional)

## Additional Information

### Technology Used
* JavaScript
* NodeJS
* ExpressJS
* Mongoose
* VSCode