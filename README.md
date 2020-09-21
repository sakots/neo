
# PaintBBS NEO
![ver1.5.1](https://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20181205/20181205141944.png)  

お絵描きしぃ掲示板 PaintBBS (&copy;2000-2004しぃちゃん) をhtml5化するプロジェクトです。  

作者行方不明のため、許諾は取れていません。

しぃちゃんのホームページ（Vector）  
http://hp.vector.co.jp/authors/VA016309/

**Flashやhtml5のお絵描きサイトはいっぱいあるんだけど、そうじゃないんだ。  
おじさんは昔のjavaアプレットそっくりの環境が欲しいんだ。**


1. 掲示板に投稿できるMac/Win用のアプリを開発します(中身はjavascript)

2. PaintBBSと見た目や操作性がだいたい同じになってきたら、  
管理人さんに連絡取って直接組み込んでもらうことを目指します  

  :

**……というわけで、ふたばでNEOが使えるようになりました！**

    105 名前：◆管理人 投稿日：2017/01/19(木) 02:20 del
    落書き板に組み込みました
    http://nov.2chan.net/q/futaba.htm
    調子が良ければ他のお絵かき板にも導入します


### <a name="animation">動画記録について</a>
v1.5で動画記録をサポートしました。
Java版の動画データ（.pch）が解析不能なため、動画データの互換性はありません。


## <a name="browser">対応環境</a>

  Chrome/FireFox/Safari/Edge
  iOS(Mobile Safari)  
  ※ 最新のバージョンのみ

  IEはサポート対象外です  
  Androidでもだいたい動くのですが、サポート対象外とします

  Windowsで線がうまく引けない場合は、以下をお試しください
  - Chromeを使う
  - Wacomのタブレットを使用している場合は「デジタルインクを使用する」をオフにする

  
[Firefox(59以降？)はタブレット関係のバグがあるらしく、](http://neo.websozai.jp/potiboard.php?res=553)線が乱れることがあるようです。  
マルチプロセスを切ると症状が解消されるかもしれません。（about:configでbrowser.tabs.remote.autostartをFalse）

Chrome(80以降？)で横に長い線を引くとジェスチャーと誤認識される場合は、chrome://flags/#overscroll-history-navigation でジェスチャーを無効にするといいかもしれません。

## <a name="deploy">お絵かき掲示板の設置方法について</a>
新しくお絵かき掲示板を設置したい方には、POTI-board改の利用をお勧めします。  

- [POTI改公式サイト](https://poti-k.info/)

公式サイトには[設置サポート掲示板](https://pbbs.sakura.ne.jp/cgi/neosample/support/)があります。  
掲示板の設置に関するご質問・不具合の報告等ありましたら、遠慮なくこちらへどうぞ。

まだ古いPOTI-baordを稼働中の方のための[移行ガイド](README-potiboard.md)  
(古いPHPのコードには色々問題がありますので、お勧めできません)

以前ここで公開していた動作確認用掲示板は[こちら](http://neo.websozai.jp)

**掲示板の設置以外についての質問・要望は[こちら](https://github.com/funige/neo/issues)でお願いします。**

### <a name="app">Mac/Win用アプリについて</a>
Mac/Win用アプリは、NEO開発の過程で使われたものです。  
NEOの入っていない掲示板に投稿して、動作を確認することができます。  
バイナリは重いので削除しました。  
興味のある方はソースコードからビルドしてください。  

    > git clone https://github.com/funige/neo.git
    > cd neo 
    > npm install
    > npm run app

## <a name="history">履歴</a>

#### ver1.5.10 (2020/09/21)
- 投稿ボタン連打対策を入れました

#### ver1.5.9 (2020/06/22)
- オリジナルのPaintBBSにあったセキュリティ関連のオプションを実装しました。

  &lt;param name="neo_emulate_security_error" value="true">

  にすると、描画時間やクリック回数が少ない時に投稿を拒否して、任意のURLに飛ばすことができます。  
  [README-potiboard.mdにも追記しました](README-potiboard.md)  
  **デフォルトはfalseです**


#### ver1.5.8 (2020/06/14)
- （v1.5.7のソースコードをprettierで整形しただけです）

#### ver1.5.7 (2020/06/08)
- Chromeで左から右にスワイプした時に前の画面に戻ってしまう問題の対処ですが……

  &lt;param name="neo_confirm_unload" value="true">
  
  にすると、戻るボタンを押した時などに「このサイトを離れますか？」という警告が出るようになります。  
  **デフォルトはfalseです**

#### ver1.5.6 (2020/05/10)
- samplebbsの保守が困難になっていたので、リポジトリから削除しました
- Apacheでmod_pagespeedを使った時、正しく表示されない問題に対処しました

#### ver1.5.5 (2020/04/11)
- lineを使った動画の再生でなぜか無限ループに入ることがあったので対処
- ツールの位置の左右入れ替えができるようになりました。

    Neo.setToolSide(true) // true|false  
  
  trueのときツールはキャンバスの左側になります

#### ver1.5.4 (2019/10/23)
- iPadOSで右ボタンが表示されない問題を修正

#### ver1.5.3 (2019/8/19)
- ベジェ曲線のプレビューの表示方法がオリジナルのPaintBBSと違っていたのを修正
- Chrome67以降でベジェ曲線のプレビューが重くなっていたのを高速化

#### ver1.5.2 (2019/8/2)
- 動画の再生エラーをちょっとだけ修正

#### ver1.5.1 (2018/11/29)
- 「続きを描く」は表示までに時間がかかるので、途中経過を表示するようにしました  
 　アニメーション中にキャンバスをクリックすると、再生を省略します
- コピーを中断して四角ツール等を使うとコピーした矩形がずっと画面に残ってしまっていたのを修正

#### ver1.5.0 (2018/11/25)
- ビューアの再生速度を変更できるようにしました
- IE11で投稿できなくなっていた問題を修正

#### ver1.4.11 (2018/11/13)
- ビューアのボタン類の実装
- 動画の再生に失敗しても続きから描けるようにしました

#### ver1.4.10 (2018/11/2)
- ぼかしツールとベジェ曲線をさらに修正

#### ver1.4.9 (2018/10/30)
- ベジェ曲線が点線になる問題を修正

#### ver1.4.8 (2018/10/26)
- 消し四角とぼかしツールもバグってたので修正しました

#### ver1.4.6 (2018/10/23)
- 全消しで動画が途切れるバグを修正
- 消しゴムの透明度が動画で再現されないバグを修正

#### ver1.4.5 (2018/10/17)
- 動画記録お試し版  
 　オリジナルのPaintBBSと同じように動画を記録することができますが、  
 　動画データ（拡張子pch）の互換性はありません。

#### ver1.3.4 (2018/05/30)
- 裏技ですが、JavaScriptコンソールに  

    Neo.painter.inputText.style.fontFamily="serif"  

  とか入力してテキストツールのフォントを変更できるようになりました
  （某所で要望があったので……）

#### ver1.3.3 (2018/05/17)
- スペイン語対応 (Spanish support)

#### ver1.3.1 (2018/04/16)
- 画面外にドラッグした時にいろいろ不具合が出ていたのを修正

#### ver1.3.0 (2018/04/04)
- 対応環境にiOS(Mobile Safari)を追加
- 「右」ボタンの場所を右側に変更

#### ver1.2.9 (2018/03/30)
- モバイルで画面左上に「右」ボタンが表示されるようになりました
  「右」をタップ→ツールをタップで右クリックと同じ動作になります
  変なUIですがこれが昔風でいいのではないかと...

#### ver1.2.8 (2018/03/22)
- safariでリロードした時に画像が保存されないバグを修正
- iPad proでペンを使った時にボタンが押せないバグを修正

#### ver1.2.6 (2018/02/22)
- 既にNEOが組み込まれている掲示板をアプリ版のNEOで開いた時は二重起動の警告を表示するようにしました
- モバイルでスライダを動かすと全体がスクロールしてしまうバグを修正
- 日本語以外の環境ではメッセージを英語で表示するように修正

#### ver1.2.3 (2017/12/31)
- Safari(iOS、MacOS)でキャンバスの右端や下端の描画がおかしくなるバグを修正。

#### ver1.2.2 (2017/12/24)
- AndroidのChromeで描けなくなっていたのを修正。

#### ver1.2.1 (2017/12/19)
- 著作権表示のしぃちゃんの名前が「しいちゃん」になってたのを修正。  
  どうもver0.3の頃からずっと間違ってたようです。すみません。

#### ver1.2.0 (2017/12/11)
- ページを離れるときに警告のポップアップを出す機能は問題が多いので  
  <s>デフォルトではオフにしました</s>削除しました

#### ver1.1.16 (2017/11/25)
- 塗り潰しのバグ修正できたかも？
- ブラシサイズを変更するとトーンの柄がずれるバグを修正
- クレジット表記のボタンを押した時の挙動を新窓表示に変更
- <s>ページを離れるときに警告のポップアップを出すように修正(ちょっとうるさいですが)</s>
- RGBスライダを動かすとカレントパレットの色も変わるように修正
- WonderCatStudioの動的パレットでgetColorsの値がおかしかった問題を修正

#### ver1.1.12 (2017/9/9)
- 掲示板開発者用のpaintBBSCallbackがちゃんと実装されていなかったので実装

#### ver1.1.11 (2017/8/16)
- スポイトツールのバグ修正

#### ver1.1.10 (2017/8/11)
- <s>/samplebbs/[README.md](https://github.com/funige/neo/tree/master/samplebbs/README.md)修正。</s>
- スポイトツールの動作変更
- ベジェツールを微妙に調整
- Chromeでペンを認識しなくなることがあるので PointerEvents を使うように修正

#### ver1.1.9 (2017/7/27)
- キャンバスの端でぼかしブラシを使うと白が混じるのを修正
- ズーム時にブラシを画面外に出すと画面が点滅する不具合を修正
- カーソルのゴミが画面端に残ってしまうことがあるのを修正

#### ver1.1.8 (2017/7/10)
- EdgeとIEではまだバグが残っていることがわかったので、警告表示を復活しました  
※Edge40以上（userAgent文字列ではEdge/15と表示されます）でバグが治ったのが確認されています

#### ver1.1.6 (2017/5/23)
- Chrome58以降でふたばの画像掲示板に投稿すると失敗する問題を修正できたような気がします

#### ver1.1.5 (2017/5/10)
- Chrome58以降でふたばの画像掲示板に投稿すると失敗するようになったので警告表示を追加しました

#### ver1.1.4 (2017/3/27)
- サムネール投稿のバグ修正
- アプレットの高さが足りないときレイアウトが崩れるのを修正しました

#### ver1.1.3 (2017/3/16)
- ベジェツールの修正。オリジナルのPaintBBSに近い、ちょっと太い線にしました

#### ver1.1.2 (2017/3/8)
- 画面をズームした時にペン先がずれる問題を修正
- ベジェツールのハンドルの表示を修正

#### ver1.1 (2017/1/31)
- ブラウザがIEとEdgeの場合ふたばへの投稿に失敗するので、  
これらのブラウザで起動すると警告を表示するようにしました。


- テキスト入力ツールの不具合修正
- 保管ペンのバグ修正
- カラースライダの上でshift+クリックして値を1ずつ上下できるように修正
- その他細かいバグ修正

#### ver1.0 (2016/12/22)
- バグ修正

  だいたい終了です  
  加算逆加算は結局できませんでした  
  そのうち誰かが直してくれると期待して撤退……

![ver1.0](https://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20161221/20161221215643.png?1482325021)  

#### ver0.9 (2016/12/18)
- <s>Edge対応</s>
- <s>IE対応</s>
- バグ修正

#### ver0.8 (2016/12/13)
- ベジェ曲線
- 角取り・ぼかし
- 加算・逆加算テスト
- リロードした時にキャンバスが保存されるように修正
- Chromeでドラッグ中のカーソルがおかしくなる問題を修正

  残り時間でバグをできるだけ取ります  

#### ver0.7 (2016/12/5)
- 覆い焼き・焼き込み
- テキスト入力テスト
- サンプル掲示板設置

#### ver0.6 (2016/11/22)
- 水彩と鉛筆はどうやっても似ないのでひとまずこれで
- トーン
- 直線
- 傾け
- 四角とか楕円とか

  しんどい

#### ver0.5 (2016/11/3)
- スクロールバーをちゃんと表示するように修正
- キーボードショートカットを一部実装
- コピーツールのテスト  
- 保管ペンのテスト
![ver0.5](https://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20161103/20161103013321.png?1478104440)  
だいぶ飽きてきましたが  
年末までには何とかver1.0にしたいと思います

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
 ![ver0.1](https://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20161004/20161004190655.png?1475575647)

#### ver0.2 (2016/9/28)
いろいろ中途半端なのでこのバージョンは見送ったほうがいいです

#### ver0.1 (2016/9/21)
とりあえず画像を既存の掲示板に送信するところだけ作って検証  
 ![ver0.1](https://cdn-ak.f.st-hatena.com/images/fotolife/f/funige/20160922/20160922095441.png?1474505726)

----
- しぃペインターとかPooとかは作りません  
