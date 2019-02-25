# SpeechCastNT

## 概要

**SpeechCastNT**は本家**よっしー**氏作成の**SpecchCast**をもとに作られた**ggslyman**氏作成の**SpeechCast**を更に改造版です。<small>(以下**NT**版)</small>  
「２ちゃんねる」「jbbs(したらば)」「わいわいkakiko」「ぜろちゃんねる」に書き込まれたレスを読み上げ、画面上に字幕のように表示するソフトです。  
SCFH/SCFFにて取り込んで配信する際に使用するのを想定して実装しています。  
主な違いはプロキシ周りを追加して*某chApiProxy*から使いやすいようにしました。  
~~gitを使い慣れていないまま~~、この**NT改造版**を公開しています。  
たたき台なので、他の人用としてはまだまだちゃんと動かないかもね  
詳しくは下記[F&Q](#fq)にて  

## ライセンス

フリーソフトです。

GPLv2ライセンスでソースを公開しています。  
https://github.com/meto4d/SpeechCastNT

本家SpeechCastはこちら  
- http://sourceforge.jp/projects/speechcast/
- https://github.com/ggslyman/SpeechCast

## 必要なソフト

SpeechCastを使用するためのソフトです。
- Microsoft .NET Framework 4.5
- SAPI5.1対応の音声エンジン もしくは Microsoft Speech Platform v11対応の音声エンジン  
  - 標準では「Microsoft Sam」という日本語非対応の音声エンジンしかインストールされていないはずです。別途、日本語対応の音声エンジンを入手してください。  
  - MSより無料の日本語音声エンジン「Microsoft Server Speech Text to Speech Voice (ja-JP, Haruka)」が提供されていますが、通常インストールのみではSpeechCastが認識できませんので、本家に同梱のMSHaruka_64bit.rrg、MSHaruka_32bit.regを実行してください。  

## 使い方

現状はRelease版を用意していません。<small>もうちょっと待ってね。。。</small>  
ReleaseフォルダからSpeechCastNT.exeをDLして起動してください。  

動かなければ、本家SpeechCastを落として、このmodのコードを差し替えてビルド  
VS2017で動作することを確認してます。  
このexeも本家SpeechCast本体は必要なはず  
本家本体にSpeechCast-master\SpeechCast\bin\Releaseの構成で置いてデバッグしてます  
Releaseフォルダのexeの動作の安定性は全く保証しません  

## NT版で主に追加された設定

### プロキシ関係

- ツールバー右の設定ボタンから通信タブにて設定を行うことができます。  
「通信タブの下記プロキシを使用する」 を主に追加しました。  
***host***に*proxy*の`host名`を、***port***に*proxy*の`port番号`を入力すると串を通してつながるはずです。  
***host***に `http://proxy.server:port/` の形式を入力しても大丈夫にしてます。  

### 代替文字列関係

- `#CLOCKm#`でコンマ秒も追加した時間を表示  
- <s>絵文字は別フォントを指定し、好きなフォントで絵文字表示が可能(α版)</s>  
もうちょいデバッグ。。。  
- レス番の表示や読み上げのONOFF(α版)  
ツールバー右側の"番"のボタンによりレス番を字幕表示と読み上げのONOFF  
ON状態で表示&読み上げ  
便宜的なONOFFトグルなため、同時にONOFFしかできていない  
字幕ではレス番を表示して読み上げない、またその逆は後日  

### タブ機能

まだだよ  
<small>ローカルでテスト中...</small>

## F&Q
- **NTって何？**  
NoTitleの略だよ。つまり名前なんてないよ。無題だよ。
- **SpeechCastMEとは何が違うの？**  
もともと2chAPI関係のゴタゴタがあった2015年ぐらいの時にLivemateの代替としてSpeechCastを弄ろう！ってことでやり始めたため、
開発の根底が2chを意識したものなので、SpeechCastMEとは方向性がちょっと違うかも？  
前の時にもgitに上げてたけど(mod版)、gitの使い方を知らずにうpろだ代わりにしか使ってなかったので、バージョンや追加機能等々もそのせいでグチャグチャだったよ。  
そこで本家SpeechCastのブランチとして、ちゃんとした形で公開できるようにSpeechCastMEさんを参考にしてSpeechCastNTにしたんだよ。  
だからちょっと似てるんだよ。  

- **ぜろちゃんねる対応ってあるけど、読み込んでくれないよ！**  
まだ僕の[掲示板](http://meto4d.pgw.jp/2ch/kagamin/)にしか対応してないよ。  
内部的にはぜろちゃんねるのdatを読めるようにしてあるので、ぜろちゃんねるのリンクさえどこかで登録すれば動くようになります…  
[BBS.JPNKN](https://bbs.jpnkn.com/)さんの掲示板にも対応できるのを確認したらその辺を公開するよ  
もうちょっと待ってね
- **動かないよ！わかりにくいよ！**  
ごめん…  
自分用にしか開発してなくて、NT版も出来上がる前にgitのお勉強も兼ねて公開してます。  
ここわからな～い！ってことなら[**Twitter**](https://twitter.com/meto4d)なり[掲示板](http://meto4d.pgw.jp/2ch/kagamin/)なりdiscordなり直接なりどっかで言ってね。  

## サポート

この**NT**版部分のサポート的なのはしたい(するとは言っていない)  
この**NT**版のサポートはGithub上および[**Twitter**](https://twitter.com/meto4d)にて  
よっしーさんやggslymanさんへこの**NT**版に関してや、自分に**SpeechCast**本体に関してのサポートを求めるようなことは控えてね

## 更新履歴

- 19/02/10 [1.0.0 Rev.3]

  - NT版として再編成
  - https接続周り
  - 便宜的なぜろチャンネル対応
  - 代替文字列に`#CLOCKm#`と入力するとコンマ秒も表示するように

- 16/12/11 [2.0.1 Rev.21] mod 1.2 
  - レス番の表示&読み上げトグルを便宜的に追加
  - 表示と読み上げのそれぞれの別々トグルはまだ

- 16/12/09 [2.0.1 Rev.21] mod 1.1

  - インターネットオプションで指定せずにSpeechCast単体でプロキシを適用させるオプション追加
  - yotuubeとかのURLを拾うのもここで指定したプロキシ経由になってる問題有り
