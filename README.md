# Manga Studio Pro
**AI駆動型日本語漫画制作システム**

Manga Studio Proは、AIが漫画制作の技術的障壁を下げ、クリエイターのイマジネーションを最大化するための統合プラットフォームです。設定を入れるだけで、「それらしい」ドラフトの作成から高品質な出力までをサポートし、特に日本の漫画文化に特化した4コマ〜長編漫画の作成を強力に支援します。

## 🎯 概要 (Overview)
- **コアバリュー**: キャラの一貫性維持、日本語の漫画法則（コマ割・引き・擬音）のAI理解、直感的なエディタ画面。
- **MVPゴール**: **4コマ漫画1本を完成させる**機能の実装。

## 🛠 技術スタック (Tech Stack)

### フロントエンド (Frontend)
- **React** + **TypeScript**
- **Tailwind CSS** (スタイリング)
- **Zustand** (状態管理)
- **Fabric.js / Canvas API** (手描き・オブジェクト編集)

### バックエンド (Backend)
- **FastAPI (Python 3.11)**
- **SQLite** (初期DB)
- **Celery + Redis** (非同期タスク処理)

### AI・API・ライブラリ
- **テキストAI**: Claude API (構成・感情分析・プロンプト最適化)
- **翻訳**: DeepL API Free (日本語→英語プロンプトの変換)
- **画像生成**:
  - *ローカル*: ComfyUI + NoobAI XL / Illustrious XL (高品質本番用)
  - *オプション・外部*: Runware (FLUX Schnell - ドラフト用), Stability AI, NovelAI 等
- **画像・テキスト処理**:
  - `rembg` (背景除去)
  - `Real-ESRGAN` (アニメ系画像拡大)
  - `MediaPipe` (顔・口元検出による吹き出し自動配置)
  - `Pillow` (テキスト画像描画)
  - `halftones` (スクリーントーン生成)

### インフラ・出力
- **ストレージ**: Cloudflare R2
- **エクスポート**: ReportLab / manga2pdf (PDF出力), cbz形式

## 📁 開発状況とドキュメント
詳細な仕様や開発のロードマップについては、以下のドキュメントを参照してください。

- [PROJECT_OVERVIEW.md](./PROJECT_OVERVIEW.md): 全体的な製品仕様書、提供価値、機能要件の一覧
- [roadmap.md](./roadmap.md): 開発フェーズ（Phase 0 〜 Phase 4）、タスクの進捗、API選定の理由
- [API.md](./API.md): 採用した無料・有料APIおよび生成AIモデルの調査結果まとめ
- [CLAUDE.md](./.claude/CLAUDE.md): Claude Code向けの開発ガイドライン・ルール

## 🚀 始め方 (Getting Started)
（※ 現在 Phase 0 の環境構築段階です。開発が進み次第更新します）

1. **フロントエンド環境** `src/` (Vite ＋ React)
2. **バックエンド環境** `server/` (FastAPI)
3. 必要な環境変数 (`.env`) の設定: `ANTHROPIC_API_KEY`, `DEEPL_API_KEY`, etc.
# RingoMyDear
# Shibumon
# Shibumon
# Shibumon
# E-Event
# JohnLennon
