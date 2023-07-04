# To do list Project

* UI - small and compact
 - input field
 - different states within the tasks or filters rather (All, active, completed)
 - number of tasks left to complete

# Atomic Design

- atoms
 * buttons
 * check box to let user know if complete
 * button to hard delete the completed tasks as far as understood

- molecules 
 * to do list item

- organisms
 * to do list with its items and respective buttons

# Stories via Agile bologna


### As an anonymous user I can:
 1. view all of my to do list items so that I can see their statuses
 2. view the to do list as completed or not completed
 3. remove an item from the list to hide it from my view
 4. check off by selecting all items with one button to save time

# Procedural 

 ## BEGIN
 ## INIT 
  - Load the todo list
  - setup the variables, listeners, and initialize state
  - Listen for Data INPUT such as a new to do item, update to existing list or a soft delete(sweep it under the rug)
  - A listen for the user to switch views - to show all, completed, active, or the archived, filter it from state

## END

# Functional
## Do not forget CRUD - Create, Read, Update, Delete

After the thing is loaded

```
function createItem()
{
   - when input is put inside the input space, it is held and creates the output as a new item, press enter to finish the input
   - when enter key is pressed, invoke the makeUnique function
}

function readandUpdate{
after id is made within the array, update the dom in the correct order based on time of creation
}

function makeUnique()
{
    when item is created, assign a number based on a sequence that is completely unique
    move the id into an array tracking all the id's of the items
}
function addTask()
{
when a button is pressed, adds the input prompt for the createItem function to be invoked later if there isn't one already
}
function softDeleteItem
{
if the task state is complete, remove it from the list, BUT KEEP ITS ID

}

function completeItem(){
upon eventlisten, if task is not complete, make complete. if complete, undo the state to not-complete
}
function remainingItems()
{
return all items that are not complete
}
``` 
Question: How in the world do I do that? Justin suggested using the epoch or a timestamp to catch when it was posted
// Date.now in js could be an option 
//https://dev.to/rahmanfadhil/how-to-generate-unique-id-in-javascript-1b13


## Object-Oriented Programming
```
Object toDoItem = {
label:text
status: //likely an integer since there are multiple states. I was hoping it would be easy and say boolean. The states are active,completed,archived or deleted
// is the ID immutable with the method?
}
Object toDoListId{
ID:[ ] // based on decided Uniqued Id methods i choose(UUID)
}
// do we want to change order of items by click and drag with the UUID method we have?
```

## Thinking in React
### Components
* Index.js
  - responsibility of displaying the items
* RenderList.js
  Question: What handles the responsibility of holding the array of items. is that in local storage? MAYBE. Are the unique ID's in local storage? YES
  - responsibility of filtering and updating the DOM and 
* CreateItem component
  - function to make the unique ID if it is a todo item
    
* ToDoItem component.
  - Is it a body div inside the project?
 
* Footer.js
  - responsible for switching the views. all, active, completed.
 
Setting State


