# AIへの引き継ぎメモ

> **新しいスレッド・新しい日を始めるとき、まずここを読む。**  
> このファイルを読んだら「引き継ぎメモを確認しました。[最終更新日]時点の状態から続けます。」と一言伝えてください。

---

## 最終更新

**日付:** 2026-06-04  
**更新者:** Claude Code（初期設定）

---

## 現在の作業コンテキスト

### リポジトリ
- **場所:** `my-project/`
- **ブランチ:** `claude/price-tracking-webapp-To6er`
- **リモート:** `charmaru2525-coder/my-project`

### 直近の作業内容
1. **買取価格比較表Webアプリ**（`index.html`）を新規作成
   - GoogleスプレッドシートのCSVアップロードで動くシングルHTMLアプリ
   - 機能: 価格変動一覧 / 店舗比較 / 価格推移グラフ（Chart.js）
2. CSVパースのバグ修正
   - UTF-8 BOM対応
   - 改行コード正規化（`\r\n` / `\r` / `\n`）
   - タブ区切り自動検出
   - `undefined` を `null` に統一（`??` 演算子）

---

## 次回やること

- [ ] ユーザーが実際のCSVをアップロードして動作確認
- [ ] Obsidian Vaultを自分のPCに移す or Obsidian Syncで同期する設定

---

## 重要な決定事項（Decisionsの要約）

| 日付 | 決定内容 |
|---|---|
| 2026-06-04 | VaultをGitリポジトリ内（`my-project/obsidian-memory/`）に作成 |
| 2026-06-04 | WebアプリはシングルHTMLで完結させる（サーバー不要） |
| 2026-06-04 | CSV読み込みはFileReader API（UTF-8）で行う |

---

## 既知の問題・注意点

- このVaultは `/home/user/my-project/obsidian-memory/` にある（クラウド環境）
  - 自分のPCのObsidianで開くには、このフォルダをローカルにコピーする必要がある
- `not JAN` はスプレッドシートの数式エラー文字列。価格列に含まれるが `null` として処理済み

---

## よく使うコマンド

```bash
# ブランチ確認・切替
git branch --show-current
git checkout claude/price-tracking-webapp-To6er

# 変更をプッシュ
git add <file> && git commit -m "..." && git push -u origin claude/price-tracking-webapp-To6er
```

---

## このVaultの読み方

```
obsidian-memory/
├── Projects/   # プロジェクト概要・方針
├── Sessions/   # 日付別の作業ログ
├── Decisions/  # 重要な判断の記録
├── Failures/   # 失敗・ハマり・回避策
└── Reference/  # このファイル + 参照資料
```
