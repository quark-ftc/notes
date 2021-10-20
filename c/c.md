# c语言

## c语言的编译过程

test.c(预处理`gcc -E > test.i`)--->test.i(编译`gcc -S test.i`)--->test.s(汇编`gcc -c test.s`)--->test.o(链接`gcc test.o`)--->test.out

## gcc常见编译选项

`-E`
>top after the preprocessing stage; do not run the compiler proper.  The output is in the form of preprocessed source code, which is sent to the standard output.Input files that don't require preprocessing are ignored.

`-S`
>Stop after the stage of compilation proper; do not assemble.  The output is in the form of an assembler code file for each non-assembler input file specified.By default, the assembler file name for a source file is made by replacing the suffix .c, .i, etc., with .s.

`-c`
>Compile or assemble the source files, but do not link.  The linking stage simply is not done.  The ultimate output is in the form of an object file for each source file. By default, the object file name for a source file is made by replacing the suffix .c, .i, .s, etc., with .o.


## 数组

### 一维数组

数组的定义`int arr[10]`

数组的初始化:

1. 不初始化

    未初始化的全局变量被默认初始化，未初始化的局部变量被的值是未定义的。

2. 全部初始化
    `int arr[10] = {1,2,3,4,5,6,7,8,9,10}`

3. 部分初始化
    `int arr[10] = {1}` arr[0]值为1，其余值被初始化为0

4. 当定义的时候进行初始化，可以省略数组的大小
    `int arr[] = {1,2,3,4,5}`

### 二维数组

二维数组的定义

二维数组的定义：`int arr[10][20]`

二维数组的初始化：

1. 不初始化

    未初始化的全局变量被默认初始化，未初始化的局部变量被的值是未定义的。

2. 全部初始化：
   
   ```c
   int arr[5][2] = {{1,2},{3,4},{5,6},{7,8},{9,10}};
   ```

   ```c
   int arr[5][2] = {1,2,3,4,5,6,7,8,9,10};
   ```

    ```C
    int arr[][2] = {1,2,3,4,5,6,7,8,9,10}//全部初始化时第二个元素可以省略
    ```

    3.部分初始化

    ```c
    int arr[5][2] = {{1,2},{3}};//第一行两个元素是1，2；第二行第一个元素是3
    ```

    ```c
    int arr[5][2] = {1,2,3} //与上一行等价
    ```









