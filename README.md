# ファイナンス （Pythonによるビジネスデータサイエンス 第4巻）

<img src="https://www.asakura.co.jp/user_data/product_image/12914/1.jpg" width="200px" >

---

本リポジトリは朝倉書店発行書籍『[ファイナンス](https://www.asakura.co.jp/detail.php?book_code=12914)』（[Pythonによるビジネスデータサイエンス](https://www.asakura.co.jp/series_books.php?series_id=349) 第4巻）のサポートサイトです。

---

## 目次
- [1. サンプルプログラム](#1.サンプルプログラム)
	- [1.1. ファイル構成](#1.1.ファイル構成)
	- [1.2. プログラムのダウンロード](#1.2.プログラムのダウンロード)
- [2. 実行環境の構築](#2.実行環境の構築)
- [3. 実行方法](#3.実行方法)
- [4. pandasリファレンス](#4.pandasリファレンス)
- [5. 関連リンク集](#4.関連リンク集)
	- [5.1. 言語/ライブラリ](#4.1.言語/ライブラリ)
	- [5.2. データベンダ](#4.2.データベンダ)

---


## 1. サンプルプログラム

### 1.1. ファイル構成

サンプルプログラムはjpyter lab(もしくはjupyter notebook)で動作するipynbの形式で配布しています。以下に示したインストール方法を参考に実行環境を構築しコードを実行してください。
|ファイル名   |説明  |
|:--          |:--   |
|`2-1.ipynb` |2.1 株式市場と4本値データ |
|`2-2-1.ipynb` |2.2.1 ゴールデンクロスとデッドクロス |
|`2-2-2.ipynb`  |2.2.2 相対力指数: RSI |
|`2-3.ipynb` |2.3 株式リターン(収益率)を計算する |
|`2-4.ipynb` |2.4 企業規模(ハブ式時価総額)とリターンの関係をみてみる |
|`2-5.ipynb` |2.5 期待リターンとリスクを計算する |
|`2-6.ipynb` |2.6 ポートフォリオ構築の基礎 |
|`2-Q.ipynb` |2章章末問題 |
|`4-9.ipynb` |4.9 V/P戦略の実装 |
|`5-3.ipynb` |5.3 ラッキセブン戦略の実装 |
|`5-5.ipynb` |5.5 Betting Against Beta戦略 |
|`6-1.ipynb` |6.1 ベータを手がかりに業界の特徴をみる |
|`6-3.ipynb` |6.3 ハーディング指数で市場をみる |
|`6-Q.ipynb` |6章章末問題 |
|`README.md` |この文章のMarkdown |
|`data` | 上記ipynbで利用する株価データ |
|`appendix` |PythonやPandasの利用方法を解説したipynb集 |

### 1.2. プログラムのダウンロード

本リポジトリのサンプルプログラムをPC環境にダウンロードします。
ZIPをダウンロードする方法と、gitによりダウンロードする方法があります。

#### 1.2.1 zipファイルのダウンロード
本ページの上部緑のアイコン「Code」をクリックし、一番下の「Download ZIP」を選択すると、finance.zipがダウンロードできます。このファイルを適当な場所で解凍してください。

#### 1.2.2 gitによるダウンロード
`git`がインストールされていない場合は下記サイトを参照してインストールしてください。

* [https://git-scm.com/book/ja/v2/使い始める-Gitのインストール](https://git-scm.com/book/ja/v2/%E4%BD%BF%E3%81%84%E5%A7%8B%E3%82%81%E3%82%8B-Git%E3%81%AE%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB)

サンプルプログラムをダウンロード（clone）する作業用のフォルダ/ディレクトリを適当に作成してください。  
作成できたら下記コマンドを実行してください。サンプルプログラムがダウンロード（clone）されます。  
※`[作業用フォルダ/ディレクトリへのパス]`の部分は作成した作業用フォルダ/ディレクトリのパス（絶対パスもしくは相対パス）に置き換えてください。
```bash
cd [作業用フォルダ/ディレクトリへのパス]
git clone https://github.com/asakura-data-science/preprocessing.git .
```
### 1.3 データのダウンロード
本書で紹介されているデータは容量が大きいため(221.9MB)、朝倉書店のページにおいてあります。
[ここから](https://app.box.com/s/8jibj2iqh3asjkgfdj3dg8fts9nluzyy) data.zipをダウンロードして解凍すると、stockDaily.csvなど6つのファイルが展開されます。これらのファイルを1.2で作成した作業用フォルダの下にdataフォルダとしてコピー(移動)してください。それぞれのファイルの内容は本書p.12の表2.1で説明しております。

## 2. 実行環境の構築
サンプルプログラムを実行するにはPython、Jupyter、各種ライブラリのインストールが必要となります。構築方法がわからない方は、本シリーズの[前処理のサポートページ](https://github.com/asakura-data-science/preprocessing)をご参照ください。
なお、本書で利用するライブラリは以下に示すとおりで(括弧内は実行確認のとれているバージョン)、pipもしくはanacondaでインストールしてください。

* pandas (1.1.3)
* numpy (1.19.2)
* matplotlib (3.5.1)
* mplfinance (0.12.7a12)
* statsmodels (0.12.1)


## 3. 実行方法

以下のようにコマンドを実行して、`jupyter`を起動してください。

```bash
cd [作業用フォルダ/ディレクトリへのパス]
jupyter-lab
```

すると、Webブラウザが起動してjupyterlabのページが開き、サンプルプログラムのフォルダ構成が表示されます。  

## 4. pandasリファレンス
本書ではpandasを用いたプログラムが多いため、リファレンスを用意しておきました。
2-1.でダウンロードしたプログラムのappendixフォルダをjupyterで開くことで参照できます。
また、以下のリンクをたどることでも参照いただけます。

[pandasリファレンス](https://asakura-data-science.github.io/finance/)

## 5. 関連リンク集

### 5.1. 言語/ライブラリ
- Python: https://www.python.jp/
- jupyter: https://jupyter.org/
- pandas: https://pandas.pydata.org/
- mplfinance: https://github.com/matplotlib/mplfinance
- statsmodels: https://www.statsmodels.org/stable/index.html

### 5.1. ファイナンス関連
- Kenneth R. Frenchによるデータライブラリ: http://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html
Fama-French 3 ファクター・モデルの元論文: https://doi.org/10.1016/0304-405X(93)90023-5
- AIで探る株価の予測可能性: https://www.jstage.jst.go.jp/article/jbef/11/0/11_121/_article/-char/ja/

### 5.3. データベンダ
- 金融データソリューションズ: https://www.fdsol.co.jp/index.html
- 日経NEEDS: http://www.nikkei.co.jp/needs/
- JPXデータクラウド: http://db-ec.jpx.co.jp/
- 日本取引所グループ: https://www.jpx.co.jp/
- EDINET: https://disclosure.edinet-fsa.go.jp/:w
- Yahoo!ファイナンス: https://finance.yahoo.co.jp/
- モーニングスター: https://www.morningstar.co.jp/
- Quandl: https://www.quandl.com/
- Bloomberg: https://www.bloomberg.co.jp/
- factset: https://www.factset.com/
