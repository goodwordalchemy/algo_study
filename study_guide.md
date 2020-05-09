Algorithms Study Guide

Dynamic Programming Study Guide
Based on https://leetcode.com/discuss/general-discussion/458695/dynamic-programming-patterns#Minimum-(Maximum)-Path-to-Reach-a-Target

Minimum (Maximum) Path to Reach a Target
- [x] 746. Min Cost Climbing Stairs
- [x] 64. Minimum Path Sum
- [x] 322. Coin Change
- [x] 931. Minimum Falling Path Sum Medium 
- [x] 983. Minimum Cost For Tickets Medium
- [x] 650. 2 Keys Keyboard Medium
- [x] 279. Perfect Squares Medium
- [x] 1049. Last Stone Weight II Medium
	* This one was very hard.  It was an intro to dp, and to partitioning into two sets with the minimum diff.  “Classic Knapsack Problem”
- [x] 120. Triangle Medium
- [x] 474. Ones and Zeroes Medium
	* apparently this one is a (2D knapsack problem).  I still don’t fully get how that works, but basically what I did on this one is fill in the portion of a 2d array that is greater than my current amount of zeros and ones with 1 + dp[i-num_zeros][j-num_ones]
- [x] 221. Maximal Square Medium
- [ ] 1240. Tiling a Rectangle with the Fewest Squares Hard
- [ ] 174. Dungeon Game Hard
- [ ] 871. Minimum Number of Refueling Stops Hard

 Distinct Ways
- [x] 70. Climbing Stairs easy
- [x] 63. Unique Paths Medium
- [x] 1155. Number of Dice Rolls With Target Sum Medium
- [x] 688. Knight Probability in Chessboard Medium
	* random walk
	* probability
- [x] 494. Target Sum Medium
- [x] 377. Combination Sum IV Medium
- [x] 935. Knight Dialer Medium
- [x] 1223. Dice Roll Simulation Medium
- [x] 416. Partition Equal Subset Sum Medium
- [x] 808. Soup Servings Medium
- [x] 790. Domino and Tromino Tiling Medium
- [x] 801. Minimum Swaps To Make Sequences Increasing
- [ ] 63. Unique Paths II Medium
- [ ] 576. Out of Boundary Paths Medium
- [ ] 1269. Number of Ways to Stay in the Same Place After Some Steps Hard
- [ ] 1220. Count Vowels Permutation Hard


 Merging Intervals
- [x] 1130. Minimum Cost Tree From Leaf Values Medium
- [x] 96. Unique Binary Search Trees Medium
- [x] 1039. Minimum Score Triangulation of Polygon Medium
	* This one was prettty hard.  Learned a lot though.  
	* First of all, the idea is to fix two points in the polygon and then swing the third point around, recursively solving the subsections.
	* The top down approach is waaaay easier than the bottom up, which I still don't even get.
	* Base case is a triangle with two sides. (in top down)
	* for bottom up, dp[i][j] is dp considering only nodes between i and j, so start with all triangles, then all 4 sided polygons, and so on. until you have everything in array.
- [x] 375. Guess Number Higher or Lower II Medium
- [ ] 546. Remove Boxes Hard
- [ ] 1000. Minimum Cost to Merge Stones Hard
- [ ] 312. Burst Balloons Hard



 DP on Strings
Advance pointers to ends of words, perhaps
- [x] 1143. Longest Common Subsequence Medium
- [x] 647. Palindromic Substrings Medium
- [ ] 516. Longest Palindromic Subsequence Medium
- [x] 5. Longest Palindromic Substring Medium
- [x] 583. Delete Operation for Two Strings Medium
- [ ] 1092. Shortest Common Supersequence Medium
- [ ] 712. Minimum ASCII Delete Sum for Two Strings Medium
- [ ] 115. Distinct Subsequences Hard
- [x] 72. Edit Distance Hard



 Decision Making
- [x] 198. House Robber Easy
- [x] 121. Best Time to Buy and Sell Stock Easy
- [ ] 714. Best Time to Buy and Sell Stock with Transaction Fee Medium
- [ ] 309. Best Time to Buy and Sell Stock with Cooldown Medium
- [ ] 123. Best Time to Buy and Sell Stock III Hard
- [ ] 188. Best Time to Buy and Sell Stock IV Hard

