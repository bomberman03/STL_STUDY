# STL_STUDY
---
##### Part 1. C Language 
- In this section we are going to study how to use **scanf** and **printf**   

###### scanf / printf
- C language function for standard input and output  
- Defined in <stdio.h> header file  
- <cstdio> can be used in C++  

###### Formatting
- %d : decimal  
```cpp
int n;  
scanf("%d",&n); // input : 5  
printf("%d\n",n); // output : 5  
```
- %i : decimal  
```cpp
int n, m;  
scanf("%d %i",&n, &m); // input : 10 10   
printf("%d %d\n",n, m); // output : 10 10  
scanf("%d %i",&n, &m); // input : 10 010   
printf("%d %d\n",n, m); // output : 10 8  
scanf("%d %i",&n, &m); // input : 10 0x10   
printf("%d %d\n",n, m); // output : 10 16  
```
- %x : hexadecimal 
- %o : octal
- %s : string  
```cpp
char s[100];  
scanf("%s", s); // input : hello world!   
printf("%s\n", s); // output : hello  
```
- %c : character  
```cpp
char c;  
scanf("%c", &c); // input : hello world!   
printf("%s\n", c); // output : h  
```
- %f : float
- %lf : double
- %Lf : long double

###### Return value of scanf
- On success, the function returns the number of items of the argument list successfully filled.  
```cpp
while ( scanf("%d %d",&a, &b) == 2 ) // read file to the end
```
###### Ignore white space and line break
- scanf ignores white space and line break
```cpp
for ( int i = 0; i<5; i++) {
    scanf("%d", &n); // input : 10 20 30 40 50
    printf("%d\n",n); // output : 10 20 30 40 50 
}
for ( int i = 0; i<5; i++) {
    scanf("%d", &n);// input : 10 
                    //          20      30 
                    //          40 
                    //              50
    printf("%d\n",n); // output : 10 20 30 40 50 
}
```
###### Case Study. 
- Reading **char** right after reading **int**
```cpp
int n;
char a,b,c;
scanf("%d", &n); // input : 10
scanf("%c %c %c", &a, &b, &c); // input : A B C
printf("%d\n", n); // output : 10
printf("%c %c %c\n", a, b, c);  // output :  
                                //          A B
```
###### Problem 
- character variable A read '\n' instead of 'A' 
 
###### Solution 1. Ignore '\n' with white space before reading **character**
```cpp
int n;
char a,b,c;
scanf("%d", &n); // input : 10
scanf(" %c %c %c", &a, &b, &c); // input : A B C
printf("%d\n", n); // output : 10
printf("%c %c %c\n", a, b, c);  // output : A B C
```
###### Solution 2. Explicitly read '\n' after reading **int**
```cpp
int n;
char a,b,c;
scanf("%d\n", &n); // input : 10
scanf("%c %c %c", &a, &b, &c); // input : A B C
printf("%d\n", n); // output : 10
printf("%c %c %c\n", a, b, c);  // output : A B C
```
