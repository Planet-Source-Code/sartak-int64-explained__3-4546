<div align="center">

## int64 Explained


</div>

### Description

This article is intended to explain the usage of 64-bit integers. It goes over how to declare them (__int64), how to use them in format functions (%I64Ld), and how to convert strings into 64-bit integers (_atoi64).
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Sartak](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/sartak.md)
**Level**          |Beginner
**User Rating**    |4.3 (34 globes from 8 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/sartak-int64-explained__3-4546/archive/master.zip)





### Source Code

<font face = "Comic Sans MS">
First thing's first: how to declare a 64-bit integer. You shouldn't need any header files to do this, depending on your compiler. (I use Microsoft Visual C++)<br>
<br>
<font face = "Courier New">
<b><font color = "#0000FF">__int64<font color = "#000000"></b> <i>identifier</i>;<br>
<font face = "Comic Sans MS">
<br>
Those are <i>two</i> underscores.<br>
<br>
To use a 64-bit integer in a format function (such as <b><font face = "Courier New">sprintf<font face = "Comic Sans MS"></b> or <b><font face = "Courier New">printf<font face = "Comic Sans MS"></b>) we use the following format code:<br>
<br>
For signed values: <font face = "Courier New"><b><font color = "#FF0000">%I64Ld<font color = "#000000"></b><br><font face = "Comic Sans MS">
For unsigned values: <font face = "Courier New"><b><font color = "#FF0000">%I64Lu<font color = "#000000"></b><br><font face = "Comic Sans MS">
<br>
Next: how to convert a string into a 64-bit integer. It's a pretty much like other <font face = "Courier New">ato*<font face = "Comic Sans MS"> functions, which are located in <i>stdlib.h</i>. Here's the prototype:<br>
<br>
<font face = "Courier New">
<i>__int64 <b>_atoi64</b>(const char *);</i><br>
<font face = "Comic Sans MS">
<br>
For example, this is how we could create and print a 64-bit integer.<br>
<br>
<hr><font face = "Courier New">
int main()<br>
{<br>
 <font color = "#0000FF">__int64<font color = "#000000"> NineQuintillion;<br>
 <font color = "#0000FF">unsigned __int64<font color = "#000000"> EighteenQuintillion = 18000000000000000000;<br>
<br>
 NineQuintillion = 9000000000000000000;<br>
<br>
 printf("My first 64-bit integer is <font color = "#FF0000">%I64Ld<font color = "#000000">!\n", NineQuintillion);<br>
 printf("My second 64-bit integer is <font color = "#FF0000">%I64Lu<font color = "#000000">!\n", EighteenQuintillion);<br>
<br>
 return 0;<br>
}
<hr><font face = "Comic Sans MS">
<br>
<br>
Signed 64-bit integers have a range of:<br>
<i>-9,223,372,036,854,775,808</i> to <i>9,223,372,036,854,775,807</i><br>
<br>
Unsigned 64-bit integers have a range of:<br>
<i>0</i> to <i>18,446,744,073,709,551,620</i><br>
<u>That's almost 18 and a half <b>quintillion</b>!</u><br>
<br>
As you can see, 64-bit integers are as simple as the other data types. They don't require any snazzy functions to get the job done, they just have slightly different naming conventions. They act the same as the other number variables, so you can add, subtract, multiply, divide, and modulo divide to your heart's content. If you have any questions, or have any additional 64-bit integer information that should be included here, please, comment. :)

