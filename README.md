# NVAITC SAMP JP RAPIDS Workshop
このリポジトリには、NVIDIA AI Technogloy Center(NVAITC)JapanのStudent Ambassador ProgramのRAPIDSワークショップのリソースが含まれています。

## 本ワークショップで取り扱うRAPIDSのツール
<img width="752" alt="image" src="https://github.com/nvidiasamp/RAPIDS-Workshop/blob/ba518233ba058250510d3b8a82d7f48335b3343f/image/rapids_fig_202402.png">

本ワークショップで扱うテーマは上記の赤枠の部分になります。

## Workshop Agenda
アジェンダ（開催日時：2024/2/27）
- [ ] 1. オープニング
- [ ] 2. XGBoostとは～ネコでもわかる解説～
- [ ] 3. ハンズオンの概要説明
- [ ] 4. ハンズオン実施
- [ ] 5. （事例紹介）cuMLの実装例について
- [ ] 6. クロージング

## インストールとセットアップのガイド
### ソフトウェアの要件 
プログラミング言語：Python \
フレームワークおよびライブラリ: 
  -  Python: 3.8
  -  LINUX_VERSION: ubuntu18.04
  -  CUDA_VERSION: 11.0
  -  RAPIDS: 22.08
  -  ベースイメージ: [rapidsai/rapidsai](https://catalog.ngc.nvidia.com/orgs/nvidia/teams/rapidsai/containers/rapidsai)
  -  依存性
  ```environment_for_docker.yml
    - cuxfilter=22.08.00
    - dash=2.5.1
    - dash-html-components=2.0.0
    - dash-core-components=2.0.0
    - dash-daq=0.5.0
    - dash-bootstrap-components=1.2.0
  ```
そのほかの情報については，Dockerfile，environtemnt_for_docker.ymlを参照してください。

### ハードウェアの要件
- CUDA: 11.0
- NVIDIA driver: 450.236.01

### セットアップガイド
#### Docker
```
docker build -t rapids_workshop .
docker run --gpus all rapids_workshop
```
docker imageのリンクは[こちら](https://hub.docker.com/layers/izumi08/nvidia-samp-workshop202402/complete_ver/images/sha256-438a427d10be08fa3080c853e9e0e351d5cf21d9248311a87c47f480d4bd6879?context=repo)

## データのダウンロード
下記のリンクからダウンロードしてください。
- ハンズオン:[House Rent Prediction Dataset](https://www.kaggle.com/datasets/iamsouravbanerjee/house-rent-prediction-dataset)
- 事例紹介:HR Analytics: Job Change of Data Scientists
  - [train data](https://www.kaggle.com/datasets/arashnic/hr-analytics-job-change-of-data-scientists)  
  - [test answer](https://www.kaggle.com/arashnic/job-change-dataset-answer)  



## Collaborators
- 上野孝⽃(Shiga Universtiy)
- 嘉悦里奈子(Shiga Universtiy)
- 小倉和己(Shiga University)
- 徳永⼀輝(Shiga University)
- Vincent Gong(NVIDIA)

## License
- Apache 2.0 (same as RAPIDS)
