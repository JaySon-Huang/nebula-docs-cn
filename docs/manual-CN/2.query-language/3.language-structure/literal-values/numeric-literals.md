# 数值字面值

数值字面值包括整数字面值和浮点字面值。

## 整数

整数为 64 位，并且可以用 `+` 和 `-` 来表明正负性。它们和 C 语言中的 `int64_t` 是一致的。

注意整数的最大值为 `9223372036854775807`。输入任何大于此最大值的整数为语法错误。整数的最小值 `-9223372036854775808` 同理。

## 双浮点数

双浮点数和 C 语言中的 `double` 是一致的。

双浮点数上限和下限分为别 `-1.79769e+308` 和 `1.79769e+308`。

### 科学计数法

Nebula Graph 中，支持用科学计数法表示 Double 类型。例如：

```ngql
nebula> CREATE TAG test1(price DOUBLE);
nebula> INSERT VERTEX test1(price) VALUES 100:(1.2E3);
```