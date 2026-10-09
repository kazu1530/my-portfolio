# my-portfolio

# Journal App

「紙と墨」の質感とミニマリズムを意識したWebジャーナル（ブログ・日記）アプリケーションです。
AI（LLM）と対話しながら設計・実装を行いました。

## 画面イメージ / デモ
- デモURL:https://kazu1530.github.io/journal.html

## 主な機能
- **記事の投稿・削除機能**: タイトルと本文を入力してリアルタイムにDOM生成
- **記事のインライン編集**: 編集ボタンを押すと入力フォームに切り替わり、内容を更新可能
- **データの永続化**: `localStorage` を使用し、ブラウザを閉じても記事データを保持
- **ユニークID管理**: `Date.now()` を活用したID管理による正確な記事更新・削除処理
- **レスポンシブデザイン**: メディアクエリを用いたCSS設計

## 技術スタック
- **HTML5**
- **CSS3** (CSS Custom Properties, Google Fonts, Flexbox)
- **JavaScript (ES6+)** (DOM Manipulation, LocalStorage API)

## 工夫した点・技術的なこだわり
1. **デザインシステム**: 
   - `--bg: #f6f4ef` (紙の色)、`--ink: #1d1d1b` (墨の色) などの変数を定義し、和モダンで洗練された世界観を構築。
   - 明朝体（Shippori Mincho）とゴシック体を組み合わせた視認性の高いタイポグラフィ。
2. **JavaScriptでの状態管理**:
   - 記事ごとにタイムスタンプに基づくユニークID (`id: Date.now()`) を割り振り、`localStorage` 上の配列操作（`map` / `filter`）とDOMを正確に同期。
   - 編集モード切り替え時に `replaceWith` を使用したスムーズなUI遷移。

## AI活用について
- 要件定義やHTML/CSSのスタイリング構築、およびJavaScriptでの `localStorage` 連携ロジックの設計においてAIツールを活用。
- コードの挙動やDOM操作の仕組み（イベントリスナー、配列メソッド等）を自ら分析・理解した上で実装を完了しています。
