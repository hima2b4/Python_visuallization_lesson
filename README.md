# Python_visuallization_lesson

**書籍『Pythonでゼロからはじめる視覚化　～Google Colabですぐに簡単に～』** で使用するNotebookと関連資料をアップしています。

![image](https://user-images.githubusercontent.com/90017759/222333279-2f9115a4-cbf7-4e79-8c5c-46f40662397b.png)

[**株式会社C&R研究所 書籍紹介ページ**](https://www.c-r.com/book/detail/1486)

***
# FAQ
- **PairPlot の実行エラーを回避する方法：20230307追加** 

　scikit-learn の Ver.up により、実行時にエラーが出ることがわかりました。scikit-learn をVer.指定してインストールすれば、エラーは回避できます。

- 以下のコードをNotebookのセルに追加して実行してください。（コード追加の位置やエラー内容は以下を参照下さい）
- ※ scikit-learnを追加インストールするタイミングにより、挙動が異なるようです。Notebookメニューの[ランタイム] → セッションの管理 → アクティブなセッションをすべて終了（ゴミ箱マーククリック）→ 「1. インストール」のセルに「!pip install scikit-learn==1.1.3」を追加 → 最初のセルから順に起動 してください。
```Python:scikit-learn ver指定してインストール
!pip install scikit-learn==1.1.3
```
<details><summary>コード追加の位置（画像キャプチャ） </summary><div>

![combine_images (1).jpg](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/b17cc22b-1455-2af1-cfc7-304445bfc01b.jpeg)
以下のように [RESTART RUNTIME]ボタン が出てきた時は、ボタンを押して、データの読込みも再度実行してください。
![image](https://user-images.githubusercontent.com/90017759/224654655-cf5be7f6-9f57-4932-8131-802dfc71d075.png)

</div></details>

<details><summary>エラー内容</summary><div>
    ImportError Traceback (most recent call last)
    in
    2
    3
    ----> 4 from seaborn_analyzer import CustomPairPlot
    5
    6 cp = CustomPairPlot()

    1 frames
    /usr/local/lib/python3.8/dist-packages/seaborn_analyzer/custom_class_plot.py in
    5 import pandas as pd
    6 from scipy import stats
    ----> 7 from sklearn.metrics import auc, plot_roc_curve, roc_curve, RocCurveDisplay
    8 from sklearn.model_selection import KFold, LeaveOneOut, GroupKFold, LeaveOneGroupOut
    9 from sklearn.preprocessing import label_binarize

    ImportError: cannot import name 'plot_roc_curve' from 'sklearn.metrics' (/usr/local/lib/python3.8/dist-packages/sklearn/metrics/init.py)
</div></details>


***
## ■CHAPTER 01　Pythonによる視覚化
　下の▶ をクリックすると、CHAPTER 01 掲載の ローズダイヤグラム（COLUMN DIAGRAM OF THE CAUSES OF MORTALITY）が確認できます。 

<details><summary>ローズダイヤグラム（Wikipediaより）</summary><div>

![FD939656-8392-4B37-964A-0028BF6921CE.jpeg](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/fe0fce78-cc2d-b3fc-db26-17e524a9da22.jpeg)
https://commons.wikimedia.org/wiki/File:Nightingale-mortality.jpg
</div></details>
 
***
## ■CHAPTER 02　ノーコードではじめるグラフ描画
　CHAPTER 02 で、**最初に使用する Notebook** は、次の通りです。 

| Notebook（クリックで起動）　　　　 | 使用データセット | データ内容 | 
| :--- | :--- | :--- |
|  [**Pythonで視覚化①.ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%E2%91%A0%20.ipynb) | Occupancy_detection :binary | 部屋の温湿度やCO2と人の存在の時系列データ |

    下の▶ をクリックすると、上記データセットで描いたpairplot が確認できます。 

<details><summary> Occupancy_detection データセットで描いたpairplot</summary><div>

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/b0026705-8f23-90dd-23a8-649b83ab8a25.png)

</div></details>

***
　CHAPTER 02 で、**2番目に使用する Notebook** は、次の通りです。 

| Notebook（クリックで起動）　  　　　　　　　| 使用データセット　　　 | データ内容 | 
| :--- | :--- | :--- |
| [**Pythonで視覚化②.ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%E2%91%A1%20.ipynb)| wine :classification | イタリアの同じ地域で栽培された3種類の異なるワインの化学分析の結果に関するデータ |

    下の▶ をクリックすると、上記データセットで描いたpairplot が確認できます。 

<details><summary> wine データセットで描いたpairplot</summary><div>

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/1e29a489-3273-0c4b-524e-33cdfede894e.png)

</div></details>

***
　CHAPTER 02 で、**3番目に使用する Notebook** は、次の通りです。 
| Notebook（クリックで起動）　　 | 使用データセット | データ内容 | 
| :--- | :--- | :--- |
| [**Pythonで視覚化③.ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%E2%91%A2.ipynb) | Titanic(seaborn) :binary | タイタニック号の乗客の生死に関する二値分類データ |

    下の▶ をクリックすると、上記データセットで描いたpairplot が確認できます。

<details><summary> Titanicデータセットで描いたpairplot</summary><div>

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/e12b5b81-2cfe-ca41-7ff9-6d177b9e6b7b.png)

