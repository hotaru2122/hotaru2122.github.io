---
layout: default
title: ホーム
---

# ホーム

ようこそ！ここはJekyllの機能を試すためのブログです。

## 投稿一覧
以下は最近の投稿です：

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url }}) ({{ post.date | date: "%Y-%m-%d" }})
{% endfor %}

---

## リンク
- [Aboutページ](/about)
- [タグ別投稿一覧](/tags)

---

## Jekyllの機能テスト

### サイト情報
- サイト名: {{ site.title }}
- 説明: {{ site.description }}
- ホストURL: {{ site.url }}

### ページ情報
- ページタイトル: {{ page.title }}
- ファイル名: {{ page.path }}

### 日付フォーマット
現在の日付: {{ "now" | date: "%Y年%m月%d日" }}

### カスタムループ
最近3つの投稿を表示：
{% for post in site.posts limit:3 %}
- {{ post.title }} ({{ post.date | date: "%Y年%m月%d日" }})
{% endfor %}
