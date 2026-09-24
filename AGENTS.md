# AGENTS.md — mirs_msgs

MIRS共通インターフェース（msg/srv/action）。

## ブランチ運用

- `main` / `develop` 直commit・直push禁止。`feature/*` → `develop` → `main` のPRのみ
- 1コミット1話題。型変更は利用側（ESP32・ROSノード）への影響を確認してから

## ビルド

```bash
colcon build --symlink-install --packages-select mirs_msgs
```
