# Andrew-Ng-s-ML-Tips-Tricks
This repository is to catalog some of the more fundamental code that helps assist in the homework and Octave. This is not a solution set to the assignments, but will help understand the commands within Octave to arrive at answers quickly. 

Given a Matrix A[m,n], find the minimum, maximum, ~=, == AND the row & column index.

>> A = rand(3,4)
A =

   0.950565   0.032692   0.584597   0.054445
   0.572088   0.406915   0.175014   0.457936
   0.889192   0.897563   0.858633   0.658966
   
   
   
>> min(A) %finds the minimum in each column
ans =

   0.572088   0.032692   0.175014   0.054445

>> min(min(A)) %finds the minimimum of the matrix
ans = 0.032692

Find the row
>> [minimum, row] = min(min(A,[],2))
minimum = 0.032692
row = 1

Find the column
>> [minimum, col] = min(min(A,[],1))
minimum = 0.032692
col = 2

OR 
>> minimum = min(min(A));
>> [i, j] = find(A == minimum)
i = 1
j = 2

The min(min(A,[],2)) & min(min(A,[],1)) are useful inside loops as it returns an index. 
   
   
   
