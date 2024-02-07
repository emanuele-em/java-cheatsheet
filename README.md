# Non-Primitive

## Collection interface

### List interface

#### `ArrayList` Implementation

```
//Definition list of Integers
List<Integers> arrList = new ArrayList<>();

//insert an element
arrList.add(num); // TC: O(1)
arrList.add(i, num); // TC: O(n)

// delete an element at index i
arrList.remove(i); // TC: O(n)

// set or update an element at index i
arrList.set(i, num); // TC: O(1)

// get an element at index i
int num = arrList.get(i); // TC: O(1)

// get the size of the list
arrList.size(); // TC: O(1)

// check for Empty
arrList.isEmpty(); // TC: O(1)

// check if there is an element
arrList.contains(num); // TC: O(n)

// get the index of a certain value 'num'
int i = arrList.indexOf(num);

// cast to a primitive list, i.e. ArrayList<Integer> -> int[]
int[] primArr = arrList.toArray();

// sorting
Collections.sort(arrList, (a, b) -> a-b); // Ascending
Collections.sort(arrList, (a, b) -> b-a); // Descending
```

### Set interface

#### `HashSet` implementation

```
//Definition
Set<Integer> set = new HashSet<>();

//insert an element num
set.add(num);

// delete an element num
set.remove(num);

// check for an element num
set.contains(num);

// get the size of the set
set.size();

// check for Empty
set.isEmpty();

// remove all map values
map.clear();
```

### Map Interface

#### `HashMap` implementation

```
//Definition
Map<K, V> map = new HashMap<>();

//insert / update an element with key k1 with value v1
map.put(k1, v1); // TC: O(1)

// Create a counter for letters in a string
Map<Character, Integer> freq = new HashMap<>();
for(char c: str.toCharArray()){
    freq.put(c, freq.getOrDefault(c, 0) + 1);
}

// delete an element with key k1
V deltedEl =  map.remove(k1); // TC: O(1)

// get an element with key k1
V el = map.get(k1); // TC: O(1)

// get the size of the map
map.size(); // TC: O(1)

// check for Empty
map.isEmpty(); // TC: O(1)

// check if there is a value with key k1
map.containsKey(k1); // TC: O(1)

// remove all map values
map.clear(); // TC: O(2n + 1) -> O(n) (n-key, n-value, 1 for map itself)

// in graph problem, when building adjacecy list from an edge List
Map<Integer, List<Integer>> graph = new HashMap<>();
for(int[] edge: edgeList){
    graph.computeIfAbsent(edge[0], val -> new ArrayList<>()).add(edge[1]);
}
```


### Queue Interface

#### `LinkedList` implementation (deque)

```
//Definition
Queue<Integers> queue = new LinkedList<>();

//insert an element
queue.add(num);

// delete element (the head)
queue.poll();

// look up the head element
queue.peek();

// get the size of the list
queue.size();

// check for Empty
queue.isEmpty();
```

##### `PiorityQueue` implementation (priority queue / heap)

```
//Definition
Queue<Integers> heap = new PiorityQueue<>();

//insert an element
heap.add(num);

// delete element (the head)
heap.poll();

// look up the head element
heap.peek();

// get the size of the list
heap.size();

// check for Empty
heap.isEmpty();
```

#### Deque Interface

##### `ArrayDeque` implementation (stack)

```
//Definition
Deque<Integer> stack = new ArrayDeque<>(); // preferred

//insert an element
stack.add(num);

// delete element (the last)
stack.pop();

// look up the last element
stack.peekLast();

// get the size of the list
stack.size();

// check for Empty
stack.isEmpty();
```

##### `ArrayDeque` implementation (deque)

```
//Definition
Deque<Integer> deque = new ArrayDeque<>(); // preferred

//insert an element
stack.add(num);

// delete element (the first)
stack.poll();

// look up the first element
stack.peekFirst();

// get the size of the list
stack.size();

// check for Empty
stack.isEmpty();
```

# String and Character

## `String`

```
//Definition
String str = new String();

// check the size
int size = str.size();

// convert to char array
char arrChar[] = str.toCharArray();

// char for a specific index i
char c = str.charAt(i);

// substring
String sub = str.substring(i, j) // i inclusive, j exclusive

// to lowercase
String newString = str.toLowerCase(); // str is invariated

// to uppercase
String newString = str.toUpperCase(); // str is invariated

// replace all occurence of 'dog' with 'cat'
String newString = str.replaceAll('dog', 'cat'); //str is invariated

// concatenation
String a = "Hello ";
String b = " world";
a += b; // Hello world;

```

## `StringBuilder`

```java
//definition
StringBuilder sb = new StringBuilder();
StringBuilder sb = new StringBuilder(n); // with capacity of int n

// add something to the stringbuilder, char, Character, int, Integer etc...
sb.append("hello"); // "hello"
sb.append(4); // "hello4"

// return the string
String str = sb.toString();
```

## `Character`

```java
// check if character c is a letter
Character.isLetter(c);

// check if character c is alphabetic
Character.isLetter(c); // i.e. 'V' as roman number is alphabetic but it is not letter

// check if character c is uppercase
Character.isUpperCase(c);

// check if character c is lowercase
Character.isLowerCase(c);

// check if character c is digit
Character.isDigit(c);

// change case without buildin functions
char lower = (char)(c | ' '); // change the c char to lowercase
char upper = (char)(c & '_'); // change the c char to uppercase
```

# Primitive 

## Array

```
//Definition array of int of size n
int arr[] = new int[n];

//insert or update an element at index i
arr[i] = v1

// get an element at index i
int num = arr[i];

// get the size of the array
arr.length; // TC: O(1)

// fill the entire array with a value v1
Arrays.fill(arr, v1);

// cast to a List, i.e. int[] -> ArrayList<Integer>
arrList = Arrays.asList(arr);

// sorting
Arrays.sort(arr; // Ascending
Arrays.sort(arr, (a, b) -> b-a); // Descending
Arrays.sort(arr2D, (a, b) -> a[0]-b[0]) //sort 2d array by the first element only
Arrays.sort(arr2D, (a, b) -> {
    if(a[0] == b[0]) return b[1]-a[1];
    return a[0]-b[0];
}); //sort 2d array by the first element and by the second reverse element (usefull for intervals)
```

