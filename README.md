# Silakka54 ZMK Config（Mac + JIS）

無線 Silakka54（nice!nano / SuperMini 互換 + ZMK）向けの個人設定です。  
MacBook Pro で **キーボード種別=JIS日本語** のまま、かな/英数とJIS記号を使います。

- GitHub: https://github.com/mystkakogawa/silakka54-zmk-config
- ベース: [vandermey/silakka54-zmk-config](https://github.com/vandermey/silakka54-zmk-config)

## ビルド（GitHub Actions）

1. この `zmk-config` フォルダを GitHub リポジトリとして push
2. Actions タブでビルド完了を待つ
3. `firmware` 成果物（zip）をダウンロード

生成される主なファイル:

- `lily58_left-nice_nano_v2-zmk.uf2`
- `lily58_right-nice_nano_v2-zmk.uf2`
- `settings_reset-nice_nano_v2-zmk.uf2`

## 書き込み

1. USB-C で片側を接続
2. リセットを素早く2回 → `NICENANO` ドライブが出る
3. 対応する `.uf2` をコピー（自動で再起動）
4. 反対側も同様

初回やペア異常時は、左右とも先に `settings_reset` を書き込んでから本体UF2を書き込む。

## Mac 接続

- Bluetooth に **Silakka54**（設定名）または Lily58 系の名前で追加
- 接続するのは **左側（マスター）**
- システム設定でキーボード種別が **JIS** であることを確認

詳細はプロジェクトの `docs/` を参照。
