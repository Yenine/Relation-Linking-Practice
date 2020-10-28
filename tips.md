
# 论文阅读心得
### 1. IWCS'19-Aligning Open IE Relatetwork Based on Word Embedding

##### 1.特征：
两个三元组的词向量（分别来自于Open IE与Wikidata KB）,三种输入模式：<br>
(1)关系短语<br>
(2)关系定义：附加关系定义<br>
(3)实体信息：附加实体信息<br>
![输入图解](https://github.com/Yenine/Relation-Linking-Practice/blob/main/images/RL2.png)
##### 2.模型流程
使用孪生神经网络，分别使用两个相同的子网络（CNN或PCNN）获得两个输入的输出，计算对比损失并利用其训练模型；最后使用训练好的模型进行判断。<br>
远程监督：同样的实体对之间的关系含义相近；如果其中一个实体不同，则为含义不同。使用交换规则获取更多正面样例。
##### 3.数据集：
Stanford Open IE <br>
Wikidata  Knowledge Base (KB)

### 2. ISWC'19-Entity Enabled Relation Linking

##### 1.特征：
自然语言描述的问题
##### 2.模型流程：
(1)关系关键词挖掘：使用TexRazor API<br>
(2)基于关键词的关系扩展：使用来自PATTY的背景知识获取相关关系列表<br>
(3)基于实体的关系扩展：对于出现的实体,利用RDF获取其显性和隐性关系，进行关系扩充<br>
(4)候选关系排序:使用SIBKB排序，进而使用三种策略重排序<br>
##### 3.数据集与工具：
QALD <br>
LC-QuAD <br> 
PATTY <br>
SIBKB <br>
ReMatch <br>
EARL <br>


### 3. Matching Natural Language Relations to Knowledge Graph
