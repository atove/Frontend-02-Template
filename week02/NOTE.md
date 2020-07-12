# 重学 JavaScript

## 语言按语法分类

非形式语言

中文、英文

形式语言(乔姆斯基谱系)

- 0型 无限制文法  ?::=?
- 1型 上下文相关文法  ?\<A\>?::=?\<B\>?
- 2型 上下文无关文法  \<A\>::=?
- 3型 正则文法  <A\>::=<A\>?

## 产生式(BNF)

- 用尖括号括起来的名称来表示语法结构名
- 语法结构分成基础结构和需要用其他语法结构定义的复核结构
  - 基础结构称为终结符
  - 复合结构称为非终结符
- 引号和中间的字符表示终结符
- 可以有括号
- *表示重复多次
- |表示或
- +表示至少一次

### 带括号四则运算产生式

带括号的四则运算：（1+2）*3
终结符：+ - * / （ ）
非终结符：MultiPlicativeExpress AddtiveExpression MixedExpression
BNF：

```html
<MultiplicativeExpression>::=<Number>|<MultiplicativeExpression>"*"<Number>|<MultiplicativeExpression>"/"<Number>|

<AddtiveExpression>::=<MultiplicativeExpression>|<AddtiveExpression>"+"<MultiplicativeExpression>|<AddtiveExpression>"-"<MultiplicativeExpression>|

<MixedExpression>::="("<AddtiveExpression>")"|<MixedExpression>"*"<MixedExpression>|<MixedExpression>"/"<MixedExpression>|<MixedExpression>"+"<MixedExpression>|<MixedExpression>"-"<MixedExpression>
```

javascript：

整体上是 上下文无关文法

表达式：大部分是正则文法， ** (乘方) 2\*\*1\*\*2 结果是2 右结合

**形式语言-用途：**
数据描述语言 JSON 、HTML、XAML、SQL、CSS 
编程语言： C++、C、Java、C#、Python、Ruby、Perl、Lisp、T-SQL、Clojure、Haskel、JavaScript

**形式语言-表达方式：**
声明式语言 JSON 、HTML、XAML、SQL、CSS 、Lisp、Clojure、Haskel
命令型语言： C++、C、Java、C#、Python、Ruby、Perl、T-SQL、JavaScript

TODO：

Number

