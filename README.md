Download Link: https://assignmentchef.com/product/solved-16-811-math-fundamentals-for-robotics-1
<br>



<ol>

 <li>Implement the <em>PA </em>= <em>LDU </em>decomposition algorithm discussed in class. Do so yourself (in other words, do not merely use predefined Gaussian elimination code in MatLab or Python).</li>

</ol>

Simplifications: (i) You may assume that the matrix <em>A </em>is square and invertible. (ii) Do not worry about column interchanges, just row interchanges.

Demonstrate that your implementation works properly on some examples.

<ol start="2">

 <li>Compute the <em>PA </em>= <em>LDU </em>decomposition and the SVD decomposition for each of the following matrices: (In fact, here it is enough to let <em>P </em>be an identity matrix, so <em>A </em>= <em>LDU</em>.)</li>

</ol>

You may use any method or tools you wish to solve this problem, including pre-defined routines from MatLab or Python, your code, and/or hand calculations. (Hand calculations may be easiest for computing the <em>PA </em>= <em>LDU </em>decompositions of these examples. We recommend using pre-defined code to compute the SVD decompositions.) Show how you obtained your solutions, that is, show your work.

<ol start="3">

 <li>Solve the systems of equations <em>Ax </em>= <em>b </em>for the values of <em>A </em>and <em>b </em>given below.</li>

</ol>

For each system, specify whether the system has zero, one, or many exact solutions. If a system has zero exact solutions, give “the SVD solution” (as defined in class) and explain what this solution means. If a system has a unique exact solution, compute that solution. If a system has more than one exact solution, specify both “the SVD solution” and all solutions, using properties of the SVD decomposition of the matrix <em>A</em>, as discussed in class. Show your work, including verifying that your answers are correct.

<table width="276">

 <tbody>

  <tr>

   <td width="63">(a)</td>

   <td width="66"></td>

   <td width="22">657</td>

   <td width="53"></td>

   <td width="72"></td>

  </tr>

  <tr>

   <td width="63">(b)</td>

   <td width="66"></td>

   <td width="22">633</td>

   <td width="53"></td>

   <td width="72"></td>

  </tr>

  <tr>

   <td width="63">(c)</td>

   <td width="66"></td>

   <td width="22">633</td>

   <td width="53"></td>

   <td width="72"></td>

  </tr>

 </tbody>

</table>

Explain the difference/similarity of the answers for parts (b) and (c) in terms of the column and null spaces provided by the SVD decomposition of <em>A</em>.

1

<ol start="4">

 <li>Suppose that <em>u </em>is an <em>n</em>-dimensional column vector of unit length in <em><sup>n</sup></em>, and let <em>u<sup>T </sup></em>be its transpose. Then <em>uu<sup>T </sup></em>is a matrix. Consider the <em>n </em>× <em>n </em>matrix <em>A </em>= <em>I </em>− <em>uu<sup>T</sup></em>.

  <ul>

   <li>Describe the action of the matrix <em>A </em></li>

   <li>Give the eigenvalues of <em>A</em>.</li>

   <li>Describe the null space of <em>A</em>.</li>

   <li>What is <em>A</em><sup>2</sup>?</li>

  </ul></li>

</ol>

(As always, show your work.)

<ol start="5">

 <li>The following problem arises in a large number of robotics and vision problems: Suppose<strong>p</strong><sub>1</sub><em>,…,</em><strong>p</strong><em><sub>n </sub></em>are the 3D coordinates of <em>n </em>points located on a rigid body in three-space. Suppose further that <strong>q</strong><sub>1</sub><em>,…,</em><strong>q</strong><em><sub>n </sub></em>are the 3D coordinates of these same points after the body has been translated and rotated by some unknown amount. Derive an algorithm in which SVD plays a central role for inferring the body’s translation and rotation. (You may assume that the coordinate values are precise not noisy, but see comment and caution below.) Show that your algorithm works correctly by running it on some examples.</li>

</ol>

<strong>Comment: </strong>Your algorithm should make use of all the information available. True, in principle you only need three pairs of points – but if you use more points your solution will be more robust, something that might come in handy some day when you need to do this for real with noisy data.

<strong>Caution: </strong>A common mistake is to derive an algorithm that finds the best affine transformation, rather than the best rigid body transformation. Even though you may assume precise coordinate values, imagine how your algorithm would behave with noise. Your algorithm should still produce a rigid body transformation.

<strong>One more comment: </strong>This problem requires some thought. You can probably find a solution on the web or in a vision text book. Try to solve it yourself before looking at any such sources. Spend some time on the problem. It is good practice to develop your analytic skills. Feel free to discuss among yourselves. (As always, cite any sources, including discussions with others.)

Consider the hints below. <strong>Hint #1: </strong>Suppose for a moment that both sets of points have the origin as centroid. Assemble all the points {<strong>p</strong><em><sub>i</sub></em>} into a matrix <em>P </em>and all the points {<strong>q</strong><em><sub>i</sub></em>} into another matrix <em>Q</em>. Now think about the relationship between <em>P </em>and <em>Q </em>and also consider matrix products involving <em>P </em>and <em>Q</em>.

<strong>Hint #2: </strong>There are different approaches to this problem. In one approach, you may find the following fact useful (assuming the dimensions are sensible):

<em>x<sup>T</sup>R<sup>T</sup>y </em>= Tr(<em>Rxy<sup>T</sup></em>)<em>.</em>

[Here <em>x </em>and <em>y </em>are column vectors (e.g., 3D vectors) and <em>R </em>is a matrix (e.g., a 3×3 rotation matrix). The superscript <em>T </em>means <em>transpose</em>, so <em>xy<sup>T </sup></em>is a matrix as well. And Tr is the <em>trace </em>operator that adds up the diagonal elements of its square matrix argument.]


