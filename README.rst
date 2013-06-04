Riak Source Code Reading @Tokyo
===============================

- `Connpass series <http://connpass.com/series/218/>`_

- 一回あたりの基本方針

 - 隔週、19時スタート、できれば火曜日
 - 入門・中級レベルと、ガチのソースコード解説を1セッションずつ
 - Open Questionsから発表できそうな問題を調べてきて発表
 - 特に資料とかは不要 (ホワイトボードあり)
 - 発表した人にはマグカップまたはビアグラスをプレゼント（したい）
 - ビールはひとり2本まで

- 皆勤賞の人にはTシャツをプレゼント（したい）
- 何か発表したい人、運営に意見あるひとはPull Requestでどうぞ


Open Questions - 発表のためのネタ
-------------------------------------

ソースコードレベルでの解説が基本(なにか気になったら随時Pull Requestください)

- リリースパッケージなど
- テスト
- get, put 性能のオーダーとか勘所
- それぞれのAPIのレビュー
- leveldbのindex書き込みはアトミックか？
- 遅いなと思ったときの解析とかチューニング (reserved for @itawasa)
- sext
- lager, dtrace
- riak_api / erlang_protobuffs, mochiweb, poolboy, erlydtl, webmachineなど
- yokozuna 入門
- riak_core 再入門
- riak_pipe 再入門

開催の趣旨というかゴール
------------------------------

- Riakの内部を理解して @kuenishi と @ksauzz が日本でちゃんと仕事できるようになる
- Riakの中で使われている技術はすごいのか？すごくないのか？？がよくわからない
- riak_coreはフレームワークなので、それを使って何か作ってもらいたい
- Riakを使ったアプリの設計のポイント、運用や設定のノウハウを知りたい

基礎知識
------------

- `Dynamo <http://www.allthingsdistributed.com/2007/10/amazons_dynamo.html>`_ `和訳 <https://gist.github.com/2657692>`_
- Erlang/OTP全般

 - `なぜErlangなのか <http://ymotongpoo.hatenablog.com/entry/20110322/1300776826>`_
 - `プログラミングErlang <http://www.amazon.co.jp/dp/4274067149>`_
 - `Learn You Some Erlang <http://learnyousomeerlang.com>`_
 - `Learn You Some Erlang 日本語訳 <http://www.ymotongpoo.com/works/lyse-ja/>`_ by ymotongpoo

- キーワード

 - DHT/Chord, Replication, Quorum, Vector Clock
 - Bloom filter
 - LevelDBとかLSM-tree
 - REST API - mochiweb, webmachineなど
 - Distributed Erlang

- Riakドキュメント `オリジナル (英語) <http://docs.basho.com/riak/latest/>`_ / `日本語訳 <http://docs.basho.co.jp/riak/latest/>`_

Logs
====

#13 2013/6/25
-------------

- Connpass page
- Yokozuna 入門 by @ksauzz
- QuickCheck でなにか @taketon_ (or riak_core by itawasa)


#12 2013/6/4
------------

- `Connpass page <http://connpass.com/event/2520/>`_
- Webmachine streaming まわり @KOBA789
- QuickCheck でなにか @taketon_ -> 延期

#11 2013/5/21
-------------

- `Connpass page <http://connpass.com/event/2423/>`_
- vector clocks 入門 -> 使用例 -> CRDT by @shino
- 起動シーケンス by @takabow

#10 2013/5/7
------------

- `Connpass page <http://connpass.com/event/2309/>`_
- riak_pipe 入門 by @mille-printemps
- ets 入門 via folsom by @kuenishi
- @takabow 皆勤賞 -> 白Tゲット！！

#9 2013/4/23
------------

- `Connpass page <http://connpass.com/event/2215/>`_
- w, dw, pw (revenge) by @taketon_
- `observer, eper デバッグ向けツール群, gen_fsm入門 <http://ksauzz.cs-ap-e1.ycloud.jp/slides/observer-eper/slide.html>`_ by @ksauzz

#8 2013/4/9
-----------

- `Connpass page <http://connpass.com/event/2096/>`_
- w, dw, pw by @taketon_
- Riak / Riak-CS(Enterprise版) ベンチマークしました by @rev4t
  http://www.slideshare.net/takashisogabe/riak-19684891

#7 2013/3/21
------------

- `Connpass page <http://connpass.com/event/1980/>`_
- poolboy by @jbking
- `deleteの動作（Tombstoneなど) <http://masahito.hatenablog.com/entry/2013/03/23/012305>`_ by @Masahito

#6 2013/3/5
------------

- `Connpass page <http://connpass.com/event/1897/>`_
- Erlang開発環境 by @shkumagai
- Active Anti-Entropy by @itawasa

#5 2013/2/19
------------

- `Connpass page <http://connpass.com/event/1796/>`_
- OTP 入門 (see directory #5)by @ksauzz
- `Erlang導入からRiakのクラスター参加まで <http://blog.tbl.jp/2013/02/riakscrjp5.html>`_ by @takabow

#4 2013/2/1
------------

- 新年会（ビール多め） @ 福らく屋
- `Connpass page <http://connpass.com/event/1659/>`_
- riak_core 入門 by @itawasa
- Erlang 入門 by @shkumagai
- Perl から Riak を使うためのモジュール by @myfinder

#3 2013/1/8
-----------

- `Connpass page <http://connpass.com/event/1383/>`_
- hinted_handoffってなに？ by @csakatoku

 - ちょっと量が多すぎて難易度が高かったので、riak_core をやった後にまたリベンジ

- Implementation of 2i ( #3/2i.rst ) by @kuenishi

 - leveldbのインデックス更新はアトミックなのか？


#2 2012/12/11
-------------

- `Connpass page <http://connpass.com/event/1518/>`_
- `MapReduce <http://www.slideshare.net/masahitojp/riak-map-reduce-for-beginners-15608362>`_ by @Masahito
- `riak-erlang-client <http://www.slideshare.net/nobu_k/riak-source-code-reading-2-erlang-client>`_ by @nobu_k

#1 2012/11/28
-------------

- `Connpass page <http://connpass.com/event/1396/>`_
- `Let's りあっくぅ <https://docs.google.com/presentation/d/1TEUie_V7kr6Z7reeNNnQTUQUWcWzFfHXFZxtgofEx5Q/edit#slide=id.p>`_ by @IanMLewis
- `Bitcask / LevelDB 使いわけ＆チューニング <https://github.com/kuenishi/riak_scr_jp/blob/master/%231/csakatoku.md>`_ @csakatoku
- Riakのインストール、Pythonクライアントで叩いてみた、riak_control
- bitcask / eleveldb の議論は割と盛り上がった

#0 2012/11/13
-------------

- `Connpass page <http://connpass.com/event/1265/>`_
- `Keynote <https://gist.github.com/4044699>`_ by @kuenishi
-  `walkthrough around put request <http://gist-slide.appspot.com/4069613/slides.md>`_ by @ksauzz

- 参加者：分散システムに興味あるひと、仕事に使いたい、MySQLであふれる、類似製品を扱っているetc - Erlangは初めてというひともちらほら
