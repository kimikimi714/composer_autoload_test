# composer_autoload_test
phpのcomposerでautoloaderを作ってみるテスト

一応このリポジトリにあるapp.phpを実行すると以下の結果が得られるはずです。

```
$ php app.php
string(5) "hello"
```

本来はvendorとかはコミットしないものですが、これはテストも兼ねているのでまるっと上げてます。  

# composerでautoloadを作るざっくり手順

1. composer.jsonをとりあえず用意する(読み込みたいパッケージの有無は問わない)
2. autoloaderを生成したいディレクトリなりファイルなりをPSR-4準拠で作成
3. composer.jsonに"autoload"の項目を追加(追加の仕方はこのリポジトリとディレクトリ構成から察してください)
4. php composer.phar install(globalにインストールしてるならcomposer installでおk)

# とても参考になったリンク

[ComposerでPSR-4仕様のオートロードを設定する](http://tec-blog.beaglee.com/?p=406)
