Download Link: https://assignmentchef.com/product/solved-comp1210-project-8-icosahedron-list2-with-junit-tests
<br>
This project consists of four classes: (1) Icosahedron is a class representing an Icosahedron object; (2) IcosahedronTest class is a JUnit test class which contains one or more test methods for each method in the Icosahedron class; (3) IcosahedronList2 is a class representing an Icosahedron list object; and (4) IcosahedronList2Test class is a JUnit test class which contains one or more test methods for each method in the IcosahedronList2 class.  <u> Note that there is no requirement</u> <u>for a class with a main method in this project</u>.




<strong><u>Since you will be modifying classes from the previous project, I strongly recommend that you</u> <u>create a new folder for this project with a copy of your Icosahedron class and IcosahedronList2</u> <u>class from the previous project</u>.    </strong>

<strong> </strong>

<strong><u>You should create a jGRASP project and add your Icosahedron class and IcosahedronList2</u> <u>class.  With this project is open, your test files will be automatically added to the project when</u> <u>they are created.  You will be able to run all test files by clicking the JUnit run button on the</u> <u>Open Projects toolbar</u>. </strong>

<em> </em>

<em>New requirements and design specifications are underlined in the descriptions <u>below</u> to help you identify them</em>.




<strong> </strong>




<ul>

 <li><strong>Icosahedron.java </strong>(a modification of the <strong>Icosahedron </strong>class in the previous project; <u>new</u> <u>requirements are underlined below</u>)</li>

</ul>

<strong> </strong>

<strong>Requirements</strong>: Create an Icosahedron class that stores the label, color, and edge (i.e., length of an edge, <u>which must be greater than zero</u>).  The Icosahedron class also includes methods to set and get each of these fields, as well as methods to calculate the surface area, volume, and surface to volume ratio of an Icosahedron object, and a method to provide a String value of an Icosahedron object (i.e., a class instance).




<table width="586">

 <tbody>

  <tr>

   <td colspan="3" width="586">An <strong>Icosahedron</strong> has 20 equilateral triangle faces, 12 vertices, and 30 edges as depicted below. The formulas are provided to assist you in computing return values for the respective methods in the Icosahedron class described in this project.</td>

  </tr>

  <tr>

   <td width="191"> </td>

   <td width="191"> Surface Area (A) Volume (V) Edge length (a) Surface/Volume ratio (A/V)</td>

   <td width="204"></td>

  </tr>

  <tr>

   <td colspan="3" width="586"> </td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Design</strong>:  The Icosahedron class has fields, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (instance variables): label of type String, color of type String, and edge of type double. Initialize the Strings to “” and the double to 0 in their respective declarations. These instance variables should be private so that they are not directly accessible from outside of the Icosahedron class, and these should be the only instance variables in the class.</li>

</ul>

<u>Class Variable – count of type int should be private and static, and it should be initialized to</u> <u>zero</u>.




<ul>

 <li><strong>Constructor</strong>: Your Icosahedron class must contain a public constructor that accepts three parameters (see types of above) representing the label, color, and edge. Instead of assigning the parameters directly to the fields, the respective set method for each field (described below) should be called. For example, instead of the statement label = labelIn; use the statement setLabel(labelIn); Below are examples of how the constructor could be used to create Icosahedron objects.  Note that although String and numeric literals are used for the actual parameters (or arguments) in these examples, variables of the required type could have been used instead of the literals.</li>

</ul>

<u>The constructor should increment the class variable count each time an Icosahedron is</u> <u>constructed</u>.




Icosahedron example1 = new Icosahedron(“Small”, “blue”, 0.01);




Icosahedron example2 = new Icosahedron(”    Medium    “, “orange”, 12.3);




Icosahedron example3 = new Icosahedron(“Large”, ”  white  “, 123.4);




