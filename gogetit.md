# Go Get It in Unknown Envrionment
このタスクでは，新たなロボットが家庭に導入された際に，人がその家庭の様々な情報をロボットへ教示することで，ロボットが知識を獲得することを想定している．特に家具や物体の配置・呼び方などを対象として，人とのインタラクションを通してロボットが新たな知識を獲得すること，またその知識を実環境の中で汎化して利用することを目的として，これらの性能を評価する．

**現在ルール策定中ですので，今後変更となる可能性があります．**

## Focus
1. HRIによる効率的な知識獲得
1. 獲得した知識の汎化
1. モバイルマニピュレーション
1. オンラインマッピング

## Task
1. **Traning Phase** 
	* ドアオープンによりロボットと，ロボットへの教示を行うチームメンバー1名（教示者）が入場．

	* 教示者はロボカップ＠ホームのルールに反しない範囲で，ロボットに部屋内に配置された5つ未知物体の特徴・名称・物体の位置等を教示する．以下の行為は原則として禁止である．

		- キーボード・マウス・タッチパッド等の入力機器からの入力
		- 教示者が所持している機器（ノートPC，スマートフォン等）からの入力

    * 教示終了後に指定された場所へロボットを移動させ，チームメンバーがTraning Phaseを終了することを審判に宣言する．

1. **Test Phase**
    以下を5回繰り返す．

    * 審判は，特定の物を持ってくるような指示文「Bring me \*. 」を生成する．物体をそのカテゴリ，見た目，位置などで特定できるような指示文となるが，どのような単語が使われるかは公開されない．以下が指示文の一例である．

		- 「Bring me a juice near the standing person. 」
		- 「Bring me a red object in front of the TV. 」
 
	* 指定場所でチームメンバー（指示者）がロボットに特定の物を持ってくるように「Bring me \*. 」と音声にて指示をする．

	* ロボットが指示文を認識できない場合や指示者が言い間違えた場合，指示者は合計3回まで同じ指示文をロボットへ与えることができる．また，チームの判断により，次の指示へと移行できる．その場合は，与えられた指示は失敗とみなされる．

	* ロボットは，指示者に対して実行していいかの確認のみを行うことができる．その際，指示者が発して良い単語は「Yes」または「No」のみである．また，明らかに「No」と答えるべき質問に，「Yes」と答えることはできない．

	* ロボットは指示された物を掴み，指定された場所へ戻り，物体を指示者に手渡す．

	* もし，ロボットが誤った物体を持ってきてしまった場合には，その物体は再度フィールド内へと戻される．

## Additional Rules and Remarks
* **リスタート:** チームは1回のみリスタートをすることができる．本タスクではGeneral Ruleにある再開に要する制限時間は設けない．ただし，タスク全体の制限時間内に復帰できない場合には，そこでタスクは終了となる．リスタートを宣言した場合，物体配置，対象となる物体などは変更される．

* **部屋と指定場所:** タスクで使用する部屋と，ロボットが戻ってくる指定場所は前日にアナウンスされる．

* **物体配置:** 物体は学習対象の物体以外の物体も置かれている．Traning Phase終了後，物体を10cm程度移動させる．

* **家具配置:** 家具の配置はタスク開始30分前に変更される．変更後，部屋へ入ることはできない． さらに，チームごとに家具の配置が変更となることがある．

* **手法の公開:** 本タスクで使用した手法・プログラムを論文・Webで公表した場合，加点される．論文・Webページは，タスク前日のチームリーダーズミーティング後に，実行委員へメールにて送付すること．実行委員で審議し，公表内容によっては加点とならない場合もある．また，ただ単にソースコードを公開するだけでは加点しない．必ず， *どのように本タスクの問題を解いているのか* を説明したReadMeやPDFも公開すること．

## OC Instruction

* **環境中に立つ人:** 環境中に立ってもらう人として1名以上のボランティアを事前に依頼する．

* **指示文・環境の確認:** 生成された指示文によって物体を特定できているかを複数人で確認する．

## Score Sheet

タスクの制限時間は10分である．
配点は今後公開予定．