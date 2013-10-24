WindowsにPyCharm CEを導入する
===================
#### ※注意   
* ***Windowsで \\ をコピペしたら ￥ になる***  
* ***Windowsのbit数(32bitか64bit)には注意する***  
* ***ダウンロードするバージョンが少し異なる場合もある***
* ***cmdの開き方は一番下を参照***

## Pythonのインストール
1. 以下のページからver2.7の最新版（2013年10月12日現在では2.7.5）のPythonをダウンロード  
   ※URL:http://www.python.org/download/releases/2.7.5    
   ※Windows 8の人はデスクトップ左下で右クリックしてシステムをクリック  
   ※***OSのbit数に注意する（「コンピュータ」のプロパティから確認）***   
2. ダブルクリックして，Nextを連打してインストールする
3. cmdで動作確認をする（動かないなら1.からやり直す）
   
   ```
   C:\Users\ユーザ名>python <- これは恐らく動かない
   C:\Users\ユーザ名>cd C:\Python27
   C:\Python27> python 
   Python 2.7.5  （略）
   Type "Help"   （略）
   >>> 
   ```
   こうなったらOK，以下のように打って終了する
   
   ```
   >>> quit()
   ```
   
4. C:\Python27の中にScriptsというディレクトリが無ければ作っておく  
   ※大文字，小文字，スペルミスに注意する
5. 環境変数の設定
   1. スタートの「コンピュータ」を右クリックして，プロパティをクリック
   2. 左側にあるシステムの詳細設定をクリック
   3. 下側の環境変数をクリック
   4. システム環境変数のPATH（Path）を選んで編集をクリック
   5. 変数値に;C:\Python27;C:\Python27\Scriptsを追加
   6. OK連打
6. Pythonのインストール終了


## pip（パッケージ管理ツール）のインストール
1. 以下のURLにアクセス  
   ※URL:http://www.lfd.uci.edu/~gohlke/pythonlibs/#pip
2. 以下のようになっているので，   

	**64bit版-Windows**  
	Pip installs packages. An easy_install replacement.  
	* pip-1.3.1.win-amd64-py2.5.exe
	* pip-1.3.1.win32-py2.5.exe
	* pip-1.4.1.win-amd64-py2.6.exe
	* **<font color="red">pip-1.4.1.win-amd64-py2.7.exe</font> <- `ここをクリック`**
	* pip-1.4.1.win-amd64-py3.2.exe
	* pip-1.4.1.win-amd64-py3.3.exe
	* pip-1.4.1.win32-py2.6.exe
	* pip-1.4.1.win32-py2.7.exe
	* pip-1.4.1.win32-py3.2.exe
	* pip-1.4.1.win32-py3.3.exe  
    
	**32bit版-Windows**  
	Pip installs packages. An easy_install replacement.  
	* pip-1.3.1.win-amd64-py2.5.exe
	* pip-1.3.1.win32-py2.5.exe
	* pip-1.4.1.win-amd64-py2.6.exe
	* pip-1.4.1.win-amd64-py2.7.exe
	* pip-1.4.1.win-amd64-py3.2.exe
	* pip-1.4.1.win-amd64-py3.3.exe
	* pip-1.4.1.win32-py2.6.exe
	* **<font color="red">pip-1.4.1.win32-py2.7.exe</font> <- `ここをクリック`**
	* pip-1.4.1.win32-py3.2.exe
	* pip-1.4.1.win32-py3.3.exe


3. ダウンロードしたexeファイルを実行してインストールする


## PyCharm CE(Community Edition)のインストール
1. GoogleでPyCharmを検索して，一番上にアクセス  
   ※URL:http://www.jetbrains.com/pycharm/
2. Downloadタブをクリックし，Download Communityをクリックして，  
   Community Editionをダウンロードする
3. ダウンロードしたファイルをダブルクリックして，Next連打でインストール

## PyCharm CEの設定
1. 初回起動時に，Complete Installationウインドウが出てくるが，  
   I do not （略）の方に，チェックがあることを確認して，OKを押す
2. 再起動した後に，PyCharm Community Edition Initial Configurationウインドウで初期設定をする
   1. Keymap schemeは使ったことや聞いたことのある名前を選択すると良い
   2. IDE themeはDarculaがオススメ
   3. Editor colors and fontsはClick to previewを押すことでカラーテーマを  
      確認できるようになるので，確認しながら好みに合わせて設定する
   4. OKを押して，再起動する
3. Create New Projectをクリック
4. Project nameはtest
5. 最初はInterpreterが設定できない状態なので，右の[…]をクリック
   1. Python Interpretersウインドウが出てくるので，右側の+マークをクリック
   2. C:\Python27\python.exeを選択してクリック，  
      出てない場合は，Localを押して，C:\Python27\python.exeを探して，OKをクリック
   3. Pycharmが指定したPythonの設定を読み込むので，少し待つ
   4. Python 2.7.5が上のリストに追加されたのを確認して，OKをクリック
