
1、Requirements

The main requirements are:
python = 3.6
torch  = 1.1.0
torchvision = 0.3.0
transformers = 3.5.1 (Pytorch version of BERT-cased: 110M parameters）

2、Usage

(1)Train

    Partial Match:
    python train.py --data_dir=dataset/WebNLG-P/data  --id=WebNLG-P --classemb_num=214 --entityclass_num=2 --relationclass_num=171

    Exact Match:
    python othertrain.py --data_dir=dataset/WebNLG-E/data  --id=WebNLG-E --classemb_num=255 --entityclass_num=2 --relationclass_num=211

(2)Evaluate on the test set

    Partial Match:
    python othereval.py --model_dir=./saved_models/WebNLG-P --data_dir=dataset/WebNLG-P/data

    Exact Match:
    python eval.py --model_dir=./saved_models/WebNLG-E --data_dir=dataset/WebNLG-E/data

(All experiments are conducted with an NVDIA GeForce RTX 2080 Ti.)