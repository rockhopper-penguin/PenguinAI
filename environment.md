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
	pip install tensorflow-hub
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
	pip install tensorflow-hub
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
## Ubuntuの場合(Anaconda環境使用)
### ※Ubuntu 18.04.2 LTS 日本語Remixを使用。
- Anacondaのダウンロード。

	<a href="https://www.anaconda.com/" target="_blank">Anacondaのサイト</a>から、Anacondaをダウンロードする。
	![Anacondaのダウンロード](environment_img/ubuntu-anaconda-dl.png)
- Anacondaのインストール

	Anacondaをダウンロードしたディレクトリに移動し、インストールコマンドを実行する。
	```
	bash Anaconda3-2019.03-Linux-x86_64.sh
	```
	![Anacondaのインストール1](environment_img/anaconda-install1.png)

	Enterキーを押し、利用規約を読む。
	![Anacondaのインストール2](environment_img/anaconda-install2.png)

	利用規約に同意するため、Yesを入力する。
	![Anacondaのインストール3](environment_img/anaconda-install3.png)

	インストール場所に変更がなければEnterキーを押す。
	![Anacondaのインストール4](environment_img/anaconda-install4.png)

	condaを使ってAnacondaを初期化すると聞かれるので、Yesを入力する。
	![Anacondaのインストール5](environment_img/anaconda-install5.png)

	Thank you installing Anaconda3と表示が出ると、インストール完了。
	![Anacondaのインストール6](environment_img/anaconda-install6.png)

- Anaconda環境でPythonの実行をしてみる。

	`jupiter notebook`と入力してJupiterNotebookを起動させる。
	![JupiterNotebookの起動](environment_img/ubuntu-jn.png)
	既定のブラウザが起動するので、好きな場所に移動して、NewからPython3を選択する。

	![JupiterNotebookの起動](environment_img/ubuntu-jn2.png)
	JupiterNotebookの入力ウィンドウに`print("Hello")`と入力してRunのボタンをクリックするか、Ctrl+EnterでPythonを実行させ、コンソールに`Hello`と表示されることを確認する。

	![JupiterNotebookの起動](environment_img/ubuntu-jn3.png)

- Anaconda上でTensorFlowの環境を作る。

	condaコマンドを使ってTensorFlow環境を作る。
	```
	conda create -n TensorFlow
	```
	![TensorFlow環境を作る](environment_img/tf-env.png)

	環境を構築する場所に変更がなければYを入力する。
	![TensorFlow環境を作る2](environment_img/tf-env2.png)
- TensorFlow環境を起動する。

	上記で作ったTensorFlow環境を起動させる。
	```
	source activate tensorflow
	```
	![TensorFlow環境の起動](environment_img/tf-activate.png)
- TensorFlow環境にTensorFlowをインストールする。

	TensorFlowをインストールする。
	```
	python3 -m pip install tensorflow
	```
	![TensorFlowのインストール](environment_img/tf-install.png)

- TensorFlow環境にTensorFlow Hubをインストールする。

	TensorFlow Hubをインストールする。
	```
	python3 -m pip install tensorflow-hub
	```
	![TensorFlow Hubのインストール](environment_img/tfh-install.png)

- エンペラーペンギンの画像を使ってチェック。

	エンペラーペンギンの画像を使って、TensorFlow、TensorFlow Hubが正常にインストール出来たかを確認する。
	![エンペラーペンギンの親子](environment_img/emp.jpg)

	実行するPythonファイルと使用する画像、学習データ、ラベルがあるディレクトリに移動して画像認識を行うコマンドを入力する。
	```
	python3 penguin.py --graph output_graph.pb --labels penguin_list.txt --input_layer Placeholder --output_layer final_result --image emp.jpg
	```
	※Python3のバージョンを指定して実行する。

	ペンギンの種類が表示されたら成功。
	![ペンギンの認識(Ubuntu)](environment_img/result.png)
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
