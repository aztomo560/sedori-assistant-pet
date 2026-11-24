# せどり助手 — Codex Pet

紺の帽子とエプロン、段ボールとバーコードスキャナーを持った、茶色のたぬきのペットです。Codexデスクトップアプリの作業状況を、表情や動きで見守れます。

**[ペットをダウンロード（ZIP）](https://github.com/aztomo560/sedori-assistant-pet/releases/latest/download/sedori-assistant.zip)**

完成したペットを配布しています。受け取る側で画像生成や作成用Skillを実行する必要はありません。ペット機能に対応したCodexデスクトップアプリが必要です。

## 動きの見本

| 作業中 | 確認待ち | 完了・レビュー | エラー |
| :---: | :---: | :---: | :---: |
| ![スキャナーで調べる](running.gif) | ![こちらの返事を待つ](waiting.gif) | ![荷物を確かめる](review.gif) | ![しょんぼりする](failed.gif) |

このほか、待機・左右移動・あいさつ・ジャンプを含む、9種類・57コマの動きを収録しています。

## Windowsで追加する

1. 上の「ペットをダウンロード」からZIPを保存し、右クリック → **すべて展開** を選びます。
2. **Windows + R** を押し、`%USERPROFILE%\.codex` と入力して開きます。
3. `pets` フォルダーがなければ作成し、展開した **`sedori-assistant` フォルダー**を中にコピーします。
4. Codexの左下のプロフィールアイコン → **設定 → Mini と Pet** を開きます。
5. 「自分のPet」の横にある **更新** を押し、**せどり助手**を選びます。
6. **Alt + Windows + P** でペットを表示します。

配置後は次の構成になります。

```text
%USERPROFILE%\.codex\pets\sedori-assistant\
├── pet.json
└── spritesheet.webp
```

同じ名前のペットが既にある場合は、既存フォルダーを別の場所に保管してから追加してください。`CODEX_HOME` を変更している場合は、その保存先の `pets` フォルダーを使います。

詳しい操作は [INSTALL.txt](INSTALL.txt) にも記載しています。

## 隠す・また表示する

- 隠す：ペットを右クリックして **非表示（Hide）**。
- また表示する：Codexを起動した状態で **Alt + Windows + P**。
- 位置を変える：ペットをマウスでドラッグ。

非表示にしてもペットのファイルは削除されません。設定名やショートカットはアプリのバージョンや個別設定で異なる場合があります。

## 対応範囲と確認状況

状態の判定・切り替え・通知はCodexが行います。このペットが独自に外部アプリやGASを監視する機能はありません。正確な進捗率や残り時間は表示しません。完了後の成果物はチャットで確認してください。

透明背景・画像形式・全57コマ・各状態の動きは検証済みです。作成環境のWindows版アプリへの読み込みと表示を確認しています。ほかのPCやmacOSでの実機確認はしていません。

## ファイル形式

- `pet.json`：名前・説明・画像ファイル名
- `spritesheet.webp`：透明背景、1536 × 1872 px、8列 × 9行
- `*.gif`：動きの見本

OpenAIの画像生成と公式 `hatch-pet` の組立・検証手順を使って制作しました。

- [Codexペットの公式ファイル形式](https://github.com/openai/skills/blob/main/skills/.curated/hatch-pet/references/codex-pet-contract.md)
- [ペット機能の公式ガイド](https://learn.chatgpt.com/docs/pets)
