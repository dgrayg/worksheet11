
# Review
1. In your own words, explain the general idea behind hashing.

2. What is a hash collision? Why is this a problem for hash tables?

3. What is *open hashing* (aka chaining)? What is *closed hashing*? What happens when a hash collision occurs in each?

4. What is the *linear probing strategy*? What is the *quadratic probing strategy*? How are they similar? How are they different?

5. In your own words, explain how insertion sort works. Make sure to also explain how this leads to its worst case time complexity (and what the complexity is).

6. In your own words, explain how merge sort works. Make sure to also explain how this leads to its worst case time complexity (and what the complexity is).

7. In your own words, explain how quicksort works. Make sure to also explain how this leads to its worst case time complexity (and what the complexity is).

8. In your own words, explain the first step of radix sort at each level of significance (i.e., at the ones, tens, hundreds, etc.). Make sure to explain what the buckets in radix sort represent.

9. In your own words, explain the second step of radix sort at each level of significance (i.e., at the ones, tens, hundreds, etc.). Why is this step necessary?

10. What is the worst case time complexity of radix sort? What about best and average case? Why?

11. What is the worst case memory complexity of radix sort? What about best and average case? Why?  

# Exploration
1. For each of the following ADTs, say whether hashing can be used to implement it. If yes, briefly describe how; if not, say why not.

    a. List

    b. Set

    c. Map

    d. Priority Queue

2. What would insertion sort do if the input array was already sorted? What would be the runtime complexity?

3. What would merge sort do if the input array was already sorted? What would be the runtime complexity?

4. What would quicksort do if the input array was already sorted (assuming good pivots)? What would be the runtime complexity?

5. How might you use a self-balancing binary search tree as part of a sorting algorithm? What would be the runtime complexity?

6. How might you use a heap as part of a sorting algorithm? What would be the runtime complexity?

7. What would radix sort do if an array was already sorted? What would be the runtime complexity?

8. The fastest comparison sorting algorithm we have discussed operates in O(nlogn) time. Is it possible sort an array faster than O(nlogn) time, while using a comparison sorting algorithm? Why or why not? (Hint: Think about how many ways there are of arranging n elements, how many ways there are of arranging them in sorted order, and how many possibilities each comparison eliminates)

9. Your textbook defines comparison sorting algorithms as those that can operate on an array of elements that can be compared to each other. Why does it not consider radix sort a comparison sorting algorithm?

10. Your textbook defines fast sorting algorithms as those with complexity O(nlogn) or better, but the fastest algorithm it shows is O(n). Is it possible to sort an array faster than O(n) time? Why or why not?

# Challenge
1.Explain what the *load factor* is for a hash table, and why it matters.

2. What will happen if we keep adding elements to a hash table that uses *closed hashing* if it is never resized? What about *open hashing*?

3. Why is resizing necessary to ensure hash tables have O(1) complexity (on average)?

4. One improvement to merge sort, called natural merge sort, takes advantage of existing sublists that are already sorted. For example, to sort the list {3, 4, 2, 1, 7, 5, 8, 9, 0, 6}, natural merge sort will first identify the sorted sublists {3, 4}, {2}, {1, 7}, {5, 8, 9}, and {0, 6}, then start merging from these sublists. Explain why this would decrease the runtime complexity of merge sort (i.e., make it run faster).

5. If an array of n elements can be broken down into p sorted sublists on average (in the example above, p=5), what is the runtime complexity of natural merge sort, taking the identification of the sorted sublists into account? Justify your answer.

6. Although standard merge sort is binary (2-ary) in that it merges two lists at a time, it is possible to write a ternary (3-ary) merge sort, where it splits the list into thirds and recurses on each third. What is the runtime complexity of ternary merge sort? Justify your answer.

7. Generalizing from 3-ary merge sort, we can imagine q-ary merge sort. What if we push this to the extreme, where q = n? What would be the complexity of this algorithm? Justify your answer. (Hint: keep in mind that comparison-based sorting cannot be faster than O(n log<sub>2</sub> n), and that log<sub>k</sub>(k) = 1 for any k.)

8. Your textbook states that radix sort is specific to integers. However, the algorithm can be modified to work on, for example, Strings. How would you modify the radix sort algorithm to sort words into lexicographical order? What would your buckets look like? How would sorting work? You may assume the 26-letter lower-case English alphabet and use Figure 3.7.2 in your textbook as a reference.

9. Watch Computerphile's video [Characters, Symbols and the Unicode Miracle](https://www.youtube.com/watch?v=MijmeoH9LT4) and read Daniel Lemire's article [Sorting Strings Properly is Stupidly Hard](https://lemire.me/blog/2018/12/17/sorting-strings-properly-is-stupidly-hard/). In your own words, explain why sorting strings lexicographically is complicated in the general case.

10. How would you modify radix sort to work on arbitrary Unicode strings? Keep in mind that the Unicode 13 standard contains 143,924 characters--some of which are multiple bytes. (You may ignore the issues raised by Lemire; any consistent sorting of Unicode strings is acceptable for the purposes of this question. However, your solution must be realistic--i.e., 143,924 buckets is not the right answer simply due to space constraints).
