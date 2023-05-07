Download Link: https://assignmentchef.com/product/solved-ift6135-assigment-1
<br>
Question 1 (4-4-4). Using the following definition of the derivative and the definition of the Heaviside step function :

 1         if <em>x &gt; </em>0



if <em>x </em>= 0 <sup></sup>0 if <em>x &lt; </em>0

<ol>

 <li>Show that the derivative of the rectified linear unit <em>g</em>(<em>x</em>) = max{0<em>,x</em>}, wherever it exists, is equal to the Heaviside step function.</li>

 <li>Give two alternative definitions of <em>g</em>(<em>x</em>) using <em>H</em>(<em>x</em>).</li>

 <li></li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="127"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Show that <em>H</em>(<em>x</em>) can be well approximated by the sigmoid function asymptotically (i.e for large <em>k</em>), where <em>k </em>is a parameter.</li>

</ul>

<ol start="2">

 <li style="list-style-type: none;"></li>

</ol>

Question 2 (3-3-3-3). Recall the definition of the softmax function : <em>S</em>(<em>x</em>)<em><sub>i </sub></em>= <em>e</em><em><sup>x</sup></em><em><sup>i</sup></em><em>/</em><sup>P</sup><em><sub>j </sub></em><em>e<sup>x</sup></em><em><sup>j</sup></em>.

<ol>

 <li>Show that softmax is translation-invariant, that is : <em>S</em>(<em>x</em>+<em>c</em>) = <em>S</em>(<em>x</em>), where <em>c </em>is a scalar constant.</li>

 <li>Show that softmax is not invariant under scalar multiplication. Let <em>S<sub>c</sub></em>(<em>x</em>) = <em>S</em>(<em>c</em><em>x</em>) where <em>c </em>≥ 0. What are the effects of taking <em>c </em>to be 0 and arbitrarily large?</li>

 <li>Let <em>x </em>be a 2-dimensional vector. One can represent a 2-class categorical probability using softmax <em>S</em>(<em>x</em>). Show that <em>S</em>(<em>x</em>) can be reparameterized using sigmoid function, i.e. <em>S</em>(<em>x</em>) = [<em>σ</em>(<em>z</em>)<em>,</em>1−<em>σ</em>(<em>z</em>)]<sup>&gt; </sup>where <em>z </em>is a scalar function of <em>x</em>.</li>

 <li>Let <em>x </em>be a <em>K</em>-dimensional vector (<em>K </em>≥ 2). Show that <em>S</em>(<em>x</em>) can be represented using <em>K </em>− 1 parameters, i.e. <em>S</em>(<em>x</em>) = <em>S</em>([0<em>,y</em><sub>1</sub><em>,y</em><sub>2</sub><em>,…,y<sub>K</sub></em><sub>−1</sub>]<sup>&gt;</sup>) where <em>y<sub>i </sub></em>is a scalar function of <em>x </em>for <em>i </em>∈ {1<em>,…,K</em>− 1}.</li>

</ol>

Question 3 (16). Consider a 2-layer neural network <em>y </em>: R<em><sup>D </sup></em>→ R<em><sup>K </sup></em>of the form :

for 1 ≤ <em>k </em>≤ <em>K</em>, with parameters Θ = (<em>ω</em><sup>(1)</sup><em>,ω</em><sup>(2)</sup>) and logistic sigmoid activation function <em>σ</em>. Show that there exists an equivalent network of the same form, with parameters Θ<sup>0 </sup>= (<em>ω</em>˜<sup>(1)</sup><em>,ω</em>˜<sup>(2)</sup>) and tanh activation function, such that for all <em>x </em>∈ R<em><sup>D</sup></em>, and express Θ<sup>0 </sup>as a function of Θ.

Question 4 (5-5). Fundamentally, back-propagation is just a special case of reverse-mode Automatic Differentiation (AD), applied to a neural network. Based on the “three-part” notation shown in Table 1 and 4, represent the evaluation trace and derivative (adjoint) trace of the following examples. In the last columns of your solution, numerically evaluate the value up to 4 decimal places.

<ol>

 <li>Forward AD, with <em>y </em>= <em>f</em>(<em>x</em><sub>1</sub><em>,x</em><sub>2</sub>) = 1<em>/</em>(<em>x</em><sub>1 </sub>+ <em>x</em><sub>2</sub>) + <em>x</em><sub>2</sub><sup>2 </sup>+ cos(<em>x</em><sub>1</sub>) at (<em>x</em><sub>1</sub><em>,x</em><sub>2</sub>) = (3<em>,</em>6) and setting <em>x</em>˙<sub>1 </sub>= 1 to compute <em>∂y/∂x</em><sub>1</sub>.</li>

 <li>Reverse AD, with <em>y </em>= <em>f</em>(<em>x</em><sub>1</sub><em>,x</em><sub>2</sub>) = 1<em>/</em>(<em>x</em><sub>1 </sub>+ <em>x</em><sub>2</sub>) + <em>x</em><sub>2</sub><sup>2 </sup>+ cos(<em>x</em><sub>1</sub>) at (<em>x</em><sub>1</sub><em>,x</em><sub>2</sub>) = (3<em>,</em>6). Setting <em>y</em>¯ = 1, <em>∂y/∂x</em><sub>1 </sub>and <em>∂y/∂x</em><sub>2 </sub>can be computed together.</li>

</ol>

Question 5 (6). Compute the <em>full</em>, <em>valid</em>, and <em>same </em>convolution (with kernel flipping) for the following 1D matrices :

Question 6 (5-5). Consider a convolutional neural network. Assume the input is a colorful image of size 256 × 256 in the RGB representation. The first layer convolves 64 8 × 8 kernels with the input, using a stride of 2 and no padding. The second layer downsamples the output of the first layer with a 5 × 5 non-overlapping max pooling. The third layer convolves 128 4 × 4 kernels with a stride of 1 and a zero-padding of size 1 on each border.

<ol>

 <li>What is the dimensionality (scalar) of the output of the last layer?</li>

 <li>Not including the biases, how many parameters are needed for the last layer?</li>

</ol>

Question 7 (4-4-6). Assume we are given data of size 3 × 64 × 64. In what follows, provide a correct configuration of a convolutional neural network layer that satisfies the specified assumption. Answer with the window size of kernel (<em>k</em>), stride (<em>s</em>), padding (<em>p</em>), and dilation (<em>d</em>, with convention <em>d </em>= 1 for no dilation). Use square windows only (e.g. same <em>k </em>for both width and height).

<ol>

 <li>The output shape (<em>o</em>) of the first layer is (64<em>,</em>32<em>,</em>32).

  <ul>

   <li>Assume <em>k </em>= 8 without dilation.</li>

  </ul></li>

</ol>




<ul>

 <li>Assume <em>d </em>= 7, and <em>s </em>= 2.</li>

</ul>

<ol start="2">

 <li>The output shape of the second layer is (64<em>,</em>8<em>,</em>8). Assume <em>p </em>= 0 and <em>d </em>= 1.

  <ul>

   <li>Specify <em>k </em>and <em>s </em>for pooling with non-overlapping window.</li>

   <li>What is output shape if <em>k </em>= 8 and <em>s </em>= 4 instead?</li>

  </ul></li>

 <li>The output shape of the last layer is (128<em>,</em>4<em>,</em>4).

  <ul>

   <li>Assume we are not using padding or dilation.</li>

   <li>Assume <em>d </em>= 2, <em>p </em>= 2. (c) Assume <em>p </em>= 1, <em>d </em>= 1.</li>

  </ul></li>

</ol>


