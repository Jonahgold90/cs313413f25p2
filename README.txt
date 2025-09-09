COMP 313/413 Project 2 Report Template

TestList.java and TestIterator.java

	TODO also try with a LinkedList - does it make any difference?

		I don't think anything functionally changes since they are both lists. It may affect performance, though.

TestList.java

	testRemoveObject()

		list.remove(5); // what does this method do?

			Removed element at index 5

		list.remove(Integer.valueOf(5)); // what does this one do?

			removed the object in the list equal to 5

TestIterator.java

	testRemove()

		i.remove(); // what happens if you use list.remove(77)?

			Your answer here.
			Fails with concurrentModificationException

TestPerformance.java

	State how many times the tests were executed for each SIZE (10, 100, 1000 and 10000)
	to get the running time in milliseconds and how the test running times were recorded.

	SIZE 10
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  26ms 29ms 27ms 27ms 26ms 29ms  ... (fill these in in ms)
        testLinkedListAddRemove: 22ms 27ms 23ms 21ms 22ms 21ms
		testArrayListAccess:     6ms  6ms  6ms  6ms  7ms  6ms
        testLinkedListAccess:    9ms  14ms 9ms  10ms 9ms  8ms

	SIZE 100
								  #1   #2   #3   #4   #5   #6 	... (as many tests as you ran)
        testArrayListAddRemove:  37ms 37ms 37ms 37ms 38ms 37ms  ... (fill these in in ms)
        testLinkedListAddRemove: 21ms 21ms 20ms 21ms 21ms 21ms
		testArrayListAccess:     9ms  9ms  6ms  8ms  9ms  9ms
        testLinkedListAccess:    26ms 26ms 25ms 25ms 26ms 24ms

	SIZE 1000
								  #1   #2   #3   	... (as many tests as you ran)
        testArrayListAddRemove:  236ms 241ms 238ms  ... (fill these in in ms)
        testLinkedListAddRemove: 20ms  21ms 22ms
		testArrayListAccess:     7ms   6ms 6ms
        testLinkedListAccess:    541ms 535ms 537ms

	SIZE 10000
								  #1   #2   #3  	... (as many tests as you ran)
        testArrayListAddRemove:  2146ms 2183ms 2155ms  ... (fill these in in ms)
        testLinkedListAddRemove: 30ms  21ms 23ms
		testArrayListAccess:     19ms  7ms 11ms
        testLinkedListAccess:    7160ms 7110ms 7140ms

	listAccess - which type of List is better to use, and why?

		Array list access works significantly better as it is O(1). Linked list time grows much quicker as it is o(n)
		as it has to access every node before the target.

	listAddRemove - which type of List is better to use, and why?

		linked list add/remove is better as it's O(1) when adding to the front or removing at the end. In an array
		It would be o(n) since the elements need to all move over.