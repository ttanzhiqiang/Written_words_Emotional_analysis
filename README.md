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
