Download Link: https://assignmentchef.com/product/solved-coen79-lab-3
<br>
A sequence class is similar to a bag—both contain a bunch of items, but unlike a bag, the items in a sequence are arranged in an order. <strong>In contrast to the bag class, the member functions of a sequence will allow a program to step through the sequence one item at a time</strong>. Member functions also permit a program to <strong>control precisely where items are inserted and removed</strong> within the sequence.

Our sequence is a class that depends on an underlying value_type, and the class also provides a size_type.




Three member functions work together to enforce the <strong>in-order retrieval</strong> rule:




void start( );

value_type current( ) const; void advance( );




<ul>

 <li>After activating start, the current function returns the first item</li>

 <li>Each time we call advance, the current function changes so that it returns the next item in the sequence</li>

</ul>







Provide some additional useful member functions, such as:

<ol>

 <li>insert_front: insert a new value at the front of the sequence. This new item should now be the current item.</li>

 <li>remove_front: remove the value at the front of the sequence. The new front item should now be the current item.</li>

 <li>attach_back: insert a new value at the back of the sequence. This new item should now be the current item.</li>

 <li><sub>end</sub>: The last item in the sequence should now be the current item.</li>

 <li>operator+ and operator+=: These operators should have the precondition that the sum of the sizes of the two sequences being added is smaller than the CAPACITY of a sequence.</li>

</ol>







<strong>Subscript operator: </strong>

For a sequence <sub>x</sub>, we would like to be able to refer to the individual items using the usual C++ notation for arrays. For example, if <sub>x</sub> has three items, then we want to be able to write x[0], x[1], and x[2] to access these three items. This use of the <strong>square brackets</strong> is called the <strong>subscript operator</strong>. The subscript operator may be overloaded as a member function, with the prototype shown here as part of the sequence class:







class sequence { public:

… value_type operator [] (size_type index) const; …







As you can see, the operator[] is a member function with one parameter. The parameter is the index of the item that we want to retrieve. The implementation of this member function should check that the index is a valid index (i.e., index is less than the sequence size), and then return the specified item.




For this project, specify, design, and implement this new subscript operator for the sequence.