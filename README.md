# exm
//FACTORIAL  OF NUMBER(NON-RECURSIVE)
//ALGORITHM:
step1:start
step2:Declare variable n,factorial,i
step3:intialize the variables
      factorial<-1
      i<-1
step4:read the value of n
step5:repeat the steps until i=n
      factorial<-factorial*i
step6:display factorial
step7:stop

//Program
#include<stdio.h>
int main()
{
    int n,i;
    unsigned long long factorial=1;
    printf("Enter the number to find its factorial\n");
    scanf("%d",&n);
    if(n<0)
    printf("Error factorial of negative number not possible\n");
    else
    {
        for(i=0;i<n;i++)
        {
            factorial*=i;
        }
        printf("The factorial of %d number is %llf",n,factorial);
    }
    return 0;
}


//FINDING MAX ELEMENT
//Algorithm
set MAX to array[0]
for i=1 to arraylength-1
if array[i]>MAX Then
set MAX to array[i]
enf if
end for
print max

//Program
#include<stdio.h>
void main()
{
    int a[100],i,max,n;
    printf("Enter the total no of elements\n");
    Scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        printf("Enter the array elements\n");
        scanf("%d",&a[i]);
    }
    max=a[0];
    for(i=0;i<n;i++)
    {
        if(a[i]>max)
        max=a[i];
    }
    printf("Largest elemnt=%d",max);
    
}

LINEAR SEARCH
//Algorithm
for i=0 to arraylength-1
if x=arr[i] Then
return i
end if
end for
return -1

//Program
#include<stdio.h>
void main()
{
    int arr[100],n,i,key;
    printf("Enter the number of elemnts in array\n");
    scanf("%d",&n);
    Printf("Enter the numbers\n");
    for(i=0;i<n;i++)
    {
        scanf("%d",&arr[i]);
    }
    printf("Enter the element to be searched\n");
    scanf("%d",&key);
    for(i=0;i<n;i++)
    {
        if(arr[i]==key)
        {
            printf("%d element is present at location %d",key,i+1);
        }
    }
    if(i==n)
    printf("%d is not present in array\n",key);
}

FACTORIAL OF A NUMBER(RECURSIVE)
//Algorithm
step1:start
step2:Read the value of n
step3:if n==1 return 1
      else return
      n*factorial(n-1)
step4:stop

//Program
#include<stdio.h>
int factorial(int);
int main()
{
    int num,result;
    printf("Enter the number to find its factorial\n");
    scanf("%d",&num);
    if(num<0)
    {
        printf("Factorial of a negative number not possible\n");
    }
    else
    {
        result=factorial(num);
        printf("The factorial of %d is %d\n",num,result);
    }
    return 0;
}
int main(int num)
{
    if(num==0||num==1)
    {
        return 1;
    }
    else
    {
        return(n*factorial(num-1));
    }
}


FINDING GCD OF EUCLIDS
//Algorithm
euclids(m,n)
function gcd(a,b)
if b==0
return a;
else
return gcd(b,a mod b)

//Program
#include<stdio.h>
int gcd(int a,int b)
{
    if(b==0)
    return a;
    return gcd(b,a%b);
}
int main()
{
    int a,b;
    printf("Enter the value of a and b");
    scanf("%d%d",&a,&b);
    printf("GCD of %d and %d is %d",a,b,gcd(a,b));
    return 0;
}


TOWER OF HANOI(RECURSIVE)
//Algorithm
start
procedure hanoi(disk,source,dest,aux)
if disk==1 then
move disk from source to dest
else
hanoi(disk-1,source,aux,dest)
move disk from source to dest
hanoi(disk-1,aux,dest,source)
end if
end procedure
stop

//Program
#include<stdio.h>
#include<time.h>
void hanoi(int n,char rodfrom,char rodmiddle,char rodto)
{
    if(n==1)
    {
        printf("Disk 1 moved from %c to %c\n",rodfrom,rodto);
        return;
    }
    hanoi(n-1,rodfrom,rodto,rodmiddle);
    printf("Disk %d moved from %c to %C\n",n,rodfrom,rodto);
    hanoi(n-1,rodmiddle,rodfrom,rodto);
}
void main()
{
    int n;
    clock_t start,end,total;
    printf("Enter the number of disk:\n");
    scanf("%d",&n);
    start=clock();
    hanoi(n,'A','B','C');
    end=clock();
    total=(end-start)/CLOCKS_PER_SEC;
    printf("Toatl time is %ld",total);
    return 0;
}


