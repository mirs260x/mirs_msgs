# コメント規約 (mirs_msgs)

AI・第三者が文脈なしで読めることを目的とする。対象は `msg/*.msg`、`srv/*.srv`、`README.md`。

## 1. timeless原則

- 来歴・議論の経緯を書かない。現在の仕様だけ残す。

## 2. 定義ファイルのコメント

- フィールドには単位・意味を1行で書く（例：`# 車輪半径 [m]`）。
- 略語は初出で展開する（例：`rkp # 右比例ゲイン`）。
- 型の使い分け（`float32` vs `float64`）に意図があれば書く。

```rosidl
float64 wheel_radius  # 車輪半径 [m]
float64 rkp           # 右輪Pゲイン
```

## 3. 契約表の維持

- `README.md` の定義表が唯一の真実。定義の追加・削除時は同表を同時に更新する。
- 型・用途・送受信ノードを明記する。

## 4. API文書の生成

```bash
doxygen Doxyfile
```

- 出力は `docs/generated/`（HTML＋XML）。git管理外。静的配置のみで動き、サーバ不要。
- 警告ゼロを維持する（`WARN_AS_ERROR=YES`）。
