Download Link: https://assignmentchef.com/product/solved-ee559-homework-7-the-primal-lagrangian-and-derive-the-dual-lagrangian
<br>
. In the parts below, you will set up the primal Lagrangian and derive the dual Lagrangian, for support vector machine classifier, for the case of data that is separable in expanded feature space.

For the SVM learning, we stated the optimization problem for the linearly separable (in <em><sub> </sub></em><em><u>u</u></em>-space) case, as:

Minimize <em>J</em>(<em><u>w</u></em>)= <u><sup>1</sup></u><sub>2 </sub><em><u>w </u></em><sup>2             </sup><sub>  </sub>

s.t. <em>z<sub>i </sub></em>(<em><u>w</u><sup>T</sup><u>u</u><sub>i </sub></em>+ <em>w</em><sub>0</sub>)−1≥ 0 ∀<em>i</em>

<em> </em>

Assume our data is linearly separable in the expanded feature space.  Also, nonaugmented notation is used throughout this problem.

<ul>

 <li>If the above set of constraints (second line of equations above) is satisfied, will all the training data be correctly classified?</li>

 <li>Write the Lagrangian function <em>L</em>(<em><u>w</u></em>,<em>w</em><sub>0</sub>,<u>λ</u>) for the minimization problem stated above.  Use  <em> </em>λ<em><sub>i</sub></em>, <em>i </em>=1, 2,!, <em>N</em> for the Lagrange multipliers.  Also state the KKT conditions.  <strong>(Hint:</strong>  there are 3 KKT conditions).</li>

 <li>Derive the dual Lagrangian <em>L<sub>D </sub></em>, by proceeding as follows:

  <ul>

   <li>Minimize <em>L</em>  r.t. the weights.</li>

  </ul></li>

</ul>

<strong>Hint:</strong> solve <em> </em>∇<em><u><sub>w</sub></u>L </em>= <u>0</u> for the optimal <sup>weight </sup><em><sub> </sub></em><em><u>w</u></em>* (<sup>in terms of </sup><em><sub> </sub></em>λ<em><sub>i</sub></em> and other

variables); and set <u>∂</u><em>L </em>= 0 and simplify.

<em> </em>∂<em>w</em>0

<ul>

 <li>Substitute your expressions from part (i) into <em>L</em>, and use your expression from</li>

</ul>

∂<u><sup>∂</sup></u><em>w</em><em><sup>L</sup></em>0 = 0 as a new constraint, to derive <em><sub> </sub>L<sub>D</sub></em> as:

<em> </em>

⎡ <em>N    N                        </em><em><sub>T       </sub></em>⎤       <em>N</em>

<em>L</em><em>D</em>λ<em>i</em>λ<em>jz</em><em>iz </em><em>j<u>u</u></em><em>i <u>u </u></em><em>j </em>⎥ + ∑λ<em>i</em>

<em><sub>                       </sub></em>⎣⎢<em>i</em>=1 <em>j</em>=1                              <sup>⎥</sup>⎦      <em>i</em>=1

<em>N</em>

subject to the (new) constraint:  ∑λ<em><sub>i</sub>z<sub>i </sub></em>= 0 .  Also give the other two KKT

<em> </em><em>i</em>=1

conditions on λ<em><sub>i </sub></em>, which carry over from the primal form.




<ol start="2">

 <li>In this problem you will do SVM learning on 2 data points, using the result from Problem 1 above.</li>

 <li>1 of 2</li>

</ol>

You are given a training data set consisting of 2 data points, in a 2-class problem.  In the expanded feature space, the data points are:

<em> <u>u</u></em>1=⎢⎡⎣ −1 ⎤⎥ ∈ <em>S</em>1;       <em><u>u</u></em>2 =⎡⎢ 01 ⎤⎥⎦ ∈ <em>S</em>2.

0 ⎦                          ⎣

(a) Solve, by hand, for the SVM decision boundary and regions.  To do this, use Lagrangian techniques to optimize <em> L<sub>D</sub></em> w.r.t. <u>λ</u>  subject to its equality constraint

<em>N</em>

∑λ<em><sub>i</sub>z<sub>i </sub></em>= 0, in order to find the optimal weight vector <em><sub> </sub></em><em><u>w</u></em>*, and also find the optimal <em> </em><em>i</em>=1

<em>w</em>0 .  Plot the training data and the decision boundary in 2D (nonaugmented) <em><u>u</u></em>–

<em> </em>

space, and show which side of the boundary is positive ( Γ<sub>1</sub>).




<strong>Hints:</strong>  Start from:

<sup>′</sup>(<u>λ</u>,µ) <em>N </em>⎡ <em>N N <sub>j</sub>z<sub>i</sub>z<sub>j</sub><u>u u </u></em>⎤ ⎛∑<em>N </em>⎞ <em>T </em>⎥ +µ

<strong>         </strong> <em>L<sub>D                      </sub></em><em>i</em>=1             <sup>⎢</sup>⎣<em>i</em>=1 <em>j</em>=1                    <em>i      j </em><sup>⎥</sup>⎦       ⎜⎝ <em>i</em>=1<em>z</em><em>i</em>λ<em>i</em>⎠⎟

in which the last term has been added to incorporate the equality constraint stated above.  Once finished, then check that the resulting <u>λ</u> satisfies the KKT conditions on <u>λ</u> that you stated in Problem 1(c)(ii); one of these can also help you find <em><sub> </sub>w</em><sub>0 </sub>*.

(b) Use the data points and solution you found in part (a), and call its solution decision boundary <strong> H </strong>.  Calculate in 2D <em><sub> </sub></em><em><u>u </u></em>− space the distance between <em><sub> </sub><u>u</u></em><sub>1</sub> and <strong> H </strong>, and the distance between <em> <u>u</u></em><sub>2</sub> and <strong> H </strong>.  Is there any other possible linear boundary in <em><sub> </sub></em><em><u>u </u></em>− space that would give larger values for both distances (“margins”) than <strong> H</strong> gives?  (No proof required.)


