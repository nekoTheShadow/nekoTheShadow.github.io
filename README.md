__★★注意★★__

このブランチは以下のレポジトリに移行しました。アーカイブ目的として、ブランチの削除は実施しません。
- レポジトリ: https://github.com/nekoTheShadow/nekoTheShadow.github.io.admin
- ブランチ: master
上記のレポジトリではGitHub Actionsを利用し、自動ビルド・デプロイを行います。


__ブランチ一覧__

- `admin`: ビルド前のモジュールを格納する。
- `master`: 静的サイトとして公開する内容を格納する。`admin`の内容を`hugo`により`build`したときに作成される`public`ディレクトリが実体。


__作業手順メモ__

1. clone
    1. `git clone --recursive -b admin https://github.com/nekoTheShadow/nekoTheShadow.github.io.git`
    2. `mkdir -vp nekoTheShadow.github.io/public`
    3. `git clone -b master https://github.com/nekoTheShadow/nekoTheShadow.github.io.git nekoTheShadow.github.io/public`
2. `admin`: 所定の修正を行う。
    - 挙動確認: `hugo server`
3. build
    - `hugo`
4. `admin`: add & commit & push
    1. `cd nekoTheShadow.github.io`
    2. `git add -A`
    3. `git commit -m ${message}`
    4. `git push origin admin`
5. `master`: add & commit & push
    1. `cd public`
    2. `git add -A`
    3. `git commit -m ${message}`
    4. `git push origin master`


