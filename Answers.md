## COMP 271 002 F17 Lab 9 (Week 11)

#### 1. Try using a TreeMap and a HashMap instead of MyHashMap.Are the resulting word frequencies any different?Is the time performance any different? If so, how would you rank the three implementations (in increasing order of time complexity)?

After debugging a missing return statement (!) in my get method, I can confirm that they all return the same values. Hash map is faster than Tree Map. MyHash map takes about the same time as Hashmap for larger tables and takes longer with smaller table sizes.

#### 2. How are % and Math.floorMod different? Which works more reliably for computing a hash table index?

% operator returns the remainder of two numbers. Math.floorMod rounds the remainder down to the lowest integer. We use Math.floorMod in case the hashcode returned is negative. Math.floorMod has greater reliability.

#### 3. What is the time complexity of MyHashMap.size(), and how could you make it much more efficient?
O(n). We could make it an instance variable that get incremented whenever a new entry is added to any of the chains. The method would then just return the value of that size variable.

#### 4. How does this implementation compare to one where you would directly use your linked Node class from the earlier assignment? Answer briefly in terms of ease of implementation, correctness, reliability, and performance.
Both implementations are correct. After timing the implementations for the previous assignment with this one, it appears MyHashmap has a faster performance. The implementation of MyHashmap feels more complex since we needed to use hashcodes to figure out which chain in the table to search, however, I think this makes it more reliable.