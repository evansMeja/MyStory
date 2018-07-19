a function that calls inself directly or indirectly and approaches towards
a terminating condition or base condition is called a recursive function

specifications
- there must be a creteria called the base criteria for which the function does not call itself
- each time the function calls itself it must be closer to the base criteria


if(some condition for which the answer is known) //base condition
  solve it directly
else
  Again redifine the problem(using revised parameters) using recursion
  
  example
  
  Recursive function of x+y where x and y are both integers
  
  the two integers can be added recursively as follows
  
  3+0=3 and 3+2=1+(3+1)) = 1+1+(3+0)
  
  In general,x+0=x and x+y=1+(x+(y-1)) for y>0
  
  
  /*equivalent c code for x+y*/
  
  int add(int x,int y){
  if(y==0){
  return(x);
  }else{
  return (1+add(x,(y-1)));
  }
  }
  
  Explanation
  
  add(x,y) = 1+ add(x,y-1)  y>0
           =x               y=0
           
  for example,
      add(3,2) = 1 + add(3,1)
      add(3,1) = 1 + add(3,0)
      add(3,0) = 0
      
      add(3,1) =1+3=4
      add(3,2) =1+4=5
      
      
   example
   
   function x^k
   
   /*equivalent c code*/
   
   float power(int x,int k){
   if(k==0){
   return 1;
   }else{
   return x * power(x,k-1)
   }
   }
   
   
   indirect recursion
   
   for example 
   f() calls g()
   g() calls f()
   
   
   nested recursion
   recursion within a recursion
   
   use definition of ackermann function to fins A(1,2)
   
   solution
   /*equivalent C code*/
   
   int A(int n,int m){
   if(n==0){
   return (m+1);
   }else{
   return A(n-1,ack(n,m-1))
   }
   }
   
   
   excessive recursion
   
   int fib(int n){
   if(n==0 || n==1){
   return n;
   }else{
   return (fib(n-1),fib(n-2));
   }
   } 
   
   
   
   
   
   
   
   
   
   
      
