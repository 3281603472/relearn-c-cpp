# scanf函数
分享我对 `scanf` 函数的一些见解
## 1.scanf函数的功能
执行格式化输入，所谓格式化输入，我认为是按照某种特定的格式从标准输入（如键盘）读取数据并存储到变量中。
## 2.scanf调用格式
    scanf("<格式化字符串>"，地址);
## 3.常见格式化说明符
用于替代<格式化字符串>部分的说明符
| 数据类型 | 格式符号 | 举例 |
| ------- | ------- | ---- |
| int | %d | scanf("%d",&n) |
| long | %ld | scanf("%ld",&n) |
| long long | %lld | scanf("%lld",&n) |
| float | %f | scanf("%f",&fl) |
| double | %lf | scanf("%lf",&db) |
| char | %c | scanf("%c",&a) |
| char数组（字符串） | %s | scanf("%s",&arr) |

**值得注意的是**，可以通过指定宽度来控制读入固定位数，格式为`%<宽度><格式符号>`
## 4.scanf返回值
返回值为成功读入的数据项数，读入数据时遇到了“文件结束”则会返回`EOF`.
    scanf("%d %d",&a,&b);
若ab都读取成功则返回2；
若a读取成功b读取失败则返回1；
若a读取失败则返回0；
若遇到错误或`end of file`，返回值为`EOF`，`end of file`为`Ctrl+Z`或者`Ctrl+D`.