# AJACSオンライン8 「ウェブツールを使ってゲノム編集の標的サイトを検索する」

PDFの資料を参照されている方へ

講義資料はリンク先のウェブページを元にしています。ウェブページでは画像なども交えていますのでこちらを参照されながら受講いただくことをオススメいたします。

講義資料リンク：[https://github.com/KazukiNakamae/AJACS-training](https://github.com/KazukiNakamae/AJACS-training)

----

プラチナバイオ株式会社 兼
広島大学 ゲノム編集イノベーションセンター   
[中前和恭](https://researchmap.jp/knakamae)
nakamae@pt-bio.com
2021年8月19日（木）
AJACSオンライン8

----

これは統合データベース講習会 AJACSオンライン8「ウェブツールを使ってゲノム編集の標的サイトを検索する」の講習資料です。  
講習会全体のプログラムは[こちら](https://biosciencedbc.jp/event/ajacs/ajacs89.html)です。
© 2021 中前 和恭, [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/deed.ja)

----
## 自己紹介
- [中前 和恭](https://researchmap.jp/knakamae)  
  - プラチナバイオ主任研究員 兼 広島大学ゲノム編集イノベーションセンター研究員
  - 研究分野：ヒト培養細胞を用いたゲノム編集実験・解析・インフォツールの開発
  - 開発ソフト
    - MMEJノックイン設計支援ソフト[PITCh designer](https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/index.html)
      - [サイトリンク](https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/index.html)
    - 変異プロファイリングツールMaChIAto
    - ゲノム編集専用データ基盤Genome Editing Cloud(プラチナバイオ・広島大学・凸版印刷による共同開発中)
      - [プレスリリース](https://www.toppan.co.jp/news/2021/03/newsrelease210305_1.html)
  - 講師歴
    - 第2・3・4・5回ゲノム編集講習会（日本ゲノム編集学会主催）
      - [日本ゲノム編集学会](http://jsgedit.jp)
  - [researchmap](https://researchmap.jp/knakamae)
  - [Twitter](https://twitter.com/kazuki_nakamae)

----
## 概要

本講習では、だれでも無償かつ自由に使うことができるウェブツールを活用して、適切なゲノム編集を行うための標的検索とその考え方について学びます。

また、さまざまな目的に特化した標的選定やゲノム編集後の解析に活用できるツールについてもできる限りご紹介します。

----

## 講習の流れ
今回の講習では、以下の内容について説明します。

- 1章. ゲノム編集を使ってノックアウトのための標的を設計する
  - CRISPR-Cas9を使ったノックアウト設計
    - CRISPRdirect
    - CRISPROR
  - CRISPR-Cas9を使ったノックアウト結果の予測
    - Microhomology-Predictor
    - InDelphi

- 2章. より応用的なゲノム編集のためのデータベース・ツールを知る
  - ゲノム編集のためのデータベース・ツール一覧
  - CRISPR-Cas9によるノックイン設計ツール：PITCh designer 2.0
  - TALENによるノックアウト設計ツール：TALEN Targeter
  - Base Editorによる塩基編集設計ツール：BE-Designer
  - Base Editorによる塩基編集予測ツール：BE-Hive
  - Prime Editorによる小規模編集設計ツール：PrimeDesign
  - Cas13によるRNA編集設計ツール：Cas13design
  - サンガーシーケンスデータを使った変異分析ツール：TIDE
  - アンプリコンシーケンシングデータを使った変異分析ツール：CRISPResso2
  - UCSC genome browserでのCas9標的の確認
  - ガイドRNA先行研究データベース：dbGuide
  - template-freeゲノム編集データベース：MHcut Browser
- 3章. ゲノム編集情報の安全な設計・解析・管理ツール
  - GGGenome（+パッケージ版）によるオフターゲット検索
  - ゲノム編集専用データ基盤Genome Editing Cloud
- 0章. 補遺
  - NCBIから遺伝子の配列情報を取得する
  - SnapGeneViewerで配列情報をわかりやすく表示する

## 講義に際して
- 今回はウェブツールを紹介しますが、同時にアクセスするとサイトにつながりにくくなる可能性があります。私自身はスムーズな進行のために資料のスクリーンショットを追っていく形式で説明していきます。受講者の方は説明を聴きながら実際に手を動かしてもらっても大丈夫ですし、ただ聴いてもらうだけでも構いません。
  - 資料を見ながら自力で進められそうな方はどんどん先に進めていっても大丈夫です。
  - タイミングをずらして実行するとうまくサイトに接続できる場合があります。

----

#### 受講前アンケートにご協力いただき、ありがとうございます (回答数 184名)(8/3時点)

|受講申込者の専門分野|人数|
|:--|--:|
|生物科学|60 名|
|基礎医学|41 名|
|バイオインフォマティクス|33 名|
|基礎生物学|32 名|
|農学|32 名|
|臨床医学|30 名|
|ゲノム科学|29 名|
|情報学|12 名|
|基礎化学|5 名|
|複合化学|3 名|

多種多様な分野の方にご参加いただきありがとうございます。
ゲノム編集は上に挙がった分野の全てで関わりがある分野なので皆様の役に立つ講義になれば幸いです。

---
|ゲノム編集の原理の説明を聞いたことがありますか？ |人数|割合|
|:--|--:|:--:|
|ある|153 名|87.9 %|
|ない|21 名|12.1 %|

本講義ではウェブツールを使った実際的な標的検索について説明するので、基本原理は事前に知っているほうが望ましいです。

講義内でもできる限り原理がわかるように説明しますが、心配な方は以下の動画等で事前学習されるとよいかもしれません。

[ゲノム編集とは|イントロダクション（2分）](https://www.mls.sci.hiroshima-u.ac.jp/smg/GEIN/genome-editing/chapter1.html)

[ゲノム編集とは|タンパク質ツールによるDNA切断（2分）](https://www.mls.sci.hiroshima-u.ac.jp/smg/GEIN/genome-editing/chapter2.html)

[ゲノム編集とは|複合型ツールによるDNA切断（2分）](https://www.mls.sci.hiroshima-u.ac.jp/smg/GEIN/genome-editing/chapter3.html)

[ゲノム編集とは|非相同末端結合（NHE-J)によるDNA修復（2分）](https://www.mls.sci.hiroshima-u.ac.jp/smg/GEIN/genome-editing/chapter4.html)

[ゲノム編集とは|相同配列依存的修復（HDR）によるDNA修復（2分）](https://www.mls.sci.hiroshima-u.ac.jp/smg/GEIN/genome-editing/chapter5.html)

---
|ゲノム編集のウェット実験を行ったことはありますか？ |人数|割合|
|:--|--:|:--:|
|ある|62 名|35.6 %|
|ない|112 名|64.4 %|

本講義は原理は知っているものの今までゲノム編集実験をしたことがない方をメインに据えているのでご参考になるかもしれません。

行ったことがある方にとってはご自身の方法と比較してみて疑問に感じる部分もあるかもしれません。その際にはご質問いただければ幸いです。

---
|アンプリコンシーケンスでゲノム編集サンプルの分析を行ったことがありますか？ |人数|割合|
|:--|--:|:--:|
|ある|15 名|8.8 %|
|ない|156 名|91.2 %|

ゲノム編集実験では設計した後に変異検出も行う必要がありますのでアンプリコンシーケンスは知っていても損はないかと思います。

本講義ではメインである１章では取り扱わない内容ですが、2章以降でこの辺りについて少し触れたいと思います。後の質疑応答で詳しくお尋ねいただいても大丈夫です。

---

## ゲノム編集とは？

ゲノム編集は、人工的な生体分子を使って配列特異的にゲノム配列を改変する技術を指します。

最も基本的なものは、TALENやCRISPR-Cas9などのゲノム編集ツールを使ってDNAに二本鎖切断を導入し、その際に発生するDNA修復経路を介して変異導入します。

![](/images/0a.png)
*ゲノム編集産業化ネットワークより引用*


特に、Cas9ヌクレアーゼとガイドRNAの複合体で編集するCRISPR-Cas9では、ガイドRNAのなかにあるわずか20塩基程度のプロトスペーサ配列を置換するだけで様々なゲノム配列を狙うことができます。

![](/images/0b.png)
*ゲノム編集産業化ネットワークより引用*

こうした変異導入によって遺伝子を破壊するノックアウト、あるいは任意の配列を好きな領域へ挿入するノックインなどが行えます。

ゲノム編集によるノックアウトでは、コード領域を標的にして、コドンの読み枠をずらすようなフレームシフト変異をゲノム編集ツールで誘導して実現するのが基本です。

しかしゲノム内の様々な標的を狙うことができるゲノム編集ツールですが、必ずしも完全ではなく、実験者が意図していない標的配列を切断するケースもあります。これをオフターゲットと呼んでいて、ゲノム編集の設計において最も懸念すべき要素の一つです。

本講義ではそういったオフターゲット等についても具体的な判断を述べながら説明していきたいと思います。


重要用語とその説明をここにメモしておきましょう。

- ゲノム編集：人工的な生体分子を使って配列特異的にゲノム配列を改変する技術
- ゲノム編集ツール：ゲノム編集を行うために使われる生体分子（タンパク質・核酸分子）
- CRISPR-Cas9：ゲノム編集ツールの一つ。DNAを切断する"Cas9ヌクレアーゼ"と任意のゲノム配列を認識する"ガイドRNA"の複合体を使って生体内のゲノムDNAを配列特異的に切断することができる
  - プロトスペーサー：ガイドRNAの一部分。この部分を標的としたいゲノムに対して相補的に結合するように設計することで、CRISPR-Cas9は任意のゲノム配列を認識することができる。
  - PAM配列：Cas9ヌクレアーゼがもつDNA結合モチーフ。特定の配列モチーフがないとCas9ヌクレアーゼはDNA切断活性を発揮しない。ガイドRNAは自由に設計できるが、このPAM配列は変えることができないので、これがCRISPR-Cas9システムにおける制約となっている。
- TALEN：ゲノム編集ツールの一つ。DNAを切断する"FokIヌクレアーゼ"と任意のゲノム配列を認識する"TALEタンパク"との融合タンパクとなっている。
- ノックアウト：特定の遺伝子の機能を不活性化させるためのゲノム操作を指す。様々な実現方法があるが、ゲノム編集ではタンパクコード領域にフレームシフト変異を誘導してアミノ酸配列情報を破壊する方法が一般的。
- ノックイン：特定の配列を特定のゲノム領域に挿入するゲノム操作を指す。
- オンターゲット：実験者が意図している標的配列、またはそれに対する切断を指す。
- オフターゲット：実験者が意図していない標的配列、またはそれに対する切断を指す。これによってランダムな表現型が導かれて正しくない考察に繋がってしまう可能性がある。あるいは治療や品種改良のうえではリスクとなり得るのでなるべく避けるように設計することが重要。

---

## 1章. ゲノム編集を使ってノックアウトのための標的を設計する

### CRISPR-Cas9を使ったノックアウト設計

#### ノックアウトについて

  - 遺伝子の機能を消失させるノックアウト法にはさまざまな方法が知られています。一種類のCRISPR-Cas9を使ったランダム変異導入や複数のCRISPR-Cas9を使ったラージデリーション導入、TALENによる変異導入、そして古典的なノックインによるノックアウトなどが知られています。今回の標的選択では現在最もシンプルな方法として知られている一種類のCRISPR-Cas9を使ったランダム変異導入を考えてみます。
  - ノックアウトを行う位置に関してですが、単純に遺伝子を破壊したいという場合であれば開始コドンの直下のExon領域をターゲットにして、ゲノム編集でフレームシフトを発生させる方法が一般的です。これによって中途半端な翻訳産物を生み出すことなく、多くの場合において遺伝子の発現を完全に抑えることが可能です。
  - 標的を選ぶ際にはできる限りしっかりとアノテーションがついた情報を参照するようにしましょう。本資料末尾にある0章ではNCBIから遺伝子情報をダウンロードしていますが、こうしたものでは一つの遺伝子に対して複数種のアイソフォームが割り当てられているものがあります。完全にノックアウトを行いたい場合はなるべく全てのアイソフォームに重複するExon領域でゲノム編集のターゲットを選択するようにしてください。

  - MYOG遺伝子座（myogeninをコード）の場合
  ![](/images/6a.png)
  ※ MYOPARRはMYOGのプロモータに関わるnon-coding RNA
  ![](/images/1i.png)

  - 場合によっては転写産物にバリアントが存在しているケースがあります。こういった場合は全てのバリアントで重複しているコード領域を見つけてノックアウトを設計するほうがいいでしょう。

  - TSC2遺伝子座（tuberinをコード）の場合
  ![](/images/6b.png)

  - またコード領域が他の遺伝子と被っていたりするケースがあります。特定の遺伝子のノックアウトの表現型をとりたい場合は、なるべく他の遺伝子のコード領域を破壊しないように設計場所を選ぶほうが無難です。あるいは他の遺伝子ではサイレント変異となるような改変の導入を検討してもいいかもしれません。

  ![](/images/6c.png)

  - ノックアウトの結果、事前情報からでは想定できなかった転写・翻訳産物が出現するケースもあります。また設計上仕方なく損傷を与えてしまった遺伝子についても発現が変わってしまっている恐れがあります。実験後はゲノム配列の確認とともに、周辺遺伝子のqPCR、ddPCR、ウェスタンブロット等で発現レベルを確認することも必要に応じて検討してみてください。

---

#### [CRISPRdirect](https://crispr.dbcls.jp)
- CRISPR-Cas9標的を検索できるウェブツール。特にオフターゲット作用を考慮した検索が可能。
    - [https://crispr.dbcls.jp](https://crispr.dbcls.jp)
    - [論文リンク](https://doi.org/10.1093/bioinformatics/btu743)
    - [紹介動画 - 統合TV](https://doi.org/10.7875/togotv.2014.025)
    トップページ
    ![](/images/1a.png)      
    検索にヒットした標的候補一覧表
    ![](/images/1b.png)
    標的候補の位置関係
    ![](/images/1c.png)
    データ出力も可能です。
    ![](/images/1d.png)
    ![](/images/1e.png)
- 標的候補一覧表の見方
  ![](/images/1f.png)
  - "position"
    - "start - end"はターゲットの位置になります。
    - "+-"はゲノムリファレンス上でどちらのstrand属するかを指します。
  - "target sequence"
    - "target seqeunce"が標的とする配列です。 四角で囲まれているのがPAM結合サイトであり、それ以外の部分はガイドRNAがもつprotospacer配列を指します。
  - "sequence information"
    - "GC% of 20mer"や"Tm of 20mer"はprotospacer配列のGC%・Tm値を指します。
    - "TTTT in 20mer"はprotospacer配列に4連続するTがあるかどうかを指します。こうした配列はプロモータによっては転写終結シグナルとなるため使用を避けた方がよいです。
    - "restriction sites"はそこに制限酵素サイトがあるかどうかを示します。ゲノム編集の解析をする場合には編集した箇所で作用する制限酵素を使って変異導入の有無を電気泳動で確認する方法があります（RFLP法）。ここで示されている制限酵素はそういった検証に利用可能です。
  - "number of target sites"
    - "20mer+PAM"はPAM結合サイトとプロトスペーサー配列のゲノム上での特異性を指します。
      - 1の場合はゲノム上に1つしかないということを表します。
      - それ以上の場合は、目的でない結合箇所（オフターゲットサイト）がゲノム上に数カ所あるということになります。
      - 0の場合はゲノム上に存在しないことを表します。成熟mRNA配列などから配列を取得した場合ではExonのつなぎ目領域でこのような結果になることがあります。こうしたものは基本的にターゲティングできません。
    - "12mer+PAM"や"8mer+PAM"はPAM結合サイトとプロトスペーサー配列の3´末端から12bp, 8bpのゲノム上での特異性を指します。SpCas9の特異性は位置依存的であることが知られており、3´側に位置するほど特異性が高くなる傾向があります。3´末端から12bp, 8bpの領域で一致するオフターゲットサイトが大量にある場合はゲノムに対して意図しない変異導入を大量に起こしてしまう可能性が高く、ゲノム編集の標的として適切とはいえません。
    - "detail"をクリックすると、検索にヒットした標的配列あるいはオフターゲットサイトがゲノム上のどのあたりに存在するか参照することが可能です。
      - "≤1 mismatch/gap"または"≤2 mismatch/gap"をクリックすることで、ミスマッチ・ギャップを含むオフターゲットサイトも表示することもできます。
      ![](/images/1g.png)

----

#### 【使用例】CRISPRdirectを使って、ノックアウトのための標的を設計する

1. 検索配列を入力します。
![](/images/1h.png)

2. 配列はSnapGene Viewerからドラッグ->コピーで取得します。今回は開始コドンから159bpを取得します。

入力配列：

\>MYOG
atggagctgtatgagacatccccctacttctaccaggaaccccgcttctatgatggggaaaactacctgcctgtccacctccagggcttcgaaccaccaggctacgagcggacggagctcaccctgagccccgaggccccagggccccttgaggacaag

![](/images/1i.png)
![](/images/1j.png)

3. Cas9のPAM配列を入力します。今回は最も一般的なSpCas9の"NGG"とします。

PAM配列：NGG

![](/images/1k.png)

4. 特異性を確認するゲノムを指定します。今回は最新のヒトゲノムリファレンスである"Human (Homo sapiens) genome, GRCh38/hg38 (Dec, 2013)"とします。
ゲノム：Human (Homo sapiens) genome, GRCh38/hg38 (Dec, 2013)
![](/images/1l.png)

5. "design"をクリックします。
![](/images/1m.png)

6. Resultsの表示を確認します。
![](/images/1n.png)

7. ゲノムに対して特異的なターゲットを表示するために、"show highly specific target only"にチェックをいれて更新します（更新は自動で行われます）。
![](/images/1o.png)

8. "20mer+PAM"が1で、なおかつ"12mer+PAM"と"8mer+PAM"の数がなるべく少ない標的を選択し、配列をコピーします。
![](/images/1p.png)

9. SnapGene Viewerを開き、Edit -> Find -> Find DNA sequenceで配列検索スペースを開き、選択したプロトスペーサ配列"accaccaggctacgagcgga"を検索する
![](/images/1q.png)
![](/images/1r.png)

9. 緑色で表示されたプロトスペーサ配列"accaccaggctacgagcgga"とその3´末端に隣接するPAM結合サイト"cgg"にフィーチャーをつける。ストランドが把握しやすいように工夫する。
![](/images/1s.png)
![](/images/1t.png)
![](/images/1u.png)

10. プロトスペーサ配列"accaccaggctacgagcgga"をもったガイドRNAを発現させるマテリアル（ベクター等）の作製に用いる一本鎖オリゴヌクレオチドを設計して注文する。

- （例）U6プロモータを介したガイドRNA発現ベクターを作製する場合
  1. U6プロモータを使ってガイドRNAを発現させる場合は、プロトスペーサ配列の5´末端がGでなければならない。
  2. また、[Addgene](https://www.addgene.org/)に寄託されている[pX330-U6-Chimeric_BB-CBh-hSpCas9プラスミド](https://www.addgene.org/42230/)などに対してBpiIによる制限酵素処理&ライゲーションでプロトスペーサ配列を組み込む場合には、BpiIに適合した突出末端を形成するようにアダプター配列をつけておく必要がある。
  - (i)(ii)を考慮した場合、プロトスペーサ配列"accaccaggctacgagcgga"をもったガイドRNAを発現させる[pX330-U6-Chimeric_BB-CBh-hSpCas9プラスミド](https://www.addgene.org/42230/)を作製するには下記の二種類の一本鎖オリゴヌクレオチドが必要となる。
    - `5´-caccGaccaccaggctacgagcgga____-3´`
    - `3´-____Ctggtggtccgatgctcgcctcaaa-5´`

11. 一本鎖オリゴヌクレオチドを注文します。
  - FASMACの場合：ウルトラオリゴ/逆相カラム精製/修飾なし
![](/images/1v.png)
FASMACのオリゴDNA注文画面

12. 注文後、CRISPR-Cas9システムを動かすためのマテリアルの作製を行い、ゲノム編集実験を行う。詳しくは下記の参考文献を参照してください。

##### 参考文献
  * [Ran, F., Hsu, P., Wright, J. et al. Genome engineering using the CRISPR-Cas9 system. Nat Protoc 8, 2281–2308 (2013).](https://doi.org/10.1038/nprot.2013.143)
  * [Zhang Lab CRISPR Plasmids](https://www.addgene.org/crispr/zhang/)
  * [山本 卓、佐久間 哲史（2019）.「完全版 ゲノム編集実験スタンダード〜CRISPR-Cas9の設計・作製と各生物種でのプロトコールを徹底解説 (実験医学別冊)」 羊土社](https://www.yodosha.co.jp/yodobook/book/9784758122443/)

##### 関連ツール
- [COSMID](https://crispr.bme.gatech.edu/)
  - 標的配列に対するオフターゲットサイトを予測するツール。ミスマッチ・ギャップの位置に基づいたスコアリング機能もついており、PCR等でオフターゲット解析をする場合の標的選定に活用できます。

- [Cas-OFFinder](http://www.rgenome.net/cas-offinder/)
  - 標的配列に対するオフターゲットサイトを予測するツール。ミスマッチやDNA側あるいはRNA側のギャップ（Bulge）を細かく指定できる。またCRISPRdirect同様に多くの生物種に対応している他、C57BL/6NJやFVB/NJといったマウス亜系統ゲノムでのオフターゲット検索もできます。

----

#### [CRISPROR](http://crispor.tefor.net)
- CRISPR-Cas9標的を検索できるウェブツール。標的検索だけでなく、そのオフターゲットの検索からプライマー設計までも含めた包括的な情報収集が可能。
    - [http://crispor.tefor.net](http://crispor.tefor.net)
    - [論文リンク](https://doi.org/10.1093/nar/gky354)
    - [紹介動画 - 統合TV](https://doi.org/10.7875/togotv.2021.023)
    トップページ
    ![](/images/2a.png)
    検索にヒットした標的候補のマップ（緑色が高い特異性をもつ標的）
    ![](/images/2b.png)
    検索にヒットした標的候補一覧表
    ![](/images/2c.png)
    "Cloning / PCR primers"をクリックするとガイドRNA構築に必要なオリゴヌクレオチド情報等が表示されます。
    ![](/images/2d.png)
    ![](/images/2e.png)
    ![](/images/2f.png)
    "show all..."->"Off-target primers"をクリックすると、各オフターゲットサイトに対するPCRプライマーが表示されます。
    ![](/images/2h.png)
    ![](/images/2i.png)
    ![](/images/2j.png)
- 標的候補一覧表の見方
  ![](/images/2k.png)
  - "Position/Strand"
    - 数字はターゲットの位置になります。
    - "fw/revでゲノムリファレンス上でどちらのstrand属するかを指します。
  - "Guide Sequence + PAM + Restriction Enzymes + Variants"
    - 標的の配列情報を指します。Restriction EnzymesはRFLP法で利用可能な制限酵素サイトを指します。VariantsはSNPを示しており、SNPを対象としたい場合はこの情報をもとに標的を選択することができます。
  - "MIT Specificity Score"
    - [Hsu et al. Nat Biotech 2013](https://doi.org/10.1038/nbt.2647)に基づいた特異性スコアです。高いほど特異性が高いとされ、50以上が推奨されています。
  - "CFD Spec. score"
    - [Doench et al. Nat Biotech 2016](https://doi.org/10.1038/nbt.3437)に基づいた特異性スコアです。
  - "Predicted Efficiency"
    - "Doench '16"は[Fusi et al. preprint 2015](https://doi.org/10.1101/021568)と[Doench et al. Nat Biotech 2016](https://doi.org/10.1038/nbt.3437)に基づいた予測切断活性のスコアです。CRISPR-Cas9をレンチウイルス導入したときの活性データを参考に作られています。
    - "Mor.-Mateos"は[Moreno-Mateos et al. Nat Method 2015](https://doi.org/10.1038/nmeth.3543)に基づいた予測切断活性のスコアです。CRISPR-Cas9をレンチウイルス導入したときの活性データに基づいています。CRISPR-Cas9をゼブラフィッシュの胚にインジェクション導入したときの活性データを参考に作られています。*in vivo*でのゲノム編集を行う場合にはこちらのほうがより参考になると考えられています。
  - "Outcome"
    - "Out-of-Frame"は[Bae et al. Nat Method 2014](https://doi.org/10.1038/nmeth.3015)に基づいて欠失によるフレームシフトの起こりやすさを予測したものです。値をクリックすると実際の予測変異パターンを見ることができます。
    - "Lindel"は[Wei Chen et al, Nucleic Acids Research 2019](https://doi.org/10.1093/nar/gkz487)に基づいて欠失・挿入によるフレームシフトの起こりやすさを予測したものです。値をクリックすると実際の予測変異パターンを見ることができます。
  - "Off-targets for 0-1-2-3-4 mismatches + next to PAM"
    - オフターゲットサイトの数を標的配列とのミスマッチ数ごとに表示しています。最初の数字（ミスマッチ0でのオフターゲットサイト）が0である標的が最低限特異的な標的です。
  - "Genome Browser links to matches sorted by CFD off-target score"
    - CFD off-target scoreが高い順にオフターゲットサイトが表示されています。
    - マウスオーバーするとScoreとミスマッチ領域を参照できます。
    - クリックすると[UCSC Genome Browser](http://genome.ucsc.edu/cgi-bin/hgTracks?db=hg19&lastVirtModeType=default&lastVirtModeExtraState=&virtModeType=default&virtMode=0&nonVirtPosition=&position=chr14%3A70883813%2D70883835&hgsid=1134497385_rBlE26ARXxLLm13wxuXQRiQjwHHc)にジャンプし、オフターゲットサイトの情報を細かく参照できます。

----

#### 【使用例】CRISPRORを使って、ノックアウトのための標的を設計する

1. 名前を入力します（入力しなくても可）。
MYOG
![](/images/2l.png)

2. 検索配列を入力します。
![](/images/2m.png)

3. 配列はSnapGene Viewerからドラッグ->コピーで取得します。今回は開始コドンから159bpを取得します。

入力配列：

atggagctgtatgagacatccccctacttctaccaggaaccccgcttctatgatggggaaaactacctgcctgtccacctccagggcttcgaaccaccaggctacgagcggacggagctcaccctgagccccgaggccccagggccccttgaggacaag

![](/images/1i.png)
![](/images/2n.png)

4. 特異性を確認するゲノム+SNPデータベースを指定します。今回は最新のヒトゲノムリファレンスである"Homo sapiens- Human - UCSC Dec. 2013 (GRCh38/hg38) + SNPs: dbSNP148, Kaviar"とします。

ゲノム+SNPデータベース：

Homo sapiens- Human - UCSC Dec. 2013 (GRCh38/hg38) + SNPs: dbSNP148, Kaviar

![](/images/2o.png)

5. PAM配列を指定します。今回は最も一般的なSpCas9の"NGG"とします。

PAM配列：20bp-NGG - SpCas9, SpCas9-HF1, eSpCas9 1.1

![](/images/2p.png)

6. "SUBMIT"をクリックします。
![](/images/2q.png)

7. 結果が表示されるまで待ちます。
![](/images/2r.png)

8. 標的のリストが特異性が高い順に表示されます。ノックアウトする上では特異性が高く、なおかつ切断活性が低すぎず、フレームシフトが起こりやすい標的を選ぶのがベストです。
  - 今回は次の基準で選んでみます。
  - 特異性を示す"MIT Specificity Score"と"CFD Spec. score"がいずれも90を上回る
  - 切断活性を示す"Doench '16"と"Mor.-Mateos"がいずれも25を下回らない
  - フレームシフトの起こりやすさを示す"Out-of-Frame"と"Lindel"がいずれも60を上回る
    - これを満たすのは"ACCACCAGGCTACGAGCGGA CGG"、"TCGAACCACCAGGCTACGAG CGG"の二標的となります。どちらでもよいですが今回は"ACCACCAGGCTACGAGCGGA CGG"を選んでみます。
![](/images/2s.png)

9. "Cloning / PCR primers"をクリックして、構築に必要なオリゴヌクレオチド情報を表示します。
![](/images/2t.png)
![](/images/2u.png)

10. [pX330-U6-Chimeric_BB-CBh-hSpCas9プラスミド](https://www.addgene.org/42230/)でガイドRNAを発現させたい場合は"U6 expression from an Addgene plasmid"の項目へ行き、"Select your Addgene plasmid:"で"pX330-U6-Chimeric_BB-CBh-hSpCas9(Zhang lab) + derivatives"を選択します。
![](/images/2v.png)

11. 配列が自動で更新されるので、更新された"Primers for gN20 guides"を記録します。
- gN20-guideRNA113fwU6sensepX330: CACCGaccaccaggctacgagcgga
- gN20-guideRNA113fwU6antisensepX330: AAACtccgctcgtagcctggtggtC
![](/images/2w.png)

12. 一本鎖オリゴヌクレオチドを注文します。
   - FASMACの場合：ウルトラオリゴ/逆相カラム精製/修飾なし
   ![](/images/2x.png)

13. 注文後、CRISPR-Cas9システムを動かすためのマテリアルの作製を行い、ゲノム編集実験を行います。詳しくは下記の参考文献を参照してもよいですし、"Click here"示されているリンク先のプロトコールを参照しても大丈夫です。
![](/images/2y.png)
![](/images/2z.png)

##### 参考文献
  * [Ran, F., Hsu, P., Wright, J. et al. Genome engineering using the CRISPR-Cas9 system. Nat Protoc 8, 2281–2308 (2013).](https://doi.org/10.1038/nprot.2013.143)
  * [Zhang Lab CRISPR Plasmids](https://www.addgene.org/crispr/zhang/)
  * [山本 卓、佐久間 哲史（2019）.「完全版 ゲノム編集実験スタンダード〜CRISPR-Cas9の設計・作製と各生物種でのプロトコールを徹底解説 (実験医学別冊)」 羊土社](https://www.yodosha.co.jp/yodobook/book/9784758122443/)

##### 関連ツール
- [CHOPCHOP](https://chopchop.cbu.uib.no)
  - Exonを参照しながらインタラクティブに標的を検索できるツール。
  - [統合TV](https://doi.org/10.7875/togotv.2020.083)

----

### CRISPR-Cas9を使ったノックアウト結果の予測

#### DSBによる変異導入

  - CRISPR-Cas9やTALENといったゲノム編集ツールではDNA二本鎖切断（DSB）を引き起こし、その修復の結果発生するフレームシフト変異によってノックアウトを達成されます。
  - 教科書的にはこの時の変異導入はランダムと説明されることも多いですが、実際にはある程度の傾向があることが知られています。
  - 哺乳類を問わず多くの生物種でみられるのが切断末端間にある相同配列がつながるような欠失変異パターンです。これらはMMEJ/SSAなどといった修復経路によって引き起こされることが知られています（※ゲノム編集の分野ではまとめてMMEJによる修復と呼ばれることが多い）。
  - またヒト等の培養細胞では切断面がC|Cとなっていると一塩基欠失によりC一塩基になったり、切断面でPAM側に位置しない方のTがTTに変わるといったリピート型の挿入が発生しやすかったりすることが知られています[Allen et al. Nat Biotech 2019](https://dx.doi.org/10.1038%2Fnbt.4317)。
  - このような変異パターンを事前に予測するためのツールを紹介します。

---

#### [Microhomology-Predictor](http://www.rgenome.net/mich-calculator/)
- DSBによって引き起こされるMMEJによる欠失変異パターンを予測するツール
    - [http://www.rgenome.net/mich-calculator/](http://www.rgenome.net/mich-calculator/)
    - [論文リンク](http://dx.doi.org/10.1038/nmeth.3015)
    トップページ
    ![](/images/3a.png)
    入力画面
    ![](/images/3b.png)
    検索結果
    ![](/images/3u.png)
    詳細な変異パターン情報
    ![](/images/3v.png)
- 結果画面の見方
  ![](/images/3x.png)
  - "Microhomology Score"
    - MMEJによる欠失変異のトータルでの起こりやすさを表します。
  - "Out-of-frame Score"
    - MMEJによる欠失変異の中でもフレームシフト変異となるパターンの起こりやすさを表します。
  - Microhomology：該当の変異パターンでつながる小さな相同配列（マイクロホモロジー配列）です。
  - Deletion Length：該当の変異パターンで引き起こされる欠失長を表します。
  - Pattern Score：該当の変異パターンの起こりやすさを表します。

----

#### 【使用例】Microhomology-Predictorを使って、ノックアウト結果を予測して標的を決定する

1. 今回はMYOG遺伝子の標的配列"ACCACCAGGCTACGAGCGGACGG"（No.1：ピンク色）と"TCGAACCACCAGGCTACGAGCGG"（No.2：緑色）を例にとって、どちらがノックアウトに相応しそうか調べてみます。
![](/images/3c.png)

2. まず標的配列ごとに配列を入力します。Microhomology-Predictorは入力配列のちょうど真ん中に切断サイトがくるように入力しなければちゃんと使えません。野生型SpCas9を使う場合、切断サイトはPAM結合サイトの5´末端から３塩基上流にとなります。したがって以下のような手順で入力配列を作っていきましょう。
![](/images/3d.png)
  - ゲノム情報をSnapGeneViewerを開き、標的配列を検索します。
    ![](/images/3e.png)
  - 以下のようにSnapGeneViewerで切断面を記録します。先ほども述べたように野生型SpCas9の場合、切断サイトはPAM結合サイトの5´末端から３塩基上流にとなります。
    ![](/images/3f.png)
    切断面を左クリックして"|"をあわせます。この状態で"Features"->"Add Cleavage Site..."を選択します。
    ![](/images/3g.png)
    切断面を登録するフィーチャーを尋ねられますので、"CRISPR-Cas9標的（プロトスペーサ部分）No.1"を選択します。
    ![](/images/3h.png)
    フィーチャー設定画面がでてくるのでOKを押します。
    完了すると、"CRISPR-Cas9標的（プロトスペーサ部分）No.1"のフィーチャー表示に"↑"マークがつけられます。これが切断面の表示です。
    ![](/images/3i.png)
  - 以下のように切断面から5´方向40bpに"Left_reference"というフィーチャーをつけます。
    ![](/images/3j.png)
    5´方向40bpの配列をドラッグして、"Features"->"Add Features..."をクリックします。
    ![](/images/3k.png)
    フィーチャー名を入力してOKを押します。好みで色をつけておくとわかりやすいです。
    ![](/images/3l.png)
    フィーチャーが反映されます。
  - 切断面から3´方向40bpに"Right_reference"というフィーチャーをつけます。
    ![](/images/3m.png)
    3´方向40bpの配列をドラッグして、"Features"->"Add Features..."をクリックします。
    ![](/images/3n.png)
    フィーチャー名を入力してOKを押します。好みで色をつけておくとわかりやすいです。
    ![](/images/3o.png)
    フィーチャーが反映されます。
  - "Left_reference"と"Right_reference"の部分をドラッグして、配列をまとめてコピーします。そしてその配列をサイトに入力します。
    ![](/images/3p.png)
    ![](/images/3q.png)

標的配列が"ACCACCAGGCTACGAGCGGACGG"の入力配列：

cctgtccacctccagggcttcgaaccaccaggctacgagcggacggagctcaccctgagccccgaggccccagggcccct

![](/images/3r.png)
一つの配列を入力したら、"Add"をクリックして入力フォームを追加して、次の配列を入力します。

標的配列が"TCGAACCACCAGGCTACGAGCGG"の入力配列：

cctgcctgtccacctccagggcttcgaaccaccaggctacgagcggacggagctcaccctgagccccgaggccccagggc

![](/images/3s.png)

3. Submitを押します。
![](/images/3t.png)

4. 結果が返ってきます。フレームシフトに起こりやすさを示す"Out-of-frame Score"を記録しておきましょう。66を上回っていればノックアウト標的としては適していると考えられています。今回のケースではどちらの場合も条件を満たしているのでより詳しく見比べてみるのがよいでしょう。
![](/images/3u.png)

5. 配列をクリックすると、予測されるMMEJ欠失パターンが表示されます。変異パターンはその起こりやすさの順で並べられています。標的"ACCACCAGGCTACGAGCGGACGG"の場合はトップに9塩基欠失というフレームイン型変異があり、一方で標的"TCGAACCACCAGGCTACGAGCGG"の場合はトップ8までの変異が全てフレームシフト型の変異となっています。この結果では"TCGAACCACCAGGCTACGAGCGG"のほうがノックアウト標的としては適していそうです。
![](/images/3v.png)
![](/images/3w.png)

補足ですが、標的の選定は変異パターンだけでなく、オフターゲット率なども含めて総合的に判断するのが理想的です。
今回のようにどちらも"Out-of-frame Score"が66以上であるという場合はオフターゲット率や次に紹介する"inDelphi"のような別ツールでの判定結果を判断材料にしてもいいでしょう。
各自の実験デザインに応じて判断していくのがよいのではないかと思います。

----

#### [inDelphi](https://indelphi.giffordlab.mit.edu)
- CRIPSR-Cas9によるDSBによって引き起こされる一塩基挿入・欠失変異パターンを予測するツール
    - [https://indelphi.giffordlab.mit.edu](https://indelphi.giffordlab.mit.edu)
    - [論文リンク](https://doi.org/10.1038/s41586-018-0686-x)
    ページ画面
    ![](/images/4a.png)
    入力画面
    ![](/images/4b.png)
    予測される変異パターンのアライメント
    ![](/images/4c.png)
    予測される変異パターンのヒストグラム
    ![](/images/4d.png)
    過去データとの比較（予測結果の評価）
    ![](/images/4e.png)
    予測変異パターンの一覧
    ![](/images/4f.png)
- "Comparison to predictions at 13,273,449 SpCas9 target sites in human exons and introns"の見方
  ![](/images/4e.png)
  - "Precision score"は変異の多様度予測したものとなります。この値が高いと細胞集団に対してゲノム編集した際に単一、もしくは少数の変異パターンに収束しやすいことを示します。もしこれが低いとモザイク度の高い編集となる可能性があります。
  - "Microhomology strength score"はマイクロホモロジー配列を介した変異が起こりやすいかどうかを示します。これが低い場合はNHEJ修復のようなマイクロホモロジー配列を介さないランダム性の高い変異が出現しやすくなると考えられます。
  - "Frameshift frequency"はインデルによるフレームシフトの起こりやすさを示します。

----

#### 【使用例】inDelphiを使って、ノックアウト結果を予測して標的を決定する

1. 今回はMYOG遺伝子の標的配列"ACCACCAGGCTACGAGCGGACGG"（No.1：ピンク色）と"TCGAACCACCAGGCTACGAGCGG"（No.2：緑色）を例にとって、どちらがノックアウトに相応しそうか調べてみます。
![](/images/3c.png)

2. 標的配列ごとに配列を入力します。inDelphiは切断面を境界として5´側、3´側配列（各40bp程度を推奨）を入力する必要があります。
  - ゲノム情報をSnapGeneViewerを開き、標的配列を検索します。
    ![](/images/3e.png)
  - 以下のようにSnapGeneViewerで切断面を記録します。先ほども述べたように野生型SpCas9の場合、切断サイトはPAM結合サイトの5´末端から３塩基上流にとなります。
    ![](/images/3f.png)
    切断面を左クリックして"|"をあわせます。この状態で"Features"->"Add Cleavage Site..."を選択します。
    ![](/images/3g.png)
    切断面を登録するフィーチャーを尋ねられますので、"CRISPR-Cas9標的（プロトスペーサ部分）No.1"を選択します。
    ![](/images/3h.png)
    フィーチャー設定画面がでてくるのでOKを押します。
    完了すると、"CRISPR-Cas9標的（プロトスペーサ部分）No.1"のフィーチャー表示に"↑"マークがつけられます。これが切断面の表示です。
    ![](/images/3i.png)
  - 以下のように切断面から5´方向40bpに"Left_reference"というフィーチャーをつけます。
    ![](/images/3j.png)
    5´方向40bpの配列をドラッグして、"Features"->"Add Features..."をクリックします。
    ![](/images/3k.png)
    フィーチャー名を入力してOKを押します。好みで色をつけておくとわかりやすいです。
    ![](/images/3l.png)
    フィーチャーが反映されます。
  - 切断面から3´方向40bpに"Right_reference"というフィーチャーをつけます。
    ![](/images/3m.png)
    3´方向40bpの配列をドラッグして、"Features"->"Add Features..."をクリックします。
    ![](/images/3n.png)
    フィーチャー名を入力してOKを押します。好みで色をつけておくとわかりやすいです。
    ![](/images/3o.png)
    フィーチャーが反映されます。
  - "Left_reference"と"Right_reference"の部分をそれぞれドラッグして、配列をコピーします。そしてサイトの左側フォームと右側フォームに入力します。
    ![](/images/3p.png)
    ![](/images/3q.png)

標的配列が"ACCACCAGGCTACGAGCGGACGG"の入力配列：

左側フォーム：cctgtccacctccagggcttcgaaccaccaggctacgagc

右側フォーム：ggacggagctcaccctgagccccgaggccccagggcccct

![](/images/4g.png)

標的配列が"TCGAACCACCAGGCTACGAGCGG"の入力配列：

左側フォーム：cctgcctgtccacctccagggcttcgaaccaccaggctac

右側フォーム：gagcggacggagctcaccctgagccccgaggccccagggc

![](/images/4h.png)

3. PAM配列を指定します。今回は最も一般的なSpCas9の"NGG"とします。
PAM配列：NGG
![](/images/4i.png)

4. "HCT116", "HEK293", "K562", "U2OS", "mESC"の中でご自身が使われている細胞株をクリックします。今回はゲノム編集技術の基礎開発でよく使われる"HEK293"細胞株を選択します。
![](/images/4j.png)

5. 自動的に予測が始まるのでしばらく待ちます。
![](/images/4k.png)

6. 結果が返ってきます。モザイク度を示す"Precision score"とフレームシフト発生率を示す"Frameshift frequency"に着目してみましょう。

  - 標的配列が"ACCACCAGGCTACGAGCGGACGG"の場合
    ![](/images/4l.png)
    Precision score：0.48（high）
    Frameshift frequency：72.9%（typical）

  - 標的配列が"TCGAACCACCAGGCTACGAGCGG"の場合
    ![](/images/4m.png)
    Precision score：0.37（typical）
    Frameshift frequency：85.3%（high）
  
  この結果をみるとどちらも極端な値の違いはありませんが、どちらかといえば"ACCACCAGGCTACGAGCGGACGG"でモザイク度が低く、一方で"TCGAACCACCAGGCTACGAGCGG"ではフレームシフト率が高いといえます。

7. 予測される変異パターンをみてみましょう。

  - 標的配列が"ACCACCAGGCTACGAGCGGACGG"の場合

    ![](/images/4n.png)

  - 標的配列が"TCGAACCACCAGGCTACGAGCGG"の場合

    ![](/images/4o.png)

  これをみると"ACCACCAGGCTACGAGCGGACGG"では変異のうち1塩基挿入・9塩基欠失が>20%という結果がでています。一方で"TCGAACCACCAGGCTACGAGCGG"では1塩基挿入が12.7%となっています。

8. この情報からどちらの標的を選ぶことを考えます。もし実験の目的が「1塩基挿入したフレームシフト変異のクローン株を数個取得したい」という場合は、モザイク性が低く1塩基挿入率が21.1%の標的"ACCACCAGGCTACGAGCGGACGG"と選ぶといいでしょう。一方で「変異パターンに拘らずフレームシフトした細胞を大量に得たい」という場合は、フレームシフト率が高い標的"TCGAACCACCAGGCTACGAGCGG"を選ぶ方がいいように考えられます。

もちろんこの指標では、そもそも変異導入率がどの程度なのかといった点やオフターゲットの多寡といった点をケアできていないのでそれらは別途調べる必要があります。
変異導入率については、HEK293の場合は実際に実験をしてみてヘテロ二本鎖移動度分析（HMA：Heteroduplex Mobility Assay)等で大まかな導入率を確認してみてもいいかもしれません。
こういったツールによる変異パターン予測とHMA（あるいは後述するTIDE解析）の結果を組み合わせることで、「全細胞のうちどれほどの細胞に変異が導入されるか？ そして導入された細胞の何%がどういった変異パターンをもつか」ということを概算することができます。
この情報は「特定の変異クローン株を取得する際にどれほどの手間がかかりそうか」といったことを把握できるようになるため、スムーズな実験スケジュールの策定に役立つと考えられます。

#### Microhomology-PredictorとinDelphiの使い分けや両ツールの注意点

Microhomology-PredictorとinDelphiの使い分けに関してはよくわからない方が多いのではないかと思います。まずHEK293などのヒト培養細胞においてはinDelphiの予測はかなり正確であることが示されているので、HEK293にCRISPR-Cas9を使う場合はinDelphiのほうがオススメです。
しかしながらinDelphiは機械学習ベースのツールであるため、学習対象にはなかった哺乳類以外の培養細胞、初代培養細胞、またin vivoでのゲノム編集での精度は不明です。
もちろん今後詳細な検証がなされていくかと思いますが、哺乳類以外の培養細胞、初代培養細胞、またin vivoでのゲノム編集では代わりにMicrohomology-Predictorのほうを活用してみてもよいかと思われます。
またMicrohomology-PredictorはTALENやZFNでも利用できるので、TALENやZFNを扱う場合にはMicrohomology-Predictorのほうを使用すべきです。

そしてこういった変異パターン予測ツールでの注意点としては、変異導入による毒性バイアスは考慮できないという点があります。
遺伝子座によってはフレームシフトを導入することで細胞の生存や増殖に大きな影響を与えてしまうケースがあり、そういったサンプルでは解析時のフレームシフト率が極端に低くなってしまいます。
長期的な実験を行う際にそういった点を見落としていると大きな損失につながります。ゲノム編集する際には予備実験として編集した細胞集団のサブクローニング・TIDE解析を行うなどして、ちゃんとフレームシフト変異の取得ができるのか確認を行うのが無難でしょう。
またこうした致死性等についてはデータベース上にヒントがある場合があります。たとえばヒト遺伝子だと[DepMap](https://depmap.org/portal/)等でGene essentialityの評価がでていますし、マウスでも[IMPC](https://www.mousephenotype.org/data/genes/MGI:1890520)で胚性致死の確認等が可能です。その他[PubMed](https://pubmed.ncbi.nlm.nih.gov/)で遺伝子名を検索すればそういった類の情報が見つかる場合もあります。事前にインターネットを活用して十分にリサーチされることをお勧めします。

- [DepMap](https://depmap.org/portal/)
  ![](/images/4p.png)

- [IMPC](https://www.mousephenotype.org/data/genes/MGI:1890520)
  ![](/images/4q.png)

##### 関連ツール
- [SPROUT](https://zou-group.github.io/SPROUT)
  - primary human T cellsでのゲノム編集結果に基づいて作製された変異パターン予測ツール。primary human T cellsを扱う場合はこちらも参考になります。

----

## 2章. より応用的なゲノム編集のためのデータベース・ツールを知る

#### 応用的なゲノム編集について

ゲノム編集でできることはDSBによるノックアウトだけではありません。

例えばDSB導入と同時にドナーDNAも導入することで人工的な配列を挿入するノックインができますし、またDNA脱アミノ化酵素をニッカーゼ型Cas9に取り付けることで二本鎖切断を伴わない塩基置換（Base Editing）を実現できます。

さらに最近では、ニッカーゼ型Cas9と融合させた逆転写酵素を利用して置換やインデルを加える方法（Prime Editing）が開発されています。

またこのようなCRISPR-Cas9、およびその派生技術が興隆する一方で、規制やライセンスの観点からZFNやTALENなども商業的に注目されています。

他にもゲノム編集から広がってRNA編集にもCRISPRが利用されつつあります。CRISPR-Cas13はその代表例で、RNAiによるノックダウンよりも特異的なノックダウン効果を実証しています。

このように世界中でゲノム編集が使われるなかで、それらを設計・解析する専用ツールやデータベースも開発されている状況です。

本章ではこのようなツールの一部を紹介し、ゲノム編集についてより理解を深めていただければと思います。

またこのようなツール・データベースに関しては演者が個人的にまとめていますので下記のQiitaのページをご参考にしていただけますと幸いです。

##### ゲノム編集のためのデータベース・ツール一覧

[ゲノム編集系のバイオインフォマティクス](https://qiita.com/KazukiNakamae/items/fa1c58351c1a8ce4c937)
- [https://qiita.com/KazukiNakamae/items/fa1c58351c1a8ce4c937](https://qiita.com/KazukiNakamae/items/fa1c58351c1a8ce4c937)

---

### CRISPR-Cas9によるノックイン設計ツール

ゲノム編集におけるノックインには非常にさまざまなものが知られています。

ドナーDNAを導入するタイプのノックインでは基本的に特定のDSB修復経路を利用しており、何を利用するかはどういったドナーDNAを扱うかによります。

たとえば相同組換え修復(HR)を利用する場合は500bp以上のホモロジーアームを両端に持たせる必要があります([Yao et al., 2017](https://doi.org/10.1038/cr.2017.76))。

また、HDR/MMEJ/NHEJを利用する場合はドナーも直鎖化しておき、修復経路に応じた長さのホモロジーアームを持たせておく必要があります（[Nakade et al., 2014](https://doi.org/10.1038/ncomms6560)、[Chu et al., 2015](https://doi.org/10.1038/nbt.3198)、[Suzuki et al., 2016](https://dx.doi.org/10.1038%2Fnature20565)、[Yao et al., 2017](https://doi.org/10.1038/cr.2017.76)、[Suzuki et al., 2019](https://doi.org/10.1038/s41422-019-0213-0)）。

さらに一本鎖DNAをドナーとして利用する場合もあり、この場合は主にSSTRという経路が利用されます([Radecke et al., 2010](https://dx.doi.org/10.1038%2Fmt.2009.304), [Yoshimi et al., 2016](https://doi.org/10.1038/ncomms10431))。

今回はMMEJ等を利用したノックイン（PITCh法）の設計ツールを紹介します。

MMEJ等を利用したノックインはホモロジーアームが20-40bpほどの相同配列（マイクロホモロジー）を取り付けるだけでドナーの作製ができるため、PCRによるアダプター付加のみでドナーを作製できます。

これは500bp以上の配列をゲノムから取得する必要があるHRなどと比べると、簡便でありなおかつさまざまな生物種で利用可能であることが示されています（[リンク参照](https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/about.html)）。

#### [PITCh designer 2.0](https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/index.html)
  - [https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/index.html](https://www.mls.sci.hiroshima-u.ac.jp/smg/PITChdesigner/index.html)
  - [論文リンク](https://doi.org/10.1080/21655979.2017.1313645)
![](/images/5a.png)

入力例

nucleotide sequence：

\>ゲノム配列サンプル
GTGACGTTTCAACACAGACCTGAGGGAGGGAGAGAGCCCCCAAGAGGAACACAGCACAGGCTCTGGAGTGGCGGCAGGAACCAGACCCCAGGGGGTACAT
GGTCTCACTCAGGATCACACGGACAGGCTTGGAACCCACATCTGCCACCCACCCCTGAGGGGCCCAGGCCCTGGGGACTCACAGGACAGAGGGCTCCGGC
AGCTTCGGGGAGGGGGTCGGGGTAATTCTGGCAAGACGGAGCTCCTTGGCCTGTGTGGAGAGGAGAAGGGGAGGAAGGGGCAGTTCCCTCGACTGGGCAG
GGGCCTGGGCCTGGACCCGGCCCAACCCTCACTCACCTGAGTGGAGGTCCCTTCCAGCCAGGAGGAGGAAGCCGAGCGCTGCAGCCCAGCCCCAGGGGCT
CCCTCCGCTGTCCGCCTTTCAGGGGGACCCAGGGCACCAGAACTCCCTGTCTTCAGGAGGCCAAAGCGCCTGGAGAAGGGGGCCTCTTCAAGCTGCTGGG
AGAAGGAGGAGGTCTCAGTTAGAGAGAAAGGATCCCTCTTCTCAGACCTCAAGGGTTAGCCCCCAAAGGACTGCAACAAACTACAATTCCCATCAGCCCC
CGGGGCAGGCACAGCCTAAAAAGGAAGCCGGTTGTCCAGGACGACTCTGGGAACTATAGTCTTCCCCCTATCTGCCCCTGCCAGAGGTTCACAGGCTGTA
TGGAATCCCACCTCCGGGCCCTCCCAGCCTCACAGGACCTCTCAGGGCATCCACTCACCACGGGACTCTTAGGGCTGGGGTGCGGCGGGGAGGAGACGCC
ATTGAGGGTTCTGGGTTCTGCAGGGGGTGGTTCTGTGATGTGGGAACACCGGGCAGGTCACAGAAGATGCCAGTTGCCTCTAGATTCAGAG

Reading frame：

Frame1

Adjustment of reading frame：

C-insertion method

Knock-in cassette：

User defined insert

insert sequence：

\>User defined insert
atggtgagcaagggcgaggagctgttcaccggggtggtgcccatcctggtcgagctggacggcgacgtaaacggccacaagttcagcgtgtccggcgagg
gcgagggcgatgccacctacggcaagctgaccctgaagttcatctgcaccaccggcaagctgcccgtgccctggcccaccctcgtgaccaccctgaccta
cggcgtgcagtgcttcagccgctaccccgaccacatgaagcagcacgacttcttcaagtccgccatgcccgaaggctacgtccaggagcgcaccatcttc
ttcaaggacgacggcaactacaagacccgcgccgaggtgaagttcgagggcgacaccctggtgaaccgcatcgagctgaagggcatcgacttcaaggagg
acggcaacatcctggggcacaagctggagtacaactacaacagccacaacgtctatatcatggccgacaagcagaagaacggcatcaaggtgaacttcaa
gatccgccacaacatcgaggacggcagcgtgcagctcgccgaccactaccagcagaacacccccatcggcgacggccccgtgctgctgcccgacaaccac
tacctgagcacccagtccgccctgagcaaagaccccaacgagaagcgcgatcacatggtcctgctggagttcgtgaccgccgccgggatcactctcggca
tggacgagctgtacaagtaa

Length of left microhomology：

40bp

PAM sequence requirement：

NGG

Length of right microhomology：

Human(Homosapiens)genome, GRCh38hg38(Dec,2013)

---

### Base Editorによる塩基編集設計ツール

Base Editingに使う脱アミノ酵素をニッカーゼ型Cas9（Base Editor）には大きく分けて二つのタイプがあります。

シトシン（C）をチミン（T）に変換するシトシン型Base Editorとアデニン（A）をグアニン（G）に変換するアデニン型Base Editorです。

これらはニッカーゼ型Cas9が結合したゲノムの特定の範囲（Windowと呼びます）に対して作用し、上記の置換を行います。

WindowはBase Editorの種類によって違っており、以下のツールではそうしたWindowを考慮した上での標的配列設計を行うことができます。

#### [BE-Designer](http://www.rgenome.net/be-designer/)
  - [http://www.rgenome.net/be-designer/](http://www.rgenome.net/be-designer/)
  - [論文リンク](https://doi.org/10.1186/s12859-018-2585-4)
![](/images/5b.png)

入力例

PAM Type：

SpCas9 from Streptococcus pyogenes: 5'-NGG-3'

Target Genome：

Vertebrates

Homo sapiens (GRCh38/hg38) - Human

Target Sequence：

\>sample
atggagctgtatgagacatccccctacttctaccaggaaccccgcttctatgatggggaaaactacctgcctgtccacctccagggc

crRNA length：

20

Base editing type：

BE（C to T）[Ref1]

Base editing window：

13 to 17

---

### Base Editorによる塩基編集予測ツール

結合したゲノム箇所に塩基置換を導入できるBase Editorですが、Window内の目的とは異なる位置にC塩基またはA塩基がある場合はその塩基も同時に置換してしまうケースがあります。また場合によってはCからGへの変換などマイナーな塩基置換を発生させることもあり、100%指向的に置換変異を入れられるわけではありません。

そのため過去のBase Editingデータを学習し、置換パターンを事前に予測するツールも開発されています。これを使うことで変異の指向性をある程度予想することが可能です。

#### [BE-Hive](https://www.crisprbehive.design)
  - [https://www.crisprbehive.design](https://www.crisprbehive.design)
  - [論文リンク](https://doi.org/10.1016/j.cell.2020.05.037)
![](/images/5c.png)

入力例

Target genomic DNA：

gacatccccctacttctaccaggaaccccgcttctatgatggggaaaactacctgcctgtcca

CRISPR protospacer：

aggaaccccgcttctatgat

Base editor / cell type：

BE4, HEK293T

Amino acid frame：

Frame 2, + strand

---

### Prime Editorによる小規模編集設計ツール

逆転写酵素を利用したゲノム編集手法であるPrime Editingはインデル置換が入り混じった複雑な小規模変異を導入可能ですが、そのために使うプロトスペーサ配列（pegRNA spacer）や逆転写テンプレートとプライマー結合サイト（pegRNA extension）、そしてニック導入用のガイドRNAのプロトスペーサ配列（ngRNA spacer）など通常のCRISPR-Cas9による変異導入やBase Editorと比べると設計がやや複雑です。

以下のツールではそのような設計の複雑さを解消するために配列の自動設計機能を提供しています。

#### [PrimeDesign](https://drugthatgene.pinellolab.partners.org)
  - [https://drugthatgene.pinellolab.partners.org](https://drugthatgene.pinellolab.partners.org)
  - [論文リンク](https://doi.org/10.1038/s41467-021-21337-7)
![](/images/5d.png)

入力例

Input sequence（これだけ入力すれば他の入力は自動でサジェストされる）：
atggagctgtatgagacatccccctacttcta(c/a)caggaaccccgcttctatgatggggaaaactacctgcctgtccacctccagggctt

pegRNA spacers：

CATCATAGAAGCGGGGTTCC

pegRNA extensions：

ACTTCTAaCAGGAACCCCGCTTCTA

ngRNA spacers：

GACATCCCCCTACTTCTAaC

---

### TALENによるノックアウト設計ツール

TALENはCRISPR-Cas9と同様に任意の配列に結合させてDNA二本鎖切断による変異導入することが可能なゲノム編集ツールです。

RNA-DNA結合のCRISPR-Cas9とは違って、TALENはタンパク質-DNA結合となっているので直感的ではありませんが、これをうまく設計するためのツールも開発されています。

ちなみに[日本語での設計プロトコル](https://www.mls.sci.hiroshima-u.ac.jp/smg/genome_editing/documents/6-module.pdf)も広島大学が公開しているので併せてご参照いただければと思います。

#### [TALEN Targeter (old version with design guidelines)](https://tale-nt.cac.cornell.edu/node/add/talen-old)
  - [https://tale-nt.cac.cornell.edu/node/add/talen-old](https://tale-nt.cac.cornell.edu/node/add/talen-old)
  - [論文リンク](https://doi.org/10.1093/nar/gks608)
![](/images/5e.png)

入力例

Sequence：

\>sample
aacaagccttttccgaccccatggagctgtatgagacatccccctacttctaccaggaaccccgcttctatgatggggaaaactacctgcctgtccacct

Spacer：

Minimum Spacer Length：12
Maximum Spacer Length：16

Repeat Array：

Minimum Repeat Array Length：16
Maximum Repeat Array Length：20

Upstream Base：

T only (Recommended)

Options：

- Require C, G, or T at position 2 (not an A)
- Percent composition
- Do not allow sites to end in G
- Require A, C, or G at position 1 (not a T)

Expires：

One hour

---

### Cas13によるRNA編集設計ツール

CRISPR-Cas13は一本鎖RNA対して配列特異的な結合をすることができます。

これによってRNAi以上の特異性でノックダウンを行えますが、その有効性は標的によってやや異なることが知られています。

このツールではその有効性を予測しつつ標的配列の選定を行うことが可能です。

#### [Cas13design](https://cas13design.nygenome.org)
  - [https://cas13design.nygenome.org](https://cas13design.nygenome.org)
  - [論文リンク](https://doi.org/10.1038/s41587-020-0456-9)
![](/images/5f.png)

入力例

- オリジナルの配列を評価する場合

  Design custom gRNAsを選択

  Input Type：

  Paste single target

  target RNA sequence：

  ggcggccacactgagggagaagcgcaggctcaagaaggtgaatgaggccttcgaggccctgaagagaagcaccctgctcaaccccaaccagcggctgcccaaggtggagatcctgcgcagtgccatccagtacatcgagcgcctccaggccctgctcagctccctcaaccaggagga

- ヒトのトランスクリプトに対して一括設計する場合

  Humanを選択
  
  Gene symbol：

  MYOG
  
  Ensemble transcript ID（自動でサジェスト）：

  ENST00000241651.4

- RNAウイルス（SARS-Cov-2）に対して一括設計する場合

  RNA virusを選択
  
  virus：

  SARS-Cov-2

  Gene name：

  S

---

### サンガーシーケンスデータを使った変異分析ツール

一般的なサンガーシーケンスで読み出せる配列は一種類であり、細胞集団に対して一斉にゲノム編集を行ったサンプル（ポピュレーションサンプル）のジェノタイピングを行う場合はサブクローニングを行う必要があります。

しかし最近では、ゲノムPCR産物を直接サンガーシーケンサーによって解析する方法も開発されてきています。

TIDE解析はそうしたアプローチのもとでゲノム編集サンプルを解析する方法です。

通常の考え方では、ゲノムPCR産物を直接サンガーシーケンスで読み出した場合は様々な配列のシグナルが混ざり合って、塩基配列として読み出すことができません。しかしTIDE解析では、こうした混合シグナルをコンピュータ上で分離することで、ゲノム編集の結果で生じた配列パターンを明らかにすることが可能です。

#### [TIDE](http://shinyapps.datacurators.nl/tide/)
  - [http://shinyapps.datacurators.nl/tide/](http://shinyapps.datacurators.nl/tide/)
  - [論文リンク](https://doi.org/10.1093/nar/gku936)
  - [統合TV](https://doi.org/10.7875/togotv.2021.040)

![](/images/5h.png)

まず以下のリンクから使用するシーケンスファイルをダウンロードしてください。
[ダウンロードリンク（自動）](https://ice.synthego.com/misc/ice_example_files.zip) from [ICE Analysis | SYNTHEGO](https://ice.synthego.com/#/)

入力例

Title plot：

sample

Guide sequence：

TGTATGAGTCGAAGATCTCC

Control Sample Chromatogram：

high_edit_GRK2_control.ab1

Test Sample Chromatogram：

high_edit_GRK2_experiment.ab1

---

### アンプリコンシーケンシングデータを使った変異分析ツール

ポピュレーションサンプルをアレルベースでのシーケンス解析するうえで最も高解像度な方法はアンプリコンシーケンスといえます。

こうしたシーケンスデータはマッピングを介した変異検出手法で解析されますが、こうした解析は必ずしもゲノム編集を前提としたデータ形式になっておらず、また解析自体にもそれなりの知識を要します。

このような状況からゲノム編集解析に特化したアンプリコンシーケンス解析ツールが発表されています。

これらを使うことでゲノム編集という文脈のなかで理解しやすいデータを得ることが可能です。

#### [CRISPResso2](https://crispresso.pinellolab.partners.org/submission)
  - [https://crispresso.pinellolab.partners.org/submission](https://crispresso.pinellolab.partners.org/submission)
  - [論文リンク](https://doi.org/10.1038/s41587-019-0032-3)
![](/images/5i.png)

入力例

以下の三角ボタンをクリックすることで例示データを自動入力することができます。
![](/images/5j.png)

CRISPR-Cas9によるノックアウトサンプルの解析の場合は"NHEJ(Non-homologous end joining)"の入力パターンがあてはまります。

Editing tool：

Cas9

Sequencing design：

Paired end reads

Fastq file R1：

nhej.r1.fastq.gz

Fastq file R2：

nhej.r2.fastq.gz

Amplicon：

AATGTCCCCCAATGGGAAGTTCATCTGGCACTGCCCACAGGTGAGGAGGTCATGATCCCCTTCTGGAGCTCCCAACGGGCCGTGGTCTGGTTCATCATCTGTAAGAATGGCTTCAAGAGGCTCGGCTGTGGTT

#### TIDEとアンプリコンシーケンシングの比較と注意点

TIDEとアンプリコンシーケンシングはどちらも変異の定量解析ができるという点で似た方法です。そこでどちらの手法を使うべきか悩むこともあるかもしれません。

TIDE解析の結果はアンプリコンシーケンシングで検出できる変異パターンと相関があることが示されており、コストという点ではNGSベースのアンプリコンシーケンシングよりも安価です。そのためTIDEはアンプリコンシーケンシングの簡易版ととらえてもいいかもしれません。

ただし、TIDE解析はアンプリコンシーケンシングほどの解像度はないため、細胞集団の中にある稀な変異パターンを検出することはできません。また挿入・置換配列の解析を十分に行うことは難しいため、Base Editingや短い配列のノックイン等の解析には不向きです。

よってTIDE解析の利用シーンとしては、ノックアウト実験に適した標的の選定やゲノム編集実験系の確認といったフェーズで利用するのに向いています。

その一方でアンプリコンシーケンシングは高い解像度や短い配列挿入（ノックイン・予期しないベクターのバックボーンの挿入等）の検出もある程度は可能なので微小なオフターゲットの検出や変異パターンの厳密なプロファイリングに向いています。

もちろんTIDE解析したものも論文用の変異解析データとして提出可能です。予算、実験系、検出したい変異パターン、安全性の要求度を考えながらどちらを行うかを判断するとよいかと思います。


また、注意すべき点としては現状のTIDE解析とNGSによるアンプリコンシーケンシングは大規模インデル等を検出するのは困難です。

しかしながらゲノム編集において数kbレベルの欠失が起こるケースは存在します。そのため慎重に実験を行うならTIDE解析・アンプリコンシーケンシングすると同時に広範囲でのgenomic PCRを行って大規模インデルが頻発していないか電気泳動レベルで確認してみたほうがよいでしょう。

---

### UCSC genome browserでのCas9標的の確認

UCSCの[UCSCのgenomue browser](http://genome-asia.ucsc.edu/cgi-bin/hgTracks?db=hg38&lastVirtModeType=default&lastVirtModeExtraState=&virtModeType=default&virtMode=0&nonVirtPosition=&position=chrX%3A15560138%2D15602945&hgsid=755575216_IGRFL7TynL4QmxVwM5RdAIoGiB93)ではあらかじめCRISPR-Cas9標的のアノテーション（CRISPR Targets）が用意されています。

これを参照することで標的可能な部位をおおよそ見積もることが可能です。

また予測切断活性やオフターゲットも評価されており、このサイトだけでも十分な選定が可能となっています。

![](/images/5k.png)

---

### ガイドRNA先行研究データベース

CRISPR-Cas9が発表されて早9年が経とうとしており、これまでさまざまなゲノム標的でCRISPR-Cas9が利用されていきました。

こうした過去の実験データは徐々にデータベースとして収録されてきており、今後はこういったものを参考に標的を選定することで効率的な実験デザインが可能となりそうです。

#### [dbGuide](https://sgrnascorer.cancer.gov/dbguide/)
  - [https://sgrnascorer.cancer.gov/dbguide/](https://sgrnascorer.cancer.gov/dbguide/)
  - [論文リンク](https://doi.org/10.1093/nar/gkaa848)
![](/images/5l.png)

入力例

Species：

Human(hg38)

HUGO gene symbol：

KRAS

---

### template-freeゲノム編集データベース

SNP配列の構築はノックインで実現されることが多いですが、MMEJを介した指向性のある変異導入を行えばドナーテンプレートを導入することなく、単純なノックアウトでSNP構築が可能です。

こうしたtemplate-freeな手法で構築可能なSNPはデータベース化されています。

#### [MHcut Browser](http://mhcut-browser.vhost38.genap.ca)
  - [http://mhcut-browser.vhost38.genap.ca](http://mhcut-browser.vhost38.genap.ca)
  - [論文リンク](https://doi.org/10.1038/s41467-019-12829-8)
![](/images/5m.png)

入力例

DATASET：

Cas9

gene name, RS ID：

KRAS

Variant Location：

intronic
exonic
intergenic
utr

Minimum consecutive first match in MH：

3

----

## 3章. ゲノム編集情報の安全な設計・解析・管理ツール

ゲノム編集を支援するデータベース・ツールは非常に多く発表されていますが、現状はほとんどのものは海外製であり、データ管理という観点で懸念が全くないわけではありません。

今回は最後に、安全なゲノム編集設計・解析・管理を行うための国産ツールとして「GGGenome」および「Genome Editing Cloud」が開発されていますのでこちらを最後に紹介しておきます。

---

### [GGGenome](https://gggenome.dbcls.jp/ja/hg38/1/)（+パッケージ版）によるオフターゲット検索
  - [https://gggenome.dbcls.jp/ja/hg38/1/](https://gggenome.dbcls.jp/ja/hg38/1/)
  - [統合TV](https://doi.org/10.7875/togotv.2018.170)

DBCLSが運営している商用利用可能な高速配列検索サイトです。

特定のゲノムを指定してミスマッチ・ギャップつきオン/オフターゲットを検索することができます。

ある程度であれば検索長の制約はないので、一般的なCRISPR-Cas9のみならず様々なゲノム編集ツールでも利用ができます。

またVやRといった縮重塩基にも対応しているのでモチーフ検索等にも活用可能です。

![](/images/5n.png)

入力例

- SpCas9（NGG-3´ PAM, プロトスペーサ 20 nt）向け

  gtccgtggaccggcggcgggNgg

  データベース：

  Human genome, GRCh38/hg38 (Dec, 2013)

  ミスマッチ/ギャップを許容：

  1塩基まで

  双方向を検索にチェック

- AsCas12a（5´-TTTV PAM, プロトスペーサ 23 nt）向け

  tttVcagacaagataaaggcagtgggg

  データベース：

  Human genome, GRCh38/hg38 (Dec, 2013)

  ミスマッチ/ギャップを許容：

  1塩基まで

  双方向を検索にチェック

またレトリバ社はGGGenomeのパッケージ版を販売しており、ローカルな環境で実行することができます。

- [https://gggenome.retrieva.jp/](https://gggenome.retrieva.jp/)

![](/images/5o.png)

---

### ゲノム編集専用データ基盤Genome Editing Cloud

プラチナバイオ・凸版印刷・広島大学が開発しているゲノム編集専用データ基盤です。

現在は商用利用可能なsgRNAの設計や活性予測、アンプリコンシーケンス解析機能を開発しており、解析データは凸版印刷のセキュアなクラウド内に保存することが可能となっています。

基本的に国内のアカデミア・企業のゲノム編集支援ツールを目指しており、要望に応じて機能拡充を行っていく予定です。

現在はクローズなテストを行っていますが、ご利用にご興味ある方は以下のアドレスまでご連絡ください。

中前 和恭：nakamae@pt-bio.com

![](/images/5p.jpg)


----

## 0章. 補遺

ゲノム編集をするうえで配列の情報収集は欠かせません。

補遺ではデモ資料で用意した配列情報を取得した流れを説明します。

### NCBIから遺伝子の配列情報を取得する

1.	まずウェブ検索でアメリカ国立生物工学情報センター（NCBI）へアクセスする。
 
![](/images/7a.png)

2.	検索欄で「Gene」を選択して、「MYOG」と入力して検索

![](/images/7b.png)

3.	検索対象をヒト（Homo sapiens）に限定するためにクリック
 
![](/images/7c.png)

4.	MYOG – myogeninがでてくるのでクリックして先に進む。

![](/images/7d.png)
 
5.	MYOG遺伝子の総合情報が表示される。この中で今回は人のゲノム上の遺伝子配列が知りたいので「Genomic regions, transcripts, and products」の欄へ行って、GenBankをクリックする。

![](/images/7e.png)
 
6.	遺伝子配列に関する総合情報（GenBankフォーマット）が表示されるので、この情報をファイルとして保存するために「Send to」をクリック。
 
![](/images/7f.png)

7.	フォーマットとして「Comple Record」「File」「GenBank」を指定して、「Create File」でダウンロードする。そうすると「sequence.gb」というファイルが手にはいる。

![](/images/7g.png)
 
### SnapGeneViewerで配列情報をわかりやすく表示する

8.	gbファイル（GenBankファイル）を読み込むには専用のソフトが必要になる。今回はSnapGene Viewerという無料ソフトをダウンロードして使う。

[配布元のリンク](https://www.snapgene.com/snapgene-viewer/)

![](/images/7h.png)

9.	自身のメールアドレスを入力してダウンロード・インストールを行う。
 
![](/images/7i.png)

10.	SnapGene Viewerでsequence.gbを開くと次のようになる。小豆色の矢印がアミノ酸に変換されるコード領域となっている。

![](/images/7j.png)
 
11.	"Sequence"をクリックすると以下のようになる。小豆色の線の上に表示されているのが該当するDNA二重鎖配列となっている。

![](/images/7k.png)

※ちなみに無料版の"SnapGene Viewer"では配列の編集ができません。編集する場合は有償版である"SnapGene"を利用するか"[Serial Cloner](http://serialbasics.free.fr/Serial_Cloner.html)"のような別ソフトを併用されるとよいでしょう。

