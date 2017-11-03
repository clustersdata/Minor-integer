# Minor-integer

Minor integer

Problem Description

求n个整数中倒数第二小的数。

每一个整数都独立看成一个数，比如，有三个数分别是1，1，3，那么，第二小的数就是1。

Input

输入包含多组测试数据。

输入的第一行是一个整数C，表示有C测试数据；

每组测试数据的第一行是一个整数n，表示本组测试数据有n个整数（2<=n<=10），接着一行是 n个整数 (每个数均小于100);

Output

请为每组测试数据输出第二小的整数，每组输出占一行。

Sample Input

2 2 1 2 3 1 1 3

Sample Output

2 1

代码：

#include<stdio.h>

main()

{
    int T,i,n,a,f,s,m;
    
    for(scanf("%d",&T);T>0;T--)
    
    {
    
        scanf("%d",&n);
        
        f=100;
        
        s=100;
        
        for(i=0;i<n;i++)
        
        {
        
         scanf("%d",&a);
         
         if(a<=s) s=a;
         
         if(s<=f) {m=s;s=f;f=m;}
         
        }
        
        printf("%d\n",s);
        
    }
    
}
