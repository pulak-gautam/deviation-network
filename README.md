# DevNet: An End-to-end Anomaly Score Learning Network
By Guansong Pang, Chunhua Shen, Anton van den Hengel. Deep anomaly detection with deviation networks (KDD19).

## Brief Introduction
Deviation network (DevNet) is introduced in our KDD19 paper, which leverages a limited number of labeled anomaly data and a large set of unlabeled data to perform end-to-end anomaly score learning. It addresses a weakly supervised anomaly detection problem in that the anomalies are partially observed only and we have no labeled normal data.

Unlike other deep anomaly detection methods that focus on using data reconstruction as the driving force to learn new representations, DevNet is devised to learn the anomaly scores directly. Therefore, DevNet directly optimize the anomaly scores, whereas most of current deep anomaly detection methods optimize the feature representations. The resulting DevNet model achieves significantly better anomaly scoring than the competing deep methods. Also, due to the end-to-end anomaly scoring, DevNet can also exploit the labeled anomaly data much more effectively. 

## Usage
A simple example of runing DevNet is shown as follows.
```python
python devnet_kdd19.py --network_depth=2 --runs=10 --known_outliers=30 --cont_rate=0.02 --data_format=0 --output=./results.csv --dataset=`annthyroid_21feat_normalised`
````
See devnet_kdd19.py for more details about each argument used in this line of code.

The relevant packages and their versions used in our algorithm implementation are listed as follows
* python==3.6.6
* keras==2.2.4
* keras-applications==1.0.6
* keras-preprocessing==1.0.5
* tensorflow-gpu==1.10.0
* scikit-learn==0.20.0
* numpy==1.14.5
* pandas==0.23.4
* scipy==1.1.0
* tensorboard==1.10.0

See the full paper below for the implemenation details of DevNet.

## Full Paper
The full paper can be found at [ACM Portal](https://dl.acm.org/citation.cfm?id=3330871) or [arXiv](https://arxiv.org/abs/1911.08623)

## Datasets
The datasets used in DevNet are also released here. See our anomaly detection dataset repository [ADRepository](https://github.com/GuansongPang/anomaly-detection-datasets) for more preprocessed datasets that are widely-used in other papers.

## Citation
>Guansong Pang, Chunhua Shen, and Anton van den Hengel. "Deep anomaly detection with deviation networks." In Proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, pp. 353-362. 2019.


