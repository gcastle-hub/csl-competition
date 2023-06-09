---
title: Evaluation
---

We evaluate the submitted causal graphs using the metric that we call g-score, which is defined based on real-world requirements and is used internally at Huawei. We want to identify more true causal relations and less false causal relations while being relatively tolerant of being unable to find some of the true causal relations (false negatives). This is a rational setting as the data limit cannot guarantee all causal relations to be founded from data, especially in just partially observed real-world scenarios. The definition of the g-score for an estimated causal graph is as follows:

![](../assets/img/gscore.png)

+ TP (True Positive): A directed edge estimated with correct direction.
+ FP (False Positive): A directed edge that is in estimated graph but not in the true graph.
+ FN (False Negative): A directed edge that is not in estimated graph but in the true graph.

Based on the above definition, the corresponding ranking score of a submission will be evaluated as follows:

![](../assets/img/rank_score.png)

where K is the number of datasets. The maximum rank-score is 1.