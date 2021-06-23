# Noah 2 雑多なメモ

情報は Rabi-Ribi ver 2.0.0 Feb に基づいた物です。

<br>

## 攻略方法

- Noah Skip をする。
- 0%+6 なら強運を引く、12 時間プレイしても引けないならやめる。

<br>

## 行動リスト

### 基本行動

- 初手は `601` 固定。

<img src="Noah2/601.png" alt="601" width="320" height="180" />

- 攻撃採用の優先度は最低だが、常に裏でカウンタが回り続けている。

| カウンタ % 15 |    ATKID    | 画像                                                         |
| :-----------: | :---------: | ------------------------------------------------------------ |
|       1       | `604, 605`  | <img src="Noah2/604.png" alt="604" width="192" height="108" /><img src="Noah2/605.png" alt="605" width="192" height="108" /> |
|       2       | `606, 607`  | <img src="Noah2/606.png" alt="606" width="192" height="108" /><img src="Noah2/607.png" alt="607" width="192" height="108" /> |
|       3       |    `601`    | <img src="Noah2/601.png" alt="601" width="192" height="108" />      |
|       4       | `603, 604`  | <img src="Noah2/603.png" alt="603" width="192" height="108" /><img src="Noah2/604.png" alt="604" width="192" height="108" /> |
|       5       |    `605`    | <img src="Noah2/605.png" alt="605" width="192" height="108" />      |
|       6       | `606, 607`  | <img src="Noah2/606.png" alt="606" width="192" height="108" /><img src="Noah2/607.png" alt="607" width="192" height="108" /> |
|       7       |    `606`    | <img src="Noah2/606.png" alt="606" width="192" height="108" />      |
|       8       | `601, 602`  | <img src="Noah2/601.png" alt="601" width="192" height="108" /><img src="Noah2/602.png" alt="602" width="192" height="108" /> |
|       9       |    `603`    | <img src="Noah2/603.png" alt="603" width="192" height="108" />      |
|      10       | `604, 605`  | <img src="Noah2/604.png" alt="604" width="192" height="108" /><img src="Noah2/605.png" alt="605" width="192" height="108" /> |
|      11       |    `602`    | <img src="Noah2/602.png" alt="602" width="192" height="108" />      |
|      12       | `604, 605`  | <img src="Noah2/604.png" alt="604" width="192" height="108" /><img src="Noah2/605.png" alt="605" width="192" height="108" /> |
|      13       |    `607`    | <img src="Noah2/607.png" alt="607" width="192" height="108" />      |
|      14       |    `601`    | <img src="Noah2/601.png" alt="601" width="192" height="108" />      |
|       0       | `601 - 607` | <img src="Noah2/601.png" alt="601" width="192" height="108" /><img src="Noah2/602.png" alt="602" width="192" height="108" /><img src="Noah2/603.png" alt="603" width="192" height="108" /><img src="Noah2/604.png" alt="604" width="192" height="108" /><img src="Noah2/605.png" alt="605" width="192" height="108" /><img src="Noah2/606.png" alt="606" width="192" height="108" /><img src="Noah2/607.png" alt="607" width="192" height="108" /> |

<br>

### HP < 40%

- カウンタは攻撃決定前に + 1 される

| カウンタ % 12 | ATKID | 画像                                                    |
| :-----------: | :---: | ------------------------------------------------------- |
|       1       | `614` | <img src="Noah2/614.png" alt="614" width="192" height="108" /> |
|       3       | `610` | <img src="Noah2/610.png" alt="610" width="192" height="108" /> |
|       4       | `615` | <img src="Noah2/615.png" alt="615" width="192" height="108" /> |
|       9       | `616` | <img src="Noah2/616.png" alt="616" width="192" height="108" /> |

<br>

### HP < 60%

- すでに決定済みの攻撃が `610` か `614` 以上の場合、この攻撃決定処理はスキップされる。
- カウンタは攻撃決定前に + 1 される。

