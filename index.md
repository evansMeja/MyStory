## LINKED LIST NOTES


- linear collection of data elements called nodes where linear order
  is given by  means of pointers
- collection of elements organizes sequentially
- datastructure that contains a finite sequence of n elements where
  n is greater or equal to zero) scattered throughout the main memory
  but related to one another in a linear fashion


each node is divided into two parts namely

data field

link field

the data element with its link form a node


we have four major groups namely

1. single linked lists
2. double linked lists
3. single circular linked lists
4. single circular linked lists

SINGLE LINKED LISTS
------------------
- is conceptually the simplest
- consists of two logical parts
i)  data part
ii) address part or link part or pointer

typedef struct node{
int data;
struct node * next;
} sNODE;

next is used to contain the address of the next node n
 the list whose datatype is struct node
 
 
 operations on a single linked list
 - creation of a new node
 - insertion of a node into linked list
 - deletion of a node
 - searching a node in a linked list
 - reverse the direction of all the links in a single linked list
 - count number of nodes in a linked list
 - concatenation of two linked lists
 
 
 creation of a new node
 Node creation means allocating space of suitable size for the node 
 in memory.In C space allocation is done by malloc(size of data_type).
 This call reserves space of size size(size of data_type) and returns the
 starting address of the allocated space if the memory space of said size
 exists as a chunk.
 
demo
#include<stdio.h>
#include<conio.h>
#include<process.h>

typedef struct node{
int data;
struct node *next;
}sNODE;

int main(){
int ch,item;
sNODE *n1,*n2,*n3;
clrscr();
n1=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n1->data);

n2=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n2->data);

n3=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n3->data);

printf("The data entered is %d\n",n1->data);
printf("The data entered is %d\n",n3->data);
printf("The data entered is %d\n",n4->data);
return 0;
}


The above program shows we have allocated  memory spaces of
three nodes but the problem is that they are independent.So we
have maintained each variable separately which impossible if
there are large numbers.This can be solved if the nodes get related
to ech other



#include   <stdio.h>
#include   <conio.h>
#include   <process.h>

typedef struct node{
int data;
struct node *next;
}sNODE;

int main(){
int ch,item;
struct node *n1,*n2,*n3,*p;
clrscr();
n1=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n1->data);

n2=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n2->data);

n3=(sNODE *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&n3->data);

n1->next=n2;
n2->next=n3;
n3->next=NULL;

p=n1;
while(p!=NULL){
printf("The data entered is %d\n",p->data);
p=p->next
}
return 0;
}



we could have done better by creating links while 
nodes are being created.This way we could have done better
by using one node pointer *n1.



#include  <stdio.h>
#include  <conio.h>
#include  <process.h>
#include  <stdlib.h>

typedef struct node{
int data;
struct node *next;
}sNODE;

int main(){
int ch,item;
struct node *n1=NULL,*p;
clrscr();

for(int i=0;i<3;i++){
p=(struct node *)malloc(sizeof(struct node));
printf("Enter the data:");
scanf("%d",&p->data);
if(n1==NULL){  //first node
p->next=NULL;
n1=p;
}else{
p->next=n1;
n1=p;
}
}
p=n1;
while(p!=NULL){
printf("The data entered is %d\n",p->data);
p=p->next
}
getch();
return 0;
}

 
INSERTION INTO A LINKED LIST
---------------------------
 
 The insertion in a linked list can be done at various positions
 
 (a) Insertion at the beginning
 (b) Insertion at the end
 (c) Insertion at after a specific node
 (d) Insertion of a node in the apppropriate position in a sorted list
 
 
 a) algorithm for insertion of a node at a specific into a linked list at the beginning
 
 -easiest of all insertions if the node you are going to insert is the first
  node
 -if head is null then the node you are inserting is the first node
 
 

 /*c code for insertion of a node into a single linked list at the front*/
 
 void ins_begi(sNODE *head,int item){
 sNODE *p;
 int item;
 
 /*creation of new which is pointed by nw*/
 nw=(sNODE)malloc(sizeof(sNODE));
 scanf("%d",&item); //put input data for the newly created node
 nw->data=item;
 nw->next=NULL;
 if(head==NULL){  //list is empty
 head=nw;
 }else{
 nw->next=head;
 head=nw;
 }
 }
 
 
 /* c code for insertion of a node into a single linked list at the end*/

 void ins_end(sNODE **head,int x){
 sNODE *nw,*q;
 q=*head;
 nw=(sNODE)malloc(sizeof(sNODE));
 if(nw==NULL){  //If creation is unsuccessfull
 printf("Allocation Error");
 exit(0);      //Quit the program
 }
 nw->data=x;
 nw->next=NULL;
 if(q==NULL){
 q=nw;
 }else{
 while(q->next != NULL){
 q=q->next;
 q->next=nw;
 }
 }
 }
 
  /* c code for insertion of a node after a specified node*/
  
  void ins_any(){
  sNODE *nw,*q+;
  int pos,c,y;
  q=*head;
  pos=1;
  
  //creation of new node which is pointed by pointer
  }


 
 
 -
 
 
