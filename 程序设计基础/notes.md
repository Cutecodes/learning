# 第二章 变量与代数思维
## 电子秤模拟
### 1.存储功能---变量
### 2.输入---输入流
    #include<stdio.h>
    int main(){
        float apple_price = 3.5;
        float banana_price = 4.2;
        float apple_weight = 0.0;
        float banana_weight = 0.0;
        float total = 0.0;
    
        printf("input the weight of apple\n");
        scanf("%f",&apple_weight);
        printf("input the weight of banana\n");
        scanf("%f",&banana_weight);
    
        total = apple_price * apple_weight + banana_price * banana_weight;
        printf("the total price is %.2f",total);
        return 0;
    }
## 代数思维
用变量来思考问题，用变量之间的运算来表达一定关系，称代数思维。
## 猜数游戏与数据表示
猜数游戏揭示了可用二进制表示数
## 变量类型
类型暗示数据操作法则（规则）
## 变量内存地址---指针
&取变量地址  
*取某地址的内存单元，可认为是一个变量，直接赋值  
指针加减与类型有关，如结构体指针+1，实则加结构体大小
# 第三章 逻辑推理与枚举解题
## 语义表示
将现实事件抽象用计算机表示
## 真假检查
if语句+条件
## （多重）循环枚举（穷举）
循环代码重用  
多重循环解决大空间问题  
多重循环同时跳出：使用标志判断  
二进制，位图表示超大空间，枚举只需++
# 第四章 筛法与查找
## 插花游戏
枚举求素数O(n^2)
## 筛法
多条件问题的通用解法：先选满足条件一的，再从满足条件一的里面选，将一维问题二维化

    for(int d = 2; d * d<=100; d++)
        if(seive[d])//d没被筛掉，d不能被小于d的数整除，是素数
            for(int n = d * d;n<=100;n+=d)//只有大于d^2,且是d的倍数的数未判断
                seive[d]=false;
## 线性查找
枚举
## 折半查找
启发式搜索
## 插入排序/选择排序
实质是查找问题
# 第五章 分治与递归
## 阶乘
1.迭代（枚举）
2.递归（问题解可由子问题解表示求解）
## 归并排序
目标：排序
策略：分治---减小规模，假设有序，合并子数组简单，如何对子数组排序？回到排序问题，递归
## 快速排序
目标：排序（轴点归位）
策略：按轴点分治，找轴点，轴点归位
## 矩阵填充
二维数组+递归
## 分书/八皇后问题
特定可变条件（需要更新条件：回溯）矩阵填充问题，枚举，递归？
## 青蛙过河
简化问题：从个别到一般,从简单到复杂
jump(s,y)=2*jump(s-1,y)
# 第六章 递推与动态规划
## 兔子数列问题
1.按大小兔分别递推  
2.按总数递推---斐波那契数列  
3.不用数组，直接用变量表示前两项
## 分鱼问题
列出相邻两人看到鱼的数量关系及限制条件  
1.A->E:  
2.E->A:
## 橱窗插花问题
1.枚举（二进制表示为三个一）  
2.枚举中存在重复计算，递推优化，计算部分和  
3.动态规划，只需保存部分最优，前几个花瓶插几朵花？二维矩阵
## 动态规划---最优递推
1. 分阶段（把插话任务按一个花瓶一个花瓶分阶段进行）  
+ 状态（每个阶段考虑若干情况）  
+ 决策（每种情况面临不同选择）  
+ 状态转移（决策导致不同阶段状态相互转化）  
2. 每个阶段的最优解是子问题最优解
## 最长公共子序列
动态规划
## 递推与递归
递推：由已知到（多情况）未知，通常会有重复计算，如数列  
递归：从未知到已知
# 第七章 文本数据处理
C++文件读写 ifstream对象
字符串处理
结构体
# 第八章 非文本数据处理
链表  
哈希链表  
先哈希，相同值在同一链表
二进制存取 
# 第九章 可配置的程序设计





