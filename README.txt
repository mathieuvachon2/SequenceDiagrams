Notes on the sequence diagrams:

At certain points, we had to modify data structures to make sure we could do the correct operations on TouchCore. An example of that is that Space has a HashMap of the Obstacles in all 4 Directions and the key is the Direction enum. TouchCore would not accept an enum as a key so we simplified it and used String direction instead. 

Since we can't link enums with classes, we can't link the GameManager with the Color Enum, so in the CreateFamilyGame sequence model we just assumed we had access to an array of Color enums.

To get the nextPlacement relationship with Spaces and their neighbors, instead of creating an association between spaces, we decided to create methods in the GameManager class that will be responsible to find out the associations and the neighbors