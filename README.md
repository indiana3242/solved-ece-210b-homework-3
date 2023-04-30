Download Link: https://assignmentchef.com/product/solved-ece-210b-homework-3
<br>



In this homework, you will review logical indexing in MATLAB, a very important technique used to efficiently index a matrix or vector. You will also have a chance to work with functions in a separate file.

<ol>

 <li><strong>Roll the Dice </strong>In this part you will work with <em>imshow </em>and logical indexing.</li>

</ol>

<ul>

 <li>Create 100×100 matrices A, B and C of all ones.</li>

 <li>In matrix A, set the values of the entries <em>a<sub>ij </sub></em>equal to zero if <sup>p</sup>(<em>i </em>− 25)<sup>2 </sup>+ (<em>j </em>− 75)<sup>2 </sup><em>&lt; </em>10</li>

</ul>

<em>or </em><sup>p</sup>(<em>i </em>− 75)<sup>2 </sup>+ (<em>j </em>− 25)<sup>2 </sup><em>&lt; </em>10. (<strong>Hint: </strong>Use <em>meshgrid </em>to create the indices, then logical indexing on A using |, &amp; or˜).

<ul>

 <li>In matrix B, set the values of the entries <em>b<sub>ij </sub></em>equal to zero if <sup>p</sup>(<em>i </em>− 25)<sup>2 </sup>+ (<em>j </em>− 25)<sup>2 </sup><em>&lt; </em>10</li>

</ul>

<em>or </em><sup>p</sup>(<em>i </em>− 75)<sup>2 </sup>+ (<em>j </em>− 75)<sup>2 </sup><em>&lt; </em>10.

<ul>

 <li>In matrix C, set the values of the entries <em>c<sub>ij </sub></em>equal to zero if <sup>p</sup>(<em>i </em>− 50)<sup>2 </sup>+ (<em>j </em>− 50)<sup>2 </sup><em>&gt; </em></li>

 <li>Now use <em>figure </em>and <em>imshow </em>to plot:</li>

</ul>

<strong>– </strong>The complement of C

<h1>– A</h1>

<strong>– </strong>The next 3 faces of a die (so 3-5) on three separate figures. Use whatever logical operations (&amp;, |, or˜) are necessary to accomplish this.

<ol start="2">

 <li><strong>Fun with find </strong>Write a function to return the value and index of a number in a vector / matrix that is closest to a desired value. The function should be called as [<em>val,ind</em>] = <em>findClosest</em>(<em>x,desiredV alue</em>). This function can be accomplished in less than five lines. You will find <em>abs</em>, <em>min </em>and/or <em>find </em>useful, <strong>Hint</strong>: You may have some trouble using <em>min </em>when x is a matrix. To convert the matrix to a vector, you can use <em>y </em>= <em>x</em>(:). Show that it works by finding the value closest to 3<em>/</em>2 (and index of said value) in <em>sin( linspace(0,5,100) ) + 1</em>.</li>

 <li><strong>Calculus Nostalgia </strong>This problem will reacquaint you with the first derivative test and points of inflection.

  <ul>

   <li>Write a function, called <em>signSwitch</em>, in a separate file which inputs a vector <em>v </em>and outputs a vector with the indices <em>i </em>which represent a sign change in <em>v</em>; i.e. report 15 if the sign changed in <em>v </em>between index 14 and index 15. Do not consider going from positive or negative to zero. We could loop through and check this condition at every point – don’t do that. Instead think of a way to use logical indexing: One suggestion is to write conditions on the vector and some kind of shifted version of itself. Beware however, when you do this you will have non-overlapping points. It is up to you to figure out what to with them. This will be a local function (see the documentation if you forgot what this means).</li>

   <li>Now we will write the main function, call it whatever you’d like, which will perform all the analysis. The function will input two vectors representing the x and y coordinates of the graph of the function and will return a vector with the approximate indices of the local extrema and a vector with the approximate indices of the points of inflection.</li>

   <li>First have the function take the first derivative (approximately, see homework 2). Then use your local function to apply the first derivative test to see where the approximate local minima and maxima are.</li>

  </ul></li>

</ol>

1

ECE-210B Homework 3

<ul>

 <li>Next, have the function take the second derivative. Then use your local function again to find approximately where the points of inflection are.</li>

 <li>Finally, have the function plot all this information using <em>figure </em>then <em>plot(x,y,xminmax,yminmax,’ko’,xpoi,ypoi,’r*’)</em>. This will plot the function then plot black circles on the local minima and maxima and red stars on the points of inflection.</li>

 <li>Apply your function to <em>x</em><sup>5 </sup>− 8<em>x</em><sup>3 </sup>+ 10<em>x </em>+ 6 sampled at 10000 points on [-3,3].</li>

</ul>


