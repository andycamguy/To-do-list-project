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
   - when input is put inside the input space, it is held and creates the output as a new item
   - invoke the makeUnique function
}



function makeUnique()
{
    when item is created, assign a number based on a sequence that is completely unique
    move the id into an array tracking all the id's of the items
}
``` 
Question: How in the world do I do that? Justin suggested using the epoch or a timestamp to catch when it was posted
// Date.now in js could be an option 
//https://dev.to/rahmanfadhil/how-to-generate-unique-id-in-javascript-1b13