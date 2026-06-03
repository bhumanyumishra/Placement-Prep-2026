recursion is where a function calls itself repeatedly until a specified condition is met.
Time complexity- O(n).
### if we want to print "Bhumanyu" 3 times using recursion.
note-not using loops but recursion.

```cpp
#include <bits/stdc++.h>
using namespace std;
void printName(int i, int n){
    if(i>n){
        return;
        cout<< "Bhumanyu";
        printName(i+1,n);

    }

}
int main(){
    int n;
    cin>>n;
    printName(1,n);
    return 0;
}
```
### print in reverse n-1:-
```cpp
#include <bits/stdc++.h>
using namespace std;
void printName(int i, int n){
    if(i<1){
        return;
    }
    cout<< i << endl;
    printName(i-1,n);
    

}
int main(){
    int n;
    cin>>n;
    printName(n,n);
    return 0;
}
```

In Backtracking, youmust first go deeper into the recursion and then return
using the function first and then printing.
### to print 1-n using backtracking:-
```cpp
#include <bits/stdc++.h>
using namespace std;
void printName(int i, int n){
    if(i<1){
        return;
    }
    printName(i-1,n);
    cout<< i << endl;
    

}
int main(){
    int n;
    cin>>n;
    printName(n,n);
    return 0;
}
```
### for n-1 using backtracking:-
```cpp
#include <bits/stdc++.h>
using namespace std;
void printName(int i, int n){
    if(i>n){
        return;
    }
    printName(i+1,n);
    cout<< i << endl;
    

}
int main(){
    int n;
    cin>>n;
    printName(1,n);
    return 0;
}
```

## Parameterized way
where function is printed only after a specific parameter is met
example:-

### Sum of N numbers 
```cpp
#include <bits/stdc++.h>
using namespace std;
void printSum(int i, int sum){
    if (i<1){
        cout<<sum;
        return;
    }
    printSum(i-1,sum+i);
    

}
int main(){
    int n;
    cin>>n;
    printSum(n,0);
    return 0;
}
```
## Functional Way:-
using functions and returning them.
Time complexity- O(n).
### sum of N numbers
```cpp
#include <bits/stdc++.h>
using namespace std;
int sum(int n){
    if(n == 0){
    return 0;
    }
    return n + sum(n-1);

    

}
int main(){
    int n;
    cin>>n;
    cout<<sum(n);

    return 0;
}
```