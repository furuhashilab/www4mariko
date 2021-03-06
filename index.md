

貴方は<!--タグはここから--><a href="http://www.rays-counter.com/"><img src="http://www.rays-counter.com/d411_f6_231/5b28c43192109/" alt="アクセスカウンター" border="0"></a><img src="http://www.rays-counter.com/images/counter_01.gif" border="0"><img src="http://www.rays-counter.com/images/counter_02.gif" border="0"><img src="http://www.rays-counter.com/images/counter_03.gif" border="0"><img src="http://www.rays-counter.com/images/counter_04.gif" border="0" ><img src="http://www.rays-counter.com/images/counter_05.gif" border="0"><!--ここまで-->　人目の訪問者です


Thank you for visiting!

## 帰宅困難者を対象とした避難場所位置情報オープン化の実践ー渋谷区を例としてー

### はじめに
地震大国と言われる我が国は、世界の国土の約０.25％程の小さな島国にも関わらず、M6.0以上の地震の発生数は世界の20.5％を占めている。そのような自然環境下に居住する我々日本人にとって、地震をはじめとする自然災害には、目を背けることが出来ないのが現実である。近い未来起きるであろう次の災害時に、どこで何をしているか、予測する事は非常に困難だ。自然災害の発災時、多くの人々は最寄りの避難所を探し、その場所までのナビゲーション目的で地図を用いる。しかし、現状公開されている様々な災害時向けの地図は避難場所の情報をすばやく受け取り、活用できる状況となってはいない。

そこで本研究では、発災時に多くの人が必要とする避難所の地理空間情報を整理し、誰でも利用可能なオープンデータライセンスとして流通可能なOpenStreetMapプラットフォーム上に帰宅困難者向けの避難所情報を入力する事で、大規模災害時に、多くの市民と帰宅困難者が必要とする地理空間情報の新しい提供方法の在り方を検討し、実際にデータを入力、公開した。また、本稿では研究対象地域として、青山学院大学青山キャンパスが存在する東京都渋谷区に着目し、避難所情報の整理・オープン化を実施した。


### 研究過程
渋谷区の避難所・避難場所・一時避難場所・帰宅困難者受け入れ施設をリストアップした。
* 避難所…災害時、家屋の倒壊などで被害を受けた区民が一定期間生活をする場所。食料等の備えあり。
* 避難場所…災害時に避難する場所で、火災等がおさまるまで一時的に避難する場所。基本的に食料の備え無し。
* 一時避難場所…避難場所に行く前に一時的に集合する場所。
* 帰宅困難者受け入れ施設…区民以外の帰宅困難者も一定期間生活が出来る場所。

本研究では帰宅困難者向けのデータ整理を行いたい為、OSMに入力するデータは
**避難場所**   /  **一時避難場所** /  **帰宅困難者受け入れ施設**   に限定した。

OSMのデータの検証に加えて、国土地理院・指定緊急避難所場所データの入力状況、公開状況を確認した。


### 結果
渋谷区/目黒区共に、OSM上に避難場所であるということを表すtag=keyの記入は無かった。

また、国土地理院・指定緊急避難所場所データに関しては

* 渋谷区⇨記入無し
* 目黒区⇨記入有り

であった。

また、OSMのタグについては、
* 一時避難場所⇨social_facility=shelter
* 避難場所⇨emergency=assembly_point

以上を採用し、OSM上のデータに掲載をした。


さらに研究を進めるうちに、帰宅困難者受け入れ施設用のOSMタグが無いことが判明した。
以下では帰宅困難者受け入れ施設用のOSMタグの決定に際してのプロセスを記述する。


### 議論
本研究では、帰宅困難者受け入れ施設のOSMタグを、
**【emergency=assembly_point:unable_to_move=yes】**と提案した。

帰宅困難者が多く居て、動けない状況を災害と見なし、unable_to_moveをタグに反映した結果である。


emergency= で災害時のタグを見てみると、
* 地震⇨assembly_point:earthquake=yes
* 火事⇨assembly_point:fire=yes
* 洪水⇨assembly_point:flood=yes
* 地滑り⇨assembly_point:landslide=yes
* 竜巻⇨assembly_point:tornado=yes
* 津波⇨assembly_point:tsunami=yes

