# sketch plugin hellworld oldschool

Helloworld, old school style.

This is a playground plugin for learning how to integrate the Sketch plugin update system with old school plugins (that written with cocoascript).

# Why?
Sketch ver.45以前向けに作らたプラグインをプラグイン更新通知に対応させ、できるだけ新しいプラグインを使ってもらいたい。
- https://sketchplugins.com/d/229-updating-plugins
- https://developer.sketchapp.com/guides/publishing-plugins/

# 試したこと
- ステップ1(v0.0.1)
  - 既存pluginを参考に、cocoascriptで最低限のコードを書く
  - githubにpush
  - releaseタグ設定、zipをダウンロードし、sketchにインストール、動作確認
    - zip登録: helloworld-oldschool.sketchpluginをzipし、Release > Edit tagからアップロード(Attach binaries by dropping them here or selecting them)する
    - ダウンロードしたzipを解凍し、helloworld-oldschool.sketchpluginをsketchで開くとプラグインインストール完了画面が表示される。
    - Sketch の Plugins > helloworld Plugin > my-command を実行するとスクリプトが実行されアラートが表示される。
- ステップ2(v0.0.2)
  - pluginバージョンを上げる
    - アラート文言変更
    - manifest.json, appcast.xmlも
  - githubに反映
  - sketch再起動、プラグイン更新が通知されるはず
    => されなかった

おそらく、Sketch起動時に https://github.com/sketchplugins/plugin-directory と同等の内容をチェックしてるのではないかと思われる。正式に登録されたプラグインでないと更新の動作を確認できなさそう。

# 参考
- https://github.com/einancunlu/Checkpoints-Plugin-for-Sketch
- https://github.com/sketchplugins/plugin-directory