<ul>

 <li><strong>Methods</strong>: Usually a class provides methods to access and modify each of its instance variables (known as get and set methods) along with any other required methods. The methods for Icosahedron, which should each be public, are described below.  See formulas in Code and Test below. o getLabel:  Accepts no parameters and returns a String representing the label field.

  <ul>

   <li>setLabel: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the label field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getColor: Accepts no parameters and returns a String representing the color field.</li>

   <li>setColor: Takes a String parameter and returns a boolean. If the string parameter is not null, then the “trimmed” String is set to the color field and the method returns true. Otherwise, the method returns false and the label is not set.</li>

   <li>getEdge: Accepts no parameters and returns a double representing the edge field.</li>

   <li>setEdge: Accepts a double parameter and returns a boolean as follows. If the edge is greater than zero, sets the edge field to the double passed in and returns true.  Otherwise, the method returns false and the edge is not set.  o surfaceArea:  Accepts no parameters and returns the double value for the total surface area calculated using the value for edge.</li>

   <li>volume: Accepts no parameters and returns the double value for the volume calculated using the value for edge.</li>

   <li>surfaceToVolumeRatio: Accepts no parameters and returns the double value calculated by dividing the total surface area by the volume.</li>

   <li>toString: Returns a String containing the information about the Icosahedron object formatted as shown below, including decimal formatting (“#,##0.0#####”) for the double values.  Newline and tab escape sequences should be used to achieve the proper layout.  In addition to the field values (or corresponding “get” methods), the following methods should be used to compute appropriate values in the toString method:</li>

  </ul></li>

</ul>

surfaceArea(), volume(), and surfaceToVolumeRatio().  Each line should have no trailing spaces (e.g., there should be no spaces before a newline (
) character).  The toString value for example1, example2, and example3 respectively are shown below (the blank lines are not part of the toString values).

Icosahedron “Small” is “blue” with 30 edges of length 0.01 units.    surface area = 0.000866 square units    volume = 0.000002 cubic units    surface/volume ratio = 396.950723




Icosahedron “Medium” is “orange” with 30 edges of length 12.3 units.

surface area = 1,310.209833 square units    volume = 4,059.844212 cubic units    surface/volume ratio = 0.322724




Icosahedron “Large” is “white” with 30 edges of length 123.4 units.    surface area = 131,874.537977 square units

volume = 4,099,581.395236 cubic units    surface/volume ratio = 0.032168

<u>New method for this project</u>

<ul>

 <li><u>getCount: A static method that accepts no parameters and returns an int representing</u> <u>the static count field</u>.   o <u>resetCount:  A static method that returns nothing, accepts no parameters, and sets the</u> <u>static count field to zero</u>.</li>

 <li><u>equals: An instance method that accepts a parameter of type Object and returns false if</u> <u>the Object is a not an Icosahedron; otherwise, when cast to an Icosahedron, if it has the</u> <u>same field values as the Icosahedron upon which the method was called. Otherwise, it</u> <u>returns false</u>. Note that this equals method with parameter type Object will be called by the JUnit Assert.assertEquals method when two Icosahedron objects are checked for equality.</li>

</ul>




Below is a version you are free to use.

public boolean equals(Object obj) {

if (!(obj instanceof Icosahedron)) {          return false;

}       else {

Icosahedron d = (Icosahedron) obj;

return (label.equalsIgnoreCase(d.getLabel())                             &amp;&amp; color.equalsIgnoreCase(d.getColor())

&amp;&amp; Math.abs(edge – d.getEdge()) &lt; .000001);

}

}

o <u>hashCode(): Accepts no parameters and returns zero of type int.  This method is</u> <u>required by Checkstyle if the </u><u>equals method above is implemented.</u>




<strong>Code and Test</strong>: As you implement the methods in your Icosahedron class, you should compile it and then create test methods as described below for the IcosahedronTest class.




<ul>

 <li><strong>IcosahedronTest<u>.java</u> </strong></li>

</ul>




<strong>Requirements</strong>: <u>Create an IcosahedronTest class that contains a set of <em>test</em> methods to test each of</u> <u>the methods in Icosahedron.</u>




<strong>Design</strong>: <u>Typically, in each test method, you will need to create an instance of Icosahedron, call</u> <u>the method you are testing, and then make an assertion about the expected result and the actual</u> <u>result (note that the actual result is commonly the result of invoking the method unless it has a</u> <u>void return type).  You can think of a test method as simply formalizing or codifying what you</u> <u>have been doing in interactions to make sure a method is working correctly.  That is, the sequence</u> <u>of statements that you would enter in interactions to test a method should be entered into a single</u> <u>test method.  You should have at least one test method for each method in Icosahedron, except for</u> <u>associated getters and setters which can be tested in the same method.  However, if a method</u> <u>contains conditional statements (e.g., an <em>if</em> statement) that results in more than one distinct</u> <u>outcome, you need a test method for each outcome.  For example, if the method returns boolean,</u> <u>you should have one test method where the expected return value is false and another test method</u> <u>that expects the return value to be true (also, each condition in boolean expression must be</u> <u>exercised true and false).  Collectively, these test methods are a set of test cases that can be</u> <u>invoked with a single click to test all of the methods in your Icosahedron class</u>.

<strong> </strong>

<strong>Code and Test</strong>: <u>Since this is the first project requiring you to write JUnit test methods, a good</u> <u>strategy would be to begin by writing test methods for those methods in Icosahedron that you</u> <u>“know” are correct.  By doing this, you will be able to concentrate on the getting the test methods</u> <u>correct.  That is, if the test method <em>fails</em>, it is most likely due to a defect in the test method itself</u> <u>rather the Icosahedron method being testing.  As you become more familiar with the process of</u> <u>writing test methods, you will be better prepared to write the test methods for the new methods in</u> <u>Icosahedron.  Be sure to call the Icosahedron toString method in one of your test cases so that</u> <u>Web-CAT will consider the toString method to be “covered” in its coverage analysis.  Remember</u> <u>that you can set a breakpoint in a JUnit test method and run the test file in Debug mode.  Then,</u> <u>when you have an instance in the Debug tab, you can unfold it to see its values or you can open a</u> <u>canvas window and drag items from the Debug tab onto the canvas</u>.







<ul>

 <li><strong>java </strong>(a modification of the <strong>IcosahedronList2 </strong>class in the previous project; <u>new requirements are underlined below</u>)</li>

</ul>




<strong>Requirements</strong>: Create an IcosahedronList2 class that stores the name of the list and an array of Icosahedron objects, and the number of Icosahedron objects in the array.  It also includes methods that return the name of the list, number of Icosahedron objects in the IcosahedronList2, total surface area, total volume, average surface area, average volume, and average surface to volume ratio for all Icosahedron objects in the IcosahedronList2.  The toString method returns a String containing the name of the list followed by each Icosahedron in the array, and a summaryInfo method returns summary information about the list (see below).




<strong>Design</strong>:  The IcosahedronList2 class has <u>three fields</u>, a constructor, and methods as outlined below.




<ul>

 <li><strong>Fields</strong> (or instance variables): (1) a String representing the name of the list, (2) an array of Icosahedron objects, and (3) an int representing the number of Icosahedron objects in the Icosahedron array. These are the only fields (or instance variables) that this class should have.</li>

 <li><strong>Constructor</strong>: Your IcosahedronList2 class must contain a constructor that accepts a parameter of type String representing the name of the list, a parameter of type</li>

</ul>

Icosahedron[], representing the list of Icosahedron objects, and a parameter of type int representing the number of Icosahedron objects in the Icosahedron array.  These parameters should be used to assign the fields described above (i.e., the instance variables).

<strong> </strong>

<ul>

 <li><strong>Methods</strong>: The methods for IcosahedronList2 are described below. o getName: Returns a String representing the name of the list.</li>

</ul>

<ul>

 <li>numberOfIcosahedrons: Returns an int representing the number of Icosahedron objects in the IcosahedronList2.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalSurfaceArea: Returns a double representing the total surface areas for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>totalVolume: Returns a double representing the total volumes for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageSurfaceArea: Returns a double representing the average surface area for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>averageVolume: Returns a double representing the average volume for all</li>

</ul>

Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong>

<ul>

 <li>averageSurfaceToVolumeRatio: Returns a double representing the average surface to volume ratio for all Icosahedron objects in the list.  If there are zero Icosahedron objects in the list, zero should be returned. <strong> </strong></li>

 <li>toString: Returns a String (does <u>not</u> begin with 
) containing the name of the list followed by each Icosahedron in the list.  In the process of creating the return result, this toString() method should include a while loop that calls the toString() method for each Icosahedron object in the list (adding a 
 before and after each).  Be sure to include appropriate newline escape sequences.  For an example, see <u>lines 2 through 19</u> in the output below from IcosahedronList2App for the <em>txt</em> input file. [<u>Note</u> <u>that the toString result should <strong>not</strong> include the return value of summaryInfo()</u>.]</li>

 <li>summaryInfo: Returns a String (does<u> not </u>begin with 
) containing the name of the list (which can change depending of the value read from the file) followed by various summary items:  number of Icosahedrons, total surface area, total volume, average surface area, average volume, and average surface to volume ratio.  Use “#,##0.0##” as the pattern to format the double values.</li>

 <li>getList: Returns the array of Icosahedron objects (the second field above).</li>

 <li>readFile: Takes a String parameter representing the file name, reads in the file, storing the list name and creating an array of Icosahedron objects, uses the list name, the array, and number of Icosahedron objects in the array to create an IcosahedronList2 object, and then returns the IcosahedronList2 object.  See note #1 under <u>Important</u> <u>Considerations</u> for the IcosahedronList2MenuApp class (last page) to see how this method should be called. <strong> </strong></li>

 <li>addIcosahedron: Returns nothing but takes three parameters (label, color, and edge), creates a new Icosahedron object, and adds it to the IcosahedronList2 object.</li>

 <li>findIcosahedron: Takes a label of an Icosahedron as the String parameter and returns the corresponding Icosahedron object if found in the IcosahedronList2 object; otherwise returns null.  <u>Case should be ignored when attempting to match the label</u>.</li>

 <li>deleteIcosahedron: Takes a String as a parameter that represents the label of the Icosahedron and returns the Icosahedron if it is found in the IcosahedronList2 object and deleted; otherwise returns null.  <u>Case should be ignored when attempting to match the</u> <u>label; consider calling/using </u><u>findIcosahedron in this method</u>.  When an element is deleted from an array, elements to the right of the deleted element must be shifted to the left. After shifting the items to the left, the last Icosahedron element in the array should be set to null.  Finally, the number of elements field must be decremented.</li>

 <li>editIcosahedron: Takes three parameters (label, color, and edge), uses the label to find the corresponding the Icosahedron object in the list.  If found, sets the color and edge to the values passed in as parameters, and returns true.  If not found, returns false.</li>

</ul>

<strong> </strong>

<u>New method for this project</u> <strong> </strong>

<ul>

 <li><u>find</u>Icosahedron<u>WithShortestEdge</u><u>: Returns the Icosahedron with the</u> <u>shortest edge; if the list contains no Icosahedron objects, returns null</u>.</li>

 <li><u>find</u>Icosahedron<u>WithLongestEdge</u><u>: Returns the Icosahedron with the longest</u> <u>edge; if the list contains no Icosahedron objects, returns null</u>.</li>

 <li><u>find</u>Icosahedron<u>WithSmallestVolume</u><u>: Returns the Icosahedron with the</u> <u>smallest volume; if the list contains no Icosahedron objects, returns null</u>.</li>

 <li><u>find</u>Icosahedron<u>WithLargestVolume</u><u>: Returns the Icosahedron with the</u> <u>largest volume; if the list contains no Icosahedron objects, returns null</u>.</li>

</ul>

<strong> </strong>

<strong>Code and Test</strong>: Remember to import java.util.Scanner, java.io.File, java.io.IOException.  These classes will be needed in the readFile method which will require a throws clause for IOException.

Some of the methods above require that you use a loop to go through the objects in the array.  You may want to implement the class below in parallel with this one to facilitate testing.  That is, after implementing one to the methods above, you can implement the corresponding test method in the test file described below.




<ul>

 <li><strong><u>IcosahedronList2Test.java</u> </strong></li>

</ul>




<strong>Requirements</strong>: <u>Create an IcosahedronList2Test class that contains a set of <em>test</em> methods to test</u> <u>each of the methods in IcosahedronList2.</u>




<strong>Design</strong>: <u>Typically, in each test method, you will need to create an instance of IcosahedronList2,</u> <u>call the method you are testing, and then make an assertion about the expected result and the</u> <u>actual result (note that the actual result is usually the result of invoking the method unless it has a</u> <u>void return type).  You can think of a test method as simply formalizing or codifying what you</u> <u>have been doing in interactions to make sure a method is working correctly.  That is, the sequence</u> <u>of statements that you would enter in interactions to test a method should be entered into a single</u> <u>test method.  You should have at least one test method for each method in IcosahedronList2.</u>  <u>However, if a method contains conditional statements (e.g., an <em>if</em> statement) that results in more</u> <u>than one distinct outcome, you need a test method for each outcome.  For example, if the method</u> <u>returns boolean, you should have one test method where the expected return value is false and</u> <u>another test method that expects the return value to be true.  Collectively, these test methods are a</u> <u>set of test cases that can be invoked with a single click to test all of the methods in your</u> <u>IcosahedronList2 class</u>.

<strong> </strong>

<strong>Code and Test</strong>: <u>Since this is the first project requiring you to write JUnit test methods, a good</u> <u>strategy would be to begin by writing test methods for those methods in IcosahedronList2 that</u> <u>you “know” are correct.  By doing this, you will be able to concentrate on the getting the test</u> <u>methods correct.  That is, if the test method <em>fails</em>, it is most likely due to a defect in the test</u> <u>method itself rather the IcosahedronList2 method being testing.  As you become more familiar</u> <u>with the process of writing test methods, you will be better prepared to write the test methods for</u> <u>the new methods in IcosahedronList2.  Be sure to call the IcosahedronList2 toString method in</u> <u>one of your test cases so that Web-CAT will consider the toString method to be “covered” in its</u> <u>coverage analysis.  Remember that you can set a breakpoint in a JUnit test method and run the</u> <u>test file in Debug mode.  Then, when you have an instance in the Debug tab, you can unfold it to</u> <u>see its values or you can open a canvas window and drag items from the Debug tab onto the</u> <u>canvas</u>.




<strong><u>Important</u></strong><u>: When comparing two arrays for equality in JUnit, be sure to use</u>

<u>Assert.assertArrayEquals rather than Assert.assertEquals</u>.  Assert.assertArrayEquals will return true only if the two arrays are the same length and the elements are equal based on an element by element comparison using the appropriate equals method.