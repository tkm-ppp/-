# **ReadLink**

## サービス概要

<aside>
💡

どんなサービスなのかを３行で説明してください。

</aside>

このアプリは、図書館の蔵書を検索し、現在どこの図書館で本を借りられるか確認を行います。又、本のマルチ検索やGoogle Books APIsを利用し本の情報を調べやすくします。図書館の本の返却日を忘れないように通知機能も実装し図書館の利用を便利にします。

## このサービスへの思い・作りたい理由

<aside>
💡

サービスの題材となるものに関してのエピソードがあれば詳しく教えて。
サービスを思いつくにあたって元となる思いがあれば詳しく教えてください。

</aside>

- 図書館をよく利用するが、借りたい本が住んでる市にはなく隣の市や大学図書館にはあることが複数回あり、今すぐ借りたい時どこで借りられるかすぐに分かれば便利であるのにという思いがあった。
- 自分がよく利用するサービスにGoogle Mapがあるが、あくまで様々な情報を取得できるサービスであるため、図書館の詳細情報を調べやすくしたアプリを作りたいと感じたから。
- リアルタイム蔵書検索機能と本の通知機能を両方備えているアプリを作りたかった。

## サービスの利用イメージ

<aside>
💡

ユーザーがこのサービスをどのように利用、それによってどんな価値を得られるかを簡単に説明してください。

</aside>



- 特定の本をすぐに借りたい時に、どこの図書館ならすぐに借りれるか分かる。
- 全国の図書館についての基本情報が分かる。
- ラインでの通知により、本を返却する期日に気づきやすくなる。

## ユーザー層について

<aside>
💡

決めたユーザー層についてどうしてその層を対象にしたのかそれぞれ理由を教えてください。

</aside>

- 本を買いたくないが今すぐ読みたい本がある人
- 図書館をよく利用する人
- 図書館で借りた本の返却期日を忘れやすい人。

## ユーザーの獲得について

<aside>
💡

想定したユーザー層に対してそれぞれどのようにサービスを届けるのか現状考えていることがあれば教えてください。

</aside>

- Xでの活用、RUNTEQコミュニティでの拡散、友人、知人への紹介

## サービスの差別化ポイント・推しポイント

<aside>
💡

似たようなサービスが存在する場合、そのサービスとの明確な差別化ポイントとその差別化ポイントのどこが優れているのか教えてください。
独自性の強いサービスの場合、このサービスの推しとなるポイントを教えてください。

</aside>

- **図書館の公式サイトからの通知：**公式はメール通知であるが、ラインでの通知にして気づきやすくする。
- **図書館日和：**iPhoneにしか対応していない。
- **カーリル：**現在どこの図書館で本が借りれるかを調べる機能はあるが、登録した図書館からの返却通知機能はない。

## 機能候補

<aside>
💡

現状作ろうと思っている機能、案段階の機能をしっかりと固まっていなくても構わないのでMVPリリース時に作っていたいもの、本リリースまでに作っていたいものをそれぞれ分けて教えてください。

</aside>

### MVP

- ログイン機能
    - メールでログイン
- 全国の図書館検索機能
- 現在どこの図書館で本が借りれるかを調べる機能

### 本リリース

- 図書館検索機能
- googlemapと連携する。
- 図書館レビュー機能
- 返却日時の通知機能
- 本に関するマルチ検索
- タグ機能
- 問い合わせリンク
- ログイン機能
    - LINEでログイン

### 余裕があったら

- ネイティブアプリ化
- 読んだ本登録する機能（タグとして、どの図書館所蔵か）
- 読みたい本を登録する機能

→案　読みたい本登録したらどの図書館にあるかが分かるなら関連性が出来る

- 生成AIによるレコメンド機能

## 機能の実装方針予定

<aside>
💡

一般的なCRUD以外の実装予定の機能についてそれぞれどのようなイメージ(使用するAPIや)で実装する予定なのか現状考えているもので良いので教えて下さい。 

</aside>

| 機能 | 使用する技術 | 具体の使用場面 |
| --- | --- | --- |
| アカウント登録 | Devise |  |
| 地図上への表示/
現在どこの図書館で本が借りれるかを調べる機能 | カーリル図書館API/googlemap api | [rubyで使用できる根拠](https://calil.jp/doc/api.html) |
| 非同期通信/オートコンプリート機能 | Hotwire(Turbo, Stimulus) |  |
| 検索機能 | Runsuck | マルチ検索時 |
| 生成AIによるレコメンド | OpenAI API |  |
| 返却日時の通知機能 | LINE Messaging API |  |
| 本の検索機能 | Google Books APIs |  |

# -

## ■ 画面遷移
https://www.figma.com/design/2QrYPgWgoUxBn6t7itM78d/ReadLink?node-id=0-1&node-type=canvas&t=f9MfXj9rV8qHNNQ4-0