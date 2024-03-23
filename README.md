Calculating the length of string without using length() function.
In this article we will learn how to code a C++ program to calculate the length of string without using length() function. To do so we will iterate each character of the string through a for loop and increase the count until null(‘\0’) is not encountered .

length of the string without using length
Algorithm:
Initialize the variable.
Accept the string.
Initiate a for loop.
Increase the count on every iteration. 
Terminate the loop when null(‘\0’).
Print length.
While loop in C
C++ program to calculate the length of string without using length() function
 

Method 1
Run
#include <iostream>
using namespace std;
 
int main()
{
        //Initializing variable.
	char str[30];
	int i,length=0;
	//Accepting input.
	cout<<"Enter the string:";
	gets(str);
	//Initializing for loop.
	for(i=0;str[i]!='\0';++i)
	{
	length++;//Counting the length.
	}
	
	cout<<"Length of the string is:"<<length<<endl;
 
	return 0;
}
Output:
Enter the string:PREPINSTA
Length of the string is:9
Note
The time complexity of this code is O(n) and if you are using the build in function like strlen or length the time complexity will still be same O(n)
Method 2 (using pointers)
Initialize a variable ‘str’ , ‘length’.
call the function string_length and pass str as parameter store this in length.
in the function loop over the string and Terminate the loop when null(‘\0’).
Print length.
#include <iostream>
using namespace std;
// C++ program to find length of a string using pointers

int string_length(char* p) {
    int count = 0;
    while (*p != '\0') {
        count++;
        p++;
    }
    return count;
}

int main() {
    char str[50];
    int length;
    cout << "Enter any string : ";
    cin >> str;
    length = string_length(str);
    cout << "The length of the given string : " << length;
    cout << endl;
    return 0;
}
