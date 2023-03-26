## 強震モニタ負荷軽減再配信 WebSocket 

URI : 非公開

## 仕様書

## Code : KEEW

 予報を配信します。

|  値名  |  型 |
| ---- | ---- |
|  IseewAttached  |  boolean  |
|  request  |  KmoniRequests  |
|  hypocenter | HypocenterInfo |
| EEWinfos | Intensities |
| reportid | string |
| report_num | string |

### KmoniRequests

| 値名 | 型 |
| ---- | ---- |
| report_time | string |
| region_code | string or null |
| request_time | string |

### HypocenterInfo

| 値名 | 型 |
| ---- | ---- |
| magunitude | string or number |
| depth | string |
| latitude | string or number |
| longitude | string or number |

### Intensities

| 値名 | 型 |
| ---- | ---- |
| calcintensity | string |
| isAleart | boolean |

  

## Code : WarningDetail

 警報の詳細を配信します。
 
 | 値名 | 型 |
 | ---- | ---- |
 | code | WarningDetail as string |
 | time | string |
 | detail | EEW_Earthquake |
 | calcelled | boolean |
 | areas | EEWAreas[]
 | license | p2pquake.net - JSONAPI v2 as string |
 
 ### EEW_Earthquake
 
 | 値名 | 型 |
 | ---- | ---- |
 | originTime | string |
 | arrivalTime | string |
 | condition | string |
 | hypocenter | EEW_Hypocenter |
 
 ### EEW_Hypocenter
 
 | 値名 | 型 |
 | ---- | ---- |
 | name | string|
 | reduceName | stirng |
 | latitude | number , -200 |
 | longitude | number , -200 |
 | depth | number , -1|
 | magunitude | number , -1 |
 
 ### EEWArea
 
 | 値名 | 型 |
 | ---- | ---- |
 | pref | string |
 | name | string |
 | scaleFrom | number |
 | scaleTo | number |
 | kindCode | EEWKindCode as enum |
 | arrivalTime | string |
 
 ### ENUM EEWKindCode
 
| 値名 | 変わる値 |
| ---- | ---- |
| 主要動未到達  | SecondaryUnReached = "10" |
| 主要動到達済  |SecondaryReached = "11" |
| 主要動の到達予想なし（PLUM法による予想）| SecondaryReachedNoForecastinPLUM = "19" |
 
## Code Hello

 初期接続時にこんにちはを送ります。
 
 # 使用API等
 
 　p2pquake.net 様 提供中 JSONAPI v2 / EEW
   www.kmoni.bosai.go.jp 様の Json
