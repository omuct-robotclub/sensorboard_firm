# センサー基板ファームウェア

## 通信プロトコル
このファームウェアは、CANIDを2つ用いて通信を行う。
[platformio.ini](platformio.ini)で`CAN_ID_1_DEF`と`CAN_ID_2_DEF`を設定すことで変更できる。

## CANフレーム

CAN_ID_1
| 0..4 bytes | 5 | 6..7 |
| ---------- | - | ---- |
| タイムスタンプ[μs] | リミットスイッチ 1..5 | エンコーダー 1 |

<br>

CAN_ID_2
| 0..1 bytes | 2..3 | 4..5 | 6..7 |
| ---------- | ---- | ---- | ---- |
| エンコーダー 2 | エンコーダー 3 | エンコーダー 4 | エンコーダー 5 |
