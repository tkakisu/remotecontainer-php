# remotecontainer-php

VS Code Remote-Containersを利用したPHP開発環境サンプル

## やりたいこと

- PHP用コンテナを使ったPHP開発環境の最小構成を用意する。

## 使用する拡張

- "felixfbecker.php-debug"
- "editorconfig.editorconfig"

EditorConfigの設定は .editorconfig ではなく .vscode/settings.json に記述します。

## 使い方

1. ローカルにリポジトリをclone
2. VS Code上でフォルダを開く
3. コマンドパレットから "Remote-Containers: Reopen in Container" を選択
4. http://localhost:8080/test.php にアクセス
