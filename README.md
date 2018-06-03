# Bag-of-Words-Meets-Bags-of-Popcorn

成绩：
	1000维特征：
		word2vec+LR:0.88364
		doc2vec_dm+doc2vec_bow+LR:0.90336
		word2vec+doc2vec_dm+doc2vec_bow+LR:0.91392 //线性模型后，用LR再次线性融合
		word2vec+doc2vec_dm+doc2vec_bow+tf-idf+LR:0.89616 //直接把所有特征拼接起来，然后LR
	400维特征：
		word2vec+doc2vec_dm+doc2vec_bow+tf-idf+两层神经网络:0.90948

update:
	word2vec+doc2vec_dm+doc2vec_bow+LR：输出概率
	
获得最好成绩的运行步骤：
	1、python feature_w2v.py
	2、python feature_d2v.py
	3、python blending.py

其他的文件是一些单模型和其他的模型融合方法，效果并没有当前这个更优秀

百度云盘
数据data
https://pan.baidu.com/s/1EEzVCcphMWYDiKR7Uak30A

英文情感分析
查看submission.csv文件和data中的testData.tsv两个文件；评分越高，表示文字感情越高兴；评分越低，表示文字感情越悲伤。

例如：
"12311_10"	"Naturally in a film who's main themes are of mortality, nostalgia, and loss of innocence it is perhaps not surprising that it is rated more highly by older viewers than younger ones. However there is a craftsmanship and completeness to the film which anyone can enjoy. The pace is steady and constant, the characters full and engaging, the relationships and interactions natural showing that you do not need floods of tears to show emotion, screams to show fear, shouting to show dispute or violence to show anger. Naturally Joyce's short story lends the film a ready made structure as perfect as a polished diamond, but the small changes Huston makes such as the inclusion of the poem fit in neatly. It is truly a masterpiece of tact, subtlety and overwhelming beauty."

评分为0.976023938，表示为高兴



而
"8348_2"	"This movie is a disaster within a disaster film. It is full of great action scenes, which are only meaningful if you throw away all sense of reality. Let's see, word to the wise, lava burns you; steam burns you. You can't stand next to lava. Diverting a minor lava flow is difficult, let alone a significant one. Scares me to think that some might actually believe what they saw in this movie.<br />
<br />Even worse is the significant amount of talent that went into making this film. I mean the acting is actually very good. The effects are above average. Hard to believe somebody read the scripts for this and allowed all this talent to be wasted. I guess my suggestion would be that if this movie is about to start on TV ... look away! It is like a train wreck: it is so awful that once you know what is coming, you just have to watch. Look away and spend your time on more meaningful content."
评分为0.037325369，表示为悲伤



