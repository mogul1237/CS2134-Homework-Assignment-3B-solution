# CS2134-Homework-Assignment-3B-solution

Download Here: [CS2134 Homework Assignment 3B solution](https://jarviscodinghub.com/assignment/cs2134-homework-assignment-3b-solution/)

For Custom/Original Work email jarviscodinghub@gmail.com/whatsapp +1(541)423-7793

Assignment 3B include a programming portion and a written part. The programming portion must compile and consist of a single ﬁle ( hw03B.cpp). he written portion should consist of a single ﬁle (hw03Bwritten) in a .pdf format. Be sure to include your name at the beginning of each ﬁle! You must hand in the ﬁle via NYU Classes.
Programming Part:
Enter data from the ﬁle MTA_train_stop_data.txt. The data from this assignment is from https://www.mta.info/developers/download.html. (Please note that we will only be using some of the information in this ﬁle for this assignment.1) In the batch phase you will read all the data from the ﬁle called MTA_train_stop_data.txt into a container of type vector. Your program will deﬁne the class trainStopData. It has the following private member variables :
string stop_id; // id of train stop (1st token) string stop_name; // name of station (4th token) double stop_lat; // latitude of train stop location double stop_lon; // longitude of train stop location
Your class should also have a constructor and the following public member functions:
string get_id( ) const string get_stop_name( ) const double get_latitude( ) const double get_longitude( ) const
1The data is in a common format; please read https://developers.google.com/transit/gtfs/reference?csw=1 for more information.
1
Written Part:
The C++ STL has many functions and functors. Here is your chance to try some of them. In a program when you use an STL algorithm add #include, and when you use an STL functor add #include. For many of these problems you will need to look up information online. Here are some sources: https://en.cppreference.com/w/cpp https://www.cplusplus.com/reference/algorithm/ https://www.cplusplus.com/reference/std/functional/ https://www.sgi.com/tech/stl/ Fill in the correct code where you see a ****
vector A {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}; vector B {1, 2, 1, 2, 1, 2}; vector C{1, 2, 3, 1, 2, 3}; vector D(6); vector E(10);
1. Copy the ﬁrst 6 items of vector A into vector D
copy(****, ****, ****); // D now equals {1, 2, 3, 4, 5, 6}
2. Count the number of ones in vector B
cout << count(****, ****, 1); //prints out the number of times a one appears in B 3. In C++, there is a way to construct a unary functor from a binary functor. To do this you use an adapter, a function called bind1st or bind2nd. We use bind1st in this example to convert the STL binary predicate functor not_equal_to into a unary predicate by setting its ﬁrst value to 1. Count the number of items that are not equal to one in B cout << count_if(B.begin( ), ****, bind1st(not_equal_to( ), 1)); /*prints out the number of times a one doesn’t appear in B.*/
4. Test to determine if the ﬁrst 3 items of A are the same as C.
bool same; same = equal(A.begin( ), ****, ****);
2
5. Find the ﬁrst item in vector A which equals 5
vector::iterator vecItr; vecItr = find(****, ****, 5); // returns an iterator to 5 in vector A if (vecItr != A.end( )) cout << ****; // prints out the value pointed to by vecItr 6. Find the ﬁrst item in C that is greater than 2 vecItr = find_if(****, ****, bind2nd(greater(), 2)); // returns an iterator to 3 in C if (vecItr != C.end( )) cout << ****; // prints out the value pointed to by vecItr 3
