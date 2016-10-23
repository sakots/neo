# PaintBBS NEO
お絵描きしぃ掲示板 PaintBBS.jar (&copy;2000-2004しぃちゃん) を無断でhtml5化する企画です。  
javaアプレットが絶滅する前に、javascriptで書き直しておきたい。

Flashやhtml5のお絵描きサイトはいっぱいあるんだけど、そうじゃないんだ。  
おじさんは昔のjavaアプレットそっくりの環境が欲しいんだ。  


1. 掲示板に投稿できるMac/Win用のアプリを開発します(中身はjavascript)

2. PaintBBSと見た目や操作性がだいたい同じになってきたら、  
管理人さんに連絡取って直接組み込んでもらうことを目指します

**質問・要望等は直接こちらへ**  
https://github.com/funige/neo/issues  

----

## Mac/Win用アプリの実行方法
1. neo-darwin-x64.zip(Mac)または  
neo-win32-ia32.zip(Win)をダウンロードして、どこかに展開する  

2. 実行ファイル (neo.app または neo.exe) をダブルクリック

## 履歴

#### ver0.4.5 (2016/10/23)
- ブラウザ化テスト
- 画像の解像度を選んで描きはじめられるようになりました

お絵かき本体はあんまり進んでないです
- 消し四角・レイヤー結合・上下反転・左右反転
- マウスポインタが指の形になっていたのを修正
- 消しペンにもマスクがかかるように修正

#### ver0.4 (2016/10/11)
- ウィンドウビュー
- マスク・逆マスク
- ボタンとかスライダとか実装

- カーソルをちゃんとxorで表示するように修正

#### ver0.3 (2016/10/4)
- 鉛筆・消しペン・塗り潰し
- 透明度
- 拡大した画像をスクロールできなかったのを修正
- マスクのテスト
- 外部のブラウザに飛ばずに送信画面を自分で開いてみるテスト  
 ![ver0.1](http://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20161004/20161004190655.png?1475575647)

#### ver0.2 (2016/9/28)
いろいろ中途半端なのでこのバージョンは見送ったほうがいいです

#### ver0.1 (2016/9/21)
とりあえず画像を既存の掲示板に送信するところだけ作って検証  
 ![ver0.1](http://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20160922/20160922095441.png?1474505726)

しぃペインターとかPooとかは作りません
