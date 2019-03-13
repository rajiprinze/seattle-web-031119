# Enumerations Review

## Objectives - SWBAT

1. Get more Familiar with using IRB
2. Get used to using the following enumeration methods
3. Figure out what methods to use in which cases
  * **EACH** -
        * Input  : Enumerates through each element of the array, acting as a reader to go through data.
        * Output : Always returns original array. In order to manipulate data, you would need to create a new array and return.
  * **SELECT (/FIND_ALL)** -
        * Input  : Enumerates through each element and evaluated based on a boolean conditional
        * Output : Returns a new array with elements that evaluated to true.
  * **FIND/DETECT VS. FIND_ALL** -
        * Input  : Enumerates through the array and find the first element in which the condition is true.
        * Output : Returns the first element.
  * **MAP/COLLECT** -
        * Input  : Enumerates through the array object.
        * Output : Return a new array with elements of the evaluated expressions provided.
  * **REDUCE/INJECT/EACH_WITH_OBJECT** :
        * Input  : Enumerates through the array object and combines into a new variable to store the new object in.
        * Output : Returns a new object\\element with the evaluated expression from the expression provided.

## Objectives - SWBAT
Commands Entered | Results                                     | Final Notes   
:---:|:-----------------------------------------------------:| :------------------------:
 arr = \[3, 6, 8, 10, 15\] | \[3, 6, 8, 10, 15\]  | Created a new array |
 arr.each \{ \|element\| true \} | \[3, 6, 8, 10, 15\]| Returns original array for all truthy values |       
 arr.each \{ \|element\| false \} | \[3, 6, 8, 10, 15\]| Returns original array for all truthy values      
 arr.each \{ \|number\| puts number \}| \[3, 6, 8, 10, 15\]| Returns original array for all truthy | values                   
 arr.select \{ \|n\| true \}| \[3, 6, 8, 10, 15\]| Returns original array for all truthy values       
 arr.select \{ \|n\| 89 \}| \[3, 6, 8, 10, 15\]| Returns original array for all truthy values      
 arr.select \{ \|n\| nil \}| \[\]| Return *nil* for falsy values
 arr.select \{ \|n\| false \}| \[\]| Return *nil* for falsy values       
 arr.select \{ \|n\| n*2 \}| \[3, 6, 8, 10, 15\]| n*2 is till a truthy value so full array returned
 arr.map \{ \|n\| n*2 \}| \[6, 12, 16, 20, 30\]| Returned new array with n*2
 arr.map \{ \|n\| n=6 \}| \[6, 6, 6, 6, 6\]| Returned new array, assigned 6 to all values |
 arr.map  \{ \|n\| n==6 \}| \[false, true, false, false, false\]| Returns new array with evaluation of the expression provided.                    
 arr.find \{ \|n\| n == 3\}| 3 | Returned first value matched with 3   
 arr.find \{ \|n\| n ==6\}| 6 | Returned first value matched with 6
 arr.find_all \{ \|n\| n ==6\}| \[6\] | returned a array with first match        
 arr.find_all| <Enumerator: \[3, 6, 8, 10, 15\]:find_all>  | Returns and Enumator object for the call           
 (1..10).reduce \{ \|sum, n\| n + 1 \}| 11| Returned the final evaluated expression (10+1)|
 (1..10).reduce \{ \|sum, n\| sum + n\}| 55| Returned the sum of all digits 1..10 |
 (1..10).reduce(8) \{ \|sum, n\| sum + n \} | 63 | Starts the iteration and 10 and tallies the range |
 ("a".."c").reduce \{ \|concat, letter\| concat + letter \}| "abc" | Enumerated through and concatenated string in range
 Array.methods| methods for that object (103 total)| Returns all the methods declarations for the Array class.                 
 Array.kind_of?(Hash) | false | Checks and object type with another Object for relatedness.
