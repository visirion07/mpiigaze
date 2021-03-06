# A PyTorch implementation of MPIIGaze and MPIIFaceGaze

## Report
Checkout the report Project_Report.pdf

## Requirements

* Linux (Tested on Ubuntu only)
* Python >= 3.7



## Faze Model

Download and save the dataset. 
Now run the MPIIGaze_1_1.ipynb notebook cell by cell with a.py given in the repo. 
Now run the Output.ipynb notebook cell by cell.

## Resnet
Update ~/pytorch_mpiigaze/gaze_estimation/models/mpiigaze/resnet_preact.py by code in resnet_preact_1.py
```bash
git clone https://github.com/visirion07/pytorch_mpiigaze.git
cd pytorch_mpiigaze
pip install -r requirements.txt
python train.py --config configs/mpiigaze/resnet_preact_train.yaml
python evaluate.py --config configs/mpiigaze/resnet_preact_eval.yaml
```

Note that we have to set test index and saved model path in both resnet_train.yaml and resnet_eval.yaml


## Combined Model


Restore the previous ~/pytorch_mpiigaze/gaze_estimation/models/mpiigaze/resnet_preact.py if the above model is run.
```bash
git clone https://github.com/visirion07/pytorch_mpiigaze.git
cd pytorch_mpiigaze
pip install -r requirements.txt
python train2.py --config configs/mpiigaze/resnet_preact_train.yaml
python evaluate.py --config configs/mpiigaze/resnet_preact_eval.yaml
```

Note that we have to set test index and saved model path in both resnet_train.yaml and resnet_eval.yaml





