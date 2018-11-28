# 第1讲

&gt; 数据结构学习笔记  
\#\# 第1讲  
\#\#\# 0. 学习目标：  
- 学习排序算法 - 插入排序 - 选择排序 - 归并排序  
- 分析排序算法的效率  
\#\#\# 1. 排序问题：  
输入：A list of n numbers  
输出：Arrange the numbers in increasing order  
\#\#\#\# 1\). 插入排序- The key steps are summarized as follows: - Swap towards left side ; - Stop until seeing an item with a smaller value.  
\#\#\#\# 2\). 选择排序  
- The key steps are summarized as follows: - Find minimum item after \(k-1\)th position - Let’s call this minimum item X - Insert X at kth position in the list  
\#\#\#\# 3\). 归并排序  
&gt; 分而治之思想 --&gt; 归并排序  
- The key steps are summarized as follows: - Step 1. Divide list to two halves, A and B - Step 2. Sort A using Merge Sort - Step 3. Sort B using Merge Sort - Step 4. Merge sorted lists of A and B  
  
\#\#\# 2. 分析运行时间  
\#\#\#\# 1\).插入排序  
- 最好的情况:  
 $T\(n\) = c\_1\(n-1\) + c\_2\(n-1\) = Kn + c$ --&gt; linear function of n  
- 最坏的情况:  
 $T\(n\) = K\_1n^2 + K\_2n + K\_3$ --&gt; quadratic function of n  
\#\#\#\# 2\). 选择排序  
\#\#\#\# 3\). 归并排序  
Pseudo-code for Merge Sort:\`\`\`c\# Merge Sort\(A, p, r\)if p &lt; r then q &lt;- {\(p + r\)/2} merge sort\(A, p, q\) merge sort\(A, q+1, q\) merge\(A, p, q, r\)\`\`\`  
- 最坏的情况: $T\(n\) = K\_{1}nlog\_n + K\_{2}n + K\_3$  
\*\*哪种算法最好?\*\*  
- Unfortunately, we still cannot tell – since constants in running times are unknown  
- But we do know that if n is VERY large, - worst-case time of Merge Sort must be smaller than that of Insertion Sort  
- Merge Sort is asymptotically faster than Insertion Sort  
  


