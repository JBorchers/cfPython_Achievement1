# cfPython_Achievement1
<!--
 _Note to viewer: The majority of this project is using Windows and Command Prompt_


## Table of Contents

1. [Exercise 1.1](#task1)
2. [Exercise 1.2](#task2)

-->

<details>
<summary><h2>Exercise 1.1: Getting Started with Python <a name="task1"></a></h2></summary>
 
#### Install Python
Check if you already have Python installed by entering `python --version` in your terminal. If you do not already have Python installed, follow the instructions provided at https://www.python.org/downloads/. _this project was made using **Python 3.8.7**_

   ![Step 1](./Exercise_1.1/step_1.png)

Create your virtual environment using `mkvirtualenv <your_env_name`

   ![Step 1](./Exercise_1.1/step_2.png)

Create an add.py Python file in Visual Studio Code (or your preferred text editor).
Your _add_ function should define two variables that a user can input when prompted. The function will add the values together and output a statement.

```python
monday_steps = int(input("How many steps did you take on Monday?"))
tuesday_steps = int(input("How many steps did you take on Tuesday?"))

total_steps = monday_steps + tuesday_steps

print("You have taken ", f"{total_steps:,}", " steps so far this week. Keep it up!")
```
Now test your function in your terminal. 
In your Windows Command Prompt, and in your environment, cd to the folder your Python script is in.

```
C:\Users\username> workon <your_environment_name>
(<your_environment_name>) C:\Users\username> cd .\path\to\script
(<your_environment_name>) C:\Users\username\path\to\script> python add.py
```
![Step 3 and 4](./Exercise_1.1/step_3and4.png)

In order to allow your script to run across environments, you can add a requirements.txt file.
This file automatically installs required packages in any other environment you want to run your script in.

```
# use 'pip freeze' to record your environment's current package list, and add to a requirements.txt file
(<your_environment_name>) C:\Users\username> pip freeze > requirements.txt

# deactivate your original environment and create a new one
(<your_environment_name>) C:\Users\username> deactivate
C:\Users\username> mkvirtualenv <your_environment_name>_copy

#install requirements.txt to new environment
(<your_environment_name>_copy) C:\Users\username> pip install -r requirements.txt
```
![Step 5](./Exercise_1.1/step_5.png)

</details>

<!--------------------------------------------------------------------------------------------------------------------------------------------->
<!--------------------------------------------------------------------------------------------------------------------------------------------->

<details>
<summary><h2>Exercise 1.2: Data Types<a name="task2"></a></h2></summary>

First, open an iPython shell in your working environment.

#### Create a Dictionary
In your iPython shell, create a *dictionary* structure for your first recipe, called `recipe_1`.
Here, our structure is made up of keys and values to make a `Tea` (str), that will take `5` minutes to make (int), and will contains a `list` of three ingredients.

![Step 1and2](./Exercise_1.2/step_1and2.png)

A *dictionary* structure is going to be used for making this recipe app, as the app will require the flexibility to easily modify recipes. Dictionaries are also composed of key/value pairs, which sets up our app for what it needs: the `keys` are the “name”, “cooking_time”, and “ingredients”.  All of these keys need to be paired with `values` which is the specific information of recipe that the user will refer to.

#### Create a List
Create an outer structure called `all_recipes`
Use `append()` to add your dictionary, recipe_1, to the list.

![Step 3](./Exercise_1.2/step_3.png)

A _list_ is used in this case as it creates a sequential and dynamic structure of our recipes, and will allow us to easily access each individual element through indexing.


#### Add More Recipes
Follow the same steps to add four more recipes...

![Step 4](./Exercise_1.2/step_4.png)

Add the rest of the dictionaries to your all_recipes list

![Step 4.2](./Exercise_1.2/step_4.2.png)

#### Print Contents
Once you have all your recipes added to the list, print out each recipe's ingredients as five different lists.

![Step 5](./Exercise_1.2/step_5.png)

</details>

<!--------------------------------------------------------------------------------------------------------------------------------------------->
<!--------------------------------------------------------------------------------------------------------------------------------------------->


<details>
<summary><h2>Exercise 1.3: Operators & Functions</h2></summary>

### Using operators and functions to display user inputs

_Step 1_<br>
Open a code editor. This example uses Visual Studio Code.

_Step 2_<br>
Create two empty lists: one called `recipes_list`, and one called `ingredients_list`

![Step 1 and 2](./Exercise_1.3/step_1and2.png)


_Step 3_<br>
Define a function called `take_recipe`
This function should call for several user inputs: a recipe’s name (string), the amount of time to cook the recipe (integer), and a list of ingredients that the recipe will call for.
Next, create a dictionary called `recipe` that will store these variables as key/value pairs.

![Step 3](./Exercise_1.3/step_3.png)


_Step 4_<br>
Prompt the user to input how many recipes they want to add. This integer will be stored to `n`.

![Step 4](./Exercise_1.3/step_4.png)


_Step 5_<br>
Create a *for loop* that will iterate through the number of recipes indicated by the user in step 4. This for loop will check if an ingredient entered by the user is already in the ingredients_list. If it is not, the new ingredient will be appended to the ingredients_list. Each new recipe is appended to the recipes_list.

![Step 5](./Exercise_1.3/step_5.png)


_Step 6, Part 1_<br>
Create a *for loop* that will check boolean logic of each recipe according to if/and statements. Four different scenarios are checked to determine the recipe’s level of difficulty.
`if` the recipe’s cooking time is _less than 10_ minutes `and` the length of ingredients in the list is _less than 4_, set difficulty to *Easy*
`if` the recipe’s cooking time is _less than 10_ minutes `and` the length of ingredients in the list is _greater than or equal to 4_, set difficulty to *Medium*
`if` the recipe’s cooking time is _greater than or equal to 10_ minutes `and` the length of ingredients in the list is _less than 4_, set difficulty to *Intermediate*
`if` the recipe’s cooking time is _greater than or equal to 10_ minutes `and` the length of ingredients in the list is _greater than 4_, set difficulty to *Hard*

![Step 6.1](./Exercise_1.3/step_6.1.png)

_Step 6, Part 2_<br>
Create a for loop that will iterate through each recipe in the recipes_list, and print the recipe’s name, the cooking time, the ingredients needed (as another for loop to loop through the list of ingredients), and the level of difficulty.

![Step 6.2](./Exercise_1.3/step_6.2.png)


_Step 7_<br>
Create a function called `display_ingredients` that will show all the ingredients available across all recipes. The list needs to be alphabetized, which can be done using Python’s built-in `sort()`.
The function then will loop through the alphabetized list of ingredients and print each one, once the function is called using `display_ingredients()`.

![Step 7](./Exercise_1.3/step_7.png)


<h3>Check your work</h3>
In Visual Studio Code, press the “play button” in the top right-hand corner of your screen. This will open up your terminal and begin prompting for user input. This will be a great place to double check for any errors in your code.

![Check your work 1](./Exercise_1.3/check_work_1.png)

Once you’ve input everything it asks for, your results will show immediately.
Play with formatting to make your output easier to read.

_example:_

![Check your work 2](./Exercise_1.3/check_work_2.png)

</details>

<!--------------------------------------------------------------------------------------------------------------------------------------------->
<!--------------------------------------------------------------------------------------------------------------------------------------------->

<details>
<summary><h2>Exercise 1.4: File Handling</h2></summary>
<details>
<summary><h4>Part 1: Create <code>recipe_input.py</code></h4></summary>

This script will load and store data into a binary file based on user input.<br>
Later, the stored data will be accessed by another script: `recipe_search.py`

 _Step 1_<br>
`import pickle` in order to work with binary files

<!--![Step 1](./Exercise_1.4/part1_step1.png)-->
<img src="./Exercise_1.4/part1_step1.png" alt="Step 1" width="50%">


_Step 2_<br>
Define a function called `take_recipe()`<br>
This is where user inputs will put together the recipes.
Recipes should include:
1. a recipe name
2. cooking time
3. necessary ingredients
4. a level of difficulty (to be defined in another function)

<!--![Step 2](./Exercise_1.4/part1_step2.png)-->
<img src="./Exercise_1.4/part1_step2.png" alt="Step 2" width="50%">


_Step 3_<br>
Level of difficulty is first calculated with another function, called `calc_difficulty`<br>
Difficulty is identified by the `cooking_time` and number of `ingredients`
The levels are returned as `Easy`, `Medium`, `Intermediate`, or `Hard`

<!--![Step 3](./Exercise_1.4/part1_step3.png)-->
<img src="./Exercise_1.4/part1_step3.png" alt="Step 3" width="50%">

All of these values should be added to a dictionary for later use.


_Step 4_<br>
Now we begin with the main code.
Define a `try-except-else-finally` block
1. `Try` a block of code where an error might occur. In this case, we will `try` opening a binary file named by the user, and load contents to it using the `pickle` module. 

<!--![Step 4](./Exercise_1.4/part1_step4a.png)-->
<img src="./Exercise_1.4/part1_step4a.png" alt="Step 4.1" width="50%">

2. If there is no file by the name the user input, the `except` block will display a `FileNotFoundError` message to the user. The script will create a file named with what the user input.
3. Other errors are handled with another `except` block
4. `Finally` the script extracts the values from the dictionary into two lists: `recipes_list` and `all_ingredients`

<!--![Step 4](./Exercise_1.4/part1_step4b.png)-->
<img src="./Exercise_1.4/part1_step4b.png" alt="Step 4.2" width="50%">


_Step 5_<br>
A for loop will loop through the number of recipes that the user enters and call the `take_recipe()` function.
It will add each new recipe to the `recipes_list` dictionary. It will also loop through existing ingredients in the `all_ingredients` dictionary and will add any new ingredients that do not already exist.

<!--![Step 5](./Exercise_1.4/part1_step5.png)-->
<img src="./Exercise_1.4/part1_step5.png" alt="Step 5" width="50%">


_Step 6_<br>
The updated `recipes_list` and `all_ingredients` are added to a dictionary named `data`

<!--![Step 6](./Exercise_1.4/part1_step6.png)-->
<img src="./Exercise_1.4/part1_step6.png" alt="Step 6" width="50%">

_Step 7_<br>
Use the pickle module to write the updated data to the user-defined file

<!--![Step 7](./Exercise_1.4/part1_step7.png)-->
<img src="./Exercise_1.4/part1_step7.png" alt="Step 7" width="50%">


</details>
<details>
<summary><h4>Part 2: Create <code>recipe_search.py</code></h4></summary>

This script will read the saved data in the binary file that `recipe_input.py` wrote to.
With more user inputs, `all_ingredients` is displayed to the user after they enter the binary file's name.
Then the user can select a specific ingredient and the script will display any recipe that has that particular ingredient stored.

_Step 1_<br>
Import the `pickle` module

<!--![Step 1](./Exercise_1.4/part2_step1.png)-->
<img src="./Exercise_1.4/part2_step1.png" alt="Step 1" width="50%">


_Step 2_<br>
Define a function called `display_recipe()`
This function will take each recipe as an argument and print all of its attributes: _Recipe Name_, _Cooking Time_, _Ingredients_, and _Difficulty_.

<!--![Step 2](./Exercise_1.4/part2_step2.png)-->
<img src="./Exercise_1.4/part2_step2.png" alt="Step 2" width="50%">


_Step 3_<br>
Define another function called `search_ingredient()`
This function should take a dictionary called `data` as an argument. It will:
1. print all available ingredients under a key `all_ingredients`<br>
Each ingredient is shown with a number; use `enumerate()` to take the index of each ingredient
2. define a `try` block<br>
the user will `try` to pick a number from the list, and if it exists, it is stored in `ingredient_searched`
3. the `except` clause warns the user if the input is incorrect
4. an `else` clause is added to display any recipe in `recipes_list` that contains the searched ingredient

<!--![Step 3](./Exercise_1.4/part2_step3.png)-->
<img src="./Exercise_1.4/part2_step3.png" alt="Step 3" width="50%">


_Step 4_<br>
Prompt the user to input the name of the binary file where recipe_input.py wrote recipe data to.

<!--![Step 4](./Exercise_1.4/part2_step4.png)-->
<img src="./Exercise_1.4/part2_step4.png" alt="Step 4" width="50%">


_Step 5_<br>
A `try` block attempts to open the file. If it successfully opens the file, it will extract the `data` using the `pickel` module

<!--![Step 5](./Exercise_1.4/part2_step5.png)-->
<img src="./Exercise_1.4/part2_step5.png" alt="Step 5" width="50%">


_Step 6_<br>
Add an `except` clause for if the file is not found, using `except FileNotFoundError:`

<!--![Step 6](./Exercise_1.4/part2_step6.png)-->
<img src="./Exercise_1.4/part2_step6.png" alt="Step 6" width="50%">


_Step 7_<br>
If the `try` block doesn’t encounter any errors, and `else` block will call the `search_ingredient` function and pass data into it as an argument.

<!--![Step 7](./Exercise_1.4/part2_step7.png)-->
<img src="./Exercise_1.4/part2_step7.png" alt="Step 7" width="50%">


</details>
<details>
<summary><h4>Testing</h4></summary>

<h4><code>recipe_input.py</code></h4>

The script prompts the user to enter a filename where they want their recipes stored.
If the file exists, the script uses that file; however, if the file does not exist, a new file is created:

<!--![Testing_1.1](./Exercise_1.4/part1_testing1.png)-->
<img src="./Exercise_1.4/part1_testing1.png" alt="Testing_1.1" width="50%">

The user then enters:
1.	how many recipes they want to add
2.	the name of the recipe
3.	the cooking time for the recipe
4.	and the ingredients needed

<!--![Testing_1.2](./Exercise_1.4/part1_testing2.png)-->
<img src="./Exercise_1.4/part1_testing2.png" alt="Testing_1.2" width="50%">

Once completed, data is added to a binary file 

<!--![Testing_1.3](./Exercise_1.4/part1_testing3.png) -->
<img src="./Exercise_1.4/part1_testing3.png" alt="Testing_1.3" width="50%">

<h4><code>recipe_search.py</code></h4>

This script starts by asking the user which file they added their recipe to.
The script searches this file and lists `all_ingredients`

<!--![Testing_2.1](./Exercise_1.4/part2_testing1.png)-->
<img src="./Exercise_1.4/part2_testing1.png" alt="Testing_2.1" width="50%">

Next it prompts the user to enter a number that’s next to an ingredient that’s been listed. Once entered, the script loads the recipe that’s found to include that ingredient, and loads the recipe to be displayed via the `pickle` method.

<img src="./Exercise_1.4/part2_testing2.png" alt="Testing_2.2" width="50%">

</details>
</details>
</details>


<!--------------------------------------------------------------------------------------------------------------------------------------------->
<!--------------------------------------------------------------------------------------------------------------------------------------------->

<details>
<summary><h2>Exercise 1.5: Object-Oriented Programming</h2></summary>

*Object-Oriented Programming* is the concept of coding with `classes` which act as a container for `objects`. This method of programming is geared toward keeping code organized, readable, and reusable.
This project demonstrates storing data – in this case a _recipe_ — into `objects`, which have their own attributes and custom methods. All of this will be in one `Recipe` class.
The _methods_ will allow a user to search for a recipe based on a selected ingredient.


<br>_Step 1_<br>
In a new .py file, define a class called `Recipe`.
`Recipe` will contain the following _data attributes_:
*	`name` of recipe
*	`ingredients` as a _list_
*	`cooking_time` as an integer defining amount of time to make the recipe
*	`difficulty`, which is defined and auto-generated by a separate class method

<img src="./Exercise_1.5/step_1.png" width="50%">


<br>_Step 2_<br>
Define procedural attributes, or `methods` for the `Recipe` class.
*	Initialize `name` of recipe, as well as *getter* and *setter* methods for `name` and `cooking_time`. _This will allow the application to read and modify the values of “name” and “cooking_time” based on user inputs. _

<img src="./Exercise_1.5/step_2a.png" width="50%">
 
*	Create a method called `add_ingredients` that can take in any number of variables and append them to an `ingredients` list.
Hint: this function will call `update_all_ingredients()`, defined later

*	Add a *getter* method for `ingredients – this will return the ingredients list 

<img src="./Exercise_1.5/step_2b.png" width="50%">

*	Create a `calculate_difficulty()` method (called in step 1) that identifies levels of recipe complexity based on cooking_time and number of ingredients

<img src="./Exercise_1.5/step_2c.png" width="50%">
 
*	A *search method* will take an ingredient as an argument, search for it in the `recipe` object, and return a boolean response if the ingredient is found or not

* `update_all_ingredients()` will go through the object’s ingredients. If new ingredients are found they are appended to the class variable, `all_ingredients`.<br>
As a *class variable*, this will be able to add new ingredients across all recipes, or `objects`.
*	Now, the entire recipe can be returned. Formatting should be applied for readability.

<img src="./Exercise_1.5/step_2d.png" width="50%">


<br>_Step 3_<br>
Add functionality to find an object containing a specific variable. In this project, _find a recipe that contains a specific ingredient_. 
*	 Define two parameters: `data` and `search_term` <br>
The *data* consists of the recipe objects available, and the *search_term* is what is searched for amongst the given object list.
*	This will operate via a `for loop`

<img src="./Exercise_1.5/step_3.png" width="50%">
 

<br>_Step 4_<br>
Create an object
*	Initialize an object with a recipe name
*	Add ingredients to the object
*	Set a cooking time
*	Display the object as a string

<img src="./Exercise_1.5/step_4.png" width="50%">

<br>_Step 5_<br>
Add more recipes, similar to _Step 4_

<img src="./Exercise_1.5/step_5.png" width="50%">

<br>_Step 6_<br>
Collect all recipes into a list (`recipes_list`)

<img src="./Exercise_1.5/step_6.png" width="50%">
 
<br>_Step 7_<br>
Try the `recipe_search()` method to search for recipes that contain specified ingredients

<img src="./Exercise_1.5/step_7.png" width="50%">


<h2>Testing</h2>

Run the Python script in the terrminal.
The output should list all of the availble recipe objects in their entirety, and then show all recipe objects that contain the ingredient that is searched for.

</details>


<!--------------------------------------------------------------------------------------------------------------------------------------------->
<!--------------------------------------------------------------------------------------------------------------------------------------------->

<details>
<summary><h2>Exercise 1.6: Databases</h2></summary>

<h3>Part 1: Create and Connect Database</h3>

<br>_Step 1_<br>
*	pip install mysql-connector-python
*	open ipython shell, and type: import mysql.connector

<img src="./Exercise_1.6/part1_step1.png" width="50%">


<br>_Step 2_<br>
*	initialize a connection object called `conn`
*	This object acts as a connection between the Python session and the MySQL server

<img src="./Exercise_1.6/part1_step2.png" width="50%">


<br>_Step 3_<br>
*	Initialize a `cursor`
*	This will allow you to perform operations on the database with SQL queries

<img src="./Exercise_1.6/part1_step3.png" width="50%">


<br>_Step 4_<br>
*	Create a database called `task_database`

<img src="./Exercise_1.6/part1_step4.png" width="50%">


<br>_Step 5_<br>
*	Connect to the newly created database with the `USE <database>` query

<img src="./Exercise_1.6/part1_step5.png" width="50%">


<br>_Step 6_<br>
*	Create a table called `Recipes`
*	`id`: integer type
*	`name`: string type with a limit of 50 characters. Used to store the name of the recipe.
*	`ingredients`: string type with a limit of 255 characters. Used to store types of ingredients.
*	`cooking_time`: integer type. Used to store recipe cooking time in minutes.
*	`difficulty`: string type with a limit of 20 characters. Used to story level of difficulty (Easy, Medium, Intermediate, Hard)
*	To view the entire table, open a mysql Command Line Client, select your database, and type DESCRIBE <table>

<img src="./Exercise_1.6/part1_step6.png" width="50%">


<h3>Part 2: Create a Main Menu</h3>

<br>_Step 1_<br>
* Implement a “main menu”. Menu should include 4 options: create recipe; search for recipe; update recipe; and delete recipe

<img src="./Exercise_1.6/part2_step1.png" width="50%">

<br>_Step 2_<br>

<img src="./Exercise_1.6/part2_step2.png" width="50%">

<br>_Step 3_<br>

<img src="./Exercise_1.6/part2_step3.png" width="50%">

<br>_Step 4_<br>

<img src="./Exercise_1.6/part2_step4.png" width="50%">



<h3>Part 3: Create a Recipe with `create_recipe()`</h3>

<br>_Step 1_<br>
*	Collect: `name`, `cooking_time`, and `ingredients`
  
<img src="./Exercise_1.6/part3_step1.png" width="50%">


<br>_Step 2_<br>
* Call the `calc_difficulty()` function
  
<img src="./Exercise_1.6/part3_step2.png" width="50%">


<br>_Step 3_<br>
* Connect information to a SQL query
  
<img src="./Exercise_1.6/part3_step3.png" width="50%">


<br>_Step 4_<br>
* Execute query and commit changes
  
<img src="./Exercise_1.6/part3_step4.png" width="50%">


<h3>Part 4: Search for Recipe with `search_recipe()`</h3>

<br>_Step 1_<br>
* Run SQL queries on the database to access recipes based on ingredients selected by user.
* `SELECT` ingredients column

<img src="./Exercise_1.6/part4_step1.png" width="50%">


<br>_Step 2_<br>
* Add each ingredient to a new list called `all_ingredients`
  
<img src="./Exercise_1.6/part4_step2.png" width="50%">


<br>_Step 3_<br>
* Display all ingredients

<img src="./Exercise_1.6/part4_step3.png" width="50%">


<br>_Step 4_<br>
* `SELECT` ingredients column `WHERE` a specific search pattern (ex: name of ingredient) occurs
  
<img src="./Exercise_1.6/part4_step4.png" width="50%">



<h3>Part 5: Update Recipe with `update_recipe`</h3>

<br>_Step 1_<br>
*	Fetch all recipes and display them to the user
*	User chooses a recipe to be updated by selecting the recipe’s corresponding id

<img src="./Exercise_1.6/part5_step1.png" width="50%">


<br>_Step 2_<br>
* User selects the column that needs to be updated. The script collects the new value from the user.
<img src="./Exercise_1.6/part5_step2.png" width="50%">


<br>_Step 3_<br>
*	Build query in the form of a string to update the table for given `id`, column, and updated value.
*	A separate query calculates a new level of difficulty if either `ingredients` or `cooking_time` are modified
  
<img src="./Exercise_1.6/part5_step3.png" width="50%">


<br>_Step 4_<br>
* Execute queries on the Recipes table and commit changes
  
<img src="./Exercise_1.6/part5_step4.png" width="50%">


<h3>Part 6: Delete a Recipe with `delete_recipe()</h3>

<br>_Step 1_<br>
*	Display all recipes in the Recipe table to the user. User selects a recipe to be deleted by id number.
  
<img src="./Exercise_1.6/part6_step1.png" width="50%">


<br>_Step 2 and 3_<br>
*	SQL query `DELETE`s row, identified by previous step
* Execute query and commit changes

<img src="./Exercise_1.6/part6_step2and3.png" width="50%">


<h3>Part 7: Testing the Script</h3>

<br>_Step 1_<br>
*	Ensure MySQL Server is running and execute the script

<img src="./Exercise_1.6/part7_step1.png" width="50%">


<br>_Step 2_<br>
* Create a new recipe

<img src="./Exercise_1.6/part7_step2.png" width="50%">


<br>_Step 3_<br>
* Search for a recipe based on ingredient

<img src="./Exercise_1.6/part7_step3.png" width="50%">


<br>_Step 4_<br>
* Update recipes

<img src="./Exercise_1.6/part7_step4a.png" width="50%">
<img src="./Exercise_1.6/part7_step4b.png" width="50%">


<br>_Step 5_<br>
* Delete recipe

<img src="./Exercise_1.6/part7_step5.png" width="50%">


<br>_Step 6_<br>
* Exit the script

<img src="./Exercise_1.6/part7_step6.png" width="50%">


<br>_Final Results After Modification_<br>

<img src="./Exercise_1.6/part7_Final_Results.png" width="50%">





</details>
