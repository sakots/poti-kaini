# POTI-board改二
phpお絵かき掲示板スクリプトPOTI-boardをさらに改良していくプロジェクトです。
  
<a href="https://github.com/funige/neo/">PaintBBS NEO</a>  
<a href="https://github.com/sakots/poti-kai/">POTI-board改</a>  
  
## 概要
POTI-board改で使用しているテンプレートエンジン「htmltemplate.inc」は老朽化が進んでいる… 
ということでなんか新しいテンプレートエンジンはないか探したところ、
  
<a href="http://skinny.sx68.net/">Skinny</a>  
  
見つけました！これに移植します！ → できました！

## 現状

- POTI改を超えた気がする！

## 今後

- セキュリティとか
- NEOでペイント画面のセキュリティクリック数関連が機能していない？ → NEOの仕様

## 使い方
基本的に <a href="https://github.com/sakots/poti-kai/">POTI-board改</a> と同じですが、スキンを置くフォルダができました。  
config.phpの設定をし、アップロードしてpotiboard.phpにアクセスするだけです。  
さとぴあさんの[詳しい記事](http://stp.sblo.jp/article/185357941.html) (改1.55系のバージョンのものですのでそこだけ注意。わたしも書かねば)。

## 改から改二へのバージョンアップ
ログの形式は同じですが、config.phpが若干違います。また、スキンの形式は全く違います。configを同じように設定して、対応したスキンをスキンフォルダに入れてpotiboard.php、config.php、スキンフォルダをアップロードすればOKのはずです。質問はPOTI改公式まで！！

## スキンについて

このスクリプトはスキン機能に対応しています。作り方（変数名）はデフォルトスキンのreadmeに詳しく書いています。

## サンプル/サポート

[POTI改公式サイト](https://poti-k.info/) をオープンしました。質問や動作確認にご利用ください。

---

## 履歴

### [2020/05/18] v2.3.2 lot.200518

- cookieを取得するだけで使用していなかった個所を削除 (by さとぴあ)

### [2020/05/17] v2.3.1 lot.200517f

- ユーザー削除の安全性向上(by さとぴあ)

### [2020/05/17] v2.3.0 lot.200517e

- ユーザー削除の画像だけ消すを廃止(config.phpに変更があります) (by さとぴあ)
- スキンの安全性、ユーザビリティ向上。

### [2020/05/17] v2.2.8 lot.200517d

- デバッグのdumpが残っていたので削除(by さとぴあ)

### [2020/05/17] v2.2.7 lot.200517c

- 「投稿者名をコピー」機能搭載。(by さとぴあ)
- スキンをそれに対応。

### [2020/05/17] v2.2.6 lot.200517b

- デフォルトスキン修正

### [2020/05/17] 

- skinディレクトリの.htaccess設定変更
- おまけスキンnee2更新

### [2020/05/17] v2.2.5 lot.200517a

- configの説明追加、デフォルト値変更。
- アプレットのセキュリティチェックに引っかかった場合のURL用htmlファイルを同梱。
  - デフォルト設定ではお絵かき掲示板のindex.htmlに飛ばされてしまうため、なぜ投稿失敗したのかがわからないから。
  - セキュリティにヒットした場合の飛び先を define('SECURITY_URL', './security_c.html'); に設定変更してください。

### [2020/05/17] v2.2.4 lot.200517

- デフォルトでしぃペインターに対応

### [2020/05/16] v2.2.3 lot.200516e

- readme_pch.html を追加。Javaのpchビューワー配布条件に必要でした。(by さとぴあ)
- thumbnail_re.php を削除。現在のバージョンのPOTIでは使っていない。(by さとぴあ)

### [2020/05/16] v2.2.2 lot.200516d

- 対応スキン用にしぃちゃんアプレットを本体に同梱。[Readme_Shichan.html](./potiboard2/Readme_Shichan.html)

### [2020/05/16] v2.2.1 lot.200516c

- Skinnyを配布用に設定変更

### [2020/05/16] v2.2.0 lot.200516b

- ミニレスフォームを日数経過で閉じる機能追加（スキンの仕様が変わりました）
- v2.1までとconfigの互換性がなくなっていますので注意。（CRYPT_PASSが大文字になっただけです）
- configデフォルト変更

### [2020/05/16]

- config説明追加

### [2020/05/16] v2.1.1 lot.200516a

- 軽微なエラーつぶし
- configの調整

### [2020/05/16] v2.1.0 lot.200516

- スキンともども安定版

### [2020/05/15] v2.0.9 lot.200515

- 改行できなくなっていたバグに完全対応

### [2020/05/15] v2.0.8 lot.200515

- 改行できなくなっていたのを暫定対処

### [2020/05/15] v2.0.7 lot.200515

- config.phpの整理(by さとぴあ) - 時系列のものを種類別にした

### [2020/05/15]

- デフォルトスキンバージョンアップ
- スキンのreadme整理

### [2020/05/15] v2.0.6　lot.200515

- PROXY_CHECK関連のコードを削除(by さとぴあ)

### [2020/05/15] v2.0.5　lot.200515

- 改行の抑制とProxyチェックを廃止によるエラーを修正

### [2020/05/15] v2.0.4　lot.200515

- 改行の抑制とProxyチェックを廃止(by さとぴあ)
- potiboard.phpの上のほうの説明を修正

### [2020/05/15] v2.0.3　lot.200515

- 独自タグ関連エラー修正(by さとぴあ)
- palette.txtの読み込み処理修正(by さとぴあ)
- デフォルトスキン

### [2020/05/15] v2.0.2　lot.200515

- palette.txtの読み込み処理(by さとぴあ)

### [2020/05/15] v2.0.1　lot.200515

- 独自タグ廃止に関するエラー修正。(2.0.0動かないです)
- スキン修正

### [2020/05/15] v2.0.0　lot.200515

- $getで記事の編集をできないように変更(byさとぴあ)
- 独自タグ廃止
- noticemailのutf-8以外を削除
- 満を持して2.0.0として公開

### [2020/05/14] v2.0.0a8

- 管理パスをグローバル定数から変数に変更(byさとぴあ)
- スキンフォルダのcss以外へアクセスできないように.htaccessを設定

### [2020/05/14] v2.0.0a7

- DEF_FONTCOLORの設定がないテンプレートの場合を想定

### [2020/05/14]

- 動画が再生されないの、スキンの問題でした。

### [2020/05/14] v2.0.0a6

- デフォルトスキン変更、スキンフォルダ作成 (config.php要再設定！)
- palleteの問題に暫定対処

### [2020/05/14] v2.0.0a5

- htmlの生成に成功(byさとぴあ) 大感謝。
- スキンのエラー修整。

### [2020/05/13] v2.0.0a4

- htmlは生成されないが、動く。

### [2020/05/07] v2.0.0a3

- いちからつくりなおす。
- ログが生成されるのは確認、HTML生成されず

### [2018/09/16] v2.0.0a2

- 記録

### [2018/09/15] v2.0.0a1

- プロジェクト開始
- ログが生成されるのは確認、HTML生成されず