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
    ```
    int n;
    scanf("%d",&n); // input : 5
    printf("%d\n",n); // output : 5
    ```
- %i : decimal  
    ```
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
    ```
    char s[100];
    scanf("%s", s); // input : hello world! 
    printf("%s\n", s); // output : hello
    ```
- %c : character  
    ```
    char c;
    scanf("%c", &c); // input : hello world! 
    printf("%s\n", c); // output : h
    ```
- %f : float
- %lf : double
- %Lf : long double
