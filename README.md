# file2list
Python: リストをテキストファイルに書き出す。テキストファイルからリストを読み込む。

# 概要

Pythonのリストの表現に近い形でファイルに書き出します。
テキストファイルの1行がリストの1要素に対応します。
整数、浮動小数点数、文字列、さらには、入れ子のリストなどがほぼそのまま使えます。
テキストファイルの例は、test_read.txtをご覧ください。
人間にとって見やすく単純な形式のテキストファイルですので、個人的なちょっとしたデータ解析や実験等で便利に使えると思います。

# 使い方

使い方の例として、sample.pyをご覧ください。

## 実行例
```
% python sample.py
lis1=[1000, 3.1415, [9.99, 12], [10.21, 18], ['abc', 'DeF', 5], 'BIG', 'small']
lis2=[1000, 3.1415, [9.99, 12], [10.21, 18], ['abc', 'DeF', 5], 'BIG', 'small']
```

## file_to_list(file_name)

ファイルfile_nameから内容を読み込み、リストにして返します。

## list_to_file(lst, file_name)

リストlstを、ファイルfile_nameに書き出します。
すでにファイルが存在する場合には、上書きします。

