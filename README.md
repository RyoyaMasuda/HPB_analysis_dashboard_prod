# ホットペッパービューティーの顧客分析ダッシュボード
個人開発として取り組んだダッシュボード開発のソースコードを公開します。

# 画面設定のお願い
window環境において
- 画面サイズ：100%
- 解像度：1920×1080
- ブラウザの倍率：80〜90%

に設定をお願いします。<br>
※その他の環境では画面崩れが生じる可能性があります。適宜調整いただけますと幸いです。

# アプリのURL(現在非公開)
~http://hpbdashboard.mydns.jp/~  
(自宅サーバにてURLを公開しておりましたが、現在別用途にて使用しておりますのでアプリの立ち上げ方法を記載します。)

# アプリ起動方法
- Documentsディレクトリにリポジトリをクローンします。(任意のディレクトリでも構いません。その場合適宜以下のコマンドを変更してください。)
- Linux環境かUnix環境(mac環境)にて実施をしてください。(windowsの場合はWSL2のubuntu22.04LTSにて実施をお勧めします。)  
- python3.9.6にて動作確認をしています。
  
### 1. Documentsディレクトリに移動します
```
cd ~/Documents
```
### 2. リポジトリをクローンします。
```
git clone git@github.com:RyoyaMasuda/HPB_analysis_dashboard.git
```
### 3. modelとdataを削除します。(サンプルデータのため)
sudoは必要ないかもしれない...  
```
cd HPB_analysis_dashboard
```
```
sudo rm -rf model data
```
### 4. 以下のリンクよりmodelとdataをそれぞれダウンロードします。
Downloadsディレクトリにダウンロードする前提で進めていきます。  
<br>
https://drive.google.com/drive/folders/115_96jMMp5Vl0aZQIrvy-2ZP8VZgy02m
  
![image](https://github.com/RyoyaMasuda/HPB_analysis_dashboard/assets/94744317/53acf4a9-9ad3-470f-99ab-74069b80b3e7)
  
### 5. ダウンロードしたらzipファイルを解凍します。(modelとdataがzipファイルとしてダウンロードされている場合)  
sudoは必要ないかもしれない... 
```
cd ~/Downloads
```
以下ファイル名は例。同じようなファイル名でダウンロードされているはずなので各自合わせてください。<br>
```
sudo unzip data-20240218T044219Z-001.zip
```
```
sudo unzip model-20240218T044219Z-001.zip
```
### 6. 解凍したディレクトリをクローンしてきたディレクトリ内に配置します。
```
sudo mv data ~/Documents/HPB_analysis_dashboard/
```
```
sudo mv model ~/Documents/HPB_analysis_dashboard/
```
### 7. HPB_analysis_dashboardディレクトリに移動します。
```
cd ~/Documents/HPB_analysis_dashboard/
```
### 8. ライブラリ等をインストールします。(必要に応じて仮想環境を作成)
```
python -m venv .env
```
```
source .env/bin/activate
```
```
pip install -r requirements.txt
```
### 9. アプリを起動します。
```
python run.py
```

![image](https://github.com/RyoyaMasuda/HPB_analysis_dashboard/assets/94744317/8a33d237-9b5b-47b5-a282-7968ddb5ad87)

### 10. ブラウザにアクセスしてください。  
標準出力されたURLにアクセスしてください。自分の環境では以下URLが出現。  
http://127.0.0.1:5000  
  
# 開発環境
- AWS VPC
- AWS EC2
- AWS Route53
- AWS ALB
- AWS S3
- docker-compose
- Nginx
- uWSGI
- pyenv
- python3.8.10
- jupyterlab
- Dash
- bootstrap4(dash_bootstrap_component)
- Plotly
- plotly express
- pandas
- numpy
- scikit-learn
- LightGBM

# 本番環境
- ubuntu 22.04 LTS server
- Nginx
- uWSGI
- pyenv
- python3.8.10
- Dash
- bootstrap4(dash_bootstrap_component)
- Plotly
- plotly express
- pandas
- numpy
- scikit-learn
- LightGBM
