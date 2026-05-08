# Changelog

## 2026-05-09

### 実行頻度を1日1回に削減

- cron `7 * * * *` (1時間毎) → `0 3 * * *` (毎日12:00 JST)
- 理由: 無意味なAPIコール削減。「興味あり」マーク後の深掘り完了は最大24時間以内になるが、運用上問題なしと判断
- 影響箇所: claude.ai Routine設定 / 本リポジトリREADME / .company/research の各ドキュメント

## 2026-05-05

### 初版

- Notion HP/News記事 DB の「興味あり」記事を1時間毎に深掘り
- 5項目調査（投与経路・研究者プロファイル・自社接点・競合・国内連携）
- ActLab×Daicel の Heat Score（A/B/C）両軸判定
- 両方C はレポート省略（API節約）
- それ以外は子ページに詳細レポート添付
- エンジン: Claude WebSearch / WebFetch（Perplexity APIは不採用）
