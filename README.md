Download Link: https://assignmentchef.com/product/solved-retail-transaction-programming-project
<br>
<strong>Project Requirements: </strong>

<ol>

 <li>Develop a program to emulate a purchase transaction at a retail store. This program will have two classes, a <strong>LineItem</strong> class and a <strong>Transaction</strong> The <strong>LineItem</strong> class will represent an individual line item of merchandise that a customer is purchasing. The <strong>Transaction</strong> class will combine several <strong>LineItem </strong>objects and calculate an overall total price for the line item within the transaction. There will also be two test classes, one for the <strong>LineItem </strong>class and one for the <strong>Transaction </strong>class.</li>

</ol>




<ol start="2">

 <li>Design and build a <strong>LineItem</strong> This class will have three instance variables. There will be an <strong>itemName</strong> variable that will hold the identification of the line item (such as, “Colgate Toothpaste”); a <strong>quantity</strong> variable that will hold the quantity of the item being purchased; and a <strong>price</strong> variable that will hold the retail price of the item. The <strong>LineItem</strong> class should have a constructor, accessors for the instance variables, a method to compute the total price for the line item, a method to update the quantity, and a method to convert the state of the object to a string. Using Unified Modeling Language (UML), the class diagram looks like this:</li>

</ol>

<table width="364">

 <tbody>

  <tr>

   <td width="364"><strong> </strong><strong>LineItem</strong><strong> </strong></td>

  </tr>

  <tr>

   <td width="364"><strong> </strong>–  <strong>itemName : String</strong>–  <strong>quantity : int</strong>–  <strong>price : double </strong> </td>

  </tr>

  <tr>

   <td width="364"><strong> </strong><strong> + LineItem( String, int, double )</strong><strong> + getName( ) : String</strong><strong> + getQuantity( ) : int</strong><strong> + getPrice( ) : double</strong><strong> + getTotalPrice( ) : double</strong><strong> + setQuantity( int ) </strong><strong> + setPrice( double ) </strong><strong> + toString( ) : String</strong></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>The constructor will assign the first parameter to the instance variable <strong>itemName</strong>, the second parameter to the instance variable <strong>quantity</strong>, and the third parameter to the instance variable <strong>price</strong>.</li>

 <li>The class will have three accessor methods—<strong>getName( )</strong>, <strong>getQuantity( )</strong>, and <strong>getPrice( )</strong>—that will return the value of each respective instance variable.</li>

 <li>The class will have two mutator methods, <strong>setQuantity( int )</strong> and <strong>setPrice( double )</strong>, that will update the quantity and price, respectively, of the item associated with the line of the transaction.</li>

 <li>The method <strong>getTotalPrice( )</strong> handles the conversion of the quantity and price into a total price for the line item.</li>

 <li>The method <strong>toString( )</strong> allows access to the state of the object in a printable or readable form. It converts the variables to a single string that is neatly formatted.</li>

</ol>




<strong>Note:</strong> Refer to the textbook for a discussion of escape sequences. These are characters that can be inserted into strings and, when printed, will format the display neatly. An escape sequence for the tab character can be inserted to get a tabular form when printing. This tab character is “<strong>t</strong>“.




The <strong>LineItem</strong> class will have a <strong>toString( )</strong> method that concatenates <strong>itemName</strong>, <strong>quantity</strong>, <strong>price</strong>, and <strong>total price</strong>—separated by tab characters—and returns this new string. When printing an object, the <strong>toString( ) </strong>method will be implicitly called, which in this case, will print a string that will look something like:




Colgate Toothpaste qty 2 @ $2.99                      $5.98




<ol start="3">

 <li>Build a <strong>Transaction</strong> class that will store information about the items being purchased in a single transaction. It should include a <strong>customerID</strong> and <strong>customerName</strong>. It should also include an <strong>ArrayList </strong>to hold information about each item that the customer is purchasing as part of the transaction.</li>

</ol>




