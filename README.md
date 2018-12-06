# GAN-AEL
the PyTorch implementation of paper: [Neural Response Generation via GAN with an Approximate Embedding Layer](http://www.aclweb.org/anthology/D/D17/D17-1065.pdf) Please refer to ###dev### branch to run the code.

1.how to run this code?

first:python toy.py -m pretrain -e 10 -tqf ./data/query_train.txt -trf ./data/response_train.txt -vqf ./data/query_valid.txt -vrf ./data/response_valid.txt --exp_dir ./model/

second：python toy.py -m pretrain -e 10 -tqf ./data/query_train.txt -trf ./data/response_train.txt -vqf ./data/query_valid.txt -vrf ./data/response_valid.txt --exp_dir ./model/ -vf vocab.143695

third：python adversarial.py -p  ./model/pretrain/2018-10-30-20-12-39/ -e 9 --filter_num 10 --filter_sizes 1,1

fourth：python inference.py -i ./data/test/query_valid.txt -p ./model/adversarial/2018-10-18-14-38-45/ -e 0 -o ./result.txt
