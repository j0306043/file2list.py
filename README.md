# file2list
Python: リストをテキストファイルに書き出す。テキストファイルからリストを読み込む。

# 概要

Pythonのリストの表現に近い形でリストをファイルに書き出します。
リストの(トップレベルの)1要素がテキストファイルの1行に対応します。
整数、浮動小数点数、文字列、さらには、入れ子のリストなどがほぼ人間に見やすい表現で書き出されます。

一方、そのようなテキストファイルを読み込んでリストにすることができます。
テキストファイルの例は、[test_read.txt](https://github.com/j0306043/file2list/blob/main/test_read.txt)をご覧ください。
整数、浮動小数点数、文字列、さらには、入れ子のリストなどがほぼそのまま使えます。
からくりとしては、ast.literal_evalを使っているだけです。
人間にとって見やすく単純な形式のテキストファイルですので、個人的なちょっとしたデータ解析や実験等で便利に使えると思います。

# 使い方

使い方の例として、[sample.py](https://github.com/j0306043/file2list/blob/main/sample.py)をご覧ください。

## file_to_list(file_name)

ファイルfile_nameから内容を読み込み、リストにして返します。

## list_to_file(lst, file_name)

リストlstを、ファイルfile_nameに書き出します。
すでにファイルが存在する場合には、上書きします。

## 実行例

```
% python sample.py
lis1=[1000, 3.1415, [9.99, 12], [10.21, 18], ['abc', 'DeF', 5], 'BIG', 'small']
lis2=[1000, 3.1415, [9.99, 12], [10.21, 18], ['abc', 'DeF', 5], 'BIG', 'small']
```

test_read.txtから読んだものがlis1です。
lis1をtest_write.txtに書いて再度読み込んだものがlis2です。
lis1とlis2が一致している様子を表しています。
