---
title: IntelliJ IDEA 教程
copyright: CC-BY-4.0
tags:
  - idea
createTime: 2026/04/15 10:04:15
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

## 5.实时模板

### 5.1.javadoc 类注释模板

**缩写**：`*`

**说明**：javadoc 类注释模板

**适用于**：`java`

**模板文本**：

```java
**
 *
 *<p></p>
 *@author gengchen
 *@since $date$ $time$
 */
```

**编辑变量**

| 变量名  | 表达式      |
|------|----------|
| date | `date()` |
| time | `time()` |

**测试输出**：

```java
/**
 *
 * <p></p>
 * @author gengchen
 * @since 2026/4/15 21:55
 */
```

### 5.2.javadoc 方法注释模板

**缩写**：`**`

**说明**：javadoc方法注释模板

**适用于**：`java`

**模板文本**：

```java
**
 *
 *<p></p>$javadoc$
 *@author gengchen
 *@since $date$ $time$
 */
```

**编辑变量**

```groovy
    //javadoc表达式
    groovyScript(
        "def r='',ps=_1.toString().replaceAll('[\\\\[|\\\\]|\\\\s]','').split(',').toList(),ts=_2.toString().replaceAll('[\\\\[|\\\\]|\\\\s]','').split(',').toList(),rt=_3.toString();def simplify={t->t.replaceAll('[a-z][a-z0-9_]*(\\\\.[a-z][a-z0-9_]*)*\\\\.','')};def hasP=!(ps.size()==0||(ps.size()==1&&(ps[0]==''||ps[0]=='null')));if(hasP){for(i=0;i<ps.size();i++){def t=simplify(ts[i]);r+=(i>0?'\\n * ':'')+('@param '+ps[i]+' {@link '+t+'}');}};def ret=rt==''||rt=='null'||rt=='void'?'':'@return {@link '+simplify(rt)+'}';if(hasP&&ret!='')r+='\\n * '+ret;else if(!hasP)r+=ret;return r==''?null:'\\n * '+r",
        methodParameters(), methodParameterTypes(), methodReturnType()
    )
```
| 变量名     | 表达式    |
|---------|--------|
| javadoc | `上述`       |
| date    | `date()` |
| time    | `time()` |

**测试输出**：

```java
/**
 * 
 * <p></p>
 * @param request {@link SysUserRequest}
 * @param ignoreDisable {@link Boolean}
 * @return {@link SysUser}
 * @author gengchen
 * @since 2026/4/15 18:57
 */
```

### 5.3.javadoc 方法继承注释模板

**缩写**：`***`

**说明**：javadoc 方法继承注释模板

**适用于**：`java`

**模板文本**：

```java
**
 *{@inheritDoc}
 */
```

**编辑变量**

| 变量名  | 表达式      |      |
|------|----------|------|
| date | `date()` |      |
| time | `time()` |      |

**测试输出**：

```java
/**
 * {@inheritDoc}
 */
```

## 6.插件

### 6.1.GitHub Copilot