</div></details>

***
## ■CHAPTER 03　Pythonでグラフを描くプログラム

    下の▶ をクリックすると、COLUMN掲載の Pythonで描いたローズダイヤグラムが確認できます。

<details><summary>Pythonで描いた COLUMN DIAGRAM OF THE CAUSES OF MORTALITY</summary><div>

**APRIL1854~MARCH1855**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/04519ac1-9855-473a-a2ae-a10cc2fc132d.png)
**APRIL1855~MARCH1856**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/4c5c79f6-9425-6c74-5650-754333a3c751.png)


</div></details>

***
## ■CHAPTER 04　実務で活かすためのテクニック

　CHAPTER 04 で、最初に使用する Notebook は、次の通りです。 
| Notebook（クリックで起動）　　　　　　　　 | 使用データセット | データ内容 | 
| :--- | :--- | :--- |
| [**Pythonで視覚化[Multi編].ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%5BMulti%E7%B7%A8%5D.ipynb) | Boston_housing: regression | 1970年代後半におけるアメリカのボストンにおけるある区画の住宅価格に関するデータ |

    下の▶ をクリックすると、CHAPTER 04掲載の 変数とグラフとライブラリの組み合わせ表 が確認できます。
<details><summary>変数とグラフとライブラリの組み合わせ表</summary><div>

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/eb81a2c2-6d98-d7e4-fb42-6f8d1c15c190.png)

</div></details>

    下の▶ をクリックすると、上記データセットで描いたpairplot が確認できます。
<details><summary> Boston_housing データセットで描いたpairplot　</summary><div>

![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/55d371c7-6856-3d9f-33dd-73d36a96771d.png)

</div></details>

***
　CHAPTER 04 で、2番目に使用する Notebook は、次の通りです。 
| Notebook（クリックで起動）　　　　　　　　　　　 |使用データセット| データ内容 | 
| :--- | :--- | :--- |
| [**Pythonで視覚化[Dataprep編].ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%5BDataprep%E7%B7%A8%5D.ipynb) | Loan_prediction :binary | 住宅ローンを取り扱う会社が管理する「ローン申請者の情報」と「ローン承認の是非」に関するデータ |

***
## ■CHAPTER 05　データクリーニングのテクニック
　CHAPTER 05 で使用する Notebook は、次の通りです。 
| Notebook（クリックで起動）　　　　　　　　 |使用データセット| データ内容 | 
| :--- | :--- | :--- |
| [**Pythonで視覚化[Preparation編].ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Python%E3%81%A7%E8%A6%96%E8%A6%9A%E5%8C%96%5BPreparation%E7%B7%A8%5D.ipynb) | Titanic(seaborn) :binary | タイタニック号の乗客生死に関する二値データ |

    下の▶ をクリックすると、CHAPTER 05 掲載の 決定木画像 が確認できます。

<details><summary>CHAPTER 05 掲載の決定木画像</summary><div>

**Titanicデータ（木の深さ：3）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/36479428-cc28-4079-1be5-aedc2dd8c2da.png)
**Titanicデータ（木の深さ：5）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/e361b911-c527-c287-fa6e-fa65a80a2acc.png)
**Boston-housingデータ（木の深さ：3）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/d9ece2a1-ec01-bee1-1a7b-c7ee74289b23.png)

</div></details>

***
## ■CHAPTER 06　機械学習モデルの最適化

    下の▶ をクリックすると、CHAPTER 06 掲載の 決定木画像 が確認できます。
<details><summary>CHAPTER 06 掲載の決定木画像</summary><div>

**最適条件で描いた決定木（Titanicデータ）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/8fbf4d1e-aafe-ca1a-bd2d-d29203d91a4b.png)
**予測結果を表示した決定木（Titanicデータ）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/3d70357f-749b-7052-8dd6-9073c6d06326.png)
**最適条件で描いた決定木（Boston-housingデータ）**
![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/1275001/7082e1eb-bc73-1300-8cde-7bb10512e7d0.png)

</div></details>

***
## ■APPENDIX　Google ColabのForms機能について
　APPENDIX 記載内容を実行する Notebook は、次の通りです。 

| Notebook（クリックで起動）　　　　　　　 | 内容 | 
| :--- | :--- |
|  [**Google_Colab_Forms_適用例.ipynb**](https://colab.research.google.com/github/hima2b4/Python_visuallization_lesson/blob/main/Google_Colab_Forms_%E9%81%A9%E7%94%A8%E4%BE%8B.ipynb) | 正規分布確率を算出するプログラム に **Google Colab の Forms機能 を適用した例**です。|
***
