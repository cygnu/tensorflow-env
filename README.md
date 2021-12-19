## Install
仮想環境を作成し、仮想環境に入る
``` Shell
$ cd tensorflow-env
$ conda env create -f python38.yaml
$ conda activate tensorflow-env
```

Jupyter Notebookを開く
``` Shell
(tensorflow-env) $ jupyter notebook
```

仮想環境を削除する

``` Shell
(tensorflow-env) $ conda deactivate

$ conda remove -n tensorflow-env --all
```

[こちら](#directories)へ続く

## Versions
主要なパッケージのversionです
```
python==3.8.12
tensorflow==2.3.0
Keras==2.4.3
matplotlib==3.5.0
numpy==1.21.2
pandas==1.3.4
scikit-learn==1.0.1
```

<a id="directories"></a>
## Directories

初期のディレクトリ構成です

``` Shell
$ tree .
.
├── README.md
├── cats-vs-dogs.ipynb
├── tensorflow-env.yaml
├── test
│   ├── cats
│   └── dogs
├── train
│   ├── cats
│   └── dogs
└── validation
    ├── cats
    └── dogs

9 directories, 3 files
```

[こちら](https://kaggle.com/c/dogs-vs-cats/data)からzipファイルでダウンロードし、このディレクトリに配置します。

zipファイルを解凍すると、3つのファイルが展開されます。

``` Shell
$ unzip dogs-vs-cats.zip

Archive:  dogs-vs-cats.zip
  inflating: sampleSubmission.csv
  inflating: test1.zip
  inflating: train.zip
```

展開したzipファイルの中にzipファイルが残っているので、同様に、

``` Shell
$ unzip test1.zip

Archive:  test1.zip
  inflating: test1/cat.0.jpg
  inflating: test1/cat.1.jpg
  inflating: test1/cat.2.jpg

$ unzip train.zip

Archive:  train.zip
  inflating: train/cat.0.jpg
  inflating: train/cat.1.jpg
  inflating: train/cat.2.jpg
```

必要なファイルが揃ったディレクトリ構成です。

``` Shell
$ tree .
.
├── README.md
├── cats-vs-dogs.ipynb
├── dogs-vs-cats.zip
├── sampleSubmission.csv
├── tensorflow-env.yaml
├── test
│   ├── cats
│   └── dogs
├── test1
│   ├── 1.jpg
│   ├── 2.jpg
│   ├── 3.jpg
│   ├── 12500.jpg
├── test1.zip
├── train
│   ├── cat.0.jpg
│   ├── cat.1.jpg
│   ├── cat.9999.jpg
│   ├── cats
│   ├── dog.0.jpg
│   ├── dog.1.jpg
│   ├── dog.9999.jpg
│   └── dogs
├── train.zip
└── validation
    ├── cats
    └── dogs

10 directories, 37507 files
```

## Reference

