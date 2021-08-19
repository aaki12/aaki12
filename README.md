/* This Pattern
**
**
**
**
*/
#include <iostream>
using namespace std;
int main(){
    int n, m;
    cin >> n >> m;
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= m; j++) cout << "*";
        if (i != n) cout << endl;
    }
    return 0;
}


// pattern 
//*
//**
//***
#include <iostream>
using namespace std;
int main(){
    int n;
    cin >> n;
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= i; j++) cout << "*";
        if (i != n) cout << endl;
    }
    return 0;
}


// n = 8, m = 3
//***#***#**
#include <iostream>
using namespace std;
int main(){
    int n, m;
    cin >> n >> m;
    for (int i = 1; i <= n; i++){
        cout << "*";
        if( i % m == 0) cout << "#";
    }
return 0;
}

/* For this pattern  
1
2 3
4 5 6
7 8 9 10
*/
#include <iostream>
using namespace std;
int main(){
    int n, k = 1;
    cin >> n;
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= i; j++){
         cout << k++;
         if (j != i) cout << " ";
        }
        if (i != n) cout << endl;
    }
    return 0;
}

/* Pattern 
*
##
***
####
*/
#include <iostream>
using namespace std;
int main(){
    int n ;
    cin >> n;
    for (int i = 1; i <= n; i++){
        for (int j = 1; j <= i; j++){
         if (i %2 == 0) cout << "#";
         else cout << "*";
        }
        if (i != n) cout << endl;
    }
    return 0;
}

/*
1234
123
12
1
*/
#include <iostream>
using namespace std;
int main(){
    int n ;
    cin >> n;
    for (int i = 4; i > 0; i--){
        for (int j = 1; j <= i; j++) cout << j;
        if (i != 1) cout << endl;
    }
    return 0;
}
 

//   *
//  * *
// * * *
//* * * *
// n = 4, i = 1, n-i = 3 spaces
// n = 4, i = 2, n-i = 2 spaces
// n = 4, i = 3, n-i = 1 space

#include <iostream>
using namespace std;
int main() {

    int n;
    cout << "Enter N \n";
    cin>>n;
    for(int i = 1;i <= n; i++)
    {
        for(int k = n-i-1; k >=0; k--)
        cout<<" ";
        for(int j = 1; j <= i; j++)
        if (j !=i ) cout<<"* ";
        else cout << "*";
        if(i != n) cout<<"\n";
    }
    return 0;
}


// Diamond shape * print
int n;
cin >> n;
for(int i=1;i<=n;i++)
{
for(int j=n;j>i;j--)cout<<" ";
for(int k=1;k<=i;k++)
{
  cout<<"*";
  if(k!=i)cout<<" ";
}
if(i!=n)cout<<endl;
}
cout<<endl;
//
for(int i=1;i<=n;i++)
{
 for(int j=1;j<=i;j++)cout<<" ";
 for(int k=n;k>i;k--)
 {
  cout<<"*";
  if(k!=i)cout<<" ";
 }
if(i!=n)cout<<endl;
}
    return 0;



//array
#include <iostream>
using namespace std;
int main(){
    int n;
    cin >> n; // size of the array
    int a[n]; // declaration of array of size n
    for (int i = 0; i < n; i++) cin >> a[i];
    for (int i = 0; i < n; i++) {
        cout << a[i];
        if (i != n) cout << " ";
    }
    return 0;
}
Admin FACE5:54 PM
#include <iostream>
using namespace std;
int main(){
    int n;
    cout << "Enter the size of the array :";
    cin >> n; // size of the array
    int a[n]; // declaration of array of size n
    for (int i = 0; i < n; i++){
        cout << "Enter the elements of the array " << i + 1 << ": ";
        cin >> a[i];
    }
    cout << "The elements of the array is:" << endl;
    for (int i = 0; i < n; i++) {
        cout << a[i];
        if (i != n) cout << " ";
    }
    return 0;
}


//Sum of an array

#include <iostream>
using namespace std;
int main(){
    int n, sum = 0;
    cout << "Enter the size of the array :";
    cin >> n; // size of the array
    int a[n]; // declaration of array of size n
    for (int i = 0; i < n; i++){
        cout << "Enter the elements of the array " << i + 1 << ": ";
        cin >> a[i];
        sum += a[i];
    }
    cout << "The sum of the elements of the array is: " << sum;
    return 0;
}

//average of array
#include<iostream>
using namespace std;
int main()
{
	int n, sum = 0;
  	cout << "Enter the number of elements in the array" << endl;
  	cin >> n;
  	if ( n > 20 ){
      	cout << "Invalid input";
  		return 0;
    }
  	int a[n];
  	cout << "Enter the elements in the array" << endl;
  	for (int i = 0; i < n; i++){
    	cin >> a[i];
      	sum += a[i];
    }
  	cout << "The mean of the array is " << sum/n;
  	return 0;
}


// array odd even or mixed
#include<iostream>
using namespace std;
int main()
{
	int n, count = 0 , evencount = 0, oddcount = 0;
	cout << "Enter the number of elements in the array" << endl;
  	cin >> n;
  	int a[n];
  	cout << "Enter the elements in the array" << endl;
  	for (int i = 0; i < n; i++){
    	cin >> a[i];
    	count += 1;
    	if(a[i]%2 == 0)
      	    evencount += 1;
      	else
      	    oddcount += 1;
    };
    if(count == evencount)
        cout << "The array is Even" <<endl
    else if(count == oddcount)
        cout << "The array is Odd" <<endl;
    else
        cout << "The array is Mixed" <<endl;
  	return 0;
}

// Check the array is same or not (if size and sum is equal then array is same)
#include <iostream>
using namespace std;
int main()
{
    int n,m,sum1=0,sum2=0;
    cout << "Enter the size of the 1st array :";
    cin >> n;
    cout << "Enter the size of the 2nd array :";
    cin >> m;
    int a[n],b[m];
    cout << "Enter the elements in the 1st array" << endl;
    for (int i = 0; i < n; i++){
        cin >> a[i];
        sum1 = sum1+ a[i];
        cout<<endl;
    }
cout << "Enter the elements in the 2nd array" << endl;
    for (int i = 0; i < m; i++){
        cin >> b[i];
        sum2 = sum2+ b[i];
        cout<<endl;
    }
    if(m==n && sum1==sum2)cout << "The array is same "<< endl;
    else cout<<"The array is not same "<<endl;
    return 0;
}
