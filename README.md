Download Link: https://assignmentchef.com/product/solved-cs-202-computer-science-ii-project-11
<br>



<strong> </strong>




<strong>Objectives:  </strong>The main objectives of this project is to introduce you to recursion, and test your ability to work with some STL functionalities. A review of your knowledge on working with templates, dynamic data structures, as well as manipulating dynamic memory, classes, pointers and iostream to all extents, is also included.




<strong>Description: </strong>

For the entirety of this project, you will work with STL <strong>std::vectors</strong>. You are free to implement any of the standard-provided functionalities with the <strong>&lt;vector&gt;</strong> libraries. For the first part of this assignment, you will create three recursive functions:













<ol>

 <li><strong>The</strong> <strong>vector_resort</strong> <strong>Function (Recursive Sort) </strong></li>

</ol>




<u>Parameters List:</u> Takes in a <strong>std::vector</strong> by-Reference. Note that a <strong>std::vector</strong> as part of the STL is a templated construct, hence the function will itself also need to be templated. <em>Hint</em>: This is the base parameter requirement. Any other parameters necessary for the function will depend on your specific implementation.

<u>Functionality:</u> The function will have to perform Recursive Sorting of the vector elements. You may implement whichever sorting variant you wish (from the ones introduced in the Lab sections or any other established variant). Note: One of the most powerful naturally-recursive sorting

algorithms is Quicksort (<u>https://en.wikipedia.org/wiki/Quicksort</u>)

<u>Output:</u> Nothing, since the <strong>std::vector</strong> is passed by reference it should be sorted at the return of the <strong>vector_resort</strong> function.













<ol>

 <li><strong>The</strong> <strong>vector_research</strong> <strong>Function (Recursive Binary Search) </strong></li>

</ol>




<u>Parameters List:</u> Takes in a <strong>std::vector</strong> by-Reference, which has to be already sorted. Note that a <strong>std::vector</strong> as part of the STL is a templated construct, hence the function will itself also need to be templated. The function also takes in a const T&amp; value, which is the one that is searched. <em>Hint</em>: These are the base parameter requirements. Any other parameters necessary for the function will depend on your specific implementation.

<u>Functionality:</u> The function will have to perform Recursive Binary Search

(<u>https://en.wikipedia.org/wiki/Binary_search_algorithm</u>) as introduced during the class Lectures, for the provided value in the <strong>std::vector</strong>. A Binary Search is performed as follows: Pick the value in the middle of the container (the pivot); if the search item is less than the pivot narrow the search to the bottom half of the container, otherwise search the top half of the container. This is done recursively until the item is found and the index (since <strong>std::vectors</strong> can have index-based access) where it is found is returned. (Return ‐1 if the item is not found).

<u>Output:</u> The index (since <strong>std::vectors</strong> can have index-based access) where the value is found is returned. (Return ‐1 if the item is not found). Extra: You may also devise an implementation that

returns <strong>std::vector&lt;T&gt;::iterator</strong> to the element in question (Return <strong>std::vector&lt;T&gt;::end()</strong> if the item is not found, not <strong>NULL</strong> – iterators are not generally pointers and should not be treated as such).




For the second part of this assignment, you will implement the following functionalities:

<ul>

 <li>Create a <strong>vecInt</strong>, which will be <strong>std::vector</strong> of <strong>int</strong>s, and fill it with 100 random <strong>int </strong>numbers which will be read from the provided file RandomData.txt. User input is not mandatory, and hard-coding the file name is allowed for this Project.</li>

</ul>

(Note: If you wish to test with your own randomly ordered numbers, you may use <strong>std::rand()</strong> (<u>http://en.cppreference.com/w/cpp/numeric/random/rand</u>) to do this).

<ul>

 <li>Create a <strong>vecIntCpy</strong>, which will be another <strong>std::vector</strong> of <strong>int</strong>s, which should be a copy of the previously created one.</li>

 <li>Apply <strong>vector_resort</strong> and <strong>vector_research</strong> on <strong>vecInt</strong>.</li>

 <li>Print out (only to terminal) the resulting <strong>vecInt</strong>.</li>

 <li><strong>Extras (not required for 100pt grade):</strong> Try <strong>std::sort</strong> and <strong>std::binary_search</strong></li>

</ul>

(<u>http://en.cppreference.com/w/cpp/algorithm/sort</u> <u>http://en.cppreference.com/w/cpp/algorithm/binary_search</u>) to perform the same tasks on the <strong>vecIntCpy</strong> container. Time the difference between your implementation and the STL one; you may perform high-resolution time-difference counting with (<u>http://en.cppreference.com/w/cpp/chrono/high_resolution_clock/now</u>):

<strong>std::chrono::time_point&lt;std::chrono::system_clock&gt; t1 = std::chrono::system_clock::now(); </strong>

<strong>//tasks to time… std::chrono::time_point&lt;std::chrono::system_clock&gt; t2 = std::chrono::system_clock::now(); std::chrono::duration&lt;double&gt; diff = t2-t1; std::cout &lt;&lt; diff.count() &lt;&lt; std::endl; </strong>




You will create the necessary VectorRecursion.h header file that will contain the <strong>templated functions’ declarations and implementations</strong>. You should also create a source file proj11.cpp which will implement the above required functionalities (File Input, populating the vectors, calling the recursive functions, Terminal Output, etc…).




<strong>If you cannot get past the </strong><strong>vector_resort function to proceed to </strong><strong>vector_research, you may use std::sort to order the elements of </strong><strong>vecInt. In such a case, only partial credit will be awarded. </strong>

<strong> </strong>

<strong>Suggestion(s): First try to implement the recursive sorting and binary search function on simple int arrays. Create the test driver for your code and verify that it works. Only then move on to write std::vector and template-based generic versions for your two functions. </strong>




<strong>The completed project should have the following properties: </strong> Ø Written, compiled and tested using Linux.

<ul>

 <li>It must compile successfully on the department machines using Makefile(s), which will be invoking the g++ compiler. Instructions how to remotely connect to department machines are included in the Projects folder in WebCampus.</li>

 <li>The code must be commented and indented properly.</li>

</ul>

Header comments are required on all files and recommended for the rest of the program. Descriptions of functions commented properly.

<ul>

 <li>A one page (minimum) typed sheet documenting your code. This should include the overall purpose of the program, your design, problems (if any), and any changes you would make given more time.</li>

</ul>

<strong> </strong>

<strong>Turn in:</strong> Compressed Header &amp; Source files, Makefile(s), and project documentation.


























