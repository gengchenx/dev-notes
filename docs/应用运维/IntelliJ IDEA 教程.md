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

### 5.2.插件

#### 5.2.1.GitHub Copilot

**插件名**：[GitHub Copilot - Your AI Pair Programmer](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer)

**说明**：[GitHub Copilot](https://github.com/features/copilot) AI 驱动型代码助手

#### 5.2.2.Maven Hepler

**插件名**：[MavenHelper](https://plugins.jetbrains.com/plugin/7179-mavenhelper)

**说明**：解决Maven依赖冲突，可以快速查找项目中的依赖冲突

#### 5.2.3.MyBatisX

**插件名**：[MyBatisX](https://plugins.jetbrains.com/plugin/10119-mybatisx)

**说明**：

#### 5.2.4.Save Actions X

**插件名**：[Save Actions X](https://plugins.jetbrains.com/plugin/22113-save-actions-x)

**说明**：

#### 5.2.5.VSCode Theme

**插件名**：[VSCode Theme](https://plugins.jetbrains.com/plugin/19177-vscode-theme)

**说明**：

#### 5.2.6.PineScript v6 Language Support

**插件名**：[PineScript v6 Language Support](https://plugins.jetbrains.com/plugin/28949-pinescript-v6-language-support)

**说明**：

#### 5.2.7.Chinese (Simplified) Language Pack / 中文语言包

**插件名**：[Chinese (Simplified) Language Pack / 中文语言包](https://plugins.jetbrains.com/plugin/13710-chinese-simplified-language-pack----)

**说明**：

#### 5.2.8.EasyYapi

**插件名**：[EasyYapi](https://plugins.jetbrains.com/plugin/12458-easyyapi)

**说明**：

#### 5.2.9.CodeGlance Pro

**插件名**：[CodeGlance Pro](https://plugins.jetbrains.com/plugin/18824-codeglance-pro)

**说明**：

#### 5.2.10.Cool Request(REST Client)

**插件名**：[Cool Request(REST Client)](https://plugins.jetbrains.com/plugin/23555-cool-request-rest-client-)

**说明**：

#### 5.2.11.Smart Input Pro (Chinese)

**插件名**：[Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280-smart-input-pro-chinese-)

**说明**：

#### 5.2.12.Translation

**插件名**：[Translation](https://plugins.jetbrains.com/plugin/8579-translation)

**说明**：

#### 5.2.13.GitToolBox

**插件名**：[GitToolBox](https://plugins.jetbrains.com/plugin/7499-gittoolbox)

**说明**：在项目文件面板中显示文件的 Git 状态，例如文件的最后一次提交时间、提交人、变更记录等，方便我们快速了解文件的版本历史情

#### 5.2.14.Private Notes

**插件名**：[Private Notes](https://plugins.jetbrains.com/plugin/17874-private-notes)

**说明**：源码中添加注释的插件




## 6.常用操作

## 7.排错与日志

## 8.升级与维护

## 9.附录