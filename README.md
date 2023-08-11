# Pytorch implementation of HSELDA(Heterogeneous Sub-Graph Learning for lncRNA-Disease Associations Prediction)


# About
HSELDA is a framework that utilizes a relational graph convolutional Neural network based on a link prediction technique via h-hop subgraphs extraction to predict the potential lncRNAs-disease associations. In this method, we first constructed a heterogeneous graph consisting of three types of nodes: lncRNAs, miRNAs, and disease, with their known associations between each node pair as edges. Then, we extracted a list of local subgraphs around each target link, where the subgraphs preserve rich heuristic information related to link existence with the neighbor nodes directly connected to the target links. We employed a relational graph convolutional network to identify the most promising lncRNAs-diseases associations based on local subgraphs.

This is the original implementation of link prediction via SEAL: https://github.com/muhanzhang/SEAL/tree/master

The original dataset is obtained from: 
http://www.sdu-idea.cn/codes.php?name=MFLDA
We have preprocessed the data into XLSX format for our use.

# Usages: 
Run C_V_Data.py in HSE/Python to shuffle and split the data for experimental usage.

Type “python Main.py --train-name IncRNA_DO_Pos_Train_#.txt --test-name 
IncRNA_DO_Testing_#.txt --hop hop_num --use-embedding” to perform training and testing.
Where:
#is the index of training and testing files
hop_num is the number of hop of your choice


# Requirements:
This code is tested with:
Python 3.11.4
Pytorch 2.0.1
Required libraries: Sklearn. Tqdm, Gensim, etc.
