# TensorFlowで画像認識を行うための環境構築の方法
## Windows10(Anaconda使用・不使用)とUbuntuの環境構築について
***
## Windows10の場合(Anaconda環境使用)
- Anacondaのダウンロード。

	<a href="https://www.anaconda.com/" target="_blank">Anacondaのサイト</a>から、Anacondaをダウンロードする。
	![Anacondaのダウンロード](environment_img/anaconda-dl.png)

- Pathを通してAnacondaのインストール。

	インストール画面で、Pathを追加するにチェックを入れる。
	![Anacondaのインストール](environment_img/anaconda-install.png)
- Anaconda環境でPythonの実行をしてみる。

	AnacondaNavigatorメニューのJupiterNotebookのLaunchをクリックして、JupiterNotebookを起動させる。
	![JupiterNotebookの起動](environment_img/jupiternotebook-boot.png)
	既定のブラウザが起動するので、好きな場所に移動して、NewからPython3を選択する。

	![JupiterNotebookの起動](environment_img/jupiternotebook-python.png)
	JupiterNotebookの入力ウィンドウに`print("Hello")`と入力してRunのボタンをクリックするか、Ctrl+EnterでPythonを実行させ、コンソールに`Hello`と表示されることを確認する。

	![JupiterNotebookの起動](environment_img/jupiternotebook-python-run.png)
- Anaconda上でTensorFlowの環境を作る。

	environmentsのCreateをクリックしてTensorFlowの環境を作る。
	![TensorFlow環境の作成](environment_img/anaconda-tensorflow-environment.png)
- TensorFlowのターミナルを起動させる

	上記で作ったTensorFlow環境を起動させる。▶マークをクリックして`Open Terminal`をクリックする。
	![TensorFlow環境の起動](environment_img/anaconda-tensorflow-boot.png)
- TensorFlowのインストール。

	TensorFlowをインストールする。α版を使う場合、バージョンを指定する。
	```
	pip install tensorflow
	```
	![TensorFlowのインストール](environment_img/anaconda-tensorflow-install.png)
- TensorFlow Hunのインストール。

	TensorFlow Hubをインストールする。
	```
	install tensorflow-hub
	```
	![TensorFlow Hubのインストール](environment_img/anaconda-tensorflowhub-install.png)
- エンペラーペンギンの画像を使ってチェック。

	エンペラーペンギンの画像を使って、TensorFlow、TensorFlow Hubが正常にインストール出来たかを確認する。
	![エンペラーペンギンの親子](environment_img/emp.jpg)

	実行するPythonファイルと使用する画像、学習データ、ラベルがあるディレクトリに移動して画像認識を行うコマンドを入力する。
	```
	python penguin.py --graph output_graph.pb --labels penguin_list.txt --input_layer Placeholder --output_layer final_result --image emp.jpg
	```
	ペンギンの種類が表示されたら成功。
	![ペンギンの認識(Anaconda環境)](environment_img/anaconda-recognition.png)
***
***
## Windows10の場合(Anaconda環境不使用)
- Pythonのダウンロード。

	<a href="https://www.python.org/" target="_blank">Pythonの公式サイト</a>から、Pythonをダウンロードする。
	![Pythonのダウンロード](environment_img/python-dl.png)
- Pathを通してPythonをインストール。

	インストール画面でPathを追加するにチェックを入れる。
	![Pythonのインストール](environment_img/python-install.png)
- Pythonが正常にインストールされたかの確認

	コマンドプロンプトで`python`と入力してPythonが起動することを確認する。起動できない場合、Pathが通っているか確認する。
	![Pythonの起動](environment_img/python-test.png)
- pipのアップデート ※必要に応じて

	pipのアップデートを行う。
	```
	pip install -U pip
	```
	![pipのアップデート](environment_img/pip-update.png)
- TensorFlowのインストール

	TensorFlowをインストールする。α版を使う場合、バージョンを指定する。
	```
	pip install tensorflow
	```
	![TensorFlowのインストール](environment_img/tensorflow-install.png)
- TensorFlow Hubのインストール。

	TensorFlow Hubをインストールする。
	```
	install tensorflow-hub
	```
	![TensorFlow Hubのインストール](environment_img/tensorflowhub-install.png)
- エンペラーペンギンの画像を使ってチェック。

	エンペラーペンギンの画像を使って、TensorFlow、TensorFlow Hubが正常にインストール出来たかを確認する。
	![エンペラーペンギンの親子](environment_img/emp.jpg)

	実行するPythonファイルと使用する画像、学習データ、ラベルがあるディレクトリに移動して画像認識を行うコマンドを入力する。
	```
	python penguin.py --graph output_graph.pb --labels penguin_list.txt --input_layer Placeholder --output_layer final_result --image emp.jpg
	```
	ペンギンの種類が表示されたら成功。
	![ペンギンの認識(非anaconda環境)](environment_img/python-recognition.png)
***
***
## Ubuntuの場合(Anaconda環境不使用)
### ※Ubuntu 18.04.2 LTS 日本語Remixを使用。
- Python3のPipをインストール。

	Python3のPipがインストールされていなかったので、Python3のPipをインストールする。
	```
	sudo apt-get install python3-pip
	```
	![Python3のpipをインストール](environment_img/python3-pip.png)
- TensorFlowをインストール。

	Python3のpipを使ってTensorFlowのインストール。
	```
	python3 -m pip install tensorflow
	```
	![TensorFlowのインストール](environment_img/ubuntu-tensorflow-install.png)
- TensorFlow Hubをインストール。

	Python3のpipを使ってTensorFlow Hubのインストール。
	```
	python3 -m pip install tensorflow-hub
	```
	![TensorFlow Hubのインストール](environment_img/ubuntu-tensorflowhub-install.png)
- エンペラーペンギンの画像を使ってチェック。

	エンペラーペンギンの画像を使って、TensorFlow、TensorFlow Hubが正常にインストール出来たかを確認する。
	![エンペラーペンギンの親子](environment_img/emp.jpg)

	実行するPythonファイルと使用する画像、学習データ、ラベルがあるディレクトリに移動して画像認識を行うコマンドを入力する。
	```
	python3 penguin.py --graph output_graph.pb --labels penguin_list.txt --input_layer Placeholder --output_layer final_result --image emp.jpg
	```
	※Python3のバージョンを指定して実行する。

	ペンギンの種類が表示されたら成功。
	![ペンギンの認識(Ubuntu)](environment_img/ubuntu-recognition.png)
***
