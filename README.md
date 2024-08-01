1 program to find GCD using recursive function

#include stdio.h

#include conio.h 

int gcd(int a,int b); 

void main()

{

int a,b, ans; 

clrscr();

printf("\n enter two numbers:"); 

scanf("%d %d",&a,&b);

ans=gcd(a,b);

printf("\n GCD=%d", ans); 

getch();

}

int gcd(int a,int b)

{

if(a==b) return(a);

else 

if(a>b)

return(gcd(a-b,b)); 

else

return(gcd(a,b-a));

}

2 program to find binomial co-efficient  ncr using recursing .

#include stdio.h

#include conio.h 

int fact(int n);

void main()

{

int n,r,ans; 

clrscr();

printf("\n enter n and r values:"); 

scanf("%d %d",&n ,&r);

ans=fact(n)/(fact(r)*fact(n-r));

printf("\n binomial coefficient %d C %d= %d",n ,r, ans); 

getch();

}

int fact(int n)

{

if(n==0)

return (1); 

else

return(n*fact(n-1));

}



3 Program to generate n Fibonacci series up to n terms using recursion.


#include stdio.h

#include conio.h

int fib(int n);

void main()

{

int i,n; 

clrscr();

printf("\n enter the number of elements:"); 

scanf("%d",&n);

printf("\n fibonacci series are: "); 

for(i=1;i<=n;i++)

{

printf("%d ",fib(i));

}

getch();

}

int fib(int n)

