# 字节跳动-ailab-视觉算法面经（2020届）

作者：过若干年后

来源链接：https://www.nowcoder.com/discuss/229358

声明：本文仅用于学习交流，非商业用途，如有侵权请联系删除～



### **一面**

1、上来直接问论文，他基本上没有问啥细节，主要是我在讲

2、一道算法题

稀疏向量的点乘 要求：尽量高效地实现，需要同时考虑时空复杂度。

代码是当时写的，不一定bug free

```
#include <iostream>
using namespace std;
struct Node{
    int index;
    int value;
};
 
int func(Node[] v1, Node[] v2){
    int p1 = 0, p2 = 0;
    int ret = 0;
    int len1 = sizeof(v1) / sizeof(Node);
    int len2 = sizeof(v2) / sizeof(Node)；
    while(p1<len1 && p2<len2){
        int index1 = v1[p1].index, index2 = v2[p2].index;
        if(index1 == index2){
            ret += v1[p1].value * v2[p2].value;
            p1++;
            p2++;
        }else if (index1 < index2){
            p1++;
        }else{
            p2++;
        }
    }
    return ret;
}
 
int main() {
    cout << "Hello World!" << endl;
}
```



### 二面 

1、先问项目的一些细节   

​    2、深度学些基础   

​    smoothL1   

​    fpn的结构   

​    roi pooling和roi align的区别   

​    3、数据结构基础   

​    链表判断是否有环，归并排序描述，二叉排序树时间复杂度   

​    4、算法题   

​    leetcode958  判断是否是完全二叉树。之前刷面经看到了，非常感谢大家分享面经。



### 三面

1、问比赛，主要是我在介绍

2、介绍下cascade rcnn

3、算法题

leetcode3 最长不重复子串



### 交叉面

1、论文讲下，没有提问题

2、RPN介绍一下

3、inception介绍一下

4、depthwise 卷积

5、shufflenet

 