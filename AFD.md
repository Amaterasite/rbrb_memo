# AFD モード色々

- この情報は Rabi-Ribi ver 2.00 Feb に基づいて書かれています。

AFD モードは 2018 / 04 / 01 で追加された April Fools モードの一つで、マップとシステムの一部に変更を加える事でゲームバランスが大きく変わった斬新なモードです。<br>
通常のゲームと比べて非常に高難易度で応用的な技術も求められるため、慣れていない方のプレイは推奨できません。<br>


## 始め方
- Rabi-Ribi の起動オプションに `-afd` を追加して起動することで AFD モードになる。
- 外部から `rabiribi.exe+0x013AFD62` の値を変更することで起動中でも AFD モードへ変更可能。
   - AFD ブロックはリロードなどでマップの再読み込みをしなければ更新されない。


## AFD モードの仕様

- 各所に AFD ブロックが追加され、ゲーム進行を大きく制限される。
- 初期 PP が 11 減少。
- 初期 HP が 30 減少。
- 敵の体力が 1.45 倍に増加。
- 全ての攻撃の威力が使用者の体力の残量に応じて 1 ～ 2 倍に増加。
  - この仕様はなぜかプレイヤー側にも適用され、HP が 1 の状態では 2 倍近い火力になる。
- 被弾時のランク減少ペナルティがゲージ 0.85 本から 2.17175 本に増加。
- プレイヤーは 6 回被弾するたびに 500 フレームの Mortality が付与される。
  - 累計 6 回被弾 = 死 とも言える仕様。
- ボス戦以外での en の発生がしなくなる。
  - 道中での回復ができなくなり、Post Gameクリア後まで所持金は有限資源となる。
- 所持金獲得量が 3.33 倍に増加。
  - 卵獲得による所持金ボーナスにも影響する。
- TM 数に応じてボスに以下のバフが付与される。

| TM | Buff | 備考 |
| :--: | :--: | :--: |
| 0 | Power Absorb |  |
| 1 | Hex Cancel |  |
| 2 | Unstable | 低速の状態なら Quick Reflux 付与中にも攻撃可能。 |
| 3 | Double Damage | 序盤の難所となるバフ。 |
| 4 | Super Armour | ほぼ無意味。 |
| 5 | Lucky Seven | 多くの場合 7 回被弾する前に死ぬので無意味。 |
| 6 | Null Slow | ほぼ無意味。 |
| 7 | Attack Up |  |
| 8 | Bunny Lover |  |
| 9 | Health Absorb |  |
| 10 | Null Melee | Post Game 以降ではこのあたりのバフが付与されたら 99 Reflect を警戒すべき。 |
| 11 | Defense Up | 99 Reflect のカウンター発生範囲がズレる事があるので注意。 |
| 12 | 99 Reflect | **最も危険なバフ。**一瞬で HP が溶ける。 |
| 13 | HP Recover | ~~Irisu 戦で BGM のピッチが勝手に戻る原因。~~ |
| 14 | Quad Damage |  |
| 15 | 300 Revenge |  |

 - 16 TM 以上の場合は 9 秒ごとに 0 から 15 の順でバフが切り替わる。
   - 1 個のバフの時間は `(100 + (難易度 * 12)) * (TM - 16) + 3` フレーム。
   - 難易度、TM 数が多いほど混在するバフの数が増える。

## AFD モードでの攻略手順
想定されていないと思われる解法や zip は使わない物とする。

### Chapter 0
- Piko Hammer 前にブロックがあるため Forgottn Cave の隠しルートから Spectral Cave へ向かう。
- Piko Hammer を入手。
- 回収可能な場所で Forest UPRPRC イベントを発生させるために Cocoa 1 を倒す。
   - Carrot Bomb は Air Jump 入手後まで入手できない。
   <img src="/afd/CarrotBomb_6Tile.png" alt="CarrotBomb_6Tile" width="320" height="180" />
- 道なりに進み Ashuri 1 を倒す。
<br>

### Chapter 1
- Chapter 1 から 2 では Cicini, Chocolate, Cocoa, Ashuri 以外を仲間にすることはできない。

