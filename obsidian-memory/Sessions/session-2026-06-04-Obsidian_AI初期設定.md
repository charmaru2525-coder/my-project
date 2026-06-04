# セッションログ: Obsidian AI長期記憶 初期設定

**日付:** 2026-06-04  
**目的:** ObsidianをAI作業の長期記憶として運用するための初期設定  
**ステータス:** 完了

---

## やったこと

- `obsidian-memory/` をVaultとして新規作成（`my-project` 内）
- フォルダ構成を作成: `Projects` / `Sessions` / `Decisions` / `Failures` / `Reference`
- 初期ノート3点を作成
  - `Sessions/session-2026-06-04-Obsidian_AI初期設定.md`（このファイル）
  - `Projects/AI作業メモリ運用.md`
  - `Reference/AIへの引き継ぎメモ.md`

## 決定したこと

- VaultはGitリポジトリ（`my-project`）内に置く形を選択
- Obsidianで「フォルダを開く」から `obsidian-memory/` を指定すれば読み込み可能

## 次回やること

- [ ] Obsidian側でこのVaultを開いて表示確認
- [ ] 必要であれば Obsidian Sync または iCloud/Dropbox 等による同期設定を追加
- [ ] `Reference/AIへの引き継ぎメモ.md` を実際の作業内容に合わせて更新

## メモ・気づき

- `obsidian-memory/` は `my-project` リポジトリの一部。`.gitignore` でVaultごと除外するか、ノートもGit管理するか決めておくと良い。
