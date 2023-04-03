 # `scanf()` 常见用法

在C++中，`scanf()`函数是从标准输入流(stdin)读取数据，并将其存储到提供的变量中。以下是它的常见用法:

```c++
scanf("%d", &integer_variable); // 读取整数并存储到integer_variable变量中
scanf("%f", &float_variable); // 读取浮点数并存储到float_variable变量中
scanf("%lf", &double_variable); // 读取双精度浮点数并存储到double_variable变量中
scanf("%s", string_variable); // 读取字符串并存储到string_variable数组中
```

其中，`%d`表示读取整数，`%f`表示读取浮点数，`%lf`表示读取双精度浮点数，`%s`表示读取字符串。需要注意的是，除`%s`外，其他格式符号前都需要加上`&`符号，表示将数据存储到对应变量的地址中。