BUBBLE SORT
//Algorithm
//input: An array A[0..n-1] of orderable elements
//output: Array A[0..n-1]sorted in non-decreasing order
for i<-0 to n-2 do
for j<-0 to n-2-i do
if a[j+1]<a[j] swap a[j] and a[j+1]

//Program
#include<stdio.h>
#include<time.h>
void main()
{
    clock_t start,end,total;
    int arr[20],i,j,n,temp;
    printf("Enter the total number of elements\n");
    scanf("%d",&n);
    printf("Enter %d numbers:\n",n);
    for(i=0;i<n;i++)
    scanf("%d",&arr[i]);
    start=clock();
    for(i=0;i<n-1;i++)
    {
        for(j=0;j<n-1-i;j++)
        {
            if(arr[j]>arr[j+1])
            {
                temp=arr[j];
                arr[j]=arr[j+1]
                arr[j+1]=temp;
            }
        }
    }
    end=cloc();
    total=(end-start)/CLOCKS_PER_SEC;
    printf("Total time is %lf",total);
    printf("sorted array\n");
    for(i=0;i<n;i++)
    printf("%d\t",arr[i]);
    return 0;

}


MIN MAX
//Algorithm
set max to array[0]
set min to array[0]
for i=1 to arraylength-1
if array[i]>max then
set max to array[i]
else
if array[i]<min then
set min to array[i]
end if-else
end for
print max and min element

//Program
#include<stdio.h>
int main()
{
    int i,n,max,min,arr[20];
    printf("Enter total number of elemnts");
    scanf("%d",&n);
    printf("\n");
    for(i=0;i<n;i++)
    {
        printf("Enter Number %d:",i+1);
        scanf("%d",&arr[i]);
    }
    max=arr[0];
    min=arr[0];
    for(i=1;i<n;i++)
    {
        if(arr[i]>max)
        max=arr[i];
        else if(arr[i]<min)
        min=arr[i];
    }
    printf("\n MAX elemnt-%d\n MIN element=%d\n",max,min);
    return 0;
}


KRUSKAL'S
//Algorithm
//Input: A weighted connected graph G = (V, E )
//Output: ET , the set of edges composing a minimum spanning tree of G
sort E in nondecreasing order of the edge weights w(ei 1 ) ≤ . . . ≤ w(ei| E| )
ET ←NULL;
ecounter ←0 //initialize the set of tree edges and its size
k←0 //initialize the number of processed edges
while ecounter < | V| − 1 do
k← k + 1
if ET 𝖴 { eik} is acyclic
ET← ET 𝖴 { eik};
ecounter ← ecounter + 1
return ET

//Program
#include<stdio.h>
int i,j,k,a,b,v,u,n,ne=1;
int min,mincost=0,cost[9][9],parent[9]; 
void main()
{
    printf("\nEnter the number of vertices\n"); 
    scanf("%d",&n);
    printf("Enter the adjacency matrix::\n"); 
    for (i=1;i<=n;i++)
    for (j=1;j<=n;j++)
    {
        scanf("%d",&cost[i][j]); 
        if(cost[i][j]==0)
        cost[i][j]=999;
    }
    printf("\nThe edges of spanning treeare:\n\n"); 
    while(ne<n)
    {
        for (i=1,min=999;i<=n;i++) 
        for (j=1;j<=n;j++)
        {
            if(cost[i][j]<min)
            {
                    min=cost[i][j];
                    a=u=i; b=v=j;
            }
        }
        while(parent[u]) 
        u=parent[u]; 
        while(parent[v]) 
        v=parent[v]; 
        if(u!=v)
        {
            printf("\n%d\tEdge(%d,%d)=%d",ne++,a,b,min); 
            mincost+=min;
            parent[v]=u;
        }
        cost[a][b]=cost[b][a]=999;
    }
    printf("\n\tMiINCOST=%d\n",mincost);
}


