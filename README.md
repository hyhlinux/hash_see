# hash_see
 
## hash 的可视化
 
 
#### 背景
 1. 在文件下载服务器中由于使用了一致性hash来保证缓存的高命中.
 2. 线上应用中，流量分布一直不够均匀，由如d01/d02/d03/d04/d05 五台机器，d01 达到来35%之高，带宽压力明显.
 3. 原定方案:
    1. 新的hash 函数，实现均衡 
    2. 调整replicate， 找到一个分布均衡的值.  groupcahe 默认选取了50. 我们在线上选择了100

#### 在对hash.crc32 值域可视化的过程中，发现了replicate 对分布由决定性的影响
    todo 给出 hash.crc32 在10-300之间取值的可视化分布图。

#### 目标
 1.使用饼图，查看一致性hash的分布百分比，在一致性缓存中快速优化和分析。
 2.针对一致性hash，副本数自己选取，做的尽可能的平均。
 
 