**插件名**：[GitHub Copilot - Your AI Pair Programmer](https://plugins.jetbrains.com/plugin/17718-github-copilot--your-ai-pair-programmer)

**说明**：[GitHub Copilot](https://github.com/features/copilot) AI 驱动型代码助手

### 6.2.Maven Hepler

**插件名**：[MavenHelper](https://plugins.jetbrains.com/plugin/7179-mavenhelper)

**说明**：解决Maven依赖冲突，可以快速查找项目中的依赖冲突

### 6.3.MyBatisX

**插件名**：[MyBatisX](https://plugins.jetbrains.com/plugin/10119-mybatisx)

**说明**：

### 6.4.Save Actions X

**插件名**：[Save Actions X](https://plugins.jetbrains.com/plugin/22113-save-actions-x)

**说明**：

### 6.5.VSCode Theme

**插件名**：[VSCode Theme](https://plugins.jetbrains.com/plugin/19177-vscode-theme)

**说明**：

### 6.6.PineScript v6 Language Support

**插件名**：[PineScript v6 Language Support](https://plugins.jetbrains.com/plugin/28949-pinescript-v6-language-support)

**说明**：

### 6.7.Chinese (Simplified) Language Pack / 中文语言包

**插件名
**：[Chinese (Simplified) Language Pack / 中文语言包](https://plugins.jetbrains.com/plugin/13710-chinese-simplified-language-pack----)

**说明**：

### 6.8.EasyYapi

**插件名**：[EasyYapi](https://plugins.jetbrains.com/plugin/12458-easyyapi)

**说明**：

### 6.9.CodeGlance Pro

**插件名**：[CodeGlance Pro](https://plugins.jetbrains.com/plugin/18824-codeglance-pro)

**说明**：

### 6.10.Cool Request(REST Client)

**插件名**：[Cool Request(REST Client)](https://plugins.jetbrains.com/plugin/23555-cool-request-rest-client-)

**说明**：

### 6.11.Smart Input Pro (Chinese)

**插件名**：[Smart Input Pro (Chinese)](https://plugins.jetbrains.com/plugin/25280-smart-input-pro-chinese-)

**说明**：

### 6.12.Translation

**插件名**：[Translation](https://plugins.jetbrains.com/plugin/8579-translation)

**说明**：

### 6.13.GitToolBox

**插件名**：[GitToolBox](https://plugins.jetbrains.com/plugin/7499-gittoolbox)

**说明**：在项目文件面板中显示文件的 Git 状态，例如文件的最后一次提交时间、提交人、变更记录等，方便我们快速了解文件的版本历史情

### 6.14.Private Notes

**插件名**：[Private Notes](https://plugins.jetbrains.com/plugin/17874-private-notes)

**说明**：源码中添加注释的插件

## 7.其他设置

### 7.1.Save Actions

| 推荐勾选 | 配置项                            | 说明                                                         |
| -------- | --------------------------------- | ------------------------------------------------------------ |
| ✅        | **Activate save actions on save** | 每次保存文件时自动执行下面勾选的动作                         |
| ☐        | Activate save actions on shortcut | 按快捷键 `CTRL+SHIFT+S` 时触发                               |
| ☐        | Activate save actions on batch    | 通过菜单 `Code > Save Actions > Execute on multiple files` 批量执行 |
| ✅        | **No action if compile errors**   | 文件有编译错误时跳过，不执行任何动作                         |
| ☐        | Process files asynchronously      | 异步处理文件，减少 UI 卡顿，但部分处理器可能异常             |

**Formatting Actions（格式化动作）**

| 推荐勾选 | 配置项                         | 说明                                                         |
| -------- | ------------------------------ | ------------------------------------------------------------ |
| ✅        | **Optimize imports**           | 自动删除未使用的 import，整理 import 顺序                    |
| ☐        | Reformat file                  | 按代码风格规则格式化整个文件                                 |
| ✅        | **Reformat only changed code** | 仅格式化 VCS 变更的代码（需配置版本控制）                    |
| ☐        | Rearrange fields and methods   | 按 `File > Settings > Editor > Code Style > Arrangement` 规则重排字段和方法顺序 |

**Build Actions（构建动作）⚠️ 实验性**

| 状态 | 配置项                           | 说明                                                         |
| ---- | -------------------------------- | ------------------------------------------------------------ |
| ☐    | Compile files                    | 保存时自动编译（等同于 `Build > Build Project`）             |
| ☐    | Reload files in running debugger | 调试中自动热重载变更的类（等同于 `Run > Reload Changed Classes`） |
| ☐    | Execute an action                | 保存时执行自定义快捷动作（在 Quick Lists 中配置）            |

**Java Inspection and Quick Fix（Java 检查与快速修复）**

| 推荐勾选 | 配置项                                                       | 说明                                                |
| -------- | ------------------------------------------------------------ | --------------------------------------------------- |
| ☐        | Add final modifier to field                                  | 字段加 `final` 修饰符                               |
| ☐        | Add final modifier to local variable or parameter            | 局部变量或参数加 `final`                            |
| ☐        | Add final modifier to local variable or parameter except if it is implicit | 同上，但隐式变量除外（如 lambda 参数）              |
| ☐        | Add static modifier to methods                               | 方法加 `static` 修饰符                              |
| ☐        | Add this to field access                                     | 字段访问加 `this.` 前缀                             |
| ☐        | Add this to method access                                    | 方法调用加 `this.` 前缀                             |
| ☐        | Add class qualifier to static member access                  | 静态成员访问加类名限定                              |
| ☐        | Add class qualifier to static member access outside declaring class | 在声明类外部访问静态成员时加类名限定                |
| ✅        | **Add missing @Override annotations**                        | 自动补全缺失的 `@Override` 注解                     |
| ✅        | **Add blocks to if/while/for statements**                    | 给没有大括号的 `if/while/for` 自动加 `{}`           |
| ☐        | Add a serialVersionUID field for Serializable classes        | 实现 `Serializable` 的类自动添加 `serialVersionUID` |
| ☐        | Remove unnecessary this to field and method                  | 删除多余的 `this.`                                  |
| ✅        | **Remove final from private method**                         | 删除 `private` 方法上多余的 `final`                 |
| ☐        | Remove unnecessary final for local variable or parameter     | 删除局部变量/参数上多余的 `final`                   |
| ☐        | Remove explicit generic type for diamond                     | 使用钻石操作符 `<>` 替换显式泛型类型                |
| ✅        | **Remove unnecessary semicolon**                             | 删除多余的分号                                      |
| ☐        | Remove blocks from if/while/for statements                   | 删除 `if/while/for` 中不必要的 `{}`                 |
| ☐        | Change visibility of field or method to lower access         | 将字段/方法的访问权限降低到最小必要级别             |

**File Path（文件路径过滤）**

| 配置项                   | 说明                                                       |
| ------------------------ | ---------------------------------------------------------- |
| **File Path Inclusions** | 指定哪些路径的文件执行 Save Actions，为空表示全部包含      |
| **File Path Exclusions** | 排除指定路径，优先级高于 Inclusions，图中已排除 `.md` 文件 |