PRIM'S
//Algorithm
//Output: ET , the set of edges composing a minimum spanning tree of G
VT←{ v 0} 
ET←NULL
for i ←1 to | V| − 1 do
find a minimum-weight edge e* = (v*, u*) among all the edges (v, u)
such that v is in VT and u is in
V − VT VT← VT 𝖴 { u*}
ET← ET 𝖴 { e*}
return ET.

//Program
#include<stdio.h>
int i, j, a, b, v, u,n, ne=1;
int min,mincost=0, cost[9][9], visited[9]; 
void main()
{
    printf( "The no of vertices=\t"); 
    scanf("%d",&n);printf("Enter the adjacency matrix=\t"); 
    for( i=1;i<=n;i++)
    for( j=1;j<=n;j++)
    {
        scanf("%d",&cost[i][j]);
        if(cost[i][j]==0) 
        cost[i][j]=999;
    }
    printf("The edges of spanning tree are \t");
    visited[1]=1; 
    while(ne<n)
    {
        for(i=1,min=999;i<=n; i++)
        {
            for(j=1;j<=n;j++)
            {
                if(cost[i][j]<min)
                {
                    if(visited[i]==0) 
                    continue;
                    else
                    {
                        min=cost[i][j]; 
                        a=u=i;
                        b=v=j;
                    }
                }
            }
        }
        if(visited[v]==0)
        {
            printf("\n%d\t Edge \t(%d, %d)=%d\n",ne++, a, b, min); 
            mincost+=min;
            visited[b]=1;
        }
        cost[a][b]=cost[b][a]=999;
    }
    printf("\n\t mincost=%d\n",mincost);
}


MERGE SORT
//Algorithm
//input: an array A[0..n-1] of orderable elemnets
//output: array A[0..n-1]sorted in non-decreasing order
if n>1
copy A[0..[n/2]-1] to B[0..[n/2]-1]
copy A[[n/2]..n-1] to C[0..[n/2]-1]
Mergesort(B[0..[n/2]-1])
Mergesort(C[0..[n/2]-1])
Merge(B,C,A)

Merge(B[0..p-1],C[0..q-1],A[0..p+q-1])
//input: array B[0..p-1] and C[0..q-1] both sorted
//output: sorted A[0..p+q-1] of the elemnts of B and C
i<-0;j<-0;k<-0
while i<p and j<q do
if B[i]<=C[j]
    A[k]<-B[i];i<-i+1
else A[k]<-C[j];j<-j+1
k<-k+1
if i=p
copy C[j..q-1] to A[k..p+q-1]
else copy B[i..p-1] to A[k..p+q-1]

//Program
#include<stdio.h> 
#include<time.h>
#define MAX 50
void mergeSort(int arr[],int low,int mid,int high); 
void partition(int arr[],int low,int high);
double tc;
time_t start,end;
void main()
{
	int a[MAX],i,n;
	printf("Enter the total number of elements: "); 
	scanf("%d",&n);
	printf("Enter the elements to be sorted:\n\n");
	for(i=0;i<n;i++)
	{
		printf("Enter the %d element:",i+1);
		scanf("%d",&a[i]);
		printf("\n");
	}
            start=clock();
	partition(a,0,n-1);
            end=clock();
	printf("After merge sorting elements are: "); 
	for(i=0;i<n;i++)
	{
		printf("%d ",a[i]);
	}
            tc=difftime(end,start)/CLOCKS_PER_SEC;
	printf("time efficiency is %lf",tc);
}

void partition(int arr[],int low,int high)
{
	int mid; 
	if(low<high)
	{
		mid=(low+high)/2; 
		partition(arr,low,mid); 
		partition(arr,mid+1,high); 
		mergeSort(arr,low,mid,high);
	}
}

