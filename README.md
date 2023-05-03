Download Link: https://assignmentchef.com/product/solved-cs213-assignment2-balancing-brackets
<br>
P1: Balancing Brackets

A bracket is considered to be any one of the following characters: ​<strong>(</strong>​, ​<strong>)</strong>​, ​<strong>{</strong>​, ​<strong>}</strong>​, ​<strong>[</strong>​ or ​<strong>]</strong>​.

Two brackets are considered to be a matched pair if an opening bracket ( i.e. ​<strong>(</strong>​, ​<strong>[</strong>​, or ​<strong>{ </strong>​) occurs to the left of a closing bracket ( i.e. <strong>)</strong>​ , ​ ​<strong>]</strong>, or ​   <strong>}</strong>​ )​ of the exact same type. There are three types of matched pairs of brackets: ​<strong>[]</strong>​, <strong>{}</strong>​ ​, and ​<strong>()</strong>.​

A matching pair of brackets is not balanced if the set of brackets it encloses are not matched. For example, ​<strong>{[(])}</strong>​ is not balanced because the contents in between ​<strong>{</strong>​ and ​<strong>}</strong>​ are not balanced. The pair of square brackets encloses a single, unbalanced opening bracket, ​<strong>(</strong>​ and the pair of parentheses encloses a single, unbalanced closing square bracket, ​<strong>]</strong>​.

By this logic, we say a sequence of brackets is balanced if the following conditions are met:

<ul>

 <li>It contains no unmatched brackets.</li>

 <li>The subset of brackets enclosed within the confines of a matched pair of brackets is also a matched pair of brackets.</li>

</ul>

Given a string of brackets, determine whether the sequence of brackets is balanced. If a string is balanced, output ​<strong>1</strong>​. Otherwise, output ​<strong>0</strong>.​

<u>Input Format:</u>

The first line contains a single integer ​<strong>n</strong>, the length of the string.​

The next line contains a single string ​<strong>s</strong>​ of length ​<strong>n</strong>​, a sequence of brackets.




<u>Constraints:</u>

<ul>

 <li>1 &lt;= ​<strong>n</strong>​ &lt;= 10^3</li>

 <li>All characters in the sequences ∈ { ​<strong>{</strong>​, ​<strong>}</strong>​, ​<strong>(</strong>​, ​<strong>)</strong>​, ​<strong>[</strong>​, ​<strong>]</strong>​ }.</li>

</ul>

<u>Examples:</u>

<table width="630">

 <tbody>

  <tr>

   <td width="315"><strong>Input </strong></td>

   <td width="315"><strong>Output </strong></td>

  </tr>

  <tr>

   <td width="315"><strong>6 {[()]} </strong></td>

   <td width="315">1</td>

  </tr>

  <tr>

   <td width="315"><strong>6 {[(])} </strong></td>

   <td width="315">0</td>

  </tr>

  <tr>

   <td width="315"><strong>12 </strong><strong>{{[[(())]]}} </strong></td>

   <td width="315">1</td>

  </tr>

 </tbody>

</table>

<em>File to be submitted : p1.cpp</em><strong><em>                          </em></strong>

<h1>P2: Truck Tour</h1>

Consider a circle with ​<strong>N</strong>​ petrol pumps spread out randomly on the periphery. Petrol pumps are numbered 0 to N-1 (both inclusive). You have two pieces of information corresponding to each of the petrol pump:

<ol>

 <li>The amount of petrol that particular petrol pump will give 2. The distance from that petrol pump to the next petrol pump.</li>

</ol>




Initially, you have a tank of infinite capacity carrying no petrol. You can start the tour at any of the petrol pumps. Calculate the first point from where the truck will be able to complete the circle. Assume that the truck will stop at each of the petrol pumps. The truck will move ​<strong>one kilometer for each litre</strong>​ of the petrol.




<u>Input Format:</u>

The first line will contain the value of ​<strong>N</strong>​.

The next ​<strong>N</strong>​ lines each will contain a pair of integers separated by a space denoting the amount of petrol that petrol pump will give and the distance between that petrol pump and the next petrol pump respectively.




<u>Constraints:</u>

1 &lt;= ​<strong>N</strong>​ &lt;= 10^5

1 &lt;= Amount of petrol, Distance between petrol pumps &lt;= 10^9 Note: use ‘long long’ instead of ‘int’ to avoid integer overflow.




<u>Output Format:</u>

An integer which will be the ​<strong>smallest</strong>​ index of the petrol pump from which we can start the tour. Output ​<strong>-1 </strong>if such a tour does not exist.




<u>Example:</u>

<table width="630">

 <tbody>

  <tr>

   <td width="315"><strong>Input </strong></td>

   <td width="315"><strong>Output </strong></td>

  </tr>

  <tr>

   <td width="315">31 510 33 4</td>

   <td width="315">1</td>

  </tr>

  <tr>

   <td width="315">32 34 510 11</td>

   <td width="315">-1</td>

  </tr>

  <tr>

   <td width="315">45  36  84 58 7</td>

   <td width="315">3 </td>

  </tr>

 </tbody>

</table>

<em> </em>

<em>File to be submitted : p2.cpp                          </em>

<h1>P3: Smaller Than Thou</h1>




Use a stack to implement the following functionality: Given an indexed list of numbers, determine the next smaller element for each number. You need to output the index of the next smaller element. Assume the sequence to be of non-negative numbers.

Formally, for each ​<strong>i</strong>​, find ​<strong>j&gt;i</strong>​ such that ​<strong>a[i]&gt;a[j]</strong>​ and ​<strong>(j-i) is minimum</strong>​. If no such ​<strong>j</strong>​ exists, output ​<strong>-1 </strong>




