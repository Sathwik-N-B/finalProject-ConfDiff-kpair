# finalProject-ConfDiff-kpair
ConfDiffABS using mutiple random pairings per sample.

## Requirements:
Python 3.6.13
numpy 1.19.2
Pytorch 1.7.1
torchvision 0.8.2
pandas 1.1.5
scipy 1.5.4

## Arguments:
-mo: model
-ds: data set
-uci: uci dataset or not
-lr: learning rate
-wd: weight decay
-gpu: the gpu index
-ep: training epoch number
-bs: training batch size
-pretrain_bs: batch size for training the probabilistic classifier
-pretrain_ep: epoch number for training the probabilistic classifier
-me: method name
-prior: class prior probability
-n: number of unlabeled data pairs
-run_times: random running times
-k_pairs: number of random pairings per sample

## Demo:
python main.py -mo mlp -ds mnist -uci 0 -lr 1e-3 -wd 1e-5 -gpu 0 -ep 200 -seed 0 -bs 256 -pretrain_bs 256 -pretrain_ep 10 -me ConfDiffABS -prior 0.5 -n 15000 -run_times 5 -k_pairs 10

# Contributions:
BrianLu0101, Sathwik-N-B: Both worked on implementing a method for multiple random pairings which is utilized a k_pairs in the command line argument. Both also worked on the project report.
