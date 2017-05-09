### Merge Request

Merge Request (以下简称 mr), 合并请求,  一般用于将自己所 fork 的分支代码合并回主干(原分支).

Gitlab 的 mr 提交时可以填写 mr 的*标题*和*描述*, 指定处理人, 标注相关标签和里程碑.
提交 mr 时可选择在代码被合并后自动删除分支, 在功能分支完成时, 可以勾选这个选项.

**Title 标题** 说明此次mr的主要变更, 标题在mr被接收时会作为默认的 commit message, 因此需要写有意义的信息, 以免在以后看 git log 时不知到此次mr做了什么.

**Description 描述** 对此次mr进行详细的说明, 可以使用 markdown 语法, 和 gitlab 支持的 markdown 扩展语法.
描述信息在 gitlab 中可见, 可详细记录此次mr的说明.

#### 引用
在 gitlab 的 markdown 格式中可以使用符号来引用 issue, commit, 成员.
使用引用可以提醒相关小伙伴查看mr, 说明此次mr是解决哪个问题, 修正哪行代码, 属于哪个标签, 对应哪个里程碑.

```
@username 用户
@groupname 组
@all 整个team

#issue
!merge_request
~label
%milestone

9ba12248   指定 commit hash
9ba12248...b19a04f5 指定 commit 比较范围
[NAME](path-to-file) 引用文件
[NAME](path-to-file#L20) 引用文件的指定行
```

可以在引用前指明项目名称来引用其他项目

```
project#issue
namespace/project#issue
```

语法高亮

```
[+foo+] 增
[-bar-] 删
```

任务列表

```
- [x] Completed task
- [ ] Incomplete task
    - [ ] Sub-task 1
    - [x] Sub-task 2
    - [ ] Sub-task 3

```
- [x] Completed task
- [ ] Incomplete task
    - [ ] Sub-task 1
    - [x] Sub-task 2
    - [ ] Sub-task 3


```
1. [x] Completed task
1. [ ] Incomplete task
    1. [ ] Sub-task 1
    1. [x] Sub-task 2

```
1. [x] Completed task
1. [ ] Incomplete task
    1. [ ] Sub-task 1
    1. [x] Sub-task 2

----
