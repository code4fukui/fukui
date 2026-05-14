# fukui

福井県のオープンデータを可視化するインタラクティブマップアプリケーション「福井オープンイベントナビ」です。福井オープンデータポータルのデータを活用し、イベント、公共施設、飲食店、その他のスポット（POI）を表示します。

## デモ

:earth_asia: **ライブマップ:** ~~https://codeforfukui.github.io/fukui/map.html~~ *(unavailable)* *(demo unavailable)*

## 機能

- **インタラクティブマップ:** 福井県内のイベント、公共施設、飲食店、その他のスポットの位置情報を表示します。
- **詳細情報:** アイコンをクリックすると、住所、電話番号、営業時間、関連リンクなどの詳細が情報ウィンドウに表示されます。
- **ライブデータ:** 稼働中のSPARQLエンドポイントから動的にデータを取得し、常に最新の情報を表示します。
- **モバイル対応:** デスクトップとモバイル端末の両方に最適化されたレスポンシブデザインです。

## セットアップと使用方法

本アプリは、Webブラウザ上で直接動作するクライアントサイドアプリケーションです。

1. **リポジトリのクローン:**
    ```sh
    git clone https://github.com/codeforfukui/fukui.git
    cd fukui
    ```

2. **Google Maps API キーの設定:**
    本プロジェクトの動作にはGoogle Maps APIキーが必要です。`map.html`を開き、以下の行のプレースホルダーとなっているキーをご自身のAPIキーに置き換えてください:
    ```html
    <script src="https://maps.google.com/maps/api/js?key=AIzaSyCfbWrf5isAqdEGdSNxa_NeUDqThEmRt8Q"></script>
    ```

3. **ブラウザで開く:**
    ローカルの`map.html`ファイルをWebブラウザで開き、アプリケーションを実行します。

## データソース

本プロジェクトでは、以下のSPARQLエンドポイントを通じて福井県のオープンデータを取得しています:

- **福井オープンデータプラットフォーム (odp.jig.jp):** `https://sparql.odp.jig.jp/data/sparql`
- **OpenData.cc:** `https://sparql.opendata.cc/data/sparql`

本アプリでは、主に公共施設（`jrrk#CivicFacility`）およびその他のスポット/POI（`jrrk#CivicPOI`）のデータセットを可視化しています。

## ライセンス

MIT License — 詳細は [LICENSE](LICENSE) を参照してください。
