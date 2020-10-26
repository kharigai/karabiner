MacBook 設定
------------


# 環境

- OS: macOS High Sierra 10.13.6


# 資料

- [MacBook Air]()  


# システム環境設定

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

# general

## brew

## font

ricty
```
brew update

# すでにRictyがインストールされている場合
brew uninstall ricty

# Rictyがインストールされていない場合tapでリポジトリを追加する
brew tap sanemat/font

brew install --vim-powerline ricty

# 展開ディレクトリは環境に合わせる
cp -f /usr/local/Cellar/ricty/3.2.3/share/fonts/Ricty*.ttf ~/Library/Fonts/ 

# フォントのキャッシュ削除
fc-cache -vf

# シェルの再起動
exec $SHELL -l
```


# アプリケーションインストール

## index

- [x] chrome dmg
- [x] slack AppStore
- [x] google日本語入力 dmg
- [x] bettertouch tool dmg
- [x] alfred dmg
- [x] karabiner dmg
- [x] macVim
- [ ] DeppL


## chrom

### Plugin

- [ ] Google翻訳
- [ ] 1password

### vimium 設定

#### Vimium Options

- vimium-options.json を読み込む 


### 検索バーにフォーカスが移動した時、表示画面に移動する対応

- [設定|検索エンジンの管理](chrome://settings/searchEngines) に移動
- [追加] ボタンを選択
  - 検索エンジン: フォーカスを元に戻す
  - キーワード: p
  - URL: javascript:

### bettertouch tool

- [BetterTouchTool 公式サイト](https://folivora.ai/) より zip ファイルをダウンロード
- BetterTouchTool2.app をアプリケーションフォルダに移動
- 設定
  - Advanced設定 Windows Snapping TAB を開く
  - Left width: 59%, Right width: 41%
  
### google 日本語入力

google 日本語入力をインストールした状態で、ことえりを削除する。  
入力ソースを「google 日本語入力」のみにする場合、ことえりのみを削除することはできない。  


### alfred

# 設定

設定(preference) にて設定画面を表示

## Default Result(Features)

- [x] Extras: Folder off to on
- Search Scope: に必要なフォルダを追加

##  Web Bookmarks(Features)

- [x] Google Chrome Bookmarks
  - この設定で、Chrome bookmark が検索条件になる 

## Dictionary

- [x] Defin a word: d
  (defin to d. keyword d で辞書検索)

# Workflow

- [alfred-chrome-window-workflow](https://github.com/caiogondim/alfred-chrome-window-workflow)
  - cw: chrome new window open
  - cw + option: chrom new window open(incognito)
- [open-with-macvim](https://github.com/franzheidl/alfred-workflows/tree/master/open-with-macvim) 
  - mvim: macvim を開く
  - mvim* : key 入力後ファイル名を入力するとファイル検索モード
  - 注意
    - 別ファイルを開く場合、新しくウィンドウが開く
- [alfred-new-terminal-window](https://github.com/miromannino/alfred-new-terminal-window) 
  - ttw: terminal new window open
  - 元の workflow は、iterm2 をターゲットにしている
  - terminal 用に修正が必要
  - keyword(tw) は、twitter とかぶるので、ttw に変更
- [colors](http://www.packal.org/workflow/colors)
  - `#9999`: 色見本を表示
  - rgb(99,99,99): 色見本を表示
  - 色見本を選択するとクリップボードに情報をコピー
- [Alfred workflowで新規ウィンドウを開く](https://noboru.hatenablog.jp/entry/2014/01/12/021321)

# 便利な使い方

- space: ファイル検索
- 1p: 1password
- alt: 入力した文字列を spotlight で検索。(with new window) 



[[Alfred] 設定、使用方法 ](quiver-note-url/AF2F7C1A-DCB1-498B-90B2-BFF4F5462D8E)

### karabiner

[karabiner] 設定、使用方法 参照
https://github.com/kharigai/karabiner

### macvim


# インストール
- macvim-kaoriya にて dmg ファイルをダウンロード
- macvim をインストール

# 初期設定

1. ~/bin へのパスが通っていて、それが優先的に読まれること
   ```
   $ vi ~/.bashrc
   -> 以下を追加
   export PATH=$HOME/bin:$PATH
   ```
2. ターミナルからmacvim-kaoriya GUIを起動する(mvimコマンドを導入する)
   ```
   $ curl https://raw.githubusercontent.com/splhack/macvim/master/src/MacVim/mvim > ~/bin/mvim
   $ chmod 755 ~/bin/mvim
   ```
3. vim コマンドを作成する
   ```
   $ cat << 'EOS' > ~/bin/vim
   #!/bin/sh
   LANG=ja_JP.UTF-8 exec /Applications/MacVim.app/Contents/MacOS/Vim "$@"
   EOS
   
   $ chmod +x ~/bin/vim
   ```

## memo

```
set backgroud=dark
```

## 色変更(hybrid)

```
$ mkdir -pv ~/.vim/colors
$ cd ~/github
$ git clone https://github.com/w0ng/vim-hybrid
$ cp -v vim-hybrid/colors/hybrid.vim ~/.vim/colors/

$ vim ~/.gvimrc
-> 以下を追加
set background=dark
colorscheme hybrid
```


### 1password

v7 からデフォルトでサブスクリプションでの購入となった。  
スタンドアロン（買い切り版）を購入した場合、複数のデバイスでの同期に制限がある模様。  
[1Passwordを違うデバイスで同期する方法(Mac、Windows、iPhone、Android)。買い切り、サブスクリプション共に解説。](https://www.tentecomai.com/entry/1Password-synchronization)

## tmux

## 環境
- MacBook Pro (13-inch, 2017, Two Thunderbolt 3 ports) 
  - CPU: 2.3 GHz Intel Core i5
  - Memory: 16 GB 2133 MHz LPDDR3
- OS: High Sierra 10.13.5

## パッケージインストール

tmux
```
$ brew install tmux
$ tmux -V
tmux 2.7
```

reattach-to-user-namespace
```
$ brew install reattach-to-user-namespace
$ reattach-to-user-namespace --version
reattach-to-user-namespace version 2.6
    Supported OSes: OS X 10.5-10.13
```


Terminal でペインを分割した際、罫線が2重に表示される問題
```
- ターミナル|環境設定 詳細
  言語環境
  □ Unicode 東アジアA（曖昧）の文字幅をW（広）にする
  □ Unicode East Asian Ambiguous characters are wide
  → チェック off
```

## tmux conf

## 資料
- [tmuxとMacのクリップボードを共有する(tmux2.4以降対応)](https://leokun0210.hatenablog.com/entry/2017/12/16/121834)