<strong>Note: </strong>You must use an ArrayList, not an array.

<ol start="4">

 <li>Build a <strong>TransactionTest</strong> class to test the application. The test class should <strong>not </strong>require any interaction with the user. It should verify the correct operation of the constructor and all methods in the <strong>Transaction</strong></li>

</ol>

<strong>Specific Requirements for the Transaction Class  </strong>

<ol>

 <li>The <strong>Transaction</strong> class should have a constructor with two parameters. The first is an integer containing the customer’s ID and the second is a String containing the customer’s name.</li>

 <li>There should be a method to allow the addition of a line item to the transcript. The three parameters for the <strong>addLineItem</strong> method will be (1) the item name, (2) the quantity, and (3) the single item price.</li>

 <li>There should be a method to allow the updating of a line item already in the transaction. Notice that updating an item means changing the quantity or price (or both). The parameters for the <strong>updateItem</strong> method are also (1) the item name,</li>

</ol>

(2) the quantity, and (3) the single item price. Notice that the updating of a

specific line item requires a search through the <strong>ArrayList</strong> to find the desired item. Anytime a search is done, the possibility exists that the search will be unsuccessful. It is often difficult to decide what action should be taken when such an “exception” occurs. Since exception handling is not covered until later in this textbook, make some arbitrary decisions for this project. If the item to be updated is not found, take the simplest action possible and <strong>do nothing</strong>. Do not print an error message to the screen. Simply leave the transaction unchanged.

<ol start="4">

 <li>The transaction class needs a method called <strong>getTotalPrice</strong> to return the total price of the transaction.</li>

 <li>There should also be a method to return information about a specific line item. It should return a single String object in the same format described for the <strong>LineItem</strong> class:</li>

</ol>




Colgate Toothpaste qty 2 @ $2.99                      $5.98




Again, the possibility exists that the search for a specific line item will fail. In this instance, you should return a string containing a message similar to this:




Colgate Toothpaste not found.




<ol start="6">

 <li>The final method needed is a <strong>toString</strong> It should return the transaction information in a single String object. It should use the following format:</li>

</ol>




<strong>Customer ID : 12345</strong>

<strong>Customer Name : John Doe</strong>

<strong> </strong>

<strong>      Colgate Toothpaste qty 2 @ $2.99          $5.98 </strong>

<strong>  Bounty Paper Towels qty 1 @ $1.49  $1.49   Kleenex Tissue  qty 1 @ $2.49  $2.49 </strong>




<strong>Transaction Total                          $9.96</strong>




Notice that a newline character “<strong>
</strong>” can be inserted into the middle of a string.




Ex.




<strong>int age = 30;</strong>

<strong>String temp = “John Doe 
 is ” + age + “
” + ” years    old”; </strong>

<strong> </strong>

The output would be:




<strong>John Doe</strong>   <strong>is 30 </strong>

<strong>years old</strong>




Notice also that “<strong>
</strong>” is a single character and could actually go inside single or double quotes, depending on the circumstances.

Here is a UML diagram for the <strong>Transaction</strong> class as described above. Notice that private instance variables and methods may be added, as needed. For all public methods use <strong>exactly</strong> the name given below.

<table width="391">

 <tbody>

  <tr>

   <td width="391"><strong> </strong><strong>Transaction</strong>  <strong> </strong></td>

  </tr>

  <tr>

   <td width="391"> –        <strong>lineItems : ArrayList&lt;LineItem&gt;</strong>–        <strong>customerID : int</strong>–        <strong>customerName : String </strong></td>

  </tr>

  <tr>

   <td width="391"> <strong> + Transaction( int, String )</strong><strong> + addLineItem( String, int, double ) </strong><strong> + updateItem( String, int, double )</strong><strong> + getTotalPrice( ) : double</strong><strong> + getLineItem( String ) : String</strong><strong> + toString( ) : String</strong></td>

  </tr>

 </tbody>

</table>


