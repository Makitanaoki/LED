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

$ cd LED/kadai1

$ make

$ sudo insmod myled.ko

$ sudo chmod 666 /dev/myled0

## 実行例

### 1(16進数)を入力した場合

$ echo 1 > /dev/myled0

![0001](https://user-images.githubusercontent.com/27545346/101144726-1c065400-365c-11eb-8720-dad8d980b16a.png)

右側のLEDが点灯。2進数で0001を表します。

### 8(16進数)を入力した場合

$ echo 8 > /dev/myled0

![ロボットシステム学課題１_1000](https://user-images.githubusercontent.com/27545346/101145106-ab136c00-365c-11eb-8b28-08ca034a193d.jpg)

左側のLEDが点灯。2進数で1000を表します。

### F(16進数)を入力した場合

$ echo F > /dev/myled0

![ロボットシステム学課題１_1111](https://user-images.githubusercontent.com/27545346/101145405-10fff380-365d-11eb-85f0-0ab9f841ca8d.jpg)

LEDが4つ点灯。2進数で1111を表します

・その他実行コマンド

$ echo 2 > /dev/myled0

$ echo 3 > /dev/myled0

$ echo 4 > /dev/myled0

$ echo 5 > /dev/myled0

$ echo 6 > /dev/myled0

$ echo 7 > /dev/myled0

$ echo 9 > /dev/myled0

$ echo A > /dev/myled0

$ echo B > /dev/myled0

$ echo C > /dev/myled0

$ echo D > /dev/myled0

$ echo E > /dev/myled0

## デモ動画

https://youtu.be/u_C2ee9Y79U
