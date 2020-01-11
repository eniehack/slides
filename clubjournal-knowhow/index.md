---
marp: true
title: How to make Dlang, our journal?
description: Hosting Marp slide deck on the web
theme: uncover
class: invert
paginate: true
_paginate: false
---

# <!--fit--> ”D言語”を支える技術



$\LaTeX$とGitLabを用いた技術合同誌制作のノウハウ

Nakaya

![](https://i.creativecommons.org/l/by/4.0/88x31.png)

<!--footer: Copyright &copy; 2019 Nakaya. licensed under by [CC-BY 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.ja), made with [Marp](https://marp.app). -->

----

# このスライドについて

speakerdeckにうpしました




----

# 目次

1. ねらい
1. 用いている技術
1. 部誌頒布まで
1. 使えてない技術
1. 文書フォーマットの話

---

# ねらい

----

* 今回から$\LaTeX$を採用した
    * ノウハウが蓄積されていない
    * 技術が伝承されるように
* みんなに技術同人誌書いてほしい
    * 楽しい

----

# 用いている技術

----

## GitLab
## $\LaTeX$

----

## GitLab

* Gitホスティングサービス
* オープンソース:tada:
* Ruby製
* TODO: Gitの説明？

----

## $\LaTeX$

* 組版システム
* 豊富な拡張機能
* ネット上に大量の知見
* 学会などでは標準
* 今回はpLaTeX-ngを使用

----

# なぜGitLab？

----

* 課金なしでGitHubより豊富な機能
    * privateリポジトリ機能
    * メンバー人数制限etc……

----

# なぜ$\LaTeX$？

----

* 豊富なマクロ（拡張機能）
    * $\LaTeX$でできることを書く
* 部内で習得者が多い
   * E科では2年で
   * J科では3年で
* Gitとの親和性

----

# 部誌頒布まで

----

1. 原稿募集
2. 校正
3. $\LaTeX$に変換

----

# 原稿募集

* Wordなどバイナリデータを禁止
    * Word重い
    * バイナリ嫌い
* テキストデータのみとした
    * MarkdownやLaTeX、Asciidoc、HTMLなど
* markdownが一番集まった

----

# 校正

* GitのBranch,GitLabのMR(PR)を用いた

----

## 校正流れ


* 著者別にブランチを立てる
* ブランチに原稿を追加する
* 校正者が著者ブランチからブランチを作成
    * 同一ブランチでやっていいかも
* 校正
* MR
* 著者がmasterにマージ :tada:

----

# $\LaTeX$へ変換

* pandocを用いた
    * haskell製
    * 文書規格のコンバータ
    * 対応規格が多い

----

# TeX小ワザ

`main.tex`には小ワザがたくさん

参考:『Linuxと$\LaTeX$で技術同人誌を書く本』わかめそば 著,2018年

----

* `\include{}`で他$\TeX$ファイルを読み込み
    * メンテナンス性向上:tada:
* `\frontmatter` 、 `\mainmatter` 、 `\backmatter`
    * 目次や奥付がページ数にカウントされない

----

# 使えてない技術

* GitLab CIで$\LaTeX$の自動コンパイル
* GitLab Release APIを用いた自動リリース

----

# 文書フォーマットの話

----

## 主な文書フォーマット

* LaTeX :thinking:
* Markdown :thinking:
* reStructuredText
* Asciidoc :thumbsup:
* DocBook :tada:
* docx :thumbsdown:
* SATySFi
* Re:View

----

## LaTeX

* 王道of王道
* 技術同人誌でも採用例が多い

----

## Markdown

* 文書書くといったらこれ感はある
* pandocを用いれば可能($\LaTeX$
* 処理系によって方言が存在
    * CommonMark
        * 浸透してない
* 表現力が乏しい
    * 長文を書くのには向かない

----

## reStructuredText

* Pythonのマークアップ言語。
* 表現力はかなりある
* Sphinx,Read the Docsが有名
* HTMlやPDFが吐ける

----

## AsciiDoc

* 表現力高い
* DocBookと互換性あり
* "Pro Git"やオレイリーなど採用事例は多数
* 様々なフォーマットに変換可能
    * HTML
    * DocBook
    * PDF
    * epub
    * $\LaTeX$

----

## DocBook

* XML上の規格
* 国際規格
* オレイリーが開発に携わる
* 商業書で採用実績あり？
* 様々なフォーマットに変換可能
    * HTML
    * PDF
    * TeX

----

## SATySFi

* 国産の組版ソフトウェア
* $\LaTeX$の問題点、エラーの曖昧さの解決を試みる
* OCaml製
* まだ発展途上
* pdfが吐ける

----

## Re:View

* 国産のソフトウェア
* Ruby製
* 様々なフォーマットに変換可能
    * HTML
    * epub
    * PDF($\LaTeX$を介して
* 同人誌での採用事例が多い
    * $\LaTeX$よりかは少ない

----

## その他

* docx(MS Word)
* OpenOffice Writer
* MS OneNote (?
* Adobe InDesign

----

# 部誌(v2019.0.1)リンク
![](https://chart.googleapis.com/chart?chs=250x250&cht=qr&chl=https%3A%2F%2Fnitgc-densan-club.gitlab.io%2F2019-club-journal)
https://nitgc-densan-club.gitlab.io/2019-club-journal

----


いつか群馬高専生が
技術合同誌を技術書典、技術書博覧会に出す日を夢見て……


----

いつか群馬で技術書即売会が開ける日を夢見て……

----

ご清聴ありがとうございました
