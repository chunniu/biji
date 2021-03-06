### 字符串编码
#### 字符串语法
>  问题 
> 1. php中字符串的定义方式有哪些？ 
> 2. 双引号中的字符串除了解析变量以外还解析哪些字符？  
> 3. 字符串与其他类型是如何转换的？ 
> 4. 如何获取和修改字符串中的字符

### 1 字符串定义
一个字符串就是由一系列的字符组成，其中每个字符等同于一个字节.php只支持256(2的８次方)的字符集,因此不支持Unicode.   
string 最大可以达到 2GB 

>注 
> 字符串是字符，字符占8位，256(2^8) 

####1.1 字符串的定义方式
1. 单引号
2. 双引号
3. heredoc 语法结构
4. nowdoc 语法结构 (5.3)

#### 1.1 单引号 ''
> 单引号，反斜线， 都用 \ 转义一下 : \' \\  
> 其他任何方式的反斜线都会被当成反斜线本身， 单引号中的变量和特殊字符的转移序列将不会被替换  

#### 1.2 双引号 ""  
> 1. php中的双引号会对转义字符串进行转义： \n 换行 ， \t 回车 \t 水平制表符 \v 垂直制表符 \e Escape(5.4) \f 换页（5.2） \\ 反斜线 \$ 美元标记 \" 双引号  
> \[0-7]{1,3} 符合正则表达式序列 八进制表示的字符  
> \x[0-9A-Fa-f]{1,2} 16进制的表达字符  
> 2. 转义其他字符都会导致反斜线被显示处理

### 1.3 Heredoc 结构
<<<标识符   
string 本身  
标识符  
> 1. 结束时所引用的标识符必须在该行的第一列。（字母,数字,下划线　字母，下划线开头）
> 2. 结束行中除了能有分号（;），不能有其他的字符，不能缩进，空白。更重要的结束符前面必须有一个被当前操作系统认可的换行
> 3. 如果不遵循上述规则，则可能会导致结束标识不“干净”，会继续查找。找不到，会出现"解析错误"。
> 4. heredoc 结构不能用来初始化类的属性。5.3后　只对不包含变量的时候不能使用。  
> 5. 变量会被替换，包含复杂变量的时候小心 

> 其他使用场景：

