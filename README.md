Download Link: https://assignmentchef.com/product/solved-ucs1411-exercise-10-page-replacement-algorithms
<br>
Develop a C program to implement the page replacement algorithms (FIFO, Optimal, LRU and LFU) using linked list.

Algorithm:

Implement the following modules and its operations using linked list.

Read module:

<ol>

 <li>Read the number of frames.</li>

 <li>Read the number of frames required by the process N.</li>

 <li>Read the reference string for allocation of page frames.</li>

</ol>

Page replacement module:

FIFO REPLACEMENT

<ol>

 <li>Allocate the first N pages into the frames and increment the page faults accordingly.</li>

 <li>When next frame in the reference string is not already available in the allocated list do

  <ol>

   <li>Look for the oldest one in the allocated frames and replace it with the next page</li>

   <li>Increment the page fault whenever a frame is replaced.</li>

  </ol></li>

</ol>

OPTIMAL REPLACEMENT

<ol>

 <li>Allocate the first N pages into the frames and increment the page faults accordingly.</li>

 <li>When next frame in the reference string is not already available in the allocated list do

  <ol>

   <li>Look for a frame in the reference string will not be used for longest period of time.</li>

   <li>Increment the page fault whenever a frame is replaced. (Hint: Locate the position of each allocated frame in the reference string; identify a frame for replacement with largest index position)</li>

  </ol></li>

 <li>Display the allocated frame list after every replacement.</li>

</ol>

LRU REPLACEMENT

<ol>

 <li>Allocate the first N pages into the frames and increment the page faults accordingly.</li>

 <li>When next frame in the reference string is not already available in the allocated list do

  <ol>

   <li>Look for a frame which is not used recently.</li>

   <li>Increment the page fault whenever a frame is replaced.</li>

  </ol></li>

 <li>Display the allocated frame list after every replacement</li>

</ol>

LFU REPLACEMENT

<ol>

 <li>Allocate the first N pages into the frames and increment the page faults accordingly.</li>

 <li>When next frame in the reference string is not already available in the allocated list do

  <ol>

   <li>Look for a frame which is least frequently used.</li>

   <li>Increment the page fault whenever a frame is replaced.</li>

  </ol></li>

 <li>Display the allocated frame list after every replacement</li>

</ol>

<u>Sample input &amp; output:</u>

PAGE REPLACEMENT ALGORITHMS

<ol>

 <li>READ_INPUT</li>

 <li>FIFO</li>

 <li>OPTIMAL</li>

 <li>LRU</li>

 <li>LFU</li>

 <li>EXIT</li>

</ol>

Enter your option: 1

Enter the number of free frames: 10

Enter the number of frames required by the process: 4

Enter the reference string: 7 0 1 2 0 3 0 4 2 3 0 3 2 1 2 0 1 7 0 1

Enter your option: 2

FIFO Page Replacement Algorithm

The reference string: 7 0 1 2 0 3 0 4 2 3 0 3 2 1 2 0 1 7 0 1

<u>Page ref  memory    PF</u>

7       7          –           –         –           1

<ul>

 <li>     7           0          –          –             2</li>

 <li>     7           0          1          –  3</li>

 <li> 7          0          1           2  4</li>

</ul>

0       7         0         1               2  –

3       3         0         1              2  5




<table width="0">

 <tbody>

  <tr>

   <td width="21">7</td>

   <td width="21">7</td>

   <td width="21">7</td>

   <td width="21">7</td>

   <td width="21">3</td>

   <td width="21">3</td>

   <td width="21">3</td>

   <td width="21">3</td>

   <td width="21">2</td>

   <td width="21">2</td>

  </tr>

  <tr>

   <td width="21"> </td>

   <td width="21">0</td>

   <td width="21">0</td>

   <td width="21">0</td>

   <td width="21">0</td>

   <td width="21">4</td>

   <td width="21">4</td>

   <td width="21">4</td>

   <td width="21">4</td>

   <td width="21">7</td>

  </tr>

  <tr>

   <td width="21"> </td>

   <td width="21"> </td>

   <td width="21">1</td>

   <td width="21">1</td>

   <td width="21">1</td>

   <td width="21">1</td>

   <td width="21">0</td>

   <td width="21">0</td>

   <td width="21">0</td>

   <td width="21">0</td>

  </tr>

  <tr>

   <td width="21"> </td>

   <td width="21"> </td>

   <td width="21"> </td>

   <td width="21">2</td>

   <td width="21">2</td>

   <td width="21">2</td>

   <td width="21">2</td>

   <td width="21">1</td>

   <td width="21">1</td>

   <td width="21">1</td>

  </tr>

 </tbody>

</table>




Total Number of Page Faults: 10