# Experiment-15

## AIM:
To study and implement recursion.

## THEORY:
A function can call itself to fix smaller instances of the same problem, which is a powerful programming technique known as recursion. Recursion is a technique used in C++ when an issue can be divided into smaller, more manageable subproblems of the same kind that can all be resolved with the same function.

## Key Components of Recursion:
### Base Case: 
The condition needed for ending the recurrence. The function would call itself endlessly in the absence of a base case, resulting in infinite recursion.
### Recursive Case:
The part of the function where it calls within itself to address a more manageable issue.
### How Recursion Works:
When a recursive function is called, the following happens:
In the point where it executes the recursive call, the function pauses.
It makes a new call to the same function but with different (usually smaller) arguments.
Every paused call takes resume where it left off when the base case is satisfied, and the function provides a result.
## FACTORIAL USING RECURSION:
```
//ashu yadav
//23070123154
#include <iostream>
using namespace std;
// Creating a function
int fact (int n){
    if (n<=1){
        // Terminating statement (base condition)
        return 1;
    }
    else {
        return (n*fact(n-1));    // Recursion
    }
}
int main (){
    int X,n;
    cout<< "Enter number : ";
    cin>>n;
    X= fact(n);      // Function calling
    cout<<n<<"!="<<X;
    return 0;
}
```
## OUTPUT:
```
Enter number : 3
3!=6
```
## SUM OF INTEGERS USING RECURSION:
```
//ashu yadav
//23070123154
#include <iostream>
using namespace std;
// Creating a function
int add (int n){
    if (n<=1){
        // Terminating statement (base condition)
        return 1;
    }
    else {
        return (n+add(n-1));    // Recursion
    }
}
int main (){
    int X,n;
    cout<< "Enter number : ";
    cin>>n;
    X= add(n);      // Function calling
    cout<<X;
    return 0;
}
```
## OUTPUT:
```
Enter number : 34
595
```
## REVERSING A STRING USING A RECURSION:
```
//ashu yadav
//23070123154
#include <iostream>
#include <string.h>
using namespace std;
// Creating function
void reverse(char *str){
    if (*str)                      //Base codition
    {
        reverse(str+1);            //Recursion
        cout<<("%c",*str);

    }
}
int main (){
    char a[50];
    cout<<" Enter a string : ";
    cin>>a;
    reverse(a);                   // Function calling
    return 0 ;
}
```
## OUTPUT:
```
Enter a string : saanvi
ivnaas
```
## REVERSING AN INTEGER USING RECURSION:
```
//ashu yadav
//23070123154
# include <iostream>
using namespace std;
// Creating function
void print_reverse(int i){
    if (i>0)                      //Base codition
    {         
        cout<<(i%10);
        print_reverse(i/10);     //Recursion

    }
}
int main (){
    int i;
    cout<<" Enter the number : ";
    cin>>i;
    print_reverse(i);                   // Function calling
    return 0 ;
}
```
## OUTPUT:
```
Enter the number : 123
321
```
## CONCLUSION:
We effectively studied and implemented the idea of recursion in C++ in this experiment. Examples of recursion, which is the process by which a function calls itself to solve smaller sub-problems, included finding the factorial, creating Fibonacci sequences, and searching algorithms. By examining recursive functions, we discovered the following important realizations:

Simpleness of Expression: When a problem is inherently recursive, such as in the case of tree traversal and divide-and-conquer algorithms, recursive solutions frequently offer a clear and simple approach to solve it.
Base Case and Termination: In the absence of suitable ending circumstances, unbounded recursion and stack overflow result. This highlights the significance of having a well-defined base case.
Stack Depth and Limitations: We also discovered that recursive methods may not be suitable for solving some problems due to the possibility of stack overflow errors resulting from deep recursion.
