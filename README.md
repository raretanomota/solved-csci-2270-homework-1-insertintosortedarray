Download Link: https://assignmentchef.com/product/solved-csci-2270-homework-1-insertintosortedarray
<br>



<strong>1A.</strong>​ ​<u>Write a function called <strong>insertIntoSortedArray</strong></u><u>​ </u>.<u>​</u>

<ol>

 <li>It should take ​<strong>three </strong>​arguments –

  <ol>

   <li>myArray[ ] :​ ​<em>sorted</em>​ array that should be able to hold at most 100 integers.</li>

   <li>numEntries : the number of elements inserted so far.</li>

   <li>newValue : the incoming value to be inserted into the sorted array (i.e.</li>

  </ol></li>

</ol>

myArray[]).

<ol>

 <li>The ​<strong>insertIntoSortedArray</strong>​ function should return a count of the elements inserted so</li>

</ol>

far (i.e. the current size of the array).This function is defined as follows:

<strong>int</strong>​ ​<strong>insertIntoSortedArray</strong>​(​<strong>int</strong>​ myArray[], ​<strong>int</strong>​ numEntries, ​<strong>int</strong>​ newValue);

31, August 2019

<strong>1 B. </strong>​<u>Write a </u><u>​<strong>complete program</strong> to do the following</u><u>​ <strong> :</strong></u><u>​</u><strong>  </strong>

<ol>

 <li><strong>Reading the file: </strong>​Your program should take a single command line argument i.e. the</li>

</ol>

name of the file where the integers are present.

<ol>

 <li>This file needs to be stored in the same directory as your program.</li>

 <li>The file should store up to 100 integers on separate lines. You can use the file named​<em> “</em>​<strong><em>txt</em></strong>​<em>”</em>​ on Moodle, or create your own if you prefer.</li>

 <li><strong>In the main function: </strong>

  <ol>

   <li>Create an array of integers to store at most 100 integers.</li>

   <li>Open the file that was passed via the command line</li>

   <li>If there is any error in opening the file then print the below statement <em>std::cout &lt;&lt; “Failed to open the file.” &lt;&lt; std::endl;</em></li>

   <li>Use the ​<strong>getline</strong>​ function to read the integers one by one.</li>

   <li>Store these integers in a sorted array by passing them to the <strong>insertIntoSortedArray</strong>​ function (you can use the code from part 1A).</li>

   <li>Each time a new number is read, print out the entire array after insertion.</li>

  </ol></li>

</ol>

The Input and Output formats are shown below:

<strong>Testcase 1: </strong>

<strong>FileContents: arr.txt </strong>

1

6

2

12

5

<strong>Your Output: </strong>

1

1, 6

1, 2, 6

1, 2, 6, 12

1, 2, 5, 6, 12

31, August 2019

Problem 2

<strong>Overview:</strong>​ In this question, you will write a program that:

<ol>

 <li>Reads a ​<strong>“.csv”</strong> file with up to 100 lines and columns containing information on national parks.</li>

 <li>Stores the information in an array of structs.</li>

 <li>Write the lines where the ​<strong>area of the park </strong>is​ greater than the minimum value into the <strong>output</strong>​ ​<strong>.csv</strong>​</li>

 <li>Prints the content of the entire array.</li>

</ol>

<strong>Specifics: </strong>

Create an array that holds the ​<strong>Park struct objects</strong>​. Use the following struct declaration:

<strong>struct</strong>​ ​<strong>Park </strong>​{ <strong>string</strong>​ parkname; <strong>string </strong>​state; <strong>int</strong>​ area;

};

<strong>2A</strong>​.  Write a function named <strong>addPark:</strong>​

<ol>

 <li>The ​<strong>addPark</strong>​ function has the following signature:</li>

</ol>

<strong>// length: Number of items currently stored in the array </strong><strong>void addPark(Park </strong>​<strong>parks[]</strong>​<strong>, string </strong><strong>parkname</strong>​             ​<strong>, string </strong>​<strong>state</strong>​<strong>, int </strong>​<strong>area</strong>​<strong>, int </strong><strong>length</strong>​<strong>); </strong>