{

if(n==0) 

return(0);

else 

if(n==1)

return(1); 

else

return(fib(n-1)+fib(n-2));

4 program to implement Towers of Hanoi

#include stdio.h

#include conio.h 

void tower(int n, char A,char B,char C); 

int count =0;

void main()

{

int n; 

clrscr();

printf("\n enter number of Disks :"); 

scanf("%d", &n);

tower(n, 'A' ,'B','C');

printf("\n number of moves=%d", count); 

getch();

}

void tower( int n, char A, char B, char C)

{

if(n==1)

{

printf("move disk from %c -> %c\n ", A , C); 

count++;

}

else

{
tower(n-1,A,C,B);

tower(1,A,B,C);

tower(n-1,B,A,C);

}

}

5 program to implement dynamic array,find smallest and largest element of the array

#include stdio.h

#include conio.h 

void main()

{

int a[10],n ,i,small ,large; 

clrscr();

printf("\n enter number of elements:"); 

scanf("%d", &n);

printf("\n enter array elements:"); 

for(i=0;i<n ; i++) 

scanf("%d",&a[i]);

large=a[0]; 

small=a[0];

for(i=1;i<n; i++)

{

if (a[ i ]>large) 

large =a[ i ];

else

{

if(a[i]<small) 

small=a[i];
}

}

printf("\n largest element=%d\n ", large); 

printf("\n smallest element = %d",small); 

getch();

}

6  Program to search an element using linear search technique.

#include<stdio.h> 

#include<conio.h>

intlsearch(int a[],int n,int key); 

void main()

{

int a[10],n,i,key,loc; 

clrscr();

printf("\n enter number of elements:"); 

scanf("%d",&n);

printf("\n enter array elements:"); 

for(i=0;i<n;i++)

scanf("%d",&a[i]);

printf("\n enter key elementto search:"); 

scanf("%d",&key);

loc=lsearch(a,n,key);

if(loc==-1)

printf("\n key element not found");
else

}

printf("\n key elementfound atlocation=%d", loc); 

getch();

int lsearch(int a[],int n,int key)

{

int i; 

for(i=0;i<n;i++)

{

if(key==a[i]) 

return(i+1);

}

return(-1);

}


7 program to search an element using recursive binary search technique


#include stdio.h

#include conio.h

int bsearch(int a[],int n,int key); 

void main()

{

int a[10],n,i,key,loc; 

clrscr();

printf("\n enter number of elements:"); 

scanf("%d",&n);

printf("\n enter array elements:"); 

for(i=0;i<n;i++)

scanf("%d",&a[i]);

printf("\n enter key elementto search:"); 

scanf("%d",&key);

loc=bsearch(a,n,key);

if(loc==-1)

printf("\n key element not found");

else

printf("\n key element found at location=%d", loc);

getch();

}
int bsearch (int a[], int n ,int key)

{

int low, high, mid; 

low =0;

high =n-1;

while (low<=high)

{

mid=(low+high)/2;

if(key ==a[mid])

return(mid+1);

else

if(key<a[mid])

high=mid-1;
else

low=mid+1;
}

return(-1);

}



part 2 

1 program to sort the given list using bubble sort technique


#include stdio.h

#include conio.h

void bubblesort(int a[],int n); 

void main()

{

int a[10],n,i; 

clrscr();

printf("\n enter number of elements:"); 

scanf("%d",&n);

printf("\n enter array elements:"); 

for(i=0;i<n;i++)

scanf("%d",&a[i]);

printf("\n before sorting:"); 

for(i=0;i<n;i++) 

printf("\n%d",a[i]);

bubblesort(a,n);

printf("\n after bubble sort:"); 

for(i=0;i<n;i++) 

printf("\n%d",a[i]);

getch();

}
void bubblesort(int a[],int n)

{

int i,j,temp; 

for(i=1;i<n;i++)

{

for(j=0;j<n-i;j++)

{

if(a[j]>a[j+1])

{

temp =a[j]; 

a[j]=a[j+1]; 

a[j+1]=temp;

}

}

}

}

2 program to sort the given list using insertion sort technique


#include stdio.h

#include conio.h

void insertionsort(int a[],int n); 

void main()

{

int a[10],i,n; 

clrscr();

printf("\n enter number of elements:\n"); 

scanf("\n%d",&n);

printf("\n enter array elements:\n"); 

for(i=0;i<n;i++)

scanf("%d",&a[i]); 

printf("\n before sorting:"); 

for(i=0;i<n;i++)

printf("\n %d",a[i]); 

insertionsort(a,n);

printf("\n after sorting insertion :"); 

for(i=0;i<n;i++)

printf("\n %d",a[i]); 

getch();

}

void insertionsort(int a[],int n)

{

int i,j,temp;
for(i=1;i<n;i++) {

for(j=i;j>0;j--

)

{

if(a[j]<a[j-1])

{

temp=a[j]; 

a[j]=a[j-1]; 

a[j-1]=temp;

}

}

}

}

3 Program to sort the given list using selection sort technique



#include stdio.h 

#include conio.h

void selectionsort(int a[],int n); 

void main()

{

int a[10],i,n; 

clrscr();

printf("\nEnter the no. of elements:"); 

scanf("%d", &n);

printf("\nEnter the array elements:"); 

for(i=0;i<n;i++)

scanf("%d", &a[i]); 

selectionsort(a, n); 

printf("\nAfter sorting :\n"); 

for(i=0;i<n;i++)

printf("\n%d", a[i]); 

getch();

}

void selectionsort(int a[],int n)

{

inti,j,temp, small, pos; 

for(i=1;i<n;i++)

{

small=a[i-1];
pos=i-1; 

for(j=i;j<n;j++) {

if(a[j]<small) {

small= a[j]; 

pos=j;

}

}

temp=a[i-1]; 

a[i-1]=a[pos]; 

a[pos]=temp;

}

}

4 program to sort the given list using merge sort technique

#include stdio.h

#include conio.h

void mergesort(int a[],int low,int high); 

void merge(int a[],intlow,int mid,int high); 

void main()

{

int a[10],n,i; 

clrscr();

printf("\n Enter number of array elements:"); 

scanf("%d", &n);

printf("\n Enter array elements:"); 

for(i=0;i<n;i++)

scanf("\n %d",&a[i]); 

printf("\n \nBefore sorting:"); 

for(i=0;i<n;i++)

printf("\n %d",a[i]);

mergesort(a,0,n-1); 

printf("\n\nAfter sorting:"); 

for(i=0;i<n;i++)

printf("\n %d",a[i]); 

getch();

}
void mergesort(int a[],int low,int high)

{

int mid; 

if(low<high)

{

mid=(low+high)/2; 

mergesort(a,low,mid); 

mergesort(a,mid+1,high); 

merge(a,low,mid,high);

}

}

void merge(int a[],int low,int mid,int high)

{

inti,j,k,c[10]; 

i=low; 

j=mid+1; 

k=low;

while((i<=mid)&&(j<=high))

{

if(a[i]<a[j])

{

c[k]=a[i]; 

i++;

k++;

}
else
{
c[k]=a[j]; 

j++;

k++;
}
}
while(i<=mid)
{

c[k]=a[i]; 

i++;

k++;
}

while(j<=high)
{

c[k]=a[j]; 

j++;

k++;
}

for(i=low;i<k;i++) 

a[i]=c[i];
}


5 program to sort the given list using quick sort technique

#include stdio.h 

#include conio.h

void quicksort(int a[],intlow,int high); 

void main()

{

int a[10],n,i; 

clrscr();

printf("\n Enter number of elements:"); 

scanf("%d",&n);

printf("\n Enter array elements:"); 

for(i=0;i<n;i++)

scanf("%d",&a[i]);

printf("\nBefore quicksort: \n"); 

for(i=0;i<n;i++)

printf(" %d\n ",a[i]);

quicksort(a,0,n-1);

printf("\nAfter quicksort: \n"); 

for(i=0;i<n;i++)

printf("%d\n ",a[i]); 

getch();

}

void quicksort(int a[],int low,int high)

{

inti,j,piv,temp; 

i=low+1; 

j=high; 

piv=a[low]; 

if(low<high)

{
while(low<high) {

while((a[i]<piv)&&(i<high)) 

i++;

while((a[j]>piv)&&(j>low)) j--;

if(i<j) {

temp=a[i]; 

a[i]=a[j]; 

a[j]=temp;

}

else {

temp=a[low]; 

a[low]=a[j]; 

a[j]=piv; 

break;

}

}

quicksort(a,low,j-1); 

quicksort(a,j+1,high); }

}



6 program to implement stack operations using array


#include stdio.h

#include conio.h

#include process.h 

#define max 5

int top=-1; 

int stack[5]; 

void Push(); 

void Pop();

void display();

int main()

{

int ch; 

clrscr(); 

while(1)

{

printf("\n\n 1. PUSH");

printf("\n 2. POP");

printf("\n 3. DISPLAY");

printf("\n 4. EXIT"); 

printf("\n\nEnter the choice:");
scanf("%d",&ch); 

switch(ch)

{

case 1: Push(); 

break;

case 2: Pop(); 

break;

case 3: display(); 

break;

case 4: exit(0);

default: printf("\nInvalid choice!!");

}

}

}

void Push()

{

int ele; 

if(top==max-1)

{

printf("\nStack is Overflow!!");

}
else

{

printf("\nEnter elementto push:"); 

scanf("%d",&ele);

top++; 

stack[top]=ele;

}

}

void Pop()

{

if(top==-1)

{

printf("\nStack is Underflow!!");

}

else

{

printf("\nPopped element: %d",stack[top]); 

top--;

}

}
void display()

{

int i; 

if(top==-1)

{

printf("\nStack is Underflow!!");

}

else

{

printf("\n Top-> ");

for(i=top;i>=0;i--)

printf(" %d",stack[i]);

}

}



7 program to implement queue operation using array

#include stdio.h

#include conio.h

#include process.h

#define max 5

int queue[5];

void Qinsert(); 

void Qdelete(); 

void Qdisplay(); 

int rear = - 1;

int front = - 1;

int main()

{

int ch; 

clrscr(); 

while (1)

{

printf("\n\n 1.Insert\n "); 

printf("2.Delete\n "); 

printf("3.Display\n ");
printf("4.Exit\n ");

printf("\n Enter your choice : "); 

scanf("%d", &ch);

switch(ch)

{

case 1:

Qinsert(); 

break;

case 2: 

Qdelete(); 

break;

case 3: 

Qdisplay(); 

break;

case 4:

exit(0); 

default:

printf("\nInvalid choice ");

}

}

}
void Qinsert()

{

int ele;

if(rear == max - 1) 

printf("\nQueue is FULL "); 

else

{

printf("\n Enter the element to insert : "); 

scanf("%d", &ele);

if(rear== - 1)

{

front = 0;

rear = 0;

}

else

rear++; 

queue[rear] = ele;

}

}
void Qdelete()

{

if(front == -1)

printf("\nQueue is Empty\n"); 

else

{

printf("\n Element deleted from queue is : %d", queue[front]); 

if(front==rear)

{

front=-1; 

rear=-1;

}

else

front++;

}

}

void Qdisplay()

{

int i;

if(front == -1)

printf("\n Queue is empty\n ");
else

{

printf("\nQueue is : "); 

printf(" front->");

for(i = front; i <= rear; i++) 

printf(" %d ", queue[i]); 

printf(" rear");

}

}

