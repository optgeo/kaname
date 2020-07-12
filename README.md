# kaname: アダプト地殻変動情報

# 対象
国土地理院ウェブサイトの[地殻変動情報](https://mekira.gsi.go.jp/index.html)

## 観測局情報
https://mekira.gsi.go.jp/api/getObservationStations?decimated=0

- [ ] `rake download` で `src/stations.json` にキャッシュすることにする。キャッシュする目的は、後続の処理を行うたびにサーバへのリクエストを起こすことの非効率を回避するためである。
- [ ] `rake geojson` で　`src/stations.json` から `src/stations.geojson` を作成することにする。`src/stations.geojson` の目的は、生データを GitHub で閲覧できるようにすることである。
- [ ] `rake geojsons` で　`src/stations.json` から `src/stations.geojsons` を作成することにする。`src/stations.geojsons` の目的は、 Tippecanoe を使ってベクトルタイルを生産することである。

## 変動情報
https://mekira.gsi.go.jp/api/getCoordinateTransformationVectors?term=year&decimated=0&fixedStationId=950462

