# GitHub Pages 仮公開手順

## 目的

中島屋サイトをまずGitHub Pagesで仮公開し、PC・スマホで表示確認できる状態にする。

この段階では正式公開ではなく、写真差し替え、電話番号・メールアドレス反映、独自ドメイン検討前の確認用とする。

## 前提

リポジトリ：`ridicule8093/nakajimaya-site`

公開対象：`main` ブランチ直下の静的HTML

主要ファイル：

- `index.html`
- `products.html`
- `company.html`
- `assets/css/style.css`

## GitHub Pages 設定手順

1. GitHubで `ridicule8093/nakajimaya-site` を開く
2. 上部メニューの `Settings` を開く
3. 左側メニューの `Pages` を開く
4. `Build and deployment` の `Source` を `Deploy from a branch` にする
5. `Branch` を `main` にする
6. フォルダは `/root` を選ぶ
7. `Save` を押す

数分待つと、GitHub Pagesの公開URLが表示される。

想定URL：

```text
https://ridicule8093.github.io/nakajimaya-site/
```

## 公開後に確認すること

PCとスマホで以下を確認する。

- トップページが表示されるか
- `products.html` へ移動できるか
- `company.html` へ移動できるか
- CSSが反映されているか
- スマホでナビゲーションやカード表示が崩れていないか
- 写真未設定のプレースホルダーが不自然すぎないか
- 問い合わせ欄に未設定の電話番号・メールアドレスが残っていることを認識できるか

## 現段階で未確定のままでよいもの

- 電話番号
- メールアドレス
- 問い合わせフォーム
- 独自ドメイン
- 実写真

## 次にやること

1. GitHub Pagesで仮公開
2. 表示URLをChatGPTに共有
3. PC・スマホ表示の違和感を確認
4. 実写真を最低3枚入れる
5. 電話番号・メールアドレスを反映
6. 独自ドメインを検討
7. 正式公開方法をGitHub Pages継続かCloudflare Pagesへ移行かで判断する

## 注意

このサイトは現在、仮公開確認用の状態。

正式公開前には、問い合わせ情報、写真、Googleビジネスプロフィール、Search Console、独自ドメインを確認する。
