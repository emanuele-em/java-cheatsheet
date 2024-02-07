# Non-Primitive

## Collection interface

### List interface


#### `ArrayList` Implementation

Definition list of Integers

```
List<Integers> arrList = new ArrayList<>();
```

Insert an element
```
arrList.add(num);
arrList.add(i, num);
```

Delete an element at index i
```
int removed = arrList.remove(i);
```

Set or update an element at index i
```
int previousElementAtI = arrList.set(i, num);
```

Get an element at index i
```
int num = arrList.get(i);
```

Get the size of the list
```
int size = arrList.size();
```

Check for Empty
```
boolean bool = arrList.isEmpty();
```

Check if there is an element
```
boolean bool = arrList.contains(num);
```

Get the index of a certain value 'num'
```
int i = arrList.indexOf(num);
```

Cast to a primitive list, i.e. ArrayList<Integer> -> int[]
```
int[] primArr = arrList.toArray();
```

Sorting
```
Collections.sort(arrList, (a, b) -> a-b); // Ascending
Collections.sort(arrList, (a, b) -> b-a); // Descending
```

### Set interface

#### `HashSet` implementation

Definition
```
Set<Integer> set = new HashSet<>();
```

Insert an element `num`, return `true` if the set not already contain `num`
```
boolean setDoesNotContainNum = set.add(num);
```

Delete an element `num`, return `true` if `num` was in `set`
```
boolean WasInSet = set.remove(num);
```

Check for an element `num`
```
boolean contains = set.contains(num);
```

Get the size of the set
```
int size = set.size();
```

Check for Empty
```
boolean isEmpty = set.isEmpty();
```

Remove all map values
```
map.clear();
```

### Map Interface

#### `HashMap` implementation

Definition
```
Map<K, V> map = new HashMap<>();
```

Insert / update an element with key k1 with value v1, return the previous element, if present, or `null` if not present
```
T previousElement = map.put(k1, v1);
```

Create a counter for letters in a string
```
Map<Character, Integer> freq = new HashMap<>();
for(char c: str.toCharArray()){
    freq.put(c, freq.getOrDefault(c, 0) + 1);
}
```

Delete an element with key k1
```
D deletedEl =  map.remove(k1);
```

Get an element with key k1
```
V el = map.get(k1);
```

Get the size of the map
```
int size = map.size();
```

Check for Empty
```
boolean isEmpty = map.isEmpty();
```

Check if there is a value with key k1
```
boolean contains = map.containsKey(k1);
```

Remove all map values
```
map.clear();
```

In graph problem, when building adjacecy list from an edge List
```
Map<Integer, List<Integer>> graph = new HashMap<>();
for(int[] edge: edgeList){
    graph.computeIfAbsent(edge[0], val -> new ArrayList<>()).add(edge[1]);
}
```


### Queue Interface

#### `LinkedList` implementation (deque)

Definition
```
Queue<Integers> queue = new LinkedList<>();
```

Insert an element
```
queue.add(num);
```

Delete element (the head), and returns it, it returns `null` if the queue is empty
```
E head = queue.poll();
```

Retrieve but does not remove the head of the queue
```
E head = queue.peek();
```

Get the size of the list
```
int size = queue.size();
```

Check for Empty
```
boolean isEmpty = queue.isEmpty();
```

##### `PriorityQueue` implementation (priority queue / heap)

Definition
```
Queue<Integers> heap = new PiorityQueue<>();
```

Insert an element
```
heap.add(num);
```

Delete element (the head)
```
E head = heap.poll();
```

Retrieve but not remove the head of the priority queue
```
E head = heap.peek();
```

Get the size of the list
```
int size = heap.size();
```

Check for Empty
```
boolean isEmpty = heap.isEmpty();
```

#### Deque Interface

##### `ArrayDeque` implementation (stack)

Definition
```
Deque<Integer> stack = new ArrayDeque<>();
```

Insert an element
```
boolean changed = stack.add(num); // it returns true if this collection is changed
boolean changed = stack.addLast(num); // it returns true if this collections is changed
```

Delete element (the last)
```
E lastElement = stack.pop();
```

Retrieve the last element but does not remove it
```
E lastElement = stack.peekLast();
```

Get the size of the list
```
int size = stack.size();
```

Check for Empty
```
boolean isEmpty = stack.isEmpty();
```

##### `ArrayDeque` implementation (deque)

Definition
```
Deque<Integer> deque = new ArrayDeque<>(); // preferred
```

Insert an element
```
boolean changed = stack.add(num);
boolean changed = stack.addFirst(num);
```

Delete the first element
```
E firstElement = stack.poll();
E firstElement = stack.pollFirst();
```

Retrieve but not remove the first element
```
E firstElement = stack.peekFirst();
E firstElement = stack.peek();
```

Get the size of the list
```
int size = stack.size();
```

Check for Empty
```
boolean isEmpty = stack.isEmpty();
```

# String and Character

## `String`

Definition
```
String str = new String();
```

Check the size
```
int size = str.size();
```

Convert to char array
```
char arrChar[] = str.toCharArray();
```

Char for a specific index i
```
char c = str.charAt(i);
```

Substring
```
String sub = str.substring(i, j) // i inclusive, j exclusive
```

To lowercase
```
String newString = str.toLowerCase(); // str is invariated
```

To uppercase
```
String newString = str.toUpperCase(); // str is invariated
```

Replace all occurence of 'dog' with 'cat'
```
String newString = str.replaceAll('dog', 'cat'); //str is invariated
```

Concatenation
```
String a = "Hello ";
String b = " world";
a += b; // Hello world;
```

## `StringBuilder`

Definition
```
StringBuilder sb = new StringBuilder();
StringBuilder sb = new StringBuilder(n); // with capacity of int n
```

Add something to the stringbuilder, char, Character, int, Integer etc..., it returns a reference to the stringbuilder itself
```
sb.append("hello"); // "hello"
sb.append(4); // "hello4"
```

Return the string
```
String str = sb.toString();
```

## `Character`

Check if character c is a letter
```
boolean isLetter = Character.isLetter(c);
```

Check if character c is alphabetic
```
boolean isAlphabetic = Character.isAlphabetic(c); // i.e. 'V' as roman number is alphabetic but it is not letter
```

Check if character c is uppercase
```
boolean isUpperCase = Character.isUpperCase(c);
```

Check if character c is lowercase
```
boolean isLowerCase = Character.isLowerCase(c);
```

Check if character c is digit
```
boolean isDigit = Character.isDigit(c);
```

Change case without built-in functions
```
char cLower = (char)(c | ' '); // change the c char to lowercase
char cUpper = (char)(c & '_'); // change the c char to uppercase
```

# Primitive 

## Array

Definition array of int of size n
```
int arr[] = new int[n];
```

Insert or update an element at index i
```
arr[i] = v1
```

Get an element at index i
```
int num = arr[i];
```

Get the size of the array
```
int size = arr.length;
```

Fill the entire array with a value v1
```
Arrays.fill(arr, v1);
```

Cast to a List, i.e. int[] -> ArrayList<Integer>
```
List<T> arrList = Arrays.asList(arr);
```

Sorting
```
Arrays.sort(arr; // Ascending
Arrays.sort(arr, (a, b) -> b-a); // Descending
Arrays.sort(arr2D, (a, b) -> a[0]-b[0]) //sort 2d array by the first element only
Arrays.sort(arr2D, (a, b) -> {
    if(a[0] == b[0]) return b[1]-a[1];
    return a[0]-b[0];
}); //sort 2d array by the first element and by the second reverse element (usefull for intervals)
```
