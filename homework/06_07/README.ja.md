[繁體中文](./README.md) · [English](./README.en.md) · **日本語**

# ブログシステム - 演習 6

Deno と SQLite で作成したシンプルなブログです。記事を追加・表示できます。

## 機能

- すべての記事を時系列で表示します。
- タイトルと本文を入力して記事を追加できます。
- 公開時刻を自動で記録します。
- 記事を 3 件自動で追加するスクリプトが付属しています。

## 実行方法

### 手順 1：記事を 3 件追加する

次のコマンドでサンプル記事を 3 件追加します。

```
deno run --allow-net --allow-read --allow-write addPosts.js
```

### 手順 2：ブログアプリを起動する

次のコマンドでアプリを起動します。

```
deno run --allow-net --allow-read --allow-write blogApp.js
```

### 手順 3：ブログを開く

ブラウザーで次の URL にアクセスします。

- ホーム：http://localhost:8000
- 記事の新規作成：http://localhost:8000/new

## 使用技術

- **Deno**：JavaScript と TypeScript 向けの安全な実行環境。
- **Oak**：Node.js の Express に似た Deno 向けのミドルウェアフレームワーク。
- **SQLite**：軽量なリレーショナルデータベース。
- **HTML/CSS**：フロントエンドに使用。

## データベース構造

ブログでは `posts` テーブルを使用します。

```sql
CREATE TABLE IF NOT EXISTS posts (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  title TEXT NOT NULL,
  content TEXT NOT NULL,
  created_at TEXT DEFAULT (datetime('now','localtime'))
)
```

## 演習について

演習 6 の「記事を 3 件追加するプログラムを書く」という要件を満たしています。`addPosts.js` を実行すると、タイトルと本文を持つ記事が 3 件作成されます。ウェブ画面から手動で記事を追加することもできます。
