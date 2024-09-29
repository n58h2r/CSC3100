java c
CSC3100 Data Structures Fall 2024
Programming Assignment 1
1 Array Problem (40% of this assignment)
1.1 Description
You are given a sequence of integers ai  of length n. Additionally, you are given m operations to perform. on this sequence. Each operation is one of the following:
- Given k,x,y,c, update the value of ak  using the formula:
ak  = ((x2 + ky + 5x) mod P) ∗ c
Obviously, the resulting value will be between [1 − P, P − 1], where c = ±1.
- Query the sum of all elements in the sequence, i.e., compute:

- Query the maximum number of distinct values in the sequence if each element is multiplied by either
1 or −1 (you can flip the sign of some elements and count the maximum number of distinct numbers). Your task is to process these operations efficiently.
1.2 Input
The first line contains three integers n, m and P (1 ≤ n,m ≤ 106 , 1 ≤ P ≤ 106 ) — the length of the sequence, the number of operations and the divisor in modulo operation, respectively.
The second line contains n integers, representing the original value of the array a, denoted as a1 , a2 , ..., an (−P < a[i] < P).
Each of the next m lines contains a description of one of the following types of operations:
-  For  update  operations,  the  line  will  contain  five  integers  1,k,x,y, c  (1  ≤ k   ≤ n, 0  ≤ x,y   < min(P,2000), c ∈ {−1, 1}).
- For sum queries, the line will contain a single integer 2.
- For distinct value queries, the line will contain a single integer 3.
1.3 Output
For each sum query, output the sum of all elements in the array.
For each distinct value query, output the maximum number of distinct values that can be obtained by multiplying each element by either 1 or −1.
Sample Input 1
5 5 3
0 0 0 1 -2
3
1 5 1 2 -1
3
1 3 2 1 1
3
Sample Output 1
3
3
4
Sample Input 2
10 10 5
-1 -2 2 -3 2 0 -4 3 3 -3
3
1 2 4 4 -1
2
1 3 1 2 -1
3
2
3
1 2 4 4 1
3
1 4 4 0 -1
Sample Output 2
7
-5
8
-9
8
8
Sample Input 3
in ’ array_sampleinput3 . in ’
Sample Output 3
in ’ array_sampleinput3 . ans ’
Problem Scale  Subtasks
For about 60% test cases, distinct value queries are not evolved.
Test Case No.
Constraints
1-4
5-7
8-10
n,m ≤ 20
n,m ≤ 5 × 103 n,m ≤ 106
Hint
If you encounter a TLE, and your algorithm’s time complexity is efficient, try optimizing your I/O operations.
2 List (50% of this assignment)
2.1 Description
Given an array, which is a permutation of size n (an array of size n where every integer from 1 to n appears exactly once), we perform. q operations. During the i-th operation, we perform. the following:
•  Choose any suba代 写CSC3100 Data Structures Fall 2024 Programming Assignment 1C/C++
代做程序编程语言rray that contains at least 2 elements.
• Split it into two non-empty arrays.
•  Obtain two integers li  and ri , where li  is the left most element in the left part of the split, and ri  is the right most element in the right part of the split.
For example, if the initial array is [6, 3, 4, 1, 2, 5], we perform. the following operations:
1.  Choose the array [6, 3, 4, 1, 2, 5] and split it into [6, 3] and [4, 1, 2, 5].  Then, l1  = 6 and r1  = 5.
2.  Choose the array [4, 1, 2, 5] and split it into [4, 1, 2] and [5]. Then, l2  = 4 and r2  = 5, resulting in the arrays [6, 3], [4, 1, 2], and [5].
3.  Choose the array [4, 1, 2] and split it into [4] and [1, 2].  Then, l3  = 4 and r3  = 2, resulting in the arrays [6, 3], [4], [1, 2], and [5].Objective. Given two integers n and q, along with two sequences [l1 , l2,...,lq ] and [r1 , r2,...,rq ], a permutation is called valid if we can perform. q operations and generate the given sequences [l1 , l2,...,lq ] and [r1 , r2,...,rq ].
Problem. Determine whether a given permutation with q operations is valid.
2.2 Input
1.  The first line contains two integers n and q (1 ≤ q < n ≤ 106 ).
2.  The second line contains a permutation of size n.
3.  The third line contains q integers, l1 , l2,...,lq  (1 ≤ li  ≤ n).
4.  The fourth line contains q integers, r1 , r2 , ...,rq  ( 1 ≤ ri  ≤ n )
2.3 Output
Output 1 if the given permutation is valid, otherwise output 0.
Sample Input 1
6 3
6 3 4 1 2 5
6 4 4
5 5 2
Sample Output 1
1
Sample Input 2
7 3
7 6 3 4 1 2 5
6 4 4
5 5 2
Sample Output 2
0
Sample Input 3
7 3
6 3 4 1 2 5 7
6 4 4
5 5 2
Sample Output 3
0
Problem Scale  Subtasks
For 100% of the test cases, 1 ≤ q < n ≤ 106 .
Test Case No.
Constraints
1-2
3-5
6-10n ≤ 10 n ≤ 103 n ≤ 106

Figure 1: Hint2
Hint
Hint1 : For C/C++ and Java users, an int type stores integers range from -2,147,483,648 to 2,147,483,647. It may be too small for this problem. You need other data types, such as long  long for C/C++ and long for Java. They store integers ranging from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807. Use scanf("%lld",n) for C, cin>>nfor C++ and n  =  scanner.nextLong() for Java to get the input   n. And the other operations for long and long long are quite same as int.
Hint2: The process of Sample Input 1 can be described as in the Figure 1.
Hint3: This problem can be easily solved by following the above process from bottom to top.
Hint4: Consider how using the data structure, such as dictionary or list, to store the indices of li  and ri  can help solve the problem.







         
加QQ：99515681  WX：codinghelp
