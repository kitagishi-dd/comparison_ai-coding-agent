---
marp: true
theme: default
paginate: true
style: |
  section {
    font-family: 'Hiragino Sans', 'Meiryo', 'Yu Gothic', sans-serif;
    font-size: 18px;
    padding: 40px 50px 30px;
    background: #ffffff;
    color: #1e293b;
  }
  h1 {
    background: #1e293b;
    color: #f1f5f9;
    font-size: 26px;
    padding: 14px 50px;
    margin: -40px -50px 20px;
    line-height: 1.35;
    border: none;
  }
  h2 {
    font-size: 17px;
    color: #1e293b;
    border-bottom: 2px solid #e2e8f0;
    padding-bottom: 4px;
    margin: 14px 0 8px;
  }
  h3 {
    font-size: 13px;
    color: #475569;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    margin: 10px 0 6px;
  }
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
    margin: 8px 0;
  }
  th {
    background: #334155;
    color: #e2e8f0;
    padding: 7px 10px;
    font-size: 12px;
    font-weight: 600;
    text-align: left;
  }
  td {
    padding: 6px 10px;
    font-size: 13px;
    vertical-align: top;
    border-bottom: 1px solid #e9eef4;
    line-height: 1.55;
  }
  tr:nth-child(even) td { background: #f8fafc; }
  blockquote {
    background: #eff6ff;
    border-left: 4px solid #3b82f6;
    padding: 8px 14px;
    margin: 10px 0;
    font-size: 13px;
    color: #1e3a5f;
    border-radius: 0 4px 4px 0;
  }
  blockquote p { color: #1e3a5f; margin: 0; }
  pre {
    background: #f8fafc;
    border: 1px solid #e2e8f0;
    border-radius: 6px;
    padding: 14px 16px;
    font-size: 12px;
    line-height: 1.85;
    color: #1e293b;
  }
  code { background: #f1f5f9; color: #1e293b; padding: 1px 4px; border-radius: 3px; font-size: 12px; }
  ul { font-size: 14px; padding-left: 18px; }
  li { margin: 4px 0; line-height: 1.55; color: #374151; }
  li strong { color: #1e293b; }
  strong { color: #1e293b; }
  p { font-size: 13px; line-height: 1.7; color: #374151; margin: 6px 0; }
  section.title {
    background: linear-gradient(135deg, #0f172a 0%, #1e3a5f 60%, #0f2946 100%);
    color: #f1f5f9;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  section.title h1 {
    background: none;
    color: #f1f5f9;
    font-size: 38px;
    margin: 0 0 10px;
    padding: 0;
    border-bottom: 2px solid #475569;
    padding-bottom: 14px;
    text-align: center;
  }
  section.title h2 {
    background: none;
    color: #94a3b8;
    font-size: 18px;
    border: none;
    margin: 8px 0;
    padding: 0;
    text-align: center;
  }
  section.title p { color: #64748b; text-align: center; }
  section.toc h1 { font-size: 26px; }
---

<!-- _class: title -->
<!-- _paginate: false -->

# AIコーディングツール比較 2026

## Claude Code　／　OpenAI Codex　／　Google Antigravity

<br>

社内DX・内製開発担当者向け｜2026年4月時点

---

<!-- _class: toc -->

# 目次

| # | スライド |
|---|---|
| 1 | AIコーディングツールとは |
| 2 | 3ツール一覧・位置付け |
| 3 | 【重要】自律度とインタラクションモデル |
| 4 | OpenAI Codex 詳細 |
| 5 | Claude Code 詳細 |
| 6 | Google Antigravity 詳細 |
| 7 | 機能比較マトリクス |
| 8 | データプライバシー・セキュリティ |
| 9 | 料金・制限比較 |
| 10 | 評判・採用状況 |
| 11 | どのツールを選ぶか |
| 12 | まとめ |

---

# 1｜AIコーディングツールとは

## 旧世代との違い

| | 旧世代（GitHub Copilot 初期など） | 現世代（本資料の3ツール） |
|---|---|---|
| できること | カーソル位置の補完（入力補助） | タスクを与えると自律的に計画・実行・検証 |
| 関与スタイル | 一緒に書く | 任せて確認する |
| 呼び方 | コード補完ツール | **コーディングエージェント** |

## エージェントが共通してできること

| カテゴリ | 具体的な機能 |
|---|---|
| コード生成 | 自然言語の指示からコードを書く、既存コードの続きを補完する |
| コードベース理解 | リポジトリ全体を読んで構造・依存関係を把握した上で提案する |
| バグ修正 | エラーログや症状から原因を特定し、修正コードを適用する |
| リファクタリング | 複数ファイルにまたがる変更を一括で実施する |
| テスト生成 | ユニットテスト・統合テストの雛形を自動生成する |
| ターミナル操作 | コマンド実行・git操作・ビルドをエージェントが代行する |
| PR作成 | 変更内容をまとめてプルリクエストの草稿を作る |

> **3ツールはすべてエージェント。ただし「どう動くか」が根本的に異なる**

---

# 2｜3ツール一覧・位置付け

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 開発元 | Anthropic | OpenAI | Google |
| 登場時期 | 2025年2月 | 2025年5月（刷新） | 2025年11月 |
| 形態 | CLIツール（ローカル） | CLIツール＋クラウド | 専用IDE（VSCode系） |
| 基盤モデル | Claude Sonnet/Opus 4.6 | GPT-5.4-Codex | Gemini 3.1 Pro/Flash（他も選択可） |
| インライン補完 | なし | なし | **あり**（IDE統合） |
| 動作方式 | 同期・ローカル実行 | 非同期・クラウド実行 | 同期＋非同期の両方 |
| 一言でいうと | コードを熟知した職人と一緒に作る | 仕事を投げると後でPRが届く | モデルを選べる全部入りの工場 |

---

# 3｜【重要】自律度とインタラクションモデル

> ツール選びの核心。3ツールの「働き方」は根本的に異なる。

## インタラクションモデルの違い

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| モード | 同期・対話型 | 非同期・自律型 | **両方**（ビューで切替） |
| 関与タイミング | 都度確認しながら進む | 最後にPRをレビュー | 設定次第 |
| 向いている作業 | 考えながら進める改修・調査・設計 | 仕様が決まっている実装・バグ修正 | 並列で複数タスクを流す |
| 感覚的なたとえ | ペアプログラミング | タスク発注→納品 | プロジェクト管理＋実行 |

## 変更の承認フロー

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 確認タイミング | 変更前に都度確認（デフォルト） | 最後にPRをレビュー | エージェントごとに設定可能 |
| 安全性の思想 | 慎重・インタラクティブ | サンドボックス隔離で安全 | 柔軟 |
| 本番コードへの直接操作 | あり（確認後） | なし（クラウド内で完結） | あり（設定次第） |

---

# 4｜OpenAI Codex 詳細

クラウドサンドボックス上で動作。PRを作って返す**非同期スタイル**が最大の特徴。ChatGPT Plus（$20/月）に同梱。週間アクティブユーザー200万人超（2026年3月時点）。

| 強み ✅ | 弱み ⚠️ |
|---|---|
| バックグラウンド並列実行（待ち時間なし） | ローカルファイルへの直接アクセス不可 |
| PR生成まで自動（GitHubフローに乗る） | インライン補完なし（エージェント専用） |
| 別エージェントによるコードレビュー機能 | エンタープライズ機能がClaude Codeより薄い |
| Webアクセス・MCP対応 | 業務利用率がまだ低い（2026年1月時点で3%） |
| セキュリティエージェント（2026年3月〜） | |

## こんなチームに向く

| 特性 | 理由 |
|---|---|
| GitHub中心のワークフローが整っている | PR生成・並列エージェントがそのまま活かせる |
| 仕様が固まったタスクを大量処理したい | バックグラウンド並列実行が真価を発揮 |
| すでにChatGPT Plusを使っている | 追加コストゼロで始められる |

---

# 5｜Claude Code 詳細

ターミナルから使うエージェント。**ローカルのコードベースに直接アクセス**し、変更〜テスト〜コミットを一気通貫で行う。年間換算売上25億ドル規模と3ツール中最も市場に浸透。

| 強み ✅ | 弱み ⚠️ |
|---|---|
| コードベース全体の理解が最強クラス | ターミナル習熟が必要（GUIなし） |
| 意図の解釈精度が業界最高評価 | インライン補完なし（エージェント専用） |
| ローカル完結（外部クラウド不要） | 並列エージェント実行が苦手 |
| **CLAUDE.md**でプロジェクト設定をgit管理・チーム共有 | 料金体系が複雑・値上げ懸念あり |
| SSO・SCIM・監査ログ・HIPAA対応 | |
| Bedrock/Vertex/Foundry経由で閉域対応可 | |

## CLAUDE.md とは

| 項目 | 内容 |
|---|---|
| 何か | リポジトリのルートに置くMarkdownファイル |
| 書けること | 設計方針・命名規則・触ってはいけないファイル・背景知識 |
| チーム共有 | gitで管理できるので全員が同じコンテキストを持てる |
| 他ツールとの差 | Codexはシステムプロンプト（組織単位）、Antigravityは未整備 |

---

# 6｜Google Antigravity 詳細

Googleが2025年11月にGemini 3と同時発表した**エージェントファーストIDE**。VSCodeフォーク。2つのビューが特徴。無料枠あり。

## 2つのビュー

| ビュー | 特徴 | 向いている場面 |
|---|---|---|
| **エディタビュー** | VSCode/Cursor感覚。インライン補完＋サイドバーエージェント | 日常的なコーディング |
| **マネージャービュー** | 複数エージェントを並列起動・監視・管理 | 複数タスクの非同期処理 |

## 選択できるモデル

| モデル | 特徴 | 向いている用途 |
|---|---|---|
| Gemini 3.1 Pro | コンテキスト長が業界最大級（約100万トークン） | 大規模コードベース・複雑な設計 |
| Gemini 3 Flash | 高速・低コスト | 単純なタスク・量産作業 |
| Claude Sonnet/Opus 4.6 | コード理解・意図把握の精度が高い | 複雑な改修・品質重視の実装 |
| GPT-OSS-120B | オープンソース系 | コスト抑制・検証用途 |

> ⚠️ 注意：Googleへの継続性リスク（サービス終了実績）・クォータ削減の不透明な課金体系が課題

---

# 7｜機能比較マトリクス

| 観点 | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| インタラクションモデル | 同期・対話型 | 非同期・自律型 | 両方 |
| インライン補完 | ✗ | ✗ | ✓ |
| コードベース理解 | ◎ ローカル全体を深く | △ クラウド上のみ | ○ IDE統合で把握 |
| 並列エージェント実行 | △ 基本は1対1 | ◎ バックグラウンド並列 | ◎ マネージャービュー |
| ローカルファイル直接操作 | ◎ | ✗ | ◎（IDE内） |
| 変更前の承認確認 | ◎ 都度確認（デフォルト） | ○ PR経由で最後に | △ 設定次第 |
| 自然言語→意図の理解 | ◎ 業界最高評価 | ○ | ○ |
| プロジェクト設定共有 | ◎ CLAUDE.md（git管理可） | △ 組織単位のみ | △ 未整備 |
| モデル選択の自由度 | ✗ Claudeのみ | ✗ GPT系のみ | ◎ Gemini・Claude・GPT-OSS |
| コンテキスト長 | ○ 約200Kトークン | ○ 同等規模 | ◎ 約100万トークン |
| PR/Gitワークフロー統合 | ◎ | ◎ | ○ |
| 既存エディタとの共存 | ◎ エディタ非依存 | ◎ エディタ非依存 | △ IDEごと移行が前提 |
| エンタープライズ機能 | ◎ SSO・SCIM・HIPAA等 | ○ | △ 未整備 |
| ベンダーロックイン（モデル） | あり（Claude固定） | あり（GPT固定） | なし（モデル選択可） |
| ベンダーロックイン（継続性） | 低リスク | 低リスク | 高リスク（終了実績あり） |

---

# 8｜データプライバシー・セキュリティ

> 内製開発チームにとって「自社コードをどこに送るか」は**導入可否を左右する**

## コードの外部送信先と学習利用

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 処理場所 | Anthropicサーバー | OpenAIクラウド（サンドボックス） | Googleクラウド |
| 学習への利用 | オプトアウト可 | オプトアウト可 | 要確認 |
| データ保持期間 | 設定により異なる | 設定により異なる | 不透明 |

## オンプレ・閉域対応・企業向け機能

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| オンプレ・閉域対応 | △ Bedrock/Vertex/Foundry経由で可 | ✗ 不可 | △ GCP Enterprise（未整備） |
| セキュリティ認証（HIPAA等） | ◎ | ○ | △ 未整備 |
| SSO / SCIM / 監査ログ | ◎ | ○ | △ |

## 結論

| 状況 | 推奨 |
|---|---|
| コードを社外に出せない・コンプライアンス要件が厳しい | **Claude Code + Bedrock/Vertex** が現時点で唯一の現実解 |
| ある程度許容できる・スタートアップ | どのツールも可（学習利用オプトアウトを確認すること） |

---

# 9｜料金・制限比較

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 無料枠 | なし | 制限付き（ChatGPT無料プラン内） | **あり**（週上限・5時間ごとリセット） |
| 個人スタンダード | $20/月（Proプラン） | $20/月（ChatGPT Plus同梱） | $20/月（AI Pro） |
| 個人ヘビー | Max $100〜$200/月 | ChatGPT Pro $200/月 | AI Ultra $249.99/月 |
| チーム | $100/人/月（Premium席・最低5席） | $25/人/月〜（ChatGPT Team） | GCP Enterprise（価格非公開） |
| API従量課金 | Haiku $1/$5・Sonnet $3/$15・Opus $5/$25（/1Mトークン） | あり（トークン課金） | クレジット制（換算率非公開） |

## 注意点と目安

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 直近の問題 | 2026年4月に一時$100/月プランのみへ変更→撤回 | ヘビー利用時は追加課金の可能性 | 2026年3月にクォータ大幅削減→批判 |
| まず試したい | ― | ChatGPT Plus持ちなら追加費用ゼロ | **無料枠あり（クレカ不要）** |

---

# 10｜評判・採用状況

## 利用率（2026年1月 JetBrains開発者調査）

| ツール | 業務利用率 | 備考 |
|---|---|---|
| **Claude Code** | 推定高 | 年換算売上$25億規模。3ツール中最も浸透 |
| **Google Antigravity** | 6% | 2025年11月発表から急速に認知拡大 |
| **OpenAI Codex** | 3% | 認知率27%に対して実利用が低い |

## コミュニティの声

| 観点 | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 好評な点 | コードベース理解が断トツ・意図を汲んだ提案 | 並列実行が便利・PR完成品で返ってくる | マネージャービューが唯一無二・Flashが速い |
| 不評な点 | CLIだけでとっつきにくい | 業務でガンガン使っている人が少ない | いつ終了するか心配・クォータ不透明 |
| 特徴的な声 | $100プラン騒動は不安だった | GPT-5.4で精度が大幅に上がった | 結局Claude Sonnetを選ぶことになる |

> **第三者評価（XDA Developers 実機比較）：** 「3ツールを同じアプリ開発に使って比較した結果、使い続ける価値があると感じたのは1つだけだった」（Claude Codeを最高評価）

---

# 11｜どのツールを選ぶか（判断フロー）

```
STEP 1：セキュリティ・コンプライアンス要件はあるか？
  ├─ 厳しい（コードを社外に出せない）
  │    → Claude Code + Bedrock/Vertex 一択
  └─ 許容できる → STEP 2へ

STEP 2：既存エディタから動かせないか？
  ├─ 動かせない（JetBrains等から変えられない）
  │    → Claude Code または Codex（エディタ非依存のCLI）
  └─ IDEごと移行OK → STEP 3へ

STEP 3：どんな開発スタイルか？
  ├─ 既存の複雑なコードへの改修・調査が中心 → Claude Code
  ├─ 仕様が固まったタスクを大量並列処理したい → Codex
  ├─ 複数プロジェクトを同時に回したい → Antigravity
  └─ まず無料で試したい → Antigravity無料枠 → Claude Code Pro
```

## プロジェクト・チーム特性別まとめ

| 特性 | 推奨 | 理由 |
|---|---|---|
| 大規模既存システムの改修 | **Claude Code** | コードベース全体理解が最強 |
| 新規プロダクト（スクラッチ・仕様探索） | **Codex** or **Antigravity** | 並列実行で量産・探索しやすい |
| セキュリティ・コンプライアンス重視 | **Claude Code** | 唯一HIPAA等の認証が整備済み |
| モデルを固定したくない | **Antigravity** | 唯一モデル層を分離できる |
| JetBrainsユーザーが多い | **Claude Code** or **Codex** | エディタ非依存のCLI |
| チームへの設定共有が重要 | **Claude Code** | CLAUDE.mdがgit管理でき設定を共有できる |

---

# 12｜まとめ

## 3ツールの特徴

| | **Claude Code** | **OpenAI Codex** | **Google Antigravity** |
|---|---|---|---|
| 一言まとめ | コードを深く理解する職人 | 仕事を投げると後でPRが届く | モデルを選べる全部入りの工場 |
| 最大の強み | 精度・安全性・企業機能が最も整備済み | GitHub連携・非同期並列処理 | モデル選択の柔軟性・マルチエージェント管理 |
| 最大の弱み | CLIのみ・並列処理が苦手 | ローカル操作不可・業務利用率が低い | 新しさゆえの不安定さ・継続性リスク |

## 2026年4月時点の結論

| 状況 | 結論 |
|---|---|
| 迷ったらどれか | **Claude Code**（実績・精度・企業機能のバランスが現時点で最良） |
| 無料で試したい | **Antigravity**（週制限ありだが無料） |
| すでにChatGPT Plus持ち | **Codex**（追加費用ゼロ） |
| モデルを縛られたくない | **Antigravity**（Gemini・Claude・GPT-OSSを使い分け） |
| 全部試してから決めたい | Antigravity無料枠 → Codex($20) → Claude Code($20) の順 |

> **今後の注目点：** Antigravityの成熟度・Codexの業務利用率拡大・Claude Codeの料金安定性・MCP対応の深化

---

<!-- _class: toc -->

# 付録｜用語集

| 用語 | 説明 |
|---|---|
| エージェント | 指示を受けて自律的に計画・実行・検証を繰り返すAI |
| インライン補完 | コードを書いている最中にリアルタイムで候補を提示する機能 |
| 同期型 | 開発者とエージェントが対話しながらリアルタイムで進める方式 |
| 非同期型 | タスクを投げておき、後でPR等の成果を受け取る方式 |
| CLI | コマンドラインインターフェース。ターミナルから操作するツール |
| MCP | Model Context Protocol。AIエージェントが外部ツールと連携する標準規格 |
| CLAUDE.md | Claude Codeのプロジェクト設定ファイル。リポジトリに置いてgit管理できる |
| クラウドサンドボックス | AIが安全に実行できるクラウド上の隔離環境 |
| コンテキスト長 | AIが一度に処理できる情報量。長いほど大きなコードベースを一括処理できる |
| SSO | シングルサインオン。企業の認証基盤との統合 |
| SCIM | ユーザー管理の自動化（入退社・権限変更の自動同期） |
| ベンダーロックイン | 特定のサービス・企業に依存し、乗り換えが困難になること |
