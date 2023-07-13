## 專案說明
* junior_painter是一個flutter package，支援多平台使用，
  AuroraWarehouseView專案是這個package的簡單應用範例，未來希望支援畫更多圖型、以及實際應用。
* junior_painter主要有Edit Mode、Preview Ｍode模式。
* [AuroraWarehouseView(可視化儲位Demo演示)](https://cheeregofa.github.io/junior_painter/)

## 主要Mode說明

#### Edit Ｍode
1. 使用Edit Mode自行編輯各料架位置、各料架中的儲位位置，完成建檔。
2. 建議用於Web or Desktop平台，類似於儀表板，所有『料架』跟『儲位擺放的位置』都透過此Mode設置，而『儲位』的來源是database中的『儲位Table』，只需提供『儲位Table內各個唯一儲位碼』即可套用此Mode。

#### Preview Mode
1. 使用Preview Ｍode根據你的商業邏輯，在Mobile平台或者其他平台上使用
2. 建議用於Mobile平台，根據條件選擇儲位後進行下一步，如入帳貨扣帳或其他等等動作。

## 資料結構
* 存取json資料呈顯所有Mode內容。
```

    {
      "id": "P06",
      "name": "一般倉",
      "updateUser": "Howard",
      "updateDate": "2023-04-26 13:20:09",
      "version": 23,
      "source": [
        {
          "id": "59b36151-f293-4b09-a25a-f99bf26ae28c",
          "name": "59b36151-f293-4b09-a25a-f99bf26ae28c",
          "defObject": {"left": 105.73112487792969, "top": 149.10671997070312, "right": 314.47265625, "bottom": 184.18807983398438},
          "diffObject": {"left": 98.30477205912274, "top": 143.95898797171458, "right": 292.3846958705357, "bottom": 177.82920564923967},
          "onWindowCgObject": {"left": 95.84906122600478, "top": 143.7346305898237, "right": 304.5905925980751, "bottom": 178.81599045310494},
          "defWindowSize": {"width": 840.0, "height": 840.0},
          "diffWindowSize": {"width": 781.0, "height": 811.0},
          "fillColor": 0,
          "borderColor": 4282682111,
          "createDateTime": "20230307",
          "offsetScale": {"dx": -0.6650147914601722, "dy": -0.6295110771807279},
          "referItems": [
            {"C1": "", "RefDirection": "top", "C2": "", "C3": "P06060101"},
            {"C1": "", "RefDirection": "top", "C2": "P06060102", "C3": ""},
            {"C1": "P06060103", "RefDirection": "top", "C2": "", "C3": ""}
          ]
        },
        {...}
      ]
    },
    {...}

```


## 備註
* 為方便演示，Demo資料是本地資料，沒有存取至database
* 目前僅支援畫矩形
* 命名有些誤導，需優化
* UI/UX還有改進空間
* 近期部分階段調整完將嘗試發布至pub.dev