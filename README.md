# magictrackrest-zmk-config

## githubアカウント準備、zmk-configフォーク

1. https://github.com/　に自分のアカウントでログイン

自分のキーマップや設定はGithubに保存します。
アカウントがなければ作成してください。


2. PersonalAccessTokenを用意

https://github.com/settings/tokens に移動して、PersonalAccessTokenを作成します。

トークン作成時に、"workflow" にチェックをつけてください。（この権限がないとファームウエアのビルドはできません）

3. 自分のアカウントでgithubにログインしたまま、https://github.com/mentako-ya/magictrackrest-zmk-config　（このページ）を開きます。

４. 画面右上の「Fork」メニューから「+ Create a new fork」を選択

作成されるフォークが　自分のアカウント/magictrackrest-zmk-config　であることを確認して Create fork を押下します。

５。自分のGithubリポジトリに移動し、「magictrackrest-zmk-config」がフォークされたことを確認します。

画面上部の[Actions]をクリック。利用許諾のメッセージが表示されていれば、許諾します。


## ファームウェアビルド

１. ファームウェアビルド

画面左側　Actioｓ　の中から.github/workflows/build.ymlをクリックして画面遷移

画面右側　RunWorkflow　のボタンをクリックするとファームウェアのビルドが開始すします。（２回目以降は変更をコミットすると、自動的にビルドされます）

2. ファームウェアダウンロード

生成された firmware.zipをダウンロードして解凍します。
* mtr-seeeduino_xiao_ble-zmk.uf2 　　　　　　　　　　　　　　　　　　　　　　　　　＜　ZMKファームウェア
* settings_reset-seeeduino_xiao_ble-zmk.uf2　　　　＜　ファームウェアリセット用


## キーマップ修正　

フォークしたリポジトリの mtr.keymap を修正します。
修正したファイルをコミットすると、自動的にファームウェアが自動でビルドされます。

キーコードについてはZMKのドキュメントを参照してください。
https://zmk.dev/docs/codes
