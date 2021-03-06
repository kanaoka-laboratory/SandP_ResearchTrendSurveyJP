CSS/SCIS論文に基づく日本のセキュリティ系研究の推移調査
====
日本国内のセキュリティとプライバシーに関連する研究は、情報処理学会のコンピュータセキュリティシンポジウム（CSS）と電子情報通信学会の暗号と情報セキュリティシンポジウム（SCIS）が最も大きな2つの学術イベントと言ってよい。そこでは毎年100を超える研究が発表され、500人を超える参加者が集まり議論をしている。

技術の高度化から産業界への一般展開のスピードが速まるなか、新しい技術に関連するセキュリティとプライバシーの問題も増加し、深くなってきている。学術研究の成果も展開のスピードアップが望まれるところである。そこで、CSSとSCISで発表された研究論文の用語をテキスト分析することによりそれぞれのイベントで研究発表されるテーマの特徴や10年間での変化を考察し、日本におけるセキュリティとプライバシー関連の研究がどういったキーワードを中心に行われているかを見る。

## 分析方法
CSSとSCISの10年分の論文PDFファイルをテキストに変換し、テキスト分析をすることで用語の頻出度合いやクラスタリング、共起関係を見る。

### PDFのテキストへの変換
PDFのテキスト変換には[pdftotext](https://www.xpdfreader.com/pdftotext-man.html) を利用した。

pdftotextの出力結果のテキストファイルはUTF-8文字エンコーディングで出力されるが、論文中の画像部分等はUTF-8の文字コード以外のデータとして出力されるために出力結果のテキストファイルを直接分析ツールに採用することはできない。
そこで、出力結果のテキストファイルから文字情報以外のデータを取り除き、そのデータを分析する。

### テキストデータの分析
[KH Coder](https://khcoder.net/)を用いた。
KH Coderはテキストデータから語を抽出し、それらの語を処理し抽出語のリスト作成や頻出語の表の出力、さらには語と語の結びつきを複数の手法により分析可能なツールである。テキスト分析において多くの[採用事例](https://khcoder.net/bib.html)がある。

分析は4種類行った
- 各イベントの頻出語抽出
- 各イベントの抽出語の多次元尺度構成法による図示とクラスタリング ([参考](https://data-analyzer.net/2019/03/26/khcoder-17-mds/))
- 各イベントの抽出語の階層的クラスター分析による語の分類とクラスタリング ([参考](https://data-analyzer.net/2019/04/08/khcoder-18-cluster/))
- 各イベントの抽出語の共起ネットワークによる図示とクラスタリング ([参考](https://data-analyzer.net/2019/04/23/khcoder20-kyoki-network-1/))



## 分析対象
調査対象としたのは、CSS2011からCSS2020までの10年分のCSS発表論文と、SCIS2012からSCIS2021までの10年分のSCIS発表論文とした。

過去10年間にCSSとSCISで発表された合計5,057件の論文をテキスト化し、分析した。
分析にあたり、研究の推移に無関係と考えられる一般的な用語のうち頻出なもの（83語）は取り除いた。取り除いた用語は[Data](/data/)ディレクトリの「対象外用語.txt」に掲載する。

## 結果
解析結果の詳細を掲載する。
データ掲載はスペースの問題で論文に記載できなかったものを掲載することを目的としている。

詳細は[Result](/result/) を参照。

## 発表

金岡 晃、：CSS/SCIS論文に基づく日本のセキュリティ系研究の推移調査、コンピュータセキュリティシンポジウム2021（CSS2021）、2021 (発表予定) 

## 謝辞
データ分析にあたり、さまざまな視点でご協力いただいた東海大学 大東俊博先生、柿崎淑郎先生に心より感謝申し上げます。

## コンタクト

金岡 晃（東邦大学）
akira.kanaoka@is.sci.toho-u.ac.jp
