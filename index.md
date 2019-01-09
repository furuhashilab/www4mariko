## 帰宅困難者を対象とした避難場所位置情報オープン化の実践ー渋谷区を例としてー

貴方は<!--タグはここから--><a href="http://www.rays-counter.com/"><img src="http://www.rays-counter.com/d411_f6_231/5b28c43192109/" alt="アクセスカウンター" border="0"></a><img src="http://www.rays-counter.com/images/counter_01.gif" border="0"><img src="http://www.rays-counter.com/images/counter_02.gif" border="0"><img src="http://www.rays-counter.com/images/counter_03.gif" border="0"><img src="http://www.rays-counter.com/images/counter_04.gif" border="0" ><img src="http://www.rays-counter.com/images/counter_05.gif" border="0"><!--ここまで-->　人目の訪問者です


Thank you for visiting!

### Introduction
地震大国と言われる我が国は、世界の国土の約０.25％程の小さな島国にも関わらず、M6.0以上の地震の発生数は世界の20.5％を占めている。そのような自然環境下に居住する我々日本人にとって、地震をはじめとする自然災害には、目を背けることが出来ないのが現実である。近い未来起きるであろう次の災害時に、どこで何をしているか、予測する事は非常に困難と言われている。自然災害の発災時、多くの人々は最寄りの避難所を探し、その場所までのナビゲーション目的で地図を用いる。しかし、現状公開されている様々な災害時向けの地図は避難場所の情報をすばやく受け取り、活用できる状況となってはいない。そこで本研究では、発災時に多くの人が必要とする避難所の地理空間情報を整理し、誰でも利用可能なオープンデータライセンスとして流通可能なOpenStreetMapプラットフォーム上に帰宅困難者向けの避難所情報を入力する事で、大規模災害時に、多くの市民と帰宅困難者が必要とする地理空間情報の新しい提供方法の在り方を検討し、実際にデータを入力、公開した。また、本稿では研究対象地域として、青山学院大学青山キャンパスが存在する東京都渋谷区に着目し、避難所情報の整理・オープン化を実施した。


### Methods
渋谷区/目黒区の避難所・避難場所・一時避難場所・帰宅困難者受け入れ施設をリストアップした。また、OpenStreetMapデータ及び国土地理院・指定緊急避難所場所データの入力、公開状況を確認した。


### Results
渋谷区/目黒区共に、OpenStreetMap上に避難場所であるということを表すtag=keyの記入無し。
また、国土地理院・指定緊急避難所場所データには
*渋谷区⇨記入無し
*目黒区⇨記入有り
であった。また、OSMのタグについては、
*一時避難場所⇨social_facility=shelter
*避難場所⇨emergency=assembly_point
以上を採用し、OSM上のデータに掲載をした。
研究を進めるうちに、帰宅困難者受け入れ施設用のOSMタグが無いことが判明した。


### Discussion
帰宅困難者受け入れ施設のOSMタグを、
【emergency=assembly_point:unable_to_move=yes】と提案した。帰宅困難者が多く居て、動けない状況を災害と見なし、unable_to_moveをタグに反映した結果である。


### Conclusion
OSMに渋谷区の避難場所、一時避難場所、帰宅困難者受け入れ施設を入力することで、情報がオープンソース化された。今後の課題として、災害の種類によって指定緊急避難場所を分けて設定すると同時に、OSM上でもタグを区別して記入すること等が挙げられる。


## About Me

青山学院大学地球社会共生学部（GSC）1期生　

古橋研究室所属




### Contact

Facebook
https://www.facebook.com/mariko.nagano.92
