# 大厂高频面试/笔试真题（LeetCode原题改编）

大厂命题常以 LeetCode 原题为基础，通过 **包装业务场景、调整输入输出约束、增加边界条件** 等方式改编，核心算法逻辑与原题高度一致。  
刷题时可先攻克对应 LeetCode 原题掌握核心思路，再结合本README的大厂改编场景强化练习，快速适配笔试面试的实际考察形式，提升解题效率与应试能力。

## 🧭 快速导航
[字节跳动](#字节跳动)  
[阿里巴巴](#阿里巴巴)
## 字节跳动
### 出题偏好
- **整体偏好**：
字节跳动算法面试整体偏好「高频LeetCode Medium-Hard题 + 变体优化」，强调时间/空间复杂度分析（如O(1)空间、O(log N)二分）和业务应用（e.g., 推荐系统的滑动窗口、视频处理的链表操作）。笔试/一面多2-3题（1小时AC），技术面（二/三面）追问边界（如k=1、空输入）和手撕代码。  
  - **高频主题占比**：动态规划（DP）35%、字符串/数组30%、链表/树20%、其他（堆/贪心/图）15%。  
  - **趋势**：AI融合增加（如序列DP变体），但基础不变。  
- **岗位偏好：**
  - 后端/客户端（e.g., 抖音、飞书）：链表/DP（40%），变体多（如k组翻转），业务场景如视频缓存。
  - 推荐/广告算法：图/贪心/堆（30%），加ML融合。
  - 前端/测试：算法少（<20%），偏项目；若考，多字符串/数组。

 ### 改编题目
| 改编描述 | 业务场景 | LeetCode原题 |
|----------|----------|--------------|
| 给定K个有序链表，合并成一个有序链表。面试常问：分治两两合并或外部日志流处理优化。 | 字节视频时间戳同步或日志聚合场景 | [LC23 合并 K 个升序链表](https://leetcode.cn/problems/merge-k-sorted-lists/) |
| 给定0/1网格，统计连通岛屿数量。面试常问：计算最大岛屿面积（LC695）。 | 字节图像分割或用户兴趣聚类场景 | [LC200 岛屿数量](https://leetcode.cn/problems/number-of-islands/) |
| 给定旋转有序数组，搜索目标值。面试常问：带重复元素（LC81）噪声处理。 | 字节推荐ID列表二分查询 | [LC33 搜索旋转排序数组](https://leetcode.cn/problems/search-in-rotated-sorted-array/) |
| 给定二叉树，求最大路径和（任意节点）。面试常问：路径必须通过根节点。 | 字节内容推荐树形权重优化 | [LC124 二叉树中的最大路径和](https://leetcode.cn/problems/binary-tree-maximum-path-sum/) |
| 实现LRU缓存，支持get/put O(1)操作。面试常问：多线程锁或LFU淘汰（LC460）。 | 字节抖音视频元数据缓存设计 | [LC146 LRU 缓存机制](https://leetcode.cn/problems/lru-cache/) |
| 给定迷宫网格，从起点滚球到目标停稳位置。面试常问：动态墙壁生成。 | 字节视频帧路径搜索或游戏导航 | [LC490 迷宫中是否有路径](https://leetcode.cn/problems/the-maze/) |
| 给定表达式字符串，计算+ - * /值（忽略优先级）。面试常问：带括号扩展（LC224），示例“2*3+5/1”。 | 字节配置表达式解析 | [LC227 基本计算器 II](https://leetcode.cn/problems/basic-calculator-ii/) |
| 给定数组和窗口k，求每个窗口最大值。面试常问：窗口中位数（LC480）。 | 字节用户行为实时峰值监控 | [LC239 滑动窗口最大值](https://leetcode.cn/problems/sliding-window-maximum/) |
| 给定角色攻击/防御数组，计数弱角色（被支配）。面试常问：弱点排序扩展。 | 字节游戏推荐系统 | [LC1996 游戏中弱角色的数量](https://leetcode.cn/problems/the-number-of-weak-characters-in-the-game/) |
| 给定股票价格数组，允许多次买卖最大利润。面试常问：手续费或单次（LC121）。 | 字节推荐多次优化模拟 | [LC122 买卖股票的最佳时机 II](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock-ii/) |
| 给定课程和先修关系，返回学习顺序（拓扑排序）。面试常问：任务依赖调度。 | 字节项目流程管理 | [LC210 课程表 II](https://leetcode.cn/problems/course-schedule-ii/) |
| 给定括号字符串，求最长有效子串长度。面试常问：括号匹配计数，使用DP或栈。 | 字节表达式验证 | [LC32 最长有效括号](https://leetcode.cn/problems/longest-valid-parentheses/) |
| 给定候选数组和目标，求所有组合（可复用）。面试常问：无复用（LC40）+背包约束。 | 字节资源组合生成 | [LC39 组合总和](https://leetcode.cn/problems/combination-sum/) |
| 在N*N棋盘放置N皇后，无攻击。面试常问：骑士巡游扩展，剪枝优化。 | 字节棋盘约束问题 | [LC51 N 皇后](https://leetcode.cn/problems/n-queens/) |
| 给定整数数组，求连续子数组最大和。面试常问：固定k长度子数组。 | 字节交易序列优化 | [LC53 最大子数组和](https://leetcode.cn/problems/maximum-subarray/) |
| 给定股票价格数组，求单次买卖最大利润。面试常问：冷却期或手续费。 | 字节交易模拟 | [LC121 买卖股票的最佳时机](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock/) |
| 给定链表，实现O(n log n)排序。面试常问：快速排序变体。 | 字节数据链表排序 | [LC148 排序链表](https://leetcode.cn/problems/sort-list/) |
| 给定基础/高级甜点成本，求最近目标成本组合。面试常问：背包体积可负。 | 字节资源枚举优化 | [LC1671 最近的甜点成本](https://leetcode.cn/problems/closest-dessert-cost/) |
| 给定整数数组，找出和为0的三元组（无重复）。面试常问：4Sum多指针扩展。 | 字节多维特征匹配 | [LC15 三数之和](https://leetcode.cn/problems/3sum/) |
| 给定带括号表达式，计算值。面试常问：优先级运算符添加。 | 字节嵌套配置计算 | [LC224 基本计算器](https://leetcode.cn/problems/basic-calculator/) |
| 给定0/1网格，计算最大岛屿面积。面试常问：动态边界更新。 | 字节连通区域分析 | [LC695 岛屿的最大面积](https://leetcode.cn/problems/max-area-of-island/) |
| 给定矩阵，按螺旋顺序遍历元素。面试常问：逆向生成（LC59）。 | 字节矩阵数据提取 | [LC54 螺旋矩阵](https://leetcode.cn/problems/spiral-matrix/) |
| 给定0/1矩阵，求最大全1正方形边长。面试常问：O(n)空间优化。 | 字节矩阵模式识别 | [LC221 最大正方形](https://leetcode.cn/problems/maximal-square/) |
| 给定数组和窗口k，求每个窗口中位数。面试常问：动态窗口调整。 | 字节数据流中位分析 | [LC480 滑动窗口中位数](https://leetcode.cn/problems/sliding-window-median/) |
| 给定开始词、结束词和字典，求最短变换序列。面试常问：双向BFS加速。 | 字节单词梯度优化 | [LC127 单词接龙](https://leetcode.cn/problems/word-ladder/) |
| 序列化/反序列化二叉树（字符串表示）。面试常问：BFS层序压缩。 | 字节树数据持久化 | [LC297 二叉树的序列化与反序列化](https://leetcode.cn/problems/serialize-and-deserialize-binary-tree/) |
| 给定图节点，深拷贝整个图。面试常问：环形图处理。 | 字节图结构克隆 | [LC133 克隆图](https://leetcode.cn/problems/clone-graph/) |
| 给定高度数组，计算陷水总量。面试常问：动态高度柱子。 | 字节柱状资源模拟 | [LC42 接雨水](https://leetcode.cn/problems/trapping-rain-water/) |
| 给定数组，找出第K大元素。面试常问：实时流处理。 | 字节排名系统 | [LC215 数组中的第K个最大元素](https://leetcode.cn/problems/kth-largest-element-in-an-array/) |
| 设计Twitter系统，支持发帖/关注/feed。面试常问：新闻流多用户排序。 | 字节社交feed设计 | [LC355 设计推特](https://leetcode.cn/problems/design-twitter/) |


## 阿里巴巴
### 出题偏好
- **整体偏好**：
阿里巴巴算法面试/笔试核心围绕「LeetCode 高频题 + 业务场景深度改编」，注重算法的工程落地性（如大数据处理、高并发场景适配）和代码鲁棒性（异常处理、边界用例覆盖）。笔试通常 3-4 题（1.5 小时），包含 1 道 Hard 题；技术面（一/二面）以 Medium 题为主，追问「优化方向」（如海量数据下的空间优化）和「业务迁移」（如将算法适配电商场景）。
  - **高频主题占比**：数组/字符串（32%）、动态规划（DP）（28%）、哈希表/贪心（18%）、树/图（15%）、其他（堆/并查集/二分）（7%）。
  - **趋势**：强绑定业务场景（如电商交易、物流调度），新增「大数据算法」（如分治、外排序变体），基础算法仍是核心但需结合场景思考。
- **岗位偏好：**
  - 后端（e.g., 淘宝、天猫、阿里云）：数组/DP/哈希表（45%），变体多为「多约束条件」（如带权重的背包变体），业务场景如订单排序、库存调度、分布式缓存优化。
  - 算法岗（推荐/广告/搜索）：图/贪心/DP（40%），侧重「大规模数据适配」（如亿级用户的最短路径变体），融合 ML 特征工程（如基于用户行为的序列 DP）。
  - 客户端（e.g., 支付宝、钉钉）：字符串/链表/树（35%），偏「内存优化型变体」（如 O(1) 空间的链表操作），业务场景如本地数据同步、界面渲染优化。
  - 大数据/数仓：分治/外排序/哈希（30%），核心考察「海量数据处理」（如超大数据组的逆序对变体），适配 Hadoop/Spark 场景。
### 改编题目
| 改编描述 | 业务场景 | LeetCode原题 |
|----------|----------|--------------|
| 给定一个字符串，找出其中没有重复字符的最长子串长度。面试常问：如果限制最多K个不同字符，怎么改？ | 阿里文本搜索场景，如查询历史无重复关键词提取 | [LC3 最长无重复字符的子串](https://leetcode.cn/problems/longest-substring-without-repeating-characters/) |
| 给定两个有序数组，找出合并后的中位数。面试常问：数组长度奇偶不同时边界处理。 | 阿里风控，如合并用户行为分数求平均风险值 | [LC4 寻找两个正序数组的中位数](https://leetcode.cn/problems/median-of-two-sorted-arrays/) |
| 给定一个字符串，找出最长的回文子串。面试常问：奇偶长度中心扩展。 | 阿里商品标题模式匹配，如检测对称描述 | [LC5 最长回文子串](https://leetcode.cn/problems/longest-palindromic-substring/) |
| 给定高度数组，求两个柱子间最大水容积（宽度*最小高度）。面试常问：动态调整高度变化。 | 阿里资源分配，如负载均衡模拟 | [LC11 盛最多水的容器](https://leetcode.cn/problems/container-with-most-water/) |
| 给定整数数组，找出和为0的三元组（无重复）。面试常问：扩展到4Sum多维去重。 | 阿里订单特征匹配 | [LC15 三数之和](https://leetcode.cn/problems/3sum/) |
| 给定数字字符串，生成所有可能的字母组合（2-9映射）。面试常问：添加字典过滤有效词。 | 阿里序列生成，如验证码组合 | [LC17 电话号码的字母组合](https://leetcode.cn/problems/letter-combinations-of-a-phone-number/) |
| 给定括号字符串，判断是否有效匹配。面试常问：多类型括号嵌套。 | 阿里配置验证，如JSON表达式解析 | [LC20 有效的括号](https://leetcode.cn/problems/valid-parentheses/) |
| 给定两个有序链表，合并成一个有序链表。面试常问：扩展到K个链表（LC23）。 | 阿里日志和订单流融合 | [LC21 合并两个有序链表](https://leetcode.cn/problems/merge-two-sorted-lists/) |
| 给定整数数组，求连续子数组的最大和。面试常问：固定k长度子数组。 | 阿里交易额连续优化 | [LC53 最大子数组和](https://leetcode.cn/problems/maximum-subarray/) |
| 给定股票价格数组，求单次买卖最大利润。面试常问：添加冷却期或手续费。 | 阿里交易风控模拟 | [LC121 买卖股票的最佳时机](https://leetcode.cn/problems/best-time-to-buy-and-sell-stock/) |
| 给定字符串和单词字典，判断是否能拆分成字典词。面试常问：返回所有拆分方式（LC140）。 | 阿里商品描述分词 | [LC139 单词拆分](https://leetcode.cn/problems/word-break/) |
| 给定0/1网格，统计连通岛屿数量。面试常问：计算最大岛屿面积（LC695）。 | 阿里用户聚类或图片分割 | [LC200 岛屿数量](https://leetcode.cn/problems/number-of-islands/) |
| 给定单链表，反转整个链表。面试常问：k组分段翻转（LC25）。 | 阿里日志链表处理 | [LC206 反转链表](https://leetcode.cn/problems/reverse-linked-list/) |
| 给定课程和先修关系，判断是否能完成（无环）。面试常问：返回顺序（LC210）。 | 阿里项目依赖管理 | [LC207 课程表](https://leetcode.cn/problems/course-schedule/) |
| 给定数组，找出第K大元素。面试常问：实时流处理。 | 阿里热搜实时排名 | [LC215 数组中的第K个最大元素](https://leetcode.cn/problems/kth-largest-element-in-an-array/) |
| 给定二叉树和两个节点，找最近公共祖先。面试常问：多节点LCA预处理。 | 阿里组织架构查询 | [LC236 二叉树的最近公共祖先](https://leetcode.cn/problems/lowest-common-ancestor-of-a-binary-tree/) |
| 给定数组，计算每个元素除自身外的乘积（无除法）。面试常问：O(1)空间优化。 | 阿里用户行为权重统计 | [LC238 除自身以外数组的乘积](https://leetcode.cn/problems/product-of-array-except-self/) |
| 给定数组和窗口大小k，求每个窗口的最大值。面试常问：窗口中位数（LC480）。 | 阿里订单价格滑动分析 | [LC239 滑动窗口最大值](https://leetcode.cn/problems/sliding-window-maximum/) |
| 给定面额数组和总金额，求最少硬币数。面试常问：完全背包变体。 | 阿里资源分配模拟 | [LC322 零钱兑换](https://leetcode.cn/problems/coin-change/) |
| 给定正整数数组，判断是否能分割成两个等和子集。面试常问：0/1背包扩展。 | 阿里流量均衡分流 | [LC416 分割等和子集](https://leetcode.cn/problems/partition-equal-subset-sum/) |
| 给定二叉树，计算最长路径（直径）。面试常问：平衡树检查。 | 阿里决策树结构分析 | [LC543 二叉树的直径](https://leetcode.cn/problems/diameter-of-binary-tree/) |
| 给定两棵二叉树，按节点值合并（非空相加）。面试常问：处理空节点。 | 阿里用户画像数据融合 | [LC617 合并两棵二叉树](https://leetcode.cn/problems/merge-two-binary-trees/) |
| 给定字符串，计数所有回文子串数量。面试常问：奇偶中心扩展。 | 阿里评论情感文本分析 | [LC647 回文子串](https://leetcode.cn/problems/palindromic-substrings/) |
| 给定有序数组和目标值，实现二分查找。面试常问：旋转数组偏移（LC33）。 | 阿里商品ID有序查询 | [LC704 二分查找](https://leetcode.cn/problems/binary-search/) |
| 给定单链表，找中间节点。面试常问：奇偶长度处理。 | 阿里分页链表操作 | [LC876 链表的中间结点](https://leetcode.cn/problems/middle-of-the-linked-list/) |
| 给定天数数组和票价，求最低旅行成本。面试常问：日程约束优化。 | 阿里员工出差路径规划 | [LC983 最低票价](https://leetcode.cn/problems/minimum-cost-for-tickets/) |
| 给定成本数组，贪心分配两城市最小总成本。面试常问：多城市扩展。 | 阿里多地调度资源分配 | [LC1029 两城市之间最优路径](https://leetcode.cn/problems/two-city-scheduling/) |
| 给定两个字符串，求最长公共子序列长度。面试常问：编辑距离相似度。 | 阿里商品描述序列匹配 | [LC1143 最长公共子序列](https://leetcode.cn/problems/longest-common-subsequence/) |
| 实现LRU缓存，支持get/put O(1)操作。面试常问：LFU频率变体（LC460）。 | 阿里淘宝热搜缓存设计 | [LC146 LRU缓存机制](https://leetcode.cn/problems/lru-cache/) |
| 给定整数数组，求连续子数组的最大乘积。面试常问：负数边界处理。 | 阿里连续收益乘积优化 | [LC152 乘积最大子数组](https://leetcode.cn/problems/maximum-product-subarray/) |
