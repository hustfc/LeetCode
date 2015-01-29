递归最容易想到，最左跟最右比，内左跟内右比，然后递归到下一级子树。

代码很舒畅，请见[这里](../../b3462e886fa4da1120c9e29570ed78f3aa9c881e/27.%20Symmetric%20Tree/solution.h#L12-L23)。

如果不用递归，的确稍稍麻烦了点，依旧用栈来做回溯。先闷头比最外面的树枝，比完了，回溯到内部来。思路也是很普通的。

-----

对于树的题目，可以稍稍来个总结：

1. 递归配树最直观，优先选择**递归**。
2. 如果考虑用迭代，那么考虑用**栈**，判断条件几乎永远是：**迭代条件＋栈不为空**。迭代条件要看具体情况，主要分两种：
    1. 根节点向下迭代，判断 root.
    2. 左右子节点分别迭代，判断 left && right.

栈空的时候几乎永远是进行迭代过程（按某种方向性，往深，往右等等），栈不空的时候几乎都是在**回溯**。