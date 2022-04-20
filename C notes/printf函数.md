/*
					            printf函数详细解析
1.printf("占位1 占位2 占位3",替换1,替换2,替换3);
2.printf是一个变参函数
3.printf第一个参数是字符串，包含需要输出的内容，包括占位符
4.printf的第二及后续参数将依次替换占位符
5.占位符的类型和数量需要与后续参数一一对应
6.类型提升：
	printf是一个可变参数，将参数传入函数的可变参数中，变量会发生自动类型提升
7.使用%d占位的：char、short、int
8.使用%ld占位：long    使用%lld占位：long long
9.无符号整型用%u，有符号整型用%d
10.占位符应改为转换规范:%	-+0#	12  	.4	  l	   d
①以%开始
②零个或多个标志字符
标志0：使用0作为填充字符
标志-：使打印左对齐，默认右对齐
标志+：让内容总产生符号
标志#：八进制前加上0，十六进制前加上0X
③十进制表示的最小字段宽度
若最小宽度小于实际，则不做处理
若最小宽度超过实际，用空格在左边补齐
④点号表示精度范围、后面跟着十进制整数
  若整型数位不足，输出将在左边补齐
  若浮点型转换，精度控制小数点后位数
⑤长度指示符、可用：h\hh\l\ll\z表示，其中h表示减半，l表示加倍
⑥单个字符表示的转换操作         整型:%d|%u  %o:八进制字符    %x|%X:十六进制字符    
								 字符型:%c      字符串：%s 
								 浮点型:%f|%e|%E(e表示科学计数法)
                                 例如：取sizeof(int)字节二进制数据—》%d—》字符    (将整型转化为字符输出，打印在控制台上)
                                 数据类型与转化操作错误搭配，有可能造成错误的转化结果
								 取sizeof(int)字节二进制数据—》%c—》ASCII字符    (将字符型转化为ASCII字符输出，打印在控制台上)
								 取sizeof(double)字节二进制数据—》%f—》字符    (将浮点型转化为字符输出，打印在控制台上)
								 取sizeof(char*)字节二进制数据(字符串首地址)—》%s—》字符串    (先找到字符串首地址，打印在控制台上)
	 */
/*
	数据类型与转化操作错误搭配，有可能造成错误的转化结果
	int number1 = -1;
	unsigned int number2 = 42949672957295;
	printf("number1 = %d\n",number1);
	printf("number1 = %u\n", number1);
	printf("number2 = %d\n", number2);
	printf("number2= %u\n", number2);

```c
超出范围，无论怎么打印都错
char number3 = 200;
unsigned short number4 = -32768;
int number5 = 4294967296;
printf("number3 = %d\n",number3);
printf("number3 = %u\n", number3);
printf("number4 = %d\n", number4);
printf("number4= %u\n", number4);
printf("number5 = %d\n", number5);
printf("number5 = %u\n", number5);

整型转换规范
int number6 = 10;
printf("number6 = %d\n",number6);
printf("number6 = %u\n", number6);
printf("number6 = %o\n", number6);
printf("number6 = %x\n", number6);

点号表示精度范围、后面跟着十进制整数
若整型数位不足，输出将在左边补齐
若浮点型转换，精度控制小数点后位数
int number7 = 3456;
double number8 = 23.12469324554;
printf("%.10d\n",number7);
printf("%.3f\n",number8);
printf("%.7f\n",number8);

标志0：使用0作为填充字符
③十进制表示的最小字段宽度
若最小宽度小于实际，则不做处理
若最小宽度超过实际，用空格在左边补齐
int number9 = 1234;
printf("number9 = %06d\n",number9);
printf("number9 = %6d\n",number9);
printf("number9 = %10d\n", number9);

标志-：使打印左对齐，默认右对齐
标志+：让内容总产生符号
int number10 = 123;
int number11 = -99;
printf("%6d %6d\n",number10,number11);
printf("%-6d %-6d\n", number10, number11);
printf("%+d %+d\n", number10, number11);

标志#：八进制前加上0，十六进制前加上0X
int number12 = 34;
printf("number12 = %o\n",number12);
printf("number12 = %#o\n", number12);
printf("number12 = %x\n", number12);
printf("number12 = %#x\n", number12);
```
*/

#include<stdio.h>
int main()
{
	return 0;
}