void mergeSort(int arr[],int low,int mid,int high)
{ 
	int i,m,k,l,temp[MAX];
	l=low; i=low; m=mid+1;
      while((l<=mid)&&(m<=high))
   { 
		if(arr[l]<=arr[m])
       
                      {
			temp[i]=arr[l]; 
			l++;
		}
		
else
		{
			temp[i]=arr[m]; 
			m++;
		}
			i++;
	}
	if(l>mid)
	{
		for(k=m;k<=high;k++)
		{ 
			temp[i]=arr[k];
			i++;
		}
	}
	else
	{
		for(k=l;k<=mid;k++)
		{ 
			temp[i]=arr[k];
			i++;
		}
	}
	for(k=low;k<=high;k++)
	{ 
		arr[k]=temp[k];
	}
}


QUICK SORT
//Algorithm
//input: subarray of array A[0..n-1],defined by its left and right indices la nd r
//output: subarray A[l..r]sorted in nondecreasing order
if l<r
s<-partition(A[l..r])
quicksort(A[l..s-1])
quicksort(A[s+1..r])

Partition(A[l..r])
//Partitions as subarray by Hoare's algorithm, using the first element as a pivot
//input: subarray of A[0..n-1],defined by its left and right indicer l and r(l<r)
//output: Partition of A[l..r],with the split partition returned as this function's value
p<-A[l]
i<-l;j<-r+1
repeat
repeat i<-i+1 until A[i]>=p
repeat j<-j-1 until A[j]<=p
swap(A[i],A[j])
until i>=j
swap(A[i],A[j])
swap(A[l],A[j])
return j

//Program
#include<stdio.h> 
# include<time.h>
#define max 500
double tc;
time_t start,end;
void qsort(int [],int,int); 
int partition(int [],int,int); 
int main()
{
	int a[max],i,n;
	printf("Enter the total number of elements: "); 
	scanf("%d",&n);
	printf("Enter the elements to be sorted:\n\n");
	for(i=0;i<n;i++)
	{
		printf("Enter the %d element:",i+1);
		scanf("%d",&a[i]);
		printf("\n");
	}

	printf("\nThe array elements before\n"); 
	for(i=0;i<n;i++)
		printf("%d\t",a[i]);
                start=clock();
	qsort(a,0,n-1);
                end=clock();
	printf("\nElements of the array after sorting are:\n"); 
	for(i=0;i<n;i++)
		printf("%d\t",a[i]);
               tc=difftime(end,start)/CLOCKS_PER_SEC;
	printf("time efficiency is %lf",tc);
}

void qsort(int a[],int low,int high)
{
	int j; if(low<high)
	{
		j=partition(a,low,high); 
		qsort(a,low,j-1); 
		qsort(a,j+1,high);
	}
}

int partition(int a[], int low,int high)
{
	int pivot,i,j,temp; pivot=a[low]; i=low+1;
	j=high; 
	while(1)
	{
		while(pivot>a[i] && i<=high) 
		i++;
		while(pivot<a[j])
		j--;
		if(i<j)
		{
			temp=a[i]; 
			a[i]=a[j]; 
			a[j]=temp;
		}
		else
		{
			temp=a[j]; 
                  a[j]=a[low]; 
			a[low]=temp;
		 return j;
		}
               }
}


INSERTION SORT
//Algorithm
//input: an array A[0..n-1] of n orderable elements
//output: array A[0..n-1] sorted in non decreasing order
for i<-1 to n-1 do
v<-A[i]
j<-i-1
while j>=0 and A[j]>v do
A[j+1]<-A[j]
j<-j-1
A[j+1]<-v

#include <math.h>
#include <stdio.h>
#include<time.h>

