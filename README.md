# Switch-DualShock2
Nintendo SwitchのゲームをSONY DUALSHOCK2コントローラを使って遊びましょう!  
AVR(ATmega32U4──これはPro Microという名前でも知られています)が必要です。

![](https://i.imgur.com/DBPr2oB.gif)

## 使いかた
avr-gccが必要です!
```
git clone --recursive https://github.com/pol8139/Switch-DualShock2.git
git clone https://github.com/abcminiuser/lufa.git
cp -r lufa/LUFA Switch-DualShock2
cd Switch-DualShock2
make
```
Switch-DualShock2ディレクトリ内にJoystick.hexがあるはずです。  
これを、ATmega32U4に書き込みます。

以下のように回路を作ります。

![](https://i.imgur.com/dHptRfF.png)

さあ、楽しみましょう!

## キャプチャボタン
DUALSHOCK2にはキャプチャボタンがありません。そのため、「複数ボタンの同時押し」によって足りないボタンを再現しています。

- select+L1=select
- select+L2=capture
- select+R2=home 

## ライセンス
ライセンスはMITです...が、HORI社のディスクリプタを勝手に使用しています。(詳しくは、progmem/Switch-FightstickのオリジナルのREADMEなどを参照してください)そのため、個人的な使用にとどめることを推奨します。