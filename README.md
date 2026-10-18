# mirs platform ROS 2 Interfaces

mirsで使用するROS 2メッセージ・サービス定義。

| 定義 | 種別 | 用途 |
|---|---|---|
| `msg/BasicParam` | msg | 車体・PIDパラメータ（`/params`） |
| `srv/BasicCommand` | srv | 4パラメータ汎用コマンド（`/esp_cmd`） |
| `srv/ParameterUpdate` | srv | `BasicParam` と同形のパラメータ更新 |
| `srv/SimpleCommand` | srv | 空リクエストの単純コマンド（`/reboot`, `/reset_encoder`） |
