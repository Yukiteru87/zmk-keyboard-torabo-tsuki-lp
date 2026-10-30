
[torabo-tsuki LP](https://github.com/sekigon-gonnoc/torabo-tsuki-lp)用のZMKファームウェア

* _centralがついているuf2をトラックボールがついている方に、_peripheralを反対側に書き込んでください
* キーマップはkeymap-editorおよびzmk-studioで編集できます
## DYA Studio 対応 (dya-studio ブランチ)

[DYA Studio](https://studio.dya.cormoran.works/) から、ビルドし直さずにトラックボールの設定を変更できます。

* ZMK は cormoran さんの fork (`v0.3-branch+dya`)。DYA Studio 用モジュールは ZMK v0.3 に対応する最後のコミットに固定
* 初回は左右とも `settings_reset` → 通常ファームの順に書き込み、Bluetooth を再ペアリング

| 機能 | 初期設定 (`config/keymap.keymap`) |
|---|---|
| オートマウスレイヤー | ボールを動かすと layer 1 (MOUSE)。キー入力後200msは発動しない / 停止後800msで解除 |
| スクロール | MOUSE レイヤーの S / L を押している間ボールがスクロール (layer 4、速度 1/8) |
| 精密モード | MOUSE レイヤーの A を押している間ポインタ速度 1/2 |
| クリック中のAML維持 | MOUSE レイヤーの &trans 以外のキー(クリック等)と修飾キーではAMLが解除されない |

速度・待ち時間・反転・回転・スクロール方向は DYA Studio の Input Processor 画面で変更・保存できます。
ミニトラックパッド(スクロール専用)はこれまでどおり動作します。
