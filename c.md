# c-language

c语言要用的的一些代码片段 ，以整理为主。



1、创建工程的时候选择OSX->Application->Command Line Tool，进入创建工程的对话框，这个时候可以选择语言了，C++，C，Swift，OC都可以。

2、默认情况下会根据你选择的语言创建一个main文件，可以直接运行，或者拷贝书上的例子运行运行的过程中，可以在output面板进行输入和查看输出。


以下是目录

/*

 题目1 ：对数组中的数据，正向输入后，反向输出

 scan  扫描  print 打印出  

 int 整形  a[10]数组(10个长度)

 "%d"是输出输入格式为整型  &a[i] 取地址符 输入时要用&;输出时不用;

 \n新行

 void 是不用返回值 如果有返回值，要写返回的类型如int float等

 %5d 代表输出占用5个字节的空间

*/
```
void main(){
 int i,a[10];
 for(i=0;i<10;i++)scanf("%d",&a[i]);
 for(i=9;i>=0;i--)printf("%5d",a[i]);
 printf("\n");
}  
```
/*
题目2 ：三个数中找出一个最大的

scanf("%d%d%d",&a,&b,&c); 输入abc三个整形  %d%d%d 为三个占位符

原理: 把ab大的给max，然后再max与c，大的给max，最后输出max;就是最大的；
*/
```
void main(){
 int a,b,c,max;
 scanf("%d%d%d",&a,&b,&c);
 printf("a=%d,b=%d,c=%d ",a,b,c);
 if(a>b)max=a;
 else max=b;
 if(c>max)max=c;
 printf("max=%d\n",max);
}
```
/*

题目3：找出水仙花数
所谓"水仙花数"是指一个3位数,其各位数字立方和等于该数本身.例如153是一个水仙花数,因为153=1的立方+5的立方+3的立方.
n是要找的数abc符合上面的概念

*/
```
void main(){
 int n,a,b,c;
 for(n=100;n<=999;n++){
    a=n%10;   //十位
    b=n/10%10; // 个位
    c=n/100;   // 百位
    if(a*a*a+b*b*b+c*c*c==n)printf("%5d",n);
 }
}
```
/*
题目4 ：求最大公约和最小公倍	

方法之一：在主函数中，最大公约使用循环  gcd 最大公约数(2数相减)   gcp 最小公位数(积/小的那个)

*/
```
void main(){ 
  int m=24,n=36,mn;
  mn=m*n;
  while(m!=n)
   if(m>n)m-=n;
   else n-=m;
  printf("gcd=%d,gcp=%d\n",m,mn/m);
}
```
/*
题目4 ：求最大公约和最小公倍 

方法之二：主函数分别调用两个函数求最大公约（递归方法）和最小公倍

*/

/* 求最大公约数 */
```
int gcd(int m , int n){ 
  if(m==n) return m;                     
  else if(m>n)return gcd(m-n,n);                       
       else return(m,n-m);
}
```
/* 求最小公倍数 */
```
int gcp(int m , int n){ 
  return m*n/gcd(m,n);
}
void main(){ 
  int a,b;
  sacnf("%d%d",&a,&b); 
  printf("a=%d,b=%d,最大公约数=%d,最小公倍数=%d\n",a,b,gcd(a,b),gcp(a,b));
}
```

/** 
 * 05 对成绩五级评分
 * @param  之一：分数为整型   自动舍去小数
 * @param return void 
 * score/10 由于score定义的类型是int ，所以得到的是 整数；
 */
```
void main(){ 
 int score;
 scanf("%d",&score);
 printf("score=%d",score);
 switch(score/10){ 
  case 10: 
  case 9:printf("优秀\n");break;
  case 8: printf("良好\n");break;
  case 7: printf("中等\n");break; 
  case 6: printf("及格\n");break; 
  default: printf("不及格\n");
 }
}
```
// 输入数据：xx↙
   

/**
 *  之二：分数为实型
 *  %.1f  %.1f后.只输出整数+小数点后1位
 *  %f float,单精度浮点型,对应%f 有效位是7位
 *  (int)(score/10)  强制类型转换
 */
```
void main(){ 
  float score;
  scanf("%f",&score);
  printf("score=%.1f ",score);
  switch((int)(score/10)){//在这进行的强制类型转换
    case 10: 
    case 9:printf("A\n");break;
    case 8:printf("B\n");break; 
    case 7:printf("C\n");break; 
    case 6:printf("D\n");break;
    default:printf("E\n");
  }
}
```
// 输入数据：xx.x↙
  

/**
 * 06  输入一串字符（换行作为结束）统计元音（a,A;e,E;i,I;o,O;u,U）各自出现的次数
 * char : 可以使用sizeof运算符获取数据类型占多少字节。一般char类型占1个字节. 如果转换成二进制就是int型，就占4个字节
 * #include<stdio.h> 头文件
 * ch=getchar( ) 从键盘输入一个字符型数据，把值赋给变量ch
 */
```
#include<stdio.h>
void main( ){
char ch;
int a=0,e=0,i=0,o=0,u=0;
 printf("输入一串字符，换行作为结束：");
 while((ch=getchar( ))!='\n')
  switch(ch){
    case  'a': 
    case  'A': a++;break;
    case  'e': 
    case  'E': e++;break;
    case  'i': 
    case  'I': i++;break;
    case  'o': 
    case  'O': o++;break;
    case  'u': 
    case  'U': u++;
  }
  printf("a,A=%d\ne,E=%d\ni,I=%d\no,O=%d\nu,U=%d\n",a,e,i,o,u);
}
```

/**
 * 正序和反序打印大小写英文字母 用的是隐士类型转换成ascii码进行的转换
 * 
 */
```
void main(){
 char ch;
 // 正序
 for(ch=’A’;ch<=’Z’;ch++)
  printf("%c",ch);
  printf("\n");
  // 反序
  for(ch=’z’;ch>=’a’;ch--)
  printf("%c",ch);
  printf("\n");
}

```
/**
 * 08-1  选择法排序 交换
 * #define N 10 宏定义 N=10 不用加分号
 */
```
#define N 10
void main(){ 
  int i,j,t,a[N]={1,0,2,9,8,4,7,6,5,3};
  for(i=0;i<N-1;i++)
   for(j=i+1;j<N;j++)if(a[i]>a[j]){t=a[i];a[i]=a[j];a[j]=t;}
  for(i=0;i<N;i++)printf("%5d",a[i]);
  printf("\n");
}
```
/**
 * 08-2 冒泡法排序
 */
```
#define N 10
void main(){

  int i,j,t,a[N];
  for(i=0;i<N;i++)scanf("%d",&a[i]);

  for(i=0;i<N-1;i++)
  for(j=0;j<N-1-i;j++)if(a[j]>a[j+1]) t=a[j],a[j]=a[j+1],a[j+1]=t;  
  
  for(i=0;i<N;i++)printf("%5d",a[i]);

  printf("\n");

}
```

/*

09	九九表 
1
2    4
3    6    9
4    8   12   16
………………………..	.   
*/
```
void main(){
  int i,j;
  for(i=1;i<=9;i++){ 
    for(j=1;j<=i;j++)printf("%4d",j*i);
         printf("\n");
  }
}
```

/**
 * 10 求字符串输出
 * Word,因为\0作为字符串结束符，使用%s格式输出时遇到\0既字符串结束。
 */  
```        
void main(){ 
   char www[ ]="World\0Wide\0Web";
     printf("%s\n",www);
 }
 ```