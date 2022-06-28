# find-maximum-1-containing-row-in-cpp

TCS NQT
** 
A parking lot in a mall has RxC number of parking spaces. Each parking space will either be  empty(0) or full(1). The status (0/1) of a parking space is represented as the element of the matrix. The task is to find index of the prpeinzta row(R) in the parking lot that has the most of the parking spaces full(1).

Note :

RxC- Size of the matrix

Elements of the matrix M should be only 0 or 1.

Example 1:

Input :

3   -> Value of R(row)

3    -> value of C(column)

[0 1 0 1 1 0 1 1 1] -> Elements of the array M[R][C] where each element is separated by new line.

Output :

3  -> Row 3 has maximum number of 1’s

Example 2:

input :

4 -> Value of R(row)

3 -> Value of C(column)

[0 1 0 1 1 0 1 0 1 1 1 1] -> Elements of the array M[R][C]

Output :

4  -> Row 4 has maximum number of 1’s
**

**CODE**

```

#include<bits/stdc++.h>
using namespace std;
int
main ()
{
  int r, c;
  cin >> r >> c;
  int a[r][c];
  
  int mx = INT_MIN;
int res;
  for (int i = 0; i < r; i++)
    {int cnt=0;
      for (int j = 0; j < c; j++)
	{
	  cin >> a[i][j];
	  if (a[i][j] == 1)
	    cnt++;

	 
	}
	 if (cnt > mx)
	    {
	      mx = cnt;
	      res = i;
	    }
    }

cout<<res+1; 
  return 0;
}

```
SECOND APPROACH

```
#include <bits/stdc++.h>
using namespace std;
int main()
{
int r,c,a,sum=0,m=INT_MIN,in=0;
cin>>r>>c;
for(int i=0;i<r;i++)
{
for(int j=0;j<c;j++)
{
cin>>a;
sum+=a;
}
cout<<"sum"<<sum;
cout<<endl;
if(sum>m)
{
m=sum;
in=i+1;
}
sum=0;
}
cout<<in;
}


