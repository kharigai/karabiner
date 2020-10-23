## karabiner

### simple modify
form to 
caps_lock -> escap
fn -> left_ctrl

### complex
Esc send
control w
chrom settign

# [Mac] MBP 初期セットアップ

# 環境

- H/W: MacBook Pro (13-inch, 2017)  
- OS: macOS High Sierra 10.13.6

# 資料

- [MacBook Pro (13-inch, 2017, Thunderbolt 3ポートx 2) - 技術仕様](https://support.apple.com/kb/SP754?locale=ja_JP)  

# システム環境設定

[Mac] MBP システム環境設定 を参照

# general

[Mac] MBP general setting を 参照

# アプリケーションインストール

## index

- [x] chrome dmg
- [x] spark AppStore 
- [x] slack AppStore
- [x] quiver AppStore
- [x] google日本語入力 dmg
- [x] bettertouch tool dmg
- [ ] alfred dmg
- [ ] karabiner dmg
- [ ] tweetbot
- [ ] anytrans
- [x] macVim

## chrom

[[Chrome] 設定、使用法](quiver-note-url/171F7618-8EA8-4B7C-AA87-3ACC9E6EFB57)

## quiver

[[Quiver] 設定、使用方法](quiver-note-url/DB88159E-FC6B-4CAB-AA08-BC35DCBEFB99)

### bettertouch tool

- [BetterTouchTool 公式サイト](https://folivora.ai/) より zip ファイルをダウンロード
- BetterTouchTool2.app をアプリケーションフォルダに移動
- 設定
  - Advanced設定 Windows Snapping TAB を開く
  - Left width: 59%, Right width: 41%
  
### google 日本語入力

google 日本語入力をインストールした状態で、ことえりを削除する。  
入力ソースを「google 日本語入力」のみにする場合、ことえりのみを削除することはできない。  
[Macの「ことえり」を削除する方法](https://hacknote.jp/archives/10031/)

### alfred

[[Alfred] 設定、使用方法 ](quiver-note-url/AF2F7C1A-DCB1-498B-90B2-BFF4F5462D8E)

### karabiner

[karabiner] 設定、使用方法 参照

### macvim

[MacVim]設定、使用方法 参照

### 1password

v7 からデフォルトでサブスクリプションでの購入となった。  
スタンドアロン（買い切り版）を購入した場合、複数のデバイスでの同期に制限がある模様。  
[1Passwordを違うデバイスで同期する方法(Mac、Windows、iPhone、Android)。買い切り、サブスクリプション共に解説。](https://www.tentecomai.com/entry/1Password-synchronization)


# [Mac] MBP システム環境設定 

## トラックパッド

スクロールとズーム
- [ ] スクロールの方向: ナチュラル(設定変更 on -> off)
- それ以外はデフォルト

## キーボード

- [x] F1, F2などのキーを標準のファンクションキーとして使用(off -> on)  
  F7でカタカナ変換が有効になる
- それ以外はデフォルト

修飾キーボタン(Karabiner VertualHDKeyboard も設定可能)
- Caps Lock: Esc
- Control: そのまま
- Option: そのまま
- Command: そのまま
- fn: Control

注意: 上記の設定を行ってもCaps Lock, fn のキーバインドは変更されていない。。。  
そのため、Karabiner Simple Modication の設定（Caps Lock to Esc, fn to Control)を行った。  
できれば、修飾キーの設定で対応ができるようにしたいが、それは後ほど調査する

## ショートカット

Mission Control
- [ ] 右の操作スペースに移動 Ctrl+>(設定変更 on -> off)
- [ ] 左の操作スペースに移動 Ctrl+<(設定変更 on -> off)
- ディスクトップ[1-6]: Option+[1-6]
- 上記に伴い壁紙を変更

Spotlight検索を表示
- [ ] Spotlight検索を表示(設定変更 on -> off)
  - alfred install 後実施 
- [x] Finderの検索ウィンドウを表示

## MIssion Control

- [ ] 最新の状況に基づいて操作スペースを自動で並び替える(設定変更 on -> off)

## セキュリティとプライバシ

- [x] ファイアウォール
- FaileVault をオンにする

## ユーザとグループ

- 自動ログイン: オフ