以上のようになっている。

帰宅困難者が多く発生した現象自体を災害と見なし、「コロン:」に続く単語の変更を行った。

そこで、帰宅困難者受け入れ施設のvalueについて
* have_difficulty_going_back_home
* unable_to_return_home
* having_trouble_returning_home

等の検討を行った。

homeとつけると帰宅のイメージが強くなってしまうが、実際は帰宅のみでなく、目的地に移動途中でその地点から動けなくなった事も表したい為、
* unabe_to_return

と決定した。

しかしながら、このタグは今回の研究において独断で決めたものであり、公式タグではない。
OSMWikiに疑問として投げかけたので、今後Discussionや投票を経て決定される。


### 最後に
OSMに渋谷区の避難場所、一時避難場所、帰宅困難者受け入れ施設の情報を入力することで、オープンソース化された。

今後起こりうる災害に備えて、この研究が今本当に求められている空間情報として有効利用されることを期待する。

更にこれからの課題として、

政府としても災害の種類によって避難所を区別して認識・公開する体制をとるよう発表していることから、
災害ごとに指定緊急避難場所を分けて設定すると同時に、OSM上のタグも区別して記入することが挙げられる。

今回、合同研究として取り組んだ区は**渋谷区**並びに**目黒区**であるが、他の区域についても同様の情報入力が不可欠であろう。

四季や自然の豊かさが誇りの日本で、災害に対してより賢く向き合って行くことが全国民に求められている。



### 参考文献
* [地理院地図指定緊急避難場所](https://maps.gsi.go.jp/#14/35.665021/139.695725/&base=std&ls=std%2C0.29%7Cskhb04&disp=11&lcd=skhb04&vs=c1j0h0k0l0u0t0z0r0s0f0&d=vl)
* [渋谷区防災地図](https://www.city.shibuya.tokyo.jp/assets/detail/files/anzen_bosai_hasai_pdf_bosaimap2017.pdf)
* [渋谷区避難所施設一覧](https://www.city.shibuya.tokyo.jp/anzen/bosai/hinan/itiran.html)
* [OSM wiki MAIN PAGE](https://wiki.openstreetmap.org/wiki/JA:Main_Page)
* [osm/wiki/tag:emergency=assembly_point](https://wiki.openstreetmap.org/wiki/JA:Tag:emergency%3Dassembly_point)
* [osm/wiki/key:emergency](https://en.wikipedia.org/wiki/Meeting_point)
* [WikiProject Emergency Cleanup](https://wiki.openstreetmap.org/wiki/JA:WikiProject_Emergency_Cleanup)
* [Talk:WikiProject Emergency Cleanup](https://wiki.openstreetmap.org/wiki/JA:Talk:WikiProject_Emergency_Cleanup)
* [JA:Tag:amenity=shelter](https://wiki.openstreetmap.org/wiki/JA:Tag:amenity%3Dshelter)
* [公共施設の入力例](https://wiki.openstreetmap.org/wiki/JA:Tag:amenity%3Dsocial_centre)
* [防災白書](http://www.bousai.go.jp/kaigirep/hakusho/h30/honbun/index.html)
* [避難場所等の図記号の標準化の取り組み](http://www.bousai.go.jp/kyoiku/zukigo/index.html)
* [防災標識ガイドブック](http://www.bousai.go.jp/kyoiku/zukigo/pdf/symbol_02.pdf)
* [都立一時滞在施設情報](http://www.bousai.metro.tokyo.jp/smart/kitaku_portal/1005196/1005247.html)
* [都立一時滞在施設情報一覧](http://www.bousai.metro.tokyo.jp/smart/_res/projects/default_project/_page_/001/005/247/20180401.pdf)
* [東京都防災マップ](http://map.bousai.metro.tokyo.jp/search_facility_list.html?p1=&p2=51&p3=)





## About Me

長野茉梨子
青山学院大学　地球社会共生学部（GSC）1期生　

古橋研究室所属




### Contact Me

[Facebook](https://www.facebook.com/mariko.nagano.92)
