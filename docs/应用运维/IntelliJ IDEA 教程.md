---
title: IntelliJ IDEA 教程
copyright: CC-BY-4.0
tags:
  - idea
createTime: 2025/04/15 10:04:15
permalink: /blog/inc8xt0r/
---

## 1.参考

[官方地址](https://www.jetbrains.com/idea/)

## 2.前置条件

**系统版本:** windows macos linux

**软件依赖:** 无

**权限要求:** 无

**网络要求:** 无

**其他注意事项:** 无

## 3.环境准备

## 4.安装部署

## 5.设置说明

### 5.1.编辑器/实时模板

#### 5.1.1.javadoc 类注释模板

**缩写**：`*`

**说明**：javadoc 类注释模板

**适用于**：`java`

**模板文本**：

```java
**
 * 
 * <p></p>
 * @author gengchen
 * @since $date$ $time$
 */
```
**编辑变量**

| 变量名 | 表达式   |
| ------ | -------- |
| date   | `date()` |
| time   | `time()` |

**测试输出**：

```java
/**
 * 
 * <p></p>
 * @author gengchen
 * @since 2026/4/15 21:55
 */
```
#### 5.1.2.javadoc 方法注释模板

**缩写**：`**`

**说明**：javadoc方法注释模板

**适用于**：`java`

**模板文本**：

```java
**
 *
 * <p></p> $javadoc$
 * @author gengchen
 * @since $date$ $time$
 */
```
**编辑变量**

| 变量名  | 表达式                                                       |      |
| ------- | ------------------------------------------------------------ | ---- |
| javadoc | `groovyScript("def r='',ps=_1.toString().replaceAll('[\\\\[|\\\\]|\\\\s]','').split(',').toList(),ts=_2.toString().replaceAll('[\\\\[|\\\\]|\\\\s]','').split(',').toList(),rt=_3.toString();def hasP=!(ps.size()==0||(ps.size()==1&&ps[0]==''));if(hasP){for(i=0;i<ps.size();i++){def t=ts[i].contains('.')?ts[i].substring(ts[i].lastIndexOf('.')+1):ts[i];r+=(i>0?'\\n * ':'')+('@param '+ps[i]+' {@link '+t+'}');}};def ret=rt==''||rt=='null'||rt=='void'?'':'@return {@link '+(rt.contains('.')?rt.substring(rt.lastIndexOf('.')+1):rt)+'}';if(hasP&&ret!='')r+='\\n * '+ret;else if(!hasP)r+=ret;return r==''?null:'\\n * '+r", methodParameters(), methodParameterTypes(), methodReturnType())` |      |
| date    | `date()`                                                     |      |
| time    | `time()`                                                     |      |

**测试输出**：

```java
/**
 * @param request {@link SysUserRequest}
 * @param ignoreDisable {@link Boolean}
 * @return {@link SysUser>>}
 * @author gengchen
 * @since 2026/4/15 18:57
 */
```
#### 5.1.3.javadoc 方法继承注释模板

**缩写**：`***`

**说明**：javadoc 方法继承注释模板

**适用于**：`java`

**模板文本**：

```java
**
 * {@inheritDoc}
 */
```
**编辑变量**

| 变量名 | 表达式   |      |
| ------ | -------- | ---- |
| date   | `date()` |      |
| time   | `time()` |      |

**测试输出**：

```java
/**
 * {@inheritDoc}
 */
```




## 6.常用操作

## 7.排错与日志

## 8.升级与维护

## 9.附录