# my-chat-bot
一个简单的基于python和sklearn的聊天机器人
此项目仅为演示代码, 可基于此代码进行接口暴露开发

##### 1.来源
公司要求做部分的智能客服, 以解决部分用户的简单咨询问题

##### 2.项目结构
```js
- data
	- dict.txt //词典,用于结巴分词
	- qa.txt  // 问答列表
	- stop_words.txt //停止词
- my-chat-bot.ipynb
```
可以再`qa.txt`中增加语料以提供回答问题的范围和准确度

##### 3.原理
对所有的QA的问题进行分词处理, 通过`tp-idf`算法计算出问题的词频, 然后转换为向量矩阵保存;
当用户咨询时分词->计算词频->余弦相似度;返回最佳匹配的问题。
此方案仅仅适用于小批量问题<10w,超过建议数据库保存


#### 4.系统环境
1. Python 3.7.6
2. jupyter 6.0.3


#### 5.参考
1. [FAQ(常见问题解答)](https://blog.csdn.net/qq_41853758/article/details/82904927)
2. [python-sklearn实现一个简易的智能问答机器人](https://blog.csdn.net/qq_26535271/article/details/100748210)
3. [手把手教你用Python轻轻松松开发一个聊天机器人系统。](https://blog.csdn.net/weixin_42608414/article/details/88198594)