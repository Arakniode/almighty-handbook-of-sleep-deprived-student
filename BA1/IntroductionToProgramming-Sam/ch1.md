# Week 4 notes

Char is used to represent any character. 

Java uses unicode for encoding here is how to work with it:

``` java
char c = 'A';
int i = (int)c; 
```

The above block stores the hexadecimal value of c in i. 

Similarly, if we tried character arithmetic with int's the compiler ends up working with the encoded value of char and the assigned value of the int. 

And here is how we read a char as a user input:

``` java
Scanner scan = new Scanner(System.in);
String s = scan.next();

char c = s.charAt(0);
```

**Difference between = and ==**

```java
// this assigns s as a reference to hello world.
String s = "hello world"
// this compares the adress of v1 with that of v2
v1 == v2
```

**Arraylist and Array data types**

In general we choose an arraylist over an array whenever either the table size is initially not known or we would like to extend the structure later on in the code. 

Array syntax:
```java
\\declaration 
int[] scores;
scores = new int[2];
\\ or a shorther way is
int[] scores = new int[2];
\\ or more simply
int[] scores = {1600, 1350, 990};
```
When declaring arrays, if each variable is unassigned here are the default values:

``` java 
int 0
double 0.0
boolean false
char ’\u0000’
(any other object) (null)
```
And some array methods now: 

``` java
scores.length; //returns length of n-1
```

Generally, if we want to make a copy of an array, we can not use the = operator as that simply creates an extra reference towards the same array. We would instead loop through:

```java

for (int i = 0; i<b.length; ++i){
    a[i] = b[i];
}
```
Similarly, to test if two arrays are equal we use the Arrays class:

``` java
Arrays.equals(arr1, arr2);
```

And now we come to the interesting bit, that it tables of multiple dimensions: 

``` java
// representing the 3x3 identity matrix 
int [][] = {
    {1,0,0},
    {0,1,0},
    {0,0,1}
}
```

And the best way to iterate through a multidimensional array is nested for loop:

``` java
for(int i = 0; i < y.length; i++){
    for(int j = 0; j < y[i].length; j++){
        System.out.println(y[i]);
    }
}
```

And finally we list some ArrayList syntax and its methods :

```java

ArrayList<int> t1 = new ArrayList<int>(); 

.size() // instead of .length
.get(index);
.set(index);
.remove(index);
.add(value);
.equals(content);
.clear();
.isEmpty();
```



