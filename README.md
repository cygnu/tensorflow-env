## Install
仮想環境を作成し、仮想環境に入る
```
$ conda env create -f tensorflow-env.yml
$ conda activate tensorflow-env
```

Jupyter Notebookを開く
```
(tensorflow-env) $ jupyter notebook
```

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

## Directories
初期のディレクトリ構成です
```
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

## Reference

