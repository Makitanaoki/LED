# ロボットシステム学第１回課題「デバイスドライバ」
## 実装内容
・ コマンド入力で16進数の0～Fまでの数を1つ入力し、LEDの点灯を用いて２進数表現をする。

・LEDの点灯を２進数表現で１、消灯を０とする。
## 用意する物
・Raspberry Pi 3 Model B+

・ブレッドボード

・抵抗220Ω *4

・LED *4

・ジャンパー線　オスーメス *5

## 回路

![配線](https://user-images.githubusercontent.com/27545346/101141244-5caf9e80-3657-11eb-998e-e820eec57e71.png)

・LEDのアノードには画像を見て上から順に、GPIO23,22,21,20と接続します。

・カソードには220Ωの抵抗を接続します。

## ビルド

実行するには、以下のコマンドを実行してください

$ git clone https://github.com/Makitanaoki/LED.git

$cd LED/kadai1

$make

$sudo insmod myled.ko

$sudo chmod 666 /dev/myled0
