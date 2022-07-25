# segmentaion_for_matlab

## segmentaion for Matlab


- train.m-学習用

- estimate.m-推論用

- json_to_label.py-jsonデータかラベルデータを作成するscript(pytorch用)

- json_to_for_matlab_labeldata.py-jsonデータかラベルデータを作成するscript(matlab用)


注意
matlabとpytorchでは使用するラベル画像のデータ形式が違うのでそれぞれに合った変換用pythonスクリプトを使用してください
また元画像はプログラム内でサイズを変更できるので入力サイズは何のサイズでもいいが、
ラベルデータのプログラム内での一斉リサイズがまだできていないのでjson_to_for_matlab_labeldata.py
内の以下の部分でモデルにあったサイズのラベル画像を生成する必要がある。

'''


'''


## 使用例

第一引数がjsonデータと元の画像が入っているフォルダのパス

第二引数がラベルデータを出力するファイルを指定(-o=は省略不可）

第三引数はラベルデータのパス(-label_file=は省略不可) ラベルテキストはlabel.txtを参考に作成

```

python json_to_for_matlab_labeldata.pyjson   json_data -o=output_folder -label_file=label.txt  


```

## 実行環境

* matlab2022a