6. Interpreterが設定できるようになっているので，Python 2.7.5を選んで，OKをクリック
7. 設定終了，Windowsのセキュリティが警告してきたら，ブロックを解除を選択する
8. ここで設定したことは，後から変更もできる

## PyCharm CEの基本的な使い方
1. プロジェクトの作成
	1. 起動時でも，Fileメニューからでも選べるNew Projectを選択
	2. Project Nameに設定した名前（以下，testと呼ぶ）で，Locationの場所に，ディレクトリが作られる
2. ソースコードの作成
	1. 左側のtestというディレクトリアイコンの場所を右クリックして，New -> Python Fileをクリック
	2. Name（今回は，spam）を設定し，KindはPython fileにしたまま，OKをクリック
	   ※このとき，Nameに拡張子（.py）は付けなくてもよい
	3. testというディレクトリの中に，spam.pyが出来ている  
	   ※エクスプローラからも確認できる
3. トライアンドエラーでソースコードを完成させていく
	1. 右側のエディタでコードを書く
	2. ソースコードを動かす
	   1. 最初は上のRunメニューから3つめのRunをクリックし，実行するソースコードの名前を選択する
	   2. 1.を行ったあとは，Ctrl+F5で実行できるようになっている  
	      ※最初に設定したKeymap schemeの設定によって，実行方法が異なる場合があるので  
	      そのときは，各メニューの右側に示してあるKeymapで実行するようにする
    3. 実行結果が出力される  
       1. 納得行ったら，さらに改良する
       2. エラーが起きたら，修正して，再度実行する
4. 1~3.を繰り返して，Pythonのプログラムをどんどん作っていく
5. ~~必要であればcmdを開いて，pipを使って必要なモジュールをインストールする~~
6. 必要なモジュールがある場合は，モジュール名，bit数などを確認し，ダウンロードしてインストールする  
	※URL:http://www.lfd.uci.edu/~gohlke/pythonlibs/

## 代表的なモジュール
下の3つモジュールは重要なモジュール（ライブラリ，パッケージ，ツール）である．  
* *NumPy* 数値計算用モジュール  
* *SciPy* 科学計算用モジュール，NumPyの兄弟分  
* *matplotlib* グラフ表示用モジュール  

3つをインストールするには以下のサイトからダウンロードする  
※URL:http://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy-stack  

**64bit版-Windows**  
Scipy-stack (experimental) is a meta package that (略)  

* **<font color="red">Scipy-stack-13.10.11.win-amd64-py2.7.exe</font> <- `ここをクリック`**  
* Scipy-stack-13.10.11.win-amd64-py3.3.exe  
* Scipy-stack-13.10.11.win32-py2.7.exe  
* Scipy-stack-13.10.11.win32-py3.3.exe  

**32bit版-Windows**  
Scipy-stack (experimental) is a meta package that (略)  

* Scipy-stack-13.10.11.win-amd64-py2.7.exe  
* Scipy-stack-13.10.11.win-amd64-py3.3.exe  
* **<font color="red">Scipy-stack-13.10.11.win32-py2.7.exe</font> <- `ここをクリック`**    
* Scipy-stack-13.10.11.win32-py3.3.exe  

## その他
### cmdの開き方
スタート押して，下の検索窓にcmdと打つとcmd.exeが出てくるので，エンターキーを押すか，クリックする．

### pipの基本的な使い方
1. モジュールの検索

   ```
   C:\Users\ユーザ名>pip search モジュール名
   ```

2. モジュールのインストール

   ```
   C:\Users\ユーザ名>pip install モジュール名
   ```

3. モジュールのアンインストール

   ```
   C:\Users\ユーザ名>pip uninstall モジュール名
   ```

4. インストールしているモジュールの一覧表示

   ```
   C:\Users\ユーザ名>pip freeze
   ```
5. その他のコマンド，オプションは単にpipと打って確認する

   ```
   C:\Users\ユーザ名>pip
   ```

### PyCharmのちょっと便利な使い方
1. とりあえずソースコードを実行する
2. メニューからTools -> Open Terminal…をクリックする
3. 下に出てきた，Terminalコンソールの右側にある歯車アイコンをクリックし，Split modeにチェックを入れる
4. もう一回，ソースコードを実行すると，実行結果画面とTerminalが分割して表示されている
5. 表示されない場合は，以下を試す
   1. 一番左下の白いアイコンをクリックし，番号とタグが表示される状態する  
      ※例:6:TODO，Event Log，4:Run，Terminalなど
   2. 左側にRun，右側にTerminalが来るように，ドラッグして動かす（他のは，そのままで良い）
   3. 再度，ソースコードを実行する
6. 右下にあるTerminalコンソールで，pythonかipythonを実行させておく
7. 実行結果を確認しつつ，右下のpythonかipythonでちょっとした動作確認も出来るようになる
   