#### Cicini
- Cicini 前でのバネイベントを発生させるために Kotri 1 を倒す。
   - DEF Trade の上が一方通行となっているためそれ以上進むことはできない。
   <img src="/afd/Park.png" alt="Park" width="320" height="180" />

#### Chocolate
- 特筆すべきことは特に無し。

#### Cocoa
- Cocoa 2 直前の回復ポイントは封鎖されている。

#### Ashuri
- Golden Riverbank の Ashuri 2 を倒す。
   - Evernight Peak の UPRPRC イベント前に壁が設置されていてそれ以上進むことはできない。
   <img src="/afd/Evernight.png" alt="Evernight" width="320" height="180" />
- Rabi-Rabi Town へ戻り、Rainbow Crystal のイベントフラグを立てる。
- Rabi-Rabi Beach から Volcanic Cavern を経由して Spectral Cave まで行き Rainbow Crystal を倒す。
   - 0% と全く同じルート。道中に AFD ブロックは無い。
   <br>

### Chapter 2
- 石碑イベントで Bunny Amulet 解禁。
- Cicini を倒していれば帰還後に研究所イベントが発生し、Golden Riverbank の下部の探索が可能となる。
  - 研究所イベント前に下部に降りてしまうと上部に戻る事ができなくなる。

#### 想定されていないと思われる解法
AFD モードを真っ向からプレイしたい方はこの時点で以下のアイテムを入手することは非推奨。

##### Bunny Whirl
- 直前の AFD ブロックの判定が抜けているため Sliding Powder 無しで素通りできる。
- 帰りは Downdrill Semisolid Clip を使う。
 <img src="/afd/BunnyWhirl.png" alt="BunnyWhirl" width="320" height="180" />

##### Sliding Powder
- 同じ部屋にいる Box を誘導し、爆弾を吐き出させる事で回収できる。
 <img src="/afd/SlidingPowder.png" alt="SlidingPowder" width="320" height="180" />

##### Carrot Bomb
- 上空の蜂を Whirl Bonk する事で回収できる。
 <img src="/afd/CarrotBomb.png" alt="CarrotBomb" width="320" height="180" />
  <br>

### Chapter 3 - 5
- Systen Interior で Air Jump 入手。
   - これ以降は移動の制限は大幅に緩和される。
- 6-Tile Jump で Carrot Bomb を入手。
   - 6-Tile Jump はシビアなので正規ルートか怪しい所だったが、これを使わなければ回収のために Bunny Whirl が必要、その回収に Sliding Powder が必要、さらにその回収に Carrot Bomb が必要…と無限ループを起こしてしまうため想定解として扱うことにした。

#### Pandora
- Pyramid の入口が封鎖されていて正規の方法では侵入できない。
- Speedrun で用いられる 4-Tile Zip によるボス部屋直行ルートが想定解だと思われる。 
 <img src="/afd/Pandora1.png" alt="Pandora1" width="320" height="180" /> <img src="/afd/Pandora2.png" alt="Pandora2" width="320" height="180" />
  - Ashuri から Shrink バフを購入し、Temp Save イベントを回避しつつ徒歩で進み、<br>サーチアイ攻撃時にボス状態になる性質を利用して Erina の判定サイズを小さくしてブロックの隙間に入り込むという手段もあるが、<br>あまりに特殊かつボス前までに回収可能なアイテム数が多くなるため想定解ではないと思われる。
  <img src="/afd/Pyramid.png" alt="Pyramid" width="320" height="180" />
- なぜかワープストーンが封鎖されていて使用することができないため、帰りは Slide Jump を使う必要がある。
 <img src="/afd/Pyramid_Warp.png" alt="Pyramid_Warp" width="320" height="180" /> <img src="/afd/Pyramid_SlideJump.png" alt="Pyramid_SlideJump" width="320" height="180" />

#### Kotri 2 / Lilith
- Floating Graveyard の道が封鎖されているため Halloween ルートから迂回する必要がある。
<br>

### Chapter 6 - 8
- Hall of Memories で Carrot Shooter 入手。
   - この時点で AFD 特有の制限は無くなる。

