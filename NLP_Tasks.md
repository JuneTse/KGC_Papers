## NLP任务

### 问答
#### Commonsense question answering
* 利用常识回答问题
* 数据集
  * CosmosQA
  > * Cosmos QA: Machine reading comprehension with contextual commonsense reasoning. [Paper](https://arxiv.org/pdf/1909.00277.pdf)
  > * 阅读一段话，给定一个问题，从候选的答案中选择正确答案（阅读理解选择题）
  
#### Open domain QA 阅读理解
* 阅读文章，根据问题从段落里面抽取答案，预测开始和结束位置
* 数据集
  * QuasarT: 
  > * Quasar: Datasets for question answering by search and reading. [Paper](https://arxiv.org/pdf/1707.03904.pdf)
  * SearchQA: 
  > * SearchQA: A New Q&A Dataset Augmented with Context from a Search Engine. [Paper](https://arxiv.org/pdf/1704.05179.pdf)
  > * 140,461 question-answer pairs.

* NewsQA
* TriviaQA
* HotpotQA
* NaturalQA

### Probing
* 数据集
  * LAMA: 
  > * Language Models as Knowledge Bases? [Paper](https://www.aclweb.org/anthology/D19-1250.pdf)
  > * Facts are either subject-relation-object triples or question-answer pairs.  Each factis converted into a cloze statement which is used to query the language model for a missing token. Weevaluate each model based on how highly it ranksthe  ground  truth  token  against  every  other  wordin  a  fixed  candidate  vocabulary.
  > * 把facts转换成完形填空的形式，给定一些候选的词表，预测缺失的token,
  > * 把多个数据集转换成了cloze templates, 包括：
  >> * Google-RE: 只使用了Google-RE的5种关系中的三种，“place  of  birth”,  “date  of  birth”  and  “place  ofdeath”。因为其他两种包括多个token的答案。手工定义了模板，e.g., “[S]was born in [O]” for “place of birth”.
  >> * T-REx： 考虑了41种关系，每种关系最多1000个facts。和Google-RE一样，为每种关系定义了模板。
  >> * ConceptNet: ConceptNet (Speer and Havasi, 2012) is a multi-lingual  knowledge  base,  initially  built  on  top  ofOpen  Mind  Common  Sense  (OMCS)  sentences. 从OMCS中找到fact对应的句子，mask掉object, 转换成cloze的形式。
  >> * SQuAD： 选择了305个context-questions, 把问题手工定义成了cloze的形式，e.g., rewriting “Who developed the theory ofrelativity?” as “The theory of relativity was devel-oped by__”
  
  * Negated LAMA: Birds cannot fly. [Paper](https://arxiv.org/abs/1911.03343)
  * 

### 关系分类/关系抽取
* 给定一个句子和句子中的两个实体，判断两个实体之间的关系。
* 数据集
  * TACRED
  > * Position-aware Attention and Supervised Data Improve Slot Filling. [Paper](https://www.aclweb.org/anthology/D17-1004.pdf)
  > * 42个关系，106,264个句子
  



### Entity Typing
* 给定context和entity, 预测实体的类型
* 数据集
  * Open Entity:
  > * Ultra-fine entity typing. [Paper](https://arxiv.org/pdf/1807.04905v1.pdf)
    
  
  * FIGER: 
  > * Design Challenges for Entity Linking [Paper](https://transacl.org/ojs/index.php/tacl/article/view/528)