Increasing subsequence
- [ ] 300. Longest Increasing Subsequence
- [ ] 549. Binary Tree Longest Consecutive Sequence II
- [ ] 673. Number of Longest Increasing Subsequence Medium


Unclassified
- [ ] 1434. Number of Ways to Wear Different Hats to Each Other
- [ ] 1035. Uncrossed Lines

Minimax
- [x] Nim Game
- [x] Stone Game
- [ ] Flip Game II
- [ ] Can I Win
- [ ] Predict the Winner
- [ ] Guess the Word
- [ ] Cat and Mouse


Sliding Window Problems

Strings With Counter
* Problem set based on https://medium.com/leetcode-patterns/leetcode-pattern-2-sliding-windows-for-strings-e19af105316b
- [x] 76. Minimum Window Substring
	* key insight on this one is probably the idea of negative numbers in the counter, and that you only increase or decrease count for numbers that aren’t negative.
- [x] 438. Find All Anagrams in a String
	* two key realizations on this one.  
		* comparing counters of lowercase letters is O(1)
		* size does not change for the window
		* delete 0s from counter
- [x] 3. Longest Substring Without Repeating Characters
- [x] 159. Longest Substring with At Most Two Distinct Characters
- [x] 567. Permutation in String
- [x] 340. Longest Substring with At Most K Distinct Characters
- [x] 424. Longest Repeating Character Replacement
- [x] 187. Repeated DNA Sequences
    * this one was pretty easy, but the length tripped me up a bit, actually.  how many windows of length 10 in a string of length 11?  2 obviously, but I was doing range(N-10), which only has one element (because 1 is not inclusive(.  I don’t know it wasn’t easy to see.

- [x] 30. Substring with Concatenation of All Words
	* key insight on this one was using multiple starting locations.  Base cases were hard

Other
- [x] 1438. Longest Continuous Subarray With Absolute Diff Less Than or Equal to Limit
	* Here’s a post about that one:  https://leetcode.com/problems/longest-continuous-subarray-with-absolute-diff-less-than-or-equal-to-limit/discuss/609771/JavaC%2B%2BPython-Deques-O(N)
	* a key fact on this one is to use properties of the fronts of the queues to determine when to pop.  The decs is always going to have the max so far at the front, and the incs is always going to have the min so far, so pop the fronts whenever those are out of range.
- [x] Number of Substrings Containing All Three Characters
	* don't forget that for a counter with a limited amount of elements, you can check equality with another ocunter.
	* This one did something clever with adding left to the result.  Every time you've got all of the letters on the right, you want to increment the count for every starting point that still allows you to have all of the letters
- [x] Count Number of Nice Subarrays
- [x] Replace the Substring for Balanced String
- [x] Max Consecutive Ones III
- [x] Binary Subarrays With Sum
- [x] Subarrays with K Different Integers
	* atMost for the win
- [ ] Fruit Into Baskets
- [ ] Shortest Subarray with Sum at Least K
- [ ] Minimum Size Subarray Sum
- [ ] 1425. Constrained Subsequence Sum  
Stacks
- [x] Minimum Cost Tree From Leaf Values
- [x] Sum of Subarray Minimums
- [x] Online Stock Span
- [x] Score of Parentheses
- [x] Next Greater Element II
	* You could just keep the indices on the array and use the indices to look up the value.
- [x] Next Greater Element 
	* key thing here was to remember that just because it's a stack problem doesn't mean there aren't other helpful data structures.
- [x] Largest Rectangle in Histogram
- [x] Maximal Rectangle(please do this problem after you solve the above one)
- [ ] Trapping Rain Water
- [ ] Remove Duplicate Letters(challenge)
- [ ] Remove K Digits
- [ ] Create Maximum Number
- [ ] 132 Pattern(challenge, instead of focusing on the elements in the stack, this problem focuses on the elements poped from the monotone stack)


Matrix
- [x] 54. Spiral Matrix
- [x] 498. Diagonal Traverse
- [x] 1424. Diagonal Traverse II
