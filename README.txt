Notes on the sequence diagrams:

To know what fireman or player sent the request we used a linklist and made it so that the first element of that list must
be the instance of player or fireman to which the request originated form.

At certain points, we had to modify data structures to make sure we could do the correct operations on TouchCore.
An example of that is that Space has a HashMap of the Obstacles in all 4 Directions and the key is the
Direction enum. TouchCore would not accept an enum as a key so we simplified it and used String direction instead. 

Since we can't link enums with classes, we can't link the GameManager with the Color Enum,
so in the CreateFamilyGame sequence model we just assumed we had access to an array of Color enums.

To get the nextPlacement relationship with Spaces and their neighbors,
instead of creating an association between spaces,
we decided to create methods in the GameManager class that will be 
responsible to find out the associations and the neighbors.

We also have differences in associations between classes from one sequence diagram to the next, as for some 
we have a HashMap for example and in another an array. We just made sure they independently made sense and 
followed the instructions in the M5 guidelines. In endTurn for example, we assumed at times we have a double
array of Spaces as that is what works with the logic in our project. Indeed, the endTurn and createGame 
sequence diagrams have notable differences when it comes to the data structures. It would have taken too 
much time to redo one in TouchCore, however our class diagram model reflects our preffered data structures.
