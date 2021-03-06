Cesiumを使って『白浪五人男「稲瀬川勢揃いの場」』のツラネに関連した土地を可視化してみました。
-----------------------------------------------------------


白浪五人男「稲瀬川勢揃いの場」では物語の舞台となっている年代が定かではないため、物語の公演上での時間軸を表現しました。<br>
Cesiumを起動すると初めに幕が引き、弁天小僧菊之助、忠信利平、赤星十三郎、南郷力丸、日本駄右衛門の順でピンが登場します。<br>
本番の舞台で花道から五人男が登場する順に合わせて制作しました。<br>
また同様に、最後にピンが消えますが、これは本番の舞台で終演の幕が引かれるときに姿が隠れる順に合わせて制作しました。<br>
タイムラインとして使用した1862年は白浪五人男が登場する『青砥稿花紅彩画』の初演の年です。<br>
<br>
<br>
各登場人物のツラネに関連する土地を地球儀にマッピングしました。<br>
ピンをクリックするとセリフの現代語訳・解説・YouTubeへのリンクが表示されます。<br>
<br>

ツラネに関する情報収集の際、以下のサイトに大変お世話になりました。ありがとうございます。
-----------------------------------------------------------
『白浪五人男ブログ』
http://srnm5men.seesaa.net/article/9600671.html
-----------------------------------------------------------
<br>
<br>

私がこの『白浪五人男「稲瀬川勢揃いの場」』マッピングを制作するに至った動機は、小学生の時に少年歌舞伎としてこれを演じたことです。<br>
私は赤星十三郎役を演じたのですが当時はツラネの意味はほぼ理解しておらず、物語自体がどうおもしろいのかも分からないような状態でした。<br>
そこでこのおもしろさを伝えるコンテンツを考えることにしました。<br>
初めにツラネの現代語訳を読んでみたのですが、物語を楽しむうえで地名を把握するところに壁があるように感じたのです。<br>
これの地名の把握の手助けとなるようなコンテンツがこの『白浪五人男 ツラネマッピング』となっております。<br>
<br>
しかしこれを演じた当時地名などを把握せずによく全て覚えていたなと、自分で感心するのですが(笑)、よく思い出してみるとセリフはほぼ音として記憶しているような状態でした。<br>
ツラネでは五・七・五調が使われていたり、セリフの音のリズムが良いので演じていて気持ち良かった覚えがあります。<br>
地名や言葉の掛けなどを全て理解していなくても楽しめるというのがこの歌舞伎のすごいところだなと、今回の制作を通して感じたところでありました。<br>
<br>
<br>



Cesiumを使ったKML可視化のサンプル
======================
Cesiumを使った日野市オープンデータを元にしたKMLファイル可視化のサンプルです。なお、日野市オープンデータに限らず、任意のKMLファイルをデジタルアース上に表示可能です。


首都大学東京システムデザイン学部インダストリアルコース3年生の授業向けに作成しました。プログラミング初心者でも、オープンデータを使ったデジタルアースコンテンツを作れます。受講者以外のかたもぜひご活用ください。

### 使い方

視点移動、ジオコーディング、ImageryLayerの切り替え、現在地へ移動、ストリートビュー起動、ヘルプ起動の各機能がすでに実装されています。これらの機能は「ヒロシマ・アーカイブ」のものに倣っています。

+ 視点移動：左上のメニューボタン
+ ジオコーディング：左上のフォーム
+ ImageryLayer切り替え：右上のパラメータボタン
+ 現在地へ移動：下中央のボタン
+ ストリートビュー起動：ビルボード（アイコン）をダブルクリック
+ ヘルプ起動：右上の「？」ボタン


### カスタマイズ

サンプルのKMLファイルと自分の作成したKMLファイルを入れ替えて、下記のカスタマイズを行うだけで表示できます。

+   `index.html 104行目` :
    視点配列を作成します。label, lat, lng, heading, pitch, rangeを指定可能です。画面左上のプルダウンメニューに表示されます。260行目のchangeViewPoint関数で処理されます。
+   `index.html 122行目` :
    KML配列を作成します。labelとurlを指定可能です。data/kmlに格納したkmlファイルについて指定してください。
+   `Cesium/Widgets/InfoBox/InfoBoxDescription.css` :
    KMLの<description>タグ内のスタイルはこのCSSで指定してください。
+   `その他` :
    自由に編集してください。

### 日野市オープンデータのKMLファイルについて

日野市オープンデータをGoogleFusionTablesを使ってKML化したものです。ただし、以下の編集を施しています。

+   `MultiGeometryタグの削除` :
    GFTからKMLを書き出すと自動的にMultiGeometryタグが追加され、PointとLinearRingが格納されています。Cesiumでそのまま表示すると、画面上にLinearRingのポリゴンが描画され、視覚的に煩雑なので、タグのみ削除しています。LinearRingタグは実害がないのでそのままにしてあります。ファイル容量を減らしたい場合はPointタグのみ残すのが良いと思います。

### 参考リンク

1. [GitHub Pagesでの閲覧](https://wtnv-lab.github.io/cesiumGitHubPages/ "日野市オープンデータ可視化")
2. [Cesium](http://cesiumjs.org/ "Cesium")
3. [KML Reference](https://developers.google.com/kml/documentation/kmlreference "KML Reference")
4. [Fusion Tablesを使ってみる](http://pc.nikkeibp.co.jp/article/column/20110829/1036486/ "Fusion Tablesを使ってみる-PC Online")
5. [オープンデータページ　日野](http://www.city.hino.lg.jp/index.cfm/196,129180,353,2132,html "オープンデータページ　日野")
6. [ヒロシマ・アーカイブ](http://hiroshima.mapping.jp/ "ヒロシマ・アーカイブ")

### ライセンス

Licensed under the [Apache License, Version 2.0][Apache]
[Apache]: http://www.apache.org/licenses/LICENSE-2.0
