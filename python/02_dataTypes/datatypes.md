# Data type or Object types

- Number : 1234 ,3.14 , 3+4j , 0b111, Decimal(), Fraction()

- String : "spam" , "Bob's" , b'a\x01c' , u'sp\xs4m'

- List : [1,[2,"three"],4.5] , list(range(10))

- Tuple : (1,'spam',4,'U') , tuple('spam') , nametuple -> list of same data type

- Dict : {'food':'spam', 'taste':'good'} , dict(hours=10)

- Set: set('abc'), {'a','b','c'} -> store unique elements

- File : open('eggs.txt')

- Boolean : True , False

- None : None

- Functions,modules, classes , instance

- Advance: Decorators , Generators , Iterators

- MetaProgramming


Every data type in python is a object.


Python has no data types so :
INTERVIEW
when the value is stored in memory and the reference attached with it does that mean inside the memory it doesn't have any type?
data ka jho type hai vho memory ma rehta hai na ki variable ma jata hai .
score = 10
score doesn't know anything about type of value.

but inside memory reference have data type.

Python numbers aur strings ko toda alag sa treat karta hai.

a = 3
a = "gys"

so generally python ka garbage collector ko 3 ko delete kar dena chaiye tha par asa nahi karta kyu ki
 (Python numbers aur strings ko toda alag sa treat karta hai.)
Python toda obtimization karka rakta hai , taki agar koi 3 ka reference aaj jaya tho, this helps in computational efficiency.(toda late delete karaga)



Time stamps : 1:57:00 - 2:24:30
// kyu ki list mutable hai.
p1 = [1,2,3]
p2 = p1
p2 = [1,2,3]  // new object created , kyu ki list mutable hai isliya naya reference create hota hai

p1[0] = 28
p1
[28,2,3]
p2
[1,2,3]


// next example

p1 = [1,2,3]
p2 = p1 // reference to same object
p1[0] = 33
p1
[33,2,3]
p2
[33,2,3]



Another Gand Faad variation
h1 = [1,2,3]
h2 = h1[:] // start sa leka end tak jayaga
// but here h2 created a copy of h1 list because of slicing , not refering to h1 object or list
h1 = [1,2,3]
>>> h2 = h1[:]
>>> h2
[1, 2, 3]
>>> h1
[1, 2, 3]
>>> h1[0] = 44
>>> h2
[1, 2, 3]


// variation
import copy
>>> h2 = copy.copy(h1)
>>> h2 = copy.deepcopy(h1)



n = [1,2,3]
m = n

m == n (checks the values are same or not)
true

m is n (checks both have same object in memory)
true
m = [1,2,3]  // new object is created here.

m == n (checks values)
true

m is n (checks for same object)
false