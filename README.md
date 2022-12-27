# mypkg
![test](https://github.com/TetsushiKawabata/mypkg/actions/workflows/test.yml/badge.svg)  
このリポジトリはROS2のパッケージです.ROS2をインストールしていない方は先にインストールをお願いします.  

# 導入
```
$ git clone https://github.com/TetsushiKawabata/mypkg.git
```

# 入力と実行結果
端末を2つ用意して以下のように入力する.  
* 端末1
```
$ ros2 run mypkg talker
```

* 端末2
```
$ ros2 run mypkg listener
```

実行結果は以下のようになる.  
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

## 必要なソフトウェア
* ROS2

## テスト環境
* ubuntu20.04

## ライセンス
* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます．
  * このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て自身の著作としたものです．
      * [ryuichiueda/my_slides robosys_2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
* © 2022 Tetsushi Kawabata