# style2inline

html内のstyle要素をinline化するツール

## 目的
管理者が別のためサイト全体のclassやidの全容が不明であり、それゆえ極力inlineでスタイルを設定するという環境下で、少しでもスタイルの使いまわしをしやすくしたい。

## 処理の流れ
1. htmlファイルを読み込む
2. スタイル要素を解析する
3. 本文の各要素にinlineで適用する
4. htmlファイルを書き出す

## 決めること:形式
目的の処理を使いやすく実行するために、どのような形式にするか
とりあえず以下の二つを当面は両方並行して試してみる
###  vscode extention
編集中のHTMLを直接変換しクリップボードに入れる。
中間ファイルの作成が必要ないため実現できれば使いやすい
Node.jsではないが、javascript自体は職場でも使うので、他の人に引き継いだりもしやすいかもしれない
VSCodeを使っていない人には共有できないのでそこはデメリットか

### 実行ファイル（rust製)
1ファイルにできるので共有はしやすい。
業務では間違いなく使わないので評価にはつながらないし、メンテを引き継いでもらうことも難しい。
単純に個人的にRustに興味があり、モチベーション的にはむしろこっちのほうが高い。
