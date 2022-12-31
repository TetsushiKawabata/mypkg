# mypkg
![test](https://github.com/TetsushiKawabata/mypkg/actions/workflows/test.yml/badge.svg)  
* このリポジトリはROS2のパッケージです.
* ROS2をインストールしていない方は先にインストールをお願いします.
* このリポジトリにはtalker.py, listener.py, そしてtalk_listen.launch.pyという名前のノードが含まれています.

# talkerとlistener
* talkerはcountupというトピックを通じて, Int16型のメッセージを送信します.
* listenerはcountupからInt16型のメッセージを受信して出力します.

### 入力と実行結果
端末を2つ用意して以下のように入力してください.
* 端末1
```
$ ros2 run mypkg talker
```

* 端末2
```
$ ros2 run mypkg listener
```
  
実行結果は以下のようになります.
* 端末2
```
[INFO] [1672139699.627192098] [listener]: Listen: 0
[INFO] [1672139700.107946714] [listener]: Listen: 1
[INFO] [1672139700.608299988] [listener]: Listen: 2
[INFO] [1672139701.108361480] [listener]: Listen: 3
[INFO] [1672139701.608395773] [listener]: Listen: 4
[INFO] [1672139702.108339639] [listener]: Listen: 5
(以下略)
```

# launchファイル
* launchファイルを使うことで, 複数のノードを同時に立ち上げることができます.  

### 入力と実行結果
```
$ ros2 launch mypkg talk_listen.launch.py
[listener-2] [INFO] [1672143521.547788850] [listener]: Listen: 0
[listener-2] [INFO] [1672143522.021609197] [listener]: Listen: 1
[listener-2] [INFO] [1672143522.521629912] [listener]: Listen: 2
[listener-2] [INFO] [1672143523.021668093] [listener]: Listen: 3
[listener-2] [INFO] [1672143523.521733415] [listener]: Listen: 4
[listener-2] [INFO] [1672143524.021810561] [listener]: Listen: 5
(以下略)
```

## 必要なソフトウェア
* ROS2 humble

## テスト環境
* ubuntu22.04

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
    * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Tetsushi Kawabata