void insertionSort(int arr[], int n)
{
    int i, key, j;
    for (i = 1; i < n; i++) {
        key = arr[i];
        j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}
int main()
{
    int arr[20],n,i;
    clock_t  start, end, total;
    printf("enter array size<20\n");
    scanf("%d",&n);
    printf("enter array elements\n");
    for(i=0;i<n;i++)
    scanf("%d",&arr[i]);
    start = clock();
    insertionSort(arr, n);
    end = clock();
    total = (end-start)/CLOCKS_PER_SEC;
    printf("array after sorting is\n");
    for (i = 0; i < n; i++)
        printf("%d ", arr[i]);
    printf("\n");
    printf("time taken=%f",total);
    return 0;
}


FLOYD'S
//Algorithm
//input: THe weight w of a graph with no negative shortest paths problem
//output: The distance matrix of the shortest paths lengths
D<-W
for k<-1 to n do
for i<-1 to n do
for j<-1 to n do
D[i,j]<-min{D[i,j],D[i,k]+D[k,j]}
return D

//Program
#include<stdio.h>
#include<time.h>
clock_t  start, end, total; 
int min(int,int);
void floyds(int p[10][10],int n)
{
int i,j,k; 
	for(k=1;k<=n;k++) 
		for(i=1;i<=n;i++) 
			for(j=1;j<=n;j++)
				if(i==j) 
					p[i][j]=0; 
				else
				p[i][j]=min(p[i][j],p[i][k]+p[k][j]);
}

int min(int a,int b)
{
if(a<b) return(a); else return(b);
}

void main()
{
	int p[10][10],w,n,e,u,v,i,j;
	printf("\n Enter the number of vertices:"); 
	scanf("%d",&n);
	printf("\n Enter the number of edges:\n"); 
	scanf("%d",&e);
	for(i=1;i<=n;i++)
		{
		for(j=1;j<=n;j++)
			p[i][j]=999;
		}
	for(i=1;i<=e;i++)
	{
		printf("\n Enter the end vertices of edge%d with its weight \n",i); 
		scanf("%d%d%d",&u,&v,&w);
		p[u][v]=w;
	}
printf("\n Matrix of input data:\n");

for(i=1;i<=n;i++)
{
	for(j=1;j<=n;j++) 
		printf("%d\t",p[i][j]); 
		printf("\n");
}
start=clock();
floyds(p,n);
end=clock();
printf("\n Transitive closure:\n"); 
for(i=1;i<=n;i++)
{
	for(j=1;j<=n;j++) 
		printf("%d\t",p[i][j]); 
		printf("\n");
}
printf("\n The shortest paths are:\n"); 
for(i=1;i<=n;i++)
	for(j=1;j<=n;j++)
	{
		if(i!=j)
		printf("\n <%d,%d>=%d",i,j,p[i][j]);
	}
total = (end-start)/CLOCKS_PER_SEC;
printf("\ntime taken=%f\n",total);
}


NQUEEN'S
//Algorithm
Backtrack(X[1..i])
//input: X[1..i] specifies first i promising components of a solution
//output:All the tuples representing the problem's solution
if X[1..i] is a solution write X[1..i]
else
for each element x<-si+1 consistent X[1..i] and the constraints do
X[i+1]<-s
Backtrack(X[1..i+1])

//Program
#include<stdio.h> 
#include<time.h> 
#include<math.h>
#include<stdlib.h>
const int max=20;
clock_t  start, end, total; 
int  place(int x[],int k)
{
int i; 
for(i=0;i<k;i++)
	if (x[i]==x[k] || abs(x[i]-x[k])==abs(i-k)) 
	return 0;
return 1;

}
void display(int x[], int n)
{
	char chessb[max][max]; 
	int i,j;
	for(i=0;i<n;i++) 
		for(j=0;j<n;j++)
			chessb[i][j]='x';
 	for(i=0;i<n;i++)
		chessb[i][x[i]]='q';

	for(i=0;i<n;i++)
	{
 		for(j=0;j<n;j++)
			printf("%c", chessb[i][j]);

		printf ("\n");
	}
      printf ("\n");

}


void nqueens(int n)
{
	int x[max]; 
	int k; 
	x[0]=-1; 
	k=0;
	while(k>=0)
	{
		x[k]=x[k]+1;
		while(x[k]<n && !place(x,k)) 
			x[k]=x[k]+1;
		if(x[k]<n)
			if (k==n-1)
				display(x,n); 
			else
			{
				k++; x[k]=-1;
			}
		else
		k--;
	}
}

void main()
{
int n;
printf("enter the no of queens\n"); 
scanf("%d", &n);
printf("the soln to %d queens problem is \n", n);
start=clock();
nqueens(n);
end=clock();
total = (end-start)/CLOCKS_PER_SEC;
printf("\ntime taken=%f\n",total);
}