#### Aruraune / Keke Bunny
- Starting Forest の Attack Up の部屋で Carrot Shooter のブーストを使い侵入。
 <img src="/afd/DarkForest.png" alt="DarkForest" width="320" height="180" />
  <br>

## AFD LOW ITEM%

Erina での攻略を想定。Extra Chapter 以降のエリアは利用せず、ストーリーも進行させない物とする。
実際にテストプレイは行っていないので詰む可能性あり。

### アイテム構成例

#### 正規ルート

|        アイテム         |    %     |                             備考                             |
| :---------------------: | :------: | :----------------------------------------------------------: |
|       Piko Hammer       |   1.00   |                  Bunny Whirl の使用に必須。                  |
|        Air Jump         |   1.00   |                Halloween エリアの通過に必須。                |
|     Sliding Powder      |   1.00   |                 Chapter 3 以降の進行に必須。                 |
|       Bunny Whirl       |   1.00   |                Halloween エリアの通過に必須。                |
|       Carrot Bomb       |   1.00   |              Halloween エリアの通過にほぼ必須。              |
|       Speed Boost       |   1.00   |            Main Game 中でのショップの利用に必須。            |
|     Carrot Shooter      |   1.00   |                 Aruraune を倒すために必須。                  |
| Fire Orb / Super Carrot |   1.00   |           DPS 稼ぎ用。 / 安定 + Carrot Bomb 活用。           |
|      Super Carrot       |   1.00   |      Carrot Bomb の 1.00% の活用と無敵時間の延長目的。       |
|        Health Up        |   0.40   |                     安定 + 端数調整用。                      |
|        Attack Up        |   0.50   | Vanilla 戦前にて強制入手。<br>Chapter 3 まで Attack Up 0個で進行しなければならない。 |
|        **Total**        | **9.90** |                                                              |

#### 非正規ルート

- Carrot Bomb を回収しないため、Main Game 中に Fire Orb を回収する事ができない。
  - Bunny Strike を諦め、代わりに Carrot Bomb を回収するルートの方が簡単な可能性もあり。

|    アイテム    |    %     |                          備考                          |
| :------------: | :------: | :----------------------------------------------------: |
|  Piko Hammer   |   1.00   |                 最も基本的な攻撃手段。                 |
|    Air Jump    |   1.00   |              単体での移動性能は最も高い。              |
| Sliding Powder |   1.00   |              Chapter 3 以降の進行に必須。              |
|  Bunny Strike  |   1.00   | 縦、横ともに飛距離を稼げ、zip も可能な優秀なアイテム。 |
|  Speed Boost   |   1.00   |         Main Game 中でのショップの利用に必須。         |
| Carrot Shooter |   1.00   |              Aruraune を倒すために必須。               |
|    Fire Orb    |   1.00   |                  DPS 、コンボ稼ぎ用。                  |
|   Health Up    |   0.40   |           安定用。Survival に頼るなら不要？            |
|   Attack Up    |   0.50   |                      DPS 稼ぎ用。                      |
|    Pack Up     |   0.67   | AFD では PP が不足するためバッジを満足に装備できない。 |
|  Lucky Seven   |   0.50   |       777 Combo による 7777 ダメージ保証を狙う。       |
|    Survival    |   0.50   |                     一撃死回避用。                     |
|   **Total**    | **9.57** |                                                        |

<br>

## その他

- cromi0256 氏が [AFD+](https://steamcommunity.com/sharedfiles/filedetails/?id=1925884590) と[ AFD- ](https://steamcommunity.com/sharedfiles/filedetails/?id=1929561750)というカスタムマップを公開している。
  - AFD- はブロックのみを追加した AFD モードとして遊ぶことができる。
  - AFD+ は多くの場面で AFD ブロックの再配置が行われていて、別のマップとして遊ぶ事ができる。
  - ver 1.99t 時代に Warp Destination にてマップをロードすると System Interior に飛ぶというバグが存在した影響でオリジナルのマップを上書きして導入する形を取っているが、ver 2.00 現在では通常のカスタムマップ同様の方法で遊ぶ事もできる。

