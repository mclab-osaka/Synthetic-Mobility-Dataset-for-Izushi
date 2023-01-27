## Introduction
我々の研究により得られた，兵庫県豊岡市出石地区を再現した車両モビリティデータセットを公開する．
<br>
公開日2023年1月23日


We present a vehicle mobility dataset obtained from our research that reproduces the Izushi district of Toyooka City, Hyogo Prefecture.
<br>
Published on January 23, 2023

## Activity
研究内容は[ここ](https://ieeexplore.ieee.org/abstract/document/9767393)から確認できる．
<br>
現在（2023年1月），IEEE Transactions on Intelligent Transportation Systemsに投稿予定．


The research can be found [here](https://ieeexplore.ieee.org/abstract/document/9767393).
<br>
Currently (January 2023), it is scheduled for submission to IEEE Transactions on Intelligent Transportation Systems.

## Data-set
データセットは2021年11月18日から2021年11月24日までの7日間において，午前9時から午後5時までの出石のモビリティをシミュレーション上で再現したものである．


The dataset is a simulation of Izushi's mobility from 9:00 a.m. to 5:00 p.m. over a seven-day period from November 18, 2021 to November 24, 2021.

### Data Format
本研究では，PTV Vissim 2022を用いてデータ出力を行った．


In this study, PTV Vissim 2022 was used for data output.

#### network.txt
対象地域の道路ネットワーク情報が記載されたテキストファイル．

- 1行目：ポリゴンポイントの正しい位置を後で計算するために使用する座標
- リンクデータブロック（ネットワーク上のリンク情報からなるブロックでLinksとEndLinksに囲まれた部分）
- 歩行者エリアデータブロック（ネットワーク上の歩行者のエリア情報からなるブロックでPedestrianAreasとEndPedestrianAreasに囲まれた部分）

それぞれのデータブロックの中は次のような構成である.

"ネットワークオブジェクト番号(：オブジェクト名)",カンマ区切りの[x座標,y座標,z座標のリスト]
<br>
g（新しい行の追加を表す）


A text file containing road network information for the target area.

- Line 1: Coordinates used to later calculate the correct position of the polygon point
- Links data block (block consisting of link information on the network, bounded by Links and EndLinks)
- Pedestrian area data block (block consisting of pedestrian area information on the network, bounded by PedestrianAreas and EndPedestrianAreas)

The inside of each data block consists of the following.

"Network object number (:object name)", comma-separated list of [x-coordinates, y-coordinates, z-coordinates].
<br>
g (indicating the addition of a new row)

#### ***.knr
車両の挙動を示すファイル．ファイル名は日付となっている．
<br>
記法は以下のとおり([引用](https://cgi.ptvgroup.com/vision-help/VISSIM_2022_ENG/Content/11_Auswertungen/AuswertungKnotenauswertung.htm)）．


A file that shows the behavior of the vehicle. The file name is a date.
<br>
The notation is as follows ([citation](https://cgi.ptvgroup.com/vision-help/VISSIM_2022_ENG/Content/11_Auswertungen/AuswertungKnotenauswertung.htm)).

|Attribute|Definition|
|:--|:--|
|VehNo|Vehicle number|
|VehType|Number of vehicle type|
|StartTime|Simulation second at which the vehicle enters the node|
|End at|Simulation second at which the vehicle exits the node|
|StartLink|Link number from which vehicle arrives at node|
|StartLane|Lane number from which vehicle arrives at node|
|StartPos|Position from the beginning of the link from which vehicle arrives at node|
|NodeNo|Node number|
|Movement|Cardinal points from-to, in which the vehicle moves through the node|
|FromLink|Number of link that leads to the node|
|ToLink|Number of link that leads out of the node. The vehicle has left the node via this link.|
|ToLane|Number of lane that leads out of the node. The vehicle has left the node via this lane.|
|ToPos|Position of the node exit on the link which leads out from the node|
|Delay|Delay in seconds that it takes to leave the node starting from crossing the start section until leaving the node|
|StopDelay|Stop delay in seconds within the node starting from crossing the start section until leaving the node|
|Stops|Number of stops within the node starting from crossing the start section until leaving the node. This includes stopping at the turning point after backing out of the parking space before the vehicle continues driving forward.|
|No_Pers|Number of persons in the vehicle|

## License
<p xmlns:cc="http://creativecommons.org/ns#" , ©＝&copy;>This work &copy; 2023 by <span property="cc:attributionName">Kazuki Hayashi</span> is licensed under <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"></a></p>
