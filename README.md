
# DDOS and DOS attack detection with ML approach
Francesco Cirotto - Università degli studi di Napoli Federico II

 * [Dataset](#dataset)
   + [Downloding](#downloding)
 * [Setup](#setup)

The repository contains notebooks and scripts for developing a ML approach for Network Intrusion Detection.
Given a sample point, the objective of machine learning model will be to classify that whether the intrusion made is Benign or is a BruteForce. In particular DOS and DDOS attacks will be studied.

## Dataset
This [dataset](https://registry.opendata.aws/cse-cic-ids2018/) was originally created by the University of New Brunswick for analyzing DDoS data. More information are [here](https://www.unb.ca/cic/datasets/ids-2018.html). The dataset has been organized per day. For each day, the raw data including the network traffic (Pcaps) and event logs (windows and Ubuntu event Logs) per machine are recorded. A feature extraction process from the raw data allows to visualize data organized in a CSV file, containing more than 80 traffic feature. 

### Downloding
The dataset is stored on AWS, so first you need to download AWS CLI by following [instructions](https://aws.amazon.com/cli/). Then you can download the full dataset by doing
```
aws s3 sync --no-sign-request "s3://cse-cic-ids2018/" <DESTINATION-DIR>
```
Since the whole dataset has a very big size, you can download only CSV file:
``` 
aws s3 sync --no-sign-request "s3://cse-cic-ids2018/Processed Traffic Data for ML Algorithms/" <DESTINATION-DIR>
```

## Setup
You can use conda to install the required packages. **CREATE A YML FILE**