For instance, assume the following input sequence:

10 1 2 6 5 9 3




The corresponding next-smaller-element for each is,

10 -&gt; 1  (10&gt;1 and the index of element 1 is 1)

<ul>

 <li>-&gt; -1 (no smaller element than this in the remaining sequence)</li>

 <li>-&gt; -1 (no element less than 2 exists subsequently)</li>

</ul>

6   -&gt; 4  (6&gt;5 and the index of element 5 is 4)

5   -&gt; 6  (5&gt;3)

9   -&gt; 6  (9&gt;3)

3   -&gt; -1 (trivial)




The trivial algorithm to do this can be in two passes over the whole sequence, and will take O(n​<sup>2</sup>​) time. A stack-based procedure can do this in O(n) time,which is the goal for this assignment..




<u>Input Format:</u>

The first line will contain the value of ​<strong>N</strong>​.

The second line will contain the <strong>N </strong>​ non-negative integers​




<u>Constraints:</u>

1 &lt;= <strong>n</strong>​ &lt;= 10^6​




<u>Examples:</u>

<table width="630">

 <tbody>

  <tr>

   <td width="315"><strong>Input </strong></td>

   <td width="315"><strong>Output </strong></td>

  </tr>

  <tr>

   <td width="315">51 4 2 3 7</td>

   <td width="315">-1 2 -1 -1 -1 </td>

  </tr>

  <tr>

   <td width="315">101 4 5 13 17 19 8 4 3 0</td>

   <td width="315">9 8 7 6 6 6 7 8 9 -1 </td>

  </tr>

 </tbody>

</table>




<em>File to be submitted : p3.cpp </em>

(Tip: You can implement the logic of next smaller element using C++ STL. Read about how to

use ​<strong>stack&lt;T&gt;</strong>​ where T can be any data type.) <strong>                          </strong>

<h1>P4: Building area maximization</h1>

Consider a sequence of numbers representing the height of buildings adjoining each other. Assume width of the building is 1 unit and we are in 2-D space, so the other dimension is the height.

You need to find a rectangle such that the whole of the rectangle is covered by buildings, and the rectangle has maximum area among all such possible.







<u>Input Format:</u>

The first line will contain the value ​<strong>N, </strong>​the number of buildings.

The second line will contain the ​<strong>N </strong>​non-negative integers, denoting the height of buildings.




<u>Output:</u>

The maximum ​<strong>rectangular</strong>​ area covered by the buildings




<u>Examples</u>​<strong>: </strong>




<table width="630">

 <tbody>

  <tr>

   <td width="315"><strong>Input </strong></td>

   <td width="315"><strong>Output </strong></td>

  </tr>

  <tr>

   <td width="315">101 4 5 13 17 19 8 4 3 0</td>

   <td width="315">39 </td>

  </tr>

  <tr>

   <td width="315">11</td>

   <td width="315">1</td>

  </tr>

  <tr>

   <td width="315">51 4 2 3 7</td>

   <td width="315">8 </td>

  </tr>

 </tbody>

</table>




<em>File to be submitted : p4.cpp                          </em>

<h1>P5: Queue using Two Stacks</h1>

A queue is an abstract data type that maintains the order in which elements were added to it, allowing the oldest elements to be removed from the front and new elements to be added to the rear. This is called a First-In-First-Out (​<strong>FIFO</strong>​) data structure because the first element added to the queue (i.e. the one that has been waiting the longest) is always the first one to be removed.




A basic queue has the following operations

<u>Enqueue:</u><u>​</u> add a new element to the end of the queue.

<u>Dequeue:</u><u>​</u> remove the element from the front of the queue and return it.




In this problem, you must first implement a queue using two stacks. Then process queries, where each query is one of the following types:

<ul>

 <li><strong>x </strong>​: Enqueue element ​<strong>x</strong>​ at the end of the queue.</li>

 <li>​: Dequeue the element at the front of the queue.</li>

 <li>​: Print the element at the front of the queue. Print ​<strong>-1 </strong>​if the queue is empty</li>

</ul>




<u>Input Format:</u>

The first line contains a single integer ​<strong>N</strong>​ denoting the number of queries.

Subsequent ​<strong>N</strong>​ lines contains a single query in the form described in the problem statement above. All three queries start with an integer denoting the query, but only query ​<strong>1</strong>​ is followed by an additional space-separated value, <strong>x</strong>​ , denoting the value to be enqueued.​




<u>Output Format:</u>

For each query of type ​<strong>3</strong>​, print the value of the element at the front of the queue on a new line.




<u>Example:</u>

<strong> </strong>

<table width="630">

 <tbody>

  <tr>

   <td width="315"><strong>Input </strong></td>

   <td width="315"><strong>Output </strong></td>

  </tr>

  <tr>

   <td width="315">111 4221 1431 2831 601 78223</td>

   <td width="315">141460</td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<u>Explanation:</u>

<strong> </strong>

We perform the following sequence of 10 actions:




Enqueue 42; queue = {42}.

Dequeue the value at the head of the queue, 42; {}.

Enqueue 14; queue = {14}.

Print the value at the head of the queue, 14; queue = {14}.

Enqueue 28; queue = {14, 28}.

Print the value at the head of the queue, 14 ; queue = {14, 28} .

Enqueue 60 ; queue = {14, 28, 60}.

Enqueue 78; queue = {14, 28, 60, 78}.

Dequeue the value at the head of the queue, 14; queue = {28, 60, 78}.

Dequeue the value at the head of the queue, 28; queue = {60, 78}.

Print the value at the head of the queue, 60 ; queue = {60, 78}.




<em>File to be submitted : p5.cpp</em>








