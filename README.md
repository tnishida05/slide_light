# スライドテンプレート（ライトモード）

## コンパイルについて

lualatexを利用します。必要ない場合、`jobname` や `output-directory` は取り除いてください。
```
lualatex -jobname=output -output-directory=output main.tex
```
上のようにコンパイルした場合は、次のように bibtex を実行してください。
windowsのcmdで実行する場合、パス区切り文字に注意してください。
```
pbibtex output/output.aux
```

相互参照のため、`lualatex` → `pbibtex` → `lualatex` → `lualatex` と実行してください。
`latexmk`など使うと、良い感じにやってくれると思います。

その他、GUIのソフトを使う場合も、`lualatex`でのコンパイルであれば問題ありません。

出力結果は、[`output/output.pdf`](/output/output.pdf)です。

## ファイルの編集について

パッケージ`subfiles`を利用しています。

スライドを追加する場合は、[`contents`](/contents)の中のファイルを編集してください。
[`contents`](/contents)にファイルを追加したときは[`main.tex`](/main.tex)で参照するのを忘れないでください。

数学記号や定理の設定は、[`styles/mysetting.sty`](/styles/mysetting.sty)を編集してください。

## 色設定について

このテンプレートは、`metropolis`というテーマを利用しています。
テーマの設定は、[`styles/mytheme.sty`](/styles/mytheme.sty)で行っています。

全体的に「脱色」をイメージして色を設定しました。
薄い色でなければ、多少追加して使ってもデザインを崩さないと思います。