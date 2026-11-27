# XIAO nRF52840 Plus - Semigorou / Rev O

**[発注用Gerber ZIP](Y13-XIAO-revO-order-gerbers.zip?raw=true)**

FR-4・2層・板厚 **1.6 mm**。

Rev Oでは左右それぞれD11〜D19に対応するφ0.65 mmの追加穴を9個配置。D0〜D19の全接続点を用意。D16は電池電圧測定、D14/D15はNFC兼用。追加穴の接触・はんだ付け方法は未確定で、穴を増設するだけでXIAOと自動接続するものではない。BAT+とRESETの追加接続も残る。通常14端子のパッド径は1.4 mm、穴径1.0 mm。旧追加配線用の離れた端子穴は、新しい対応位置の穴へ置き換え。ネジ穴とUSB基準位置は維持。

B面の左右に1行目 https://github.com/semigorou、2行目 XIAO nRF52840 Plus - Semigorouを印字。B面を正面から見て、左は上から下、右は下から上へ読める向き。

|部品|左|右|
|---|---|---|
|XIAO nRF52840 Plus|B面|B面|
|RESETボタン|F面|F面|
|スライド電源|F面|F面|

XIAOの部品面はキャリアへ向ける。基板にはXIAO B、PWR F、RST F、F/Bを印字した。左の14端子をB面取付けに合わせて反転し、再配線している。

## F面

![F面の電源・RESETパッド](front.png)

## B面から見た向き

![B面のマイコン取付側](back.png)

## 配線・検証

- [取付と検証記録](verification-report.md)
- [ピン接続表](pin-connections.csv)
- [センサー配線表](trackball.csv)
- [DRC](drc.txt)は違反0・未配線0。
- [Gerber検証記録](verification.json)で基板とドリル位置を照合済み。電源の位置決め穴は左右2個ずつφ0.90 mm。

右下端子はF面からUSBを上に見てGND / MOTION / SCLK / SDIO / CS / VCC。

GPIO信号の割当は既存XIAO用ファームウェアと同じ。左右各5行6列で左29キー、右27キー＋トラックボールに対応する。

高さと支持部材は実物で調整する。修正版での実装・ケース適合・充電・無線動作は未検証。Rev J以前の取付構成・接続座標は旧版。
