Download Link: https://assignmentchef.com/product/solved-cs1xc3-assignment-5-typedef-struct-and-realloc
<br>
<h1>Primary Learning Objectives</h1>

<ul>

 <li>Write a C program that uses typedef and struct to create a ‘new type’.</li>

 <li>Write a C program that uses realloc() to reallocate memory.</li>

</ul>

<h1>Requirements</h1>

Create a program that allows the user to enter a set of geographic positions, prints out the positions, sorts them by northernmost position using selection sort, and prints out the sorted positions.

Your program must use typedef and struct together to define a ‘new geographic position type’ for representing geographic coordinates with a latitude and longitude.  Your program must create a dynamically allocated array of this geographic position type that is initially able store one (and only one) geographic position.

Your program must then begin to ask the user to enter latitude and longitude coordinates.  After each position is entered, your program must ask the user whether they wish to continue entering geographic positions, accepting the characters ‘y’ or ‘n’ as a response.  If the user wishes to continue entering geographic positions, then space for one more geographic position should be dynamically reallocated with realloc(), and the user should be asked again to enter latitude and longitude coordinates.  While latitude and longitude coordinates have specific ranges, you do not need to implement input validation for this assignment.  You can also assume the user will enter in either ‘y’ or ‘n’ when prompted.

Once the user selects ‘n’ to stop entering geographic positions, the positions that were entered should be printed in the order in which they were entered.  A function should be created to handle printing geographic positions, and this function should be used to print the geographic positions.  Don’t worry about decimal points of precision for the output of the coordinates.

The geographic positions should be sorted using the <strong>selection sort</strong> algorithm from northernmost positions to southernmost positions.  Research how the selection sort algorithm works and implement it with a function in C to sort your geographic positions from northernmost to southernmost.  After sorting the geographic positions, use the print function you’ve created to print out the now sorted geographic positions.  Remember to free your dynamically allocated array.

Your program should work identically or near-identically to this example:




<strong>Hint:</strong> If you use scanf to read in double values for the latitude and longitude position, you may find that if you try to use scanf to then read in a char value (for ‘y’ or ‘n’) that the scanf is “skipped”.  If this is the case, what is likely happening is that after the user hits enter on the previous scanf (say to read in longitude), a ‘
’ character remains the input buffer, and your scanf to read in the char value sees the ‘
’ in the input buffer and returns.  You may need to clear the input buffer of any newline characters then before using your scanf to read a character, which you could do with code like this: <strong>while (getchar() != ‘
’); </strong>