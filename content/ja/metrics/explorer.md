---
title: メトリクスエクスプローラー
kind: documentation
description: すべてのメトリクスを調査し分析する
aliases:
  - /ja/graphing/metrics/explorer/
further_reading:
  - link: /metrics/summary/
    tag: ドキュメント
    text: メトリクスの概要
  - link: /metrics/distributions/
    tag: ドキュメント
    text: ディストリビューションメトリクス
---
## 概要

[メトリクスエクスプローラー][1]は、メトリクスを Datadog で調査するための基本のインターフェースです。より高度なオプションを使用するには、[ノートブック][2]またはダッシュボード（[スクリーンボード][3]や[タイムボード][4]）を作成します。

## グラフ

**Graph** テキストボックス内をクリックすると、Datadog に送信したすべてのメトリクスがリストされます。テキストボックスに入力してメトリクスを絞り込んでから、メトリクスをクリックして選択します。選択したメトリクスに対して、ページの右側にグラフがリアルタイムで作成されます。

グラフの上部で、タイムフレームとグラフのサイズを指定できます。

{{< img src="metrics/explorer/graphs.png" alt="メトリクスエクスプローラー"  style="width:80%;" >}}

**注**: **Calculate as count where applicable** チェックボックスは、`RATE` タイプのメトリクスに表示されます。

### スコープ

**Over** テキストボックスでタグの値を選択または検索すると、スコープを定義できます。たとえば、**Over** テキストボックスを使用して、メトリクスの値を特定のホスト、クラスター、環境、リージョンなどで絞り込むことができます。

### グループ化

**One graph per** テキストボックスでタグキーを選択または検索すると、グループ化を定義できます。たとえば、1 つのメトリクスをホスト、コンテナ、リージョン、環境などに基づいて複数のグラフに分けることができます。`<キー>:<値>` の形式でタグ付けされたメトリクスをグループ化できます。

### 空間集計

**On each graph, aggregate with the** テキストボックスで、メトリクス値の結合に使用する[空間集計][5]を定義できます。以下のオプションを使用できます。

* 報告された値の平均値（デフォルト）
* 報告された値の最大値
* 報告された値の最小値
* 報告された値の合計値

**注**: これらのオプションは、選択したメトリクスのタイプによって変わります。

### オプション

メトリクスエクスプローラーの以下のオフションを変更できます。

* グラフタイトルのプレフィックスを `<VALUE>` で指定します。デフォルトは空白です。
* 同時に表示されるグラフの数を `<NUMBER>` で指定します。デフォルトは 20 です。

### エクスポート

左下のボタンを使用し、すべてのグラフを新規または既存のタイムボードにエクスポートできます。グラフを個別にエクスポートするには、各グラフの右上に表示されるエクスポートアイコンをクリックします。

### スナップショット

グラフの右上にあるカメラアイコンをクリックすると、各グラフのスナップショットを作成できます。

## その他の参考資料

{{< partial name="whats-next/whats-next.html" >}}

[1]: https://app.datadoghq.com/metric/explorer
[2]: /ja/notebooks/
[3]: /ja/dashboards/screenboard/
[4]: /ja/dashboards/timeboard/
[5]: /ja/metrics/introduction/#space-aggregation