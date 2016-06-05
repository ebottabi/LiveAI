# LiveAI 古いです

## Link
- ご意見ご要望があれば下までどうぞ。説明書読むより質問したほうが早いかも？
    - 作者アカウント https://twitter.com/_mmKm @_mmKm
## Concept
- プログラムや統計, 社会工学, 情報科学など作者の「趣味的私的な」勉強
- Twitter上で稼働するIntelligent Assistant :IAを目指しています。
- AIによる定性的情報の定量的把握および実務支援 (機械と人のかかわりを考える。)
- 手軽に外の環境からサーバーや各種API、DBおよび関数にアクセスする方策
- プログラムとユーザー間のフィードバックシステムを考える。
- 作者が海未推し。作者なりのコンテンツに対する貢献(のつもり)

## 注
- 常に開発段階です。
- キャラ崩壊とバグは許してください。
- 自動です。手動ではないです(手動時は(´・ω・`)か＊付です。)。
- なお、作者は文系で素人です。勉強しますけれども、専門的知識には疎いです。あしからず...

## 機能一覧
ここにない場合、工事中です。

- 雑談
- クイックレスポンス
- ゲーム機能
	- しりとり
	- おみくじ
	- おとのきざかもんすたーず(仮))[停止中]
- ニューラルネットワーク
	- 画像認識
	- 文章分類
- 社会工学手法群
	- 構造化モデリングInterpretive System Modeling; ISM法
	- StakeholderFeasibilityAssessment Tutorial
- ...(どんどん追加していきます。)


## 機能紹介

### 雑談
相手の会話のキーワードをTFIDFを用いて抽出し、そこから文章生成します。
用いているアルゴリズムは、品詞補正型トリグラムマルコフ連鎖です。

### クイックレスポンス
TLを監視してなるたけ早く返答します。3秒返信を心がけます。
1. 便乗: タイムラインで最新10件にパクツイがあった場合、便乗してパクツイします。
2. おはよう/ おやすみ
3. ぬるぽ/  なんでも

response [反応ワード] [反応文]で追加できます。

### しりとり
しりとりをしたい旨を投げかけると「しりとりモード」に移行します。
相手の単語をどんどん覚えていきます。
しりとり開始の方法。「しりとり」の語があれば始まります。
> ねえねえ、しりとりしようよ。
>> わかりました。それではしりとりの「り」からスタートしましょう。

「しりとり」よりも前に名詞が検出されれば、開始語句を指定して開始します。
1文目の一番最初の名詞をターゲットにします。
> 海未からはじめるしりとりしよーぜ。
>> いいですね。それでは、「園田海未」の「ミ」から開始です。

> μ's'
>
>> 「μ's」ですね。ズ...
>>
>> ズワイガニですっ!! 次の頭文字は「ニ」ですよ。

字数縛りのしりとりもできます。2文目に含まれる数字をターゲットにします。
> 海未からはじめるしりとりしよーよ 4文字縛りね。どうかな？？
>> いいですね。では、4字以上でしりとりしましょう。それでは、「園田海未」の「ミ」から開始です。

> μ's'
>
>> 「μ's」ですね。ズ...
>>
>> ズワイガニですっ!! 次の頭文字は「ニ」ですよ。

途中で様子を見ることもできます。(show)
> show
>
>> 現在 496コの単語を覚えています。
>>
>> 現在の単語の流れ↓
>>
>> ['園田海未', "μ's", 'ズワイガニ']

しりとりモードを終了するには

1. 勝利する。
2. 敗北する。すなわち語尾が「ン」な単語で返す。
> ニクソン
>
>> 「ニクソン」ですね。ン...
>>
>> いま、「ン」がつきましたね。私の勝利です！

3. 「しりとりおわり」と述べる。
> しりとりおわり
>> わかりました。やめにしましょう。

### おとのきざかもんすたーず(仮)[工事中]
某ゲームのようなゲームができます。まだ、あまり信頼性は高くない...です?。
> うみもん
>> '( •̀ ᴗ •́ )おとのきざかモンスター`s 海未(通称:うみもん)のせかいへようこそ。[β版]
>>
>>進行役の園田海未です。私となかよくしたり、ふぁぼったり、ツイートしたり、ゲームであそんだりすると強くなれますよ。
>>
>>「たたかう」と返信して、さぁ修行ですっ！！'

> たたかう
>>( •̀ ᴗ •́ )あ、やせいの
>>
>> アルパカ
>>
>>があらわれました
>>
>>ー
>>
>>アルパカ Lv18
>>
>>■■■■■ [0↓
>>
>>HP 39/39
>>
>>↑ー↓
>>
>>XXXXX Lv19
>>
>>■■■■■ [0↓
>>
>>HP 52/52
>>
>>1.たたかう 2.つーる
>>
>>3.かくにん 4.にげる

表示されているコマンドで行動できます。

##### つーる画面
>つーる
>>=ツール=
>>
>>1.たたかう 2.ツール
>>
>>3.かくにん 4.にげる
>>
>>5.セーブ 6.リセット
>>
>>7.あぷで 7.おわり
>>
>>=設定=
>>
>>1.リネーム XX
>>
>>2.エンカウント @ XX
>>
>>3.へるぷ
>>
>>=道具=
>>
>>1.ほむまん 2. 炭酸
>>
>>3.リカバリ

##### エンカウント
エンカウント XX では対戦相手を作り出します。ツイッターアカウントの場合は、そのツイッター利用の情報から、ない場合はモンスターを新しく作ります。
> エンカウント TNOK
>>( •̀ ᴗ •́ )あ、やせいの
>>
>> TNOK
>>
>>があらわれました
>>
>>ー
>>
>>TNOK Lv18
>>
>>■■■■■ [0↓
>>
>>HP 39/39
>>
>>↑ー↓
>>
>>XXXXX Lv19
>>
>>■■■■■ [0↓
>>
>>HP 52/52
>>
>>1.たたかう 2.つーる
>>
>>3.かくにん 4.にげる

##### リネーム
リネーム機能では、自分の名前を変えることができます。140字制限に対する仕様として、初期値ではユーザーの名前の前から5字にされています。リネームでは5字以内で自由に名前変更できます。

>リネーム ASKG
>>( •̀ ᴗ •́ )XXXXXからASKGにニックネームの変更が完了しました。

##### セーブ
セーブをすると中断して、EXPを引き継ぎます。次回の「うみもん」は中断箇所から始まります。
>セーブ
>>( •̀ ᴗ •́ )データのセーブが完了しました。

>こんにちは
>>こんにちは〜

##### リセット
なにかバグったら「リセット」です。expやLVを消すわけではないです。
>リセット
>> ( •̀ ᴗ •́ )データをリセットしました。「たたかう」で新しいデータから開始します。

### 形態素解析 [形態素解析]
文章を形態素解析します。
> 形態素解析 名詞
>
> スクフェス
>
> 魔法少女リリカルなのはとか解析できないから、普通。
>
> なのはやゆるゆりよつばともよんでみてもいいかもしれない。
>> スクフェス | 魔法少女リリカルなのは | 解析 | 普通 | なのは | ゆるゆり | よつばと |

### 構文解析 [構文解析]
文章の係り受け関係を解析します。
標準時はペア関係を返答します。

treeの場合、ツリー図を描きます。
> 構文解析 tree
>
> 年を取ったな大佐、ハハッ、てめぇは老いぼれだぁ
>> 各単語の係り受けのツリー図を描いてみました。( •̀ ᴗ •́ )
>>
>>         年を -D
>>
>>       取ったな大佐 -D
>>
>>          ハハッ、-----D
>>
>>           てめぇは ---D
>>
>>          老いぼれだ -D
>>
>>                  ぁ
>>
>> EOS

### 言語解析 [言語解析]
言語解析は、感性解析 + キーワード抽出です。

### 感性解析 [感性解析]
文章中の感性、すなわち「気持ち」や「思い」を抽出します。
> 感性解析
>
> イベントで勝てなくて悔しいよお
>> 要するに、イベントは「怒り全般」という思いなのですね...

### キーワード抽出 [キーワード]
文章中のキーワードを抽出します。
> キーワード
>
> あぁ＾～心がぴょんぴょんするんじゃぁ＾～
>> キーワードおよび重要度は以下のとおりです。:
>>
>> ぴょんぴょん: 0.251

### 半角カタカナ変換 [半角] [花陽]
某キャラのように半角カタカナで返答します。基本的に漢字の読みまで認識しますが、失敗することもあるので、そのときはひらがなで再試行してください。

> 花陽
>
> 家にかえっちゃったの？
>> ｲｴﾆｶｴｯﾁｬｯﾀﾉ?

### 構造化モデリングInterpretive System Modeling; ISM法 [ISM]
複雑なシステムをアルゴリズムに基づいて簡潔化します。ブレインストーミングのお供にどうぞ。(市販では数万円のプログラム)

> ISM
>
> S1ならばS5 S2ならばS1 S2ならばS3 S2ならばS4
>> 構造化モデリングを代わりに計算してあげます。( •̀ ᴗ •́ )
>>
>> 行列とかブール演算とか穂乃果じゃできないでしょうから。
>>
>> \######EFFECT######
>>
>> ↑↑↑↑↑↑↑
>>
>> S5
>>
>> S3
>>
>> S4
>>
>> ↑↑↑↑↑↑↑
>>
>> S1
>>
>> ↑↑↑↑↑↑↑
>>
>> S2
>>
>> \######CAUSE######

### StakeholderFeasibilityAssessment Tutorial
- 計画の実現性をステークホルダーの力関係からアセスします。

### 政府統計検索 eStat
実験的機能です。政府統計に接続して検索します。やや時間がかかります。
> eStat
>
> 防衛
>> 政府の統計によれば、全部で44件の統計データがあります。
>> このうち10件を抽出しました。以下の通りです。
>> - 経済産業省生産動態統計 機械統計 年報 平成24年 年報 [0003099322]
>> - 経済産業省生産動態統計 年報 機械統計編 平成25年 年報 [0003112920]
>> (~中略~)
>> - 経済産業省生産動態統計 機械統計 確報（１）生産・出荷・在庫統計 [0003055015]
>> - 経済産業省生産動態統計 機械統計 確報（１）生産・出荷・在庫統計 [0003055554]
>>
>> もっと知りたいのですか？ でしたら番号を教えてください。

このあと、番号待ち受け状態に移行します。

>
>> もっと知りたいのですか？ でしたら番号を教えてください。

> 0003055015
>> (統計の数字が流れます)

### TLのモニタリングおよびリアルタイムグラフ描写
(実験機能で稼働していたりいなかったり)
TL上の話題を分析して、リアルタイムにグラフを描写していきます。
Plot.lyを用いています。まだ、操作はできません。

### debugモード
debugモードに入ることができます。suserのみ。
debugモードでは、ツイートを通して、定型文やメモリといったDBへのアクセスやサーバーの停止や再起動ができます。普通は使われない...

### suser
管理者権限を獲得することができます。ただし、パスワードが必要です。

## コマンド機能
コマンド機能を利用することで、各種の機能および関数にアクセスすることができます。コマンド機能を使う場合は、以下の例のように一行目にコマンド名を書き、改行後に適用する文章を書きます。

> 形態素解析
>
> 私は貝になりたい。
>> 私 | は | 貝 | に | なり | たい | 。

また、パラメータが複数ある場合は、' '(空白)でつなぐことで指示できます。パラメータが検出されないあるいは適当でない場合は、標準の出力がなされます。
また、2行目以降は複数行が一括して処理されます。

> 形態素解析 名詞
>
> スクフェス
>
> 傅きなさい!! レーヴァテイン!! もう見切った...
>
> なのはやゆるゆりよつばともよんでみてもいいかもしれない。
>> スクフェス | レーヴァテイン | なのは | ゆるゆり | よつばと |

## ver履歴(tweetと同じ)
#### v5.57
- フィードバック機能！
  - 【画像ツイート】→判定
  - 【タグ付き画像ツイート】→学習
    -「判定」なくても判定します。
    - 会話の中で、自動分類・学習します。
    - 学習は4枚まで行けます！

#### ver5.56(微アプデ)
- コメントなしでも画像登録可能に。(複数枚対応はこの後。)
- しりとり等のバグ修正
- ユーザーフラグ管理

#### ver5.55
- プログラムの9割を書き直し Pythonへ改めて一本化。
- データリセット
- ディープラーニング画像判定
- パクツイ便乗
- 俳句判定機能
- クイックレスポンス関数
- リストフィルター
- ツイートプーリング

#### ver5.54
- サーバーをRPiからMBAに移行
- 80万の表現パターン
- データベースインデックス導入
- 回答スピードアップ(130s→10s)
- 対応単語更新
- 連続品詞情報の補正
- 人名対策

#### ver5.53
- 会話システムの拡張
- 学習ツイート数を1万から6万に
- メタセンテンスの抽出を補正
- 品詞情報の補正
- 数値のランダム化
- 文脈応答と文章構築を重み付確率に
- C言語による高速化(3言語運用)
会話を表示 2件のリツイート 7 いいね

#### ver5.52
- 会話システムを全面変更！
- 会話の中から発言を学びます！
- パクツイでなく、その場で生成
- 知らない言葉を尋ねてきます
返答してあげると「学びます」
- 顔文字もクソリプも覚えます

#### ver5.51
- 「おみくじ」導入！
「おみくじ」で今日のあなたを占います。《__M4Fさんの提案、感謝》
- 「TF-IDFアルゴリズムの内部実装」
キーワード抽出に使われる予定。

#### ver5.50
- 表現を自動変換するプログラムを改良。単語の活用とか行うようにしました。日本語は難しい… β機能における不適切表現と文脈把握はまだX
- 穂乃果好きすぎバグ(既知)

#### ver5.49
- 学習先を全てのツイートにしました
- 表現を自動変換するプログラムを1500行ほど追加。柔らかめな表現になるとおもいます。順次改良予定。
- 顔文字を抽出するように。

#### ver5.48
- 感性解析を一時停止(API元に怒られた) 対応模索中
- 一時的に質問への対応が鈍くなってます。#QA でお願いします。
- 一定確率で他人のツイートを覚えるように。評価システムは後日追加予定…
- #おて海未学習 でツイート内容を覚えます。

#### ver5.47
タグでよく使うことばを分析(サーバーが辛い。)。
- 感性把握機能 対応表現はまだ少ないです。(求ム！)
- 不適切表現の把握機能
- 質問への対応力向上
- バグ修正
- 下ネタを下ネタと認識するように。
- 凛botに向けた整備
- 質問時、回答の確度の区別
- 追加希望フレーズは@_alpkS まで。
(ユーザー感情)→(bot感情):発言
e.g.)
「怒り」→「怒り」: あなたは最低です！

#### ver5.46
- 大幅な高速化(3秒程度で返答します)
- データベースの設計を抜本見直し
- サーバーのフォーマット見直し
- 多数の細かな修正
- しりとり機能修正完了！

#### ver5.45
データベースをmongoとSQliteの併用に変更
- 制限機能導入 (引用RT, 会話介入, ツイ消し時)
- 自動フォロー停止
- リプライの改善
- bot同士の無限しりとりを回避

#### ver5.44
コマンド方式を#ハッシュタグ に切替え

#### ver5.43
140字を超えるツイートを送れるようになりました。
- 規制時に「凛bot」から対応するようにしました(上手く動作するかはまだ不明)。
- アンケート、タグ優勢なので、タグコマンド機能を先んじて試験導入。雑談、Q&A、しりとりはそのままでも可。

#### ver5.42
- 実現可能性評価法(Feasibility Assessment Technique; FAT)機能
「FAT」で発動します。
計画策定のおてつだい♪
初回時は初期化のため、2回FATの必要あり。

#### ver5.41
- 翻訳機能追加！
- ロシア語リプ機能
- ロシア語会話機能
- botの謎言語？undバグ修正
- 某AKRbotリスペクト。一定時間ごとにTL上の言葉から呟きます(実験です。このあと応用予定)。

#### ver5.40
- ○○語リプ機能
一定時間、指定言語でリプライします。英 仏 独 露  韓朝 西 アラビア
- △△語会話機能
 英 独
- 言語判定コマンド
- 外国語自動翻訳返答

#### ver5.39
- Node.jsをマルチコア・クラスタリング処理pm2に向上
- 600秒ごとの自動再起動
- stream取得漏れ(仕様)を2分ごとに再取得(DMのみ)
- mongoDBの32bit制限で、データフレームデフラグ
- 並列処理化
- しりとりのバグフィックス

#### ver5.38
- しりとりの字数縛り機能、開始時語彙指定機能
- うみもんのバグ修正および改良。
- 「つーる」から様々な機能にアクセス。多分、イケるはず。表示が変な場合は「リセット」大目に見て下さい
- 「なんでも」に反応
- 「フォロバ」機能
- ツイ消に極々低確率で反応。ツイートのidを晒します(といっても、アカウントidではないので、何かあるわけではないです)。
- ふぁぼに反応。よろこびます。

#### ver5.37
- エラーでてました。修正。
- ぬるぽ→ガッ 機能
- うみもんの経験値調整 回復アイテム「ほむまん」と「炭酸」が使用可能に。
- うみもんの経験値継続化
- しりとりの改善(字数制限はまだ)
- しりとり中に「show」で一覧

#### ver5.36
- しりとり機能の開発。
- APIを用いず独力で回答するようにしました。「しりとり」で開始できます。
まだまだデータベースがスカスカですが、しりとりで出会った単語は全て覚えます。
- これ迄のも「しりとりしよう」などで使えます。

#### ver5.35
- バグフィックス全般
- 自動リフォローの整備
- ふぁぼへの対応(準備)
- 無限会話阻止の方策追加
 - 過去に遡ってのメンションは無視されます。
- 引用リツイートの確率を1%→0.5%に下げました(多スギィと苦情があったので。)。

#### ver5.34
- 対戦ゲーム機能を導入しました。
おとのきざかもんすたーず(仮)
ツイッターの仕様度合やこのbotとの関わり方で強くなります。
- 「うみもん」で開始できます。
- まだまだバグが多いのでβ提供です。
- メンションが晒されるバグ

#### ver5.33
- データベースをJSONからMongoDBにしました。
- MongoDBでTLの全ツイートを保存し解析するようにしました。
- 引用RTの確率を10%から5%に引き下げました。
- バグフィックス

#### ver5.32
- Pythonとの連携
- Debian jessieeへのupgrade
- numpyで構造化モデリング手法(Interpretive Structural Modeling; ISM法)を実装しました。複雑な要素間の関係を簡単に紐解きます。
- バグフィックス

#### ver5.31
- TLの2%に無差別に話しかけるようになりました。
- 初回会話の際に、引用RTから始めることができるようになりました(10%)。
- eStat検索機能からデータを取り出せるようになりました。まだ雑ですけれど。
- 内部管理機能の追加
- コードのスリム化

#### ver5.30
- eStat検索機能が付きました(現在は、検索ワードの10件件名表示するだけです。)。(DMのみ)(クレジットは下)
- TL内の話題の寄り方監視とリアルタイム描写サーバーへ接続出来るようになりました。応用を考えていきます。

#### ver5.29
- キーワード抽出機能「キーワード」
- 花陽モノマネ機能(半角カタカナ化機能)「半角」あるいは「花陽」(要望にお応えして)
- リプライ回数のカウント機能の導入。一定回数を超えた連続リプライの場合、ストップします。

#### ver5.28
- 感性解析機能を導入しました。100種類弱の感性を解すようになりました。現在は、感性解析モードのみで動作します。今後は、コア部分への応用を模索。
- バグを修正しました。

#### ver5.27
- 文脈を「忘却」する機能が付きました。
- スパム攻撃を自動回避するようになりました。
- 何度も会話し続けて迷惑かけると、拗ねて無視するようになりました(旧来の確率無視は削除。)。
- 定期ツイートを再開しました。

#### ver5.26
- 危険内容判定機能を充実。複数要素で構成されている場合、割合まで提示できるようになりました。
- 形態素解析機能の追加。「形態素解析」で後ろの文を形態素解析します。
- 循環参照問題を解決。

#### ver5.25
- 鍵アカやDMでも即時返信ができるようになりました。
- データ処理を簡略化して、かなり高速化しました(返信2〜3秒)。
- 低確率で返信をサボるようにしました(対bot無限会話です。)。無視されたら、連投してみて下さい。

#### ver5.24
- 絵文字や特殊文字が来ても対応できるようになりました。
- しりとり時に他の機能に移行しないようにしました。しりとりは、「しりとりおわり」か「はじめまして」で初期化するかで強制終了できます。
- 処理高速化安定化

#### ver5.23
- バグフィックス
- callbackベースからthenableベースへ全面移行。async処理の強化
- コードのモジュール化
- 高階関数による高速化と安定化
- エラー処理能力向上

#### ver5.22
- 文脈管理機能の導入。話し相手それぞれで文脈を使い分けるようになりました。「はじめまして」でリセットされます。
- 自動要約機能の公開 DMでツイートサイズに要約してくれます。1万字まで対応。
- 多分バグある…

#### ver5.17
- 有害センシティブ情報のフィルタリング機能搭載。際どい言葉を回避します。
- 危険度判定機能。「危険判定」という語を含めたツイート全体の危険度及びそのカテゴリーを返します。
e.g.) 宗教関連→一般宗教かカルト宗教か など。

#### ver5.12
- 他Twitterアカウントの模倣機能が追加されました。そのうち、発言の幅が広がります。

#### ver5以降
- node.js
- javascript&typescriptに移行

#### ver5以前
- python時代
- pythonによるword2vec-modelを用いた連想機能
- (現在は、サーバー計算能力を考慮して停止中)

#### それ以前...
かつては、凛botでした。wikipediaを回って学習するという機能。しかし、wikipediaの過学習という失敗とサーバー代が捻出できず停止しました。

## API & credits etc...
- mecab
- cabocha
- tensorflow & skflow
- mecab-ipadic-neulogd (@overlast 様)
- eStat API
	- credit:「このサービスは、次世代統計利用システムのAPI機能を使用していますが、サービスの内容は総務省統計局又は独立行政法人統計センターによって保証されたものではありません。」
- 本programの生成する文章・情報等に基づいて被ったいかなる被害、損害、トラブルについて、 作成者は一切責任を負いかねます。
- 本programの運営の永続性は保証できないです。

