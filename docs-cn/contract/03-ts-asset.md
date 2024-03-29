## 类
超脑TS_lib的ACTION的类如下所示

| 类                                                                                        | 描述                                                 |
| :------------------------------------------------------------------------------------------| :----------------------------------------------------|
| [Asset](docs-cn/contract/03-ts-asset#Asset)                          |类资产管理存储在链上的数字资产。有效资产有两部分：金额和符号。不同的资产有不同的符号。例如，“1000 ugs”和“1000 sys”都是有效资产，但它们是不同的。您可以进行+、-、*、/和逻辑比较，例如=、！=，<=，>=在具有相同符号的资产上。                             |

## Asset
类资产管理存储在链上的数字资产。有效资产有两部分：金额和符号。不同的资产有不同的符号。例如，“1000 ugs”和“1000 sys”都是有效资产，但它们是不同的。您可以进行+、-、*、/和逻辑比较，例如=、！=，<=，>=在具有相同符号的资产上。

#### 使用示例
```nodejs
import { Asset } from "ultrain-contract/src/asset";
```

## 方法列表
超脑TS_lib的ASSET所支持的方法如下表所示。

| 方法                                                                                        | 描述                                                 |
| :------------------------------------------------------------------------------------------| :----------------------------------------------------|
| [StringToSymbol](docs-cn/contract/03-ts-asset#StringToSymbol)                           |将字符串编码为uint64值，例如，让symbol=stringtosymbol（4，“abc”）；//symbol=0x43424104精度数字4表示“.”，资产“100.0000 abc”将与此符号匹配。                              |
| [SymbolNameLength](docs-cn/contract/03-ts-asset#SymbolNameLength)                           |检索符号                              |



## StringToSymbol
```
StringToSymbol(precision: u8, str: string)
```
将字符串编码为uint64值，例如，让symbol=stringtosymbol（4，“abc”）；//symbol=0x43424104精度数字4表示“.”，资产“100.0000 abc”将与此符号匹配。

#### 参数说明
|参数               |类型    |说明                            |是否必填|
| :----------------| :------| :-----------------------------|:-----|
|precision              |u8  |符号精度                     |是     |
|str              |string  |符号为字符串                     |是     |

#### 参考示例
```nodejs
import { StringToSymbol } from "ultrain-contract/src/asset";
```

#### 返回结果类型
`u64`


## SymbolNameLength
```
SymbolNameLength(symbolName: u64)
```
检索符号

#### 参数说明
|参数               |类型    |说明                            |是否必填|
| :----------------| :------| :-----------------------------|:-----|
|symbolName              |u64  |编码符号名称                     |是     |


#### 返回结果类型
`u32`