<ol>

 <li>Instantiate a struct and store the​<strong> parkname, state</strong>​, ​<strong>area </strong>values in it.​</li>

 <li>Add the struct to the ​<strong>parks </strong>​</li>

</ol>

<strong>2B</strong>​.  Write a function named <strong>printList:</strong>​

<ol>

 <li>The​<strong> printList</strong>​ function has the following signature:</li>

</ol>

<strong>// length: Number of items in the array </strong>

<strong>void</strong>​ ​<strong>printList</strong>​(​<strong>const</strong>​ ​<strong>Park </strong>​<strong>parks[]</strong>​<strong>, int </strong>​<strong>length</strong>​);

<ol>

 <li>Loop through the ​<strong>parks</strong>​</li>

 <li>Print out each element of the ​<strong>parks</strong>​ array in the following format.</li>

</ol>

“&lt;PARKNAME&gt; [&lt;STATE&gt;] area: &lt;AREA&gt;” using the below cout statement




std::​<em>cout &lt;&lt; park.parkname &lt;&lt;” [” &lt;&lt; park.state &lt;&lt; “] area: “&lt;&lt; park.area &lt;&lt; </em>

<em>std::endl;</em>

<strong>                        Example, </strong>“Acadia National Park  [ME] area: 47390”​







<strong>2C</strong>​.  ​<u>Write a </u><u>​<strong>complete program</strong></u><u>​ which includes the following</u><u>​<strong>:</strong></u>

<ol>

 <li>The ​<strong>park</strong><u>​ </u>​struct and the ​<strong>addPark, printList </strong>​functions coded above.</li>

 <li>A <strong>main()</strong>​ function defined as below:​      <strong>             </strong>

  <ol>

   <li>Your ​<strong>main() </strong>​should handle three command line arguments: the name of the <strong>input</strong> “​<strong>.csv” file</strong>​, the name of the ​<strong>output</strong> “​<strong>.csv” file</strong> and a ​<strong>minimum area </strong>respectively​<strong>.</strong></li>

   <li>Input and output files need to be stored in the same directory as your program.</li>

   <li>Read from the input file, “​<strong><em>csv</em></strong>​” :

    <ol>

     <li>Each line of the file can be read using <strong>getline </strong>​ ​</li>

     <li>Parse each line using ​<strong>stringstream</strong> and convert each entry into its appropriate data type. <strong>parkname</strong>​ should be a string, <strong>state</strong>​ should​ be a string, and ​<strong>area </strong>​should be an integer. ​<em>(Hint: Use </em>​<strong><em>stoi, stof</em></strong><em> functions to convert from strings to numbers)</em></li>

     <li>Call ​<strong>addPark</strong>​ function to update the ​<strong>parks</strong>​</li>

    </ol></li>

   <li>Call the ​<strong>printList </strong>​function after the array has been filled with data.</li>

   <li>Write into ​<strong>output</strong>​ ​<strong>“.csv”</strong> file:​

    <ol>

     <li>Write the &lt;parkname&gt;, &lt;state&gt;, &lt;area&gt; of the parks, whose</li>

    </ol></li>

  </ol></li>

</ol>

&lt;area&gt; is more than the ​<strong>minimum_area</strong> (read from command line) into the ​<strong>output “.csv”</strong>​ file.

<ol start="6">

 <li>Make sure you close the file when you are done.</li>

</ol>







<strong>Check next page for sample input and output. </strong>




























<strong><em> </em></strong>

Assignment 1

31, August 2019




<strong>Sample Input and Output: </strong>

<strong>Testcase 1:</strong>

​<strong>File Contents: data.csv  </strong>

Acadia National Park, ME, 47390

Arches National Park, UT, 76519

Badlands National Park, SD, 242756

Big Bend National Park, TX, 801163

Biscayne National Park, FL, 172924




​<strong>Your print Output: </strong>

Acadia National Park [ME] area: 47390

Arches National Park [UT] area: 76519

Badlands National Park [SD] area: 242756

Big Bend National Park [TX] area: 801163

Biscayne National Park [FL] area: 172924




<strong>Your output.csv file with minimum area 200000 should contain the following: </strong>

Badlands National Park, SD, 242756

Big Bend National Park, TX, 801163