| カウンタ % 13 | ATKID | 画像                                                    |
| :-----------: | :---: | ------------------------------------------------------- |
|       1       | `611` | <img src="Noah2/611.png" alt="611" width="192" height="108" /> |
|       5       | `612` | <img src="Noah2/612.png" alt="612" width="192" height="108" /> |
|     `10`      | `613` | <img src="Noah2/613.png" alt="613" width="192" height="108" /> |

<br>

### HP < 80%

- すでに決定済みの攻撃が `610` 以上の場合、この攻撃決定処理はスキップされる。
- カウンタは攻撃決定前に + 1 される。

| カウンタ % 14 | ATKID | 画像                                                    |
| :-----------: | :---: | ------------------------------------------------------- |
|       1       | `608` | <img src="Noah2/608.png" alt="608" width="192" height="108" /> |
|       6       | `609` | <img src="Noah2/609.png" alt="609" width="192" height="108" /> |
|     `11`      | `610` | <img src="Noah2/610.png" alt="610" width="192" height="108" /> |

<br>

## 各攻撃詳細
- 一部のみ抜粋。

### 602

![602](Noah2/602.png)
- 運が悪いと詰む。

### 605

![605](Noah2/605.png)
- Air Jump を装備していない場合、即座にこの攻撃を終了し次の攻撃体勢に移る。
- Rabi Slippers を装備していない場合、Noah 2 の回転速度が約 1.24 倍になる。

### 606

![606](Noah2/606.png)

- `ATKTIME % (77 - pow(Difficulty, 2) * 2)) == 0` の時 8 Way 自機狙い弾を発射する。
- 難易度 UNKNOWN ではプレイヤー視点で 4 フレーム毎に弾をばらまく不可避行動となる。
   - 攻撃時に移動を取らないパターンなら回避可能。
   - 0%+6 では `605` のスキップの影響でこの攻撃を散々喰らう羽目になる。

### 608

![608](Noah2/608.png)
- 難易度 IMPOSSIBLE では不可避な攻撃。TAS でも回避のためには相当な乱数調整が必要だと思われる。

### 610

![610](Noah2/610.png)
- スライディングでも回避可能。行動ごとに Rainbow Pellet を発射していればコンボが切れる事も無い。

### 611

![611](Noah2/611.png)
- Air Jump を装備していない場合、弾の発生頻度が約 1/4 になる。
- Hitbox Down を装備している場合、棒立ちでも回避可能。

### 612

![612](Noah2/612.png)
- 運が悪いと詰む。

### 614

![614](Noah2/614.png)
- 単純に低速状態で移動しているだけだとラインが不足する。

<br>

## 当たり判定

- 一部のみ抜粋。
- 弾の hitbox の色はダメージの高さを表し、青いほど低く、赤いほど高い。
- 表示されている hitbox はドット単位で正確である事を保証できない。

### 602
![602c](Noah2/602c.png)

### 608
![608c](Noah2/608c.png)

### 609
![609c](Noah2/609c.png)

### 610

![610c](Noah2/610c.png)

### 611

![611c](Noah2/611c.png)

### 612
![612c](Noah2/612c.png)

### 615
![615c](Noah2/615c.png)

<br>


## その他

### メモリマップ
- Noah 2 は `EntityID = 8` 固定。
- データ型はすべて `float` 型。

| Address         | メモリ内容               | 値の範囲        |
| --------------- | ------------------------ | --------------- |
| `Entity[0x57C]` | 攻撃カウンタ `HP < 100%` | `10000 - 10014` |
| `Entity[0x584]` | 攻撃カウンタ `HP < 80%`  | `0 - 13`        |
| `Entity[0x578]` | 攻撃カウンタ `HP < 60%`  | `0 - 12`        |
| `Entity[0x580]` | 攻撃カウンタ `HP < 40%`  | `0 - 11`        |

