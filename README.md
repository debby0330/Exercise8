---

## 偵測結果

| 偵測目標 | 波段組合 | 面積 |
|----------|----------|------|
| 堰塞湖（Act 1→2） | NIR drop + SWIR + 空間閘 | ~0.86 km² |
| 崩塌源區（Act 1→3） | NIR drop + SWIR surge | 依門檻而定 |
| 土石流鋪面（Act 1→3） | NDVI drop + BSI spike | 下游光復地區 |

---

## 覆蓋缺口發現

W3/W7 圖層集中於花蓮市，距離光復鄉約 30 km，導致堰塞湖潰決影響範圍完全不在既有 ARIA 覆蓋區內。本週新增 `guangfu_overlay.gpkg` 補足此缺口。

---

## 環境需求

```bash
pip install pystac-client planetary-computer stackstac rioxarray
pip install geopandas shapely rasterio pyproj scikit-learn
pip install python-dotenv requests
```

---

## 專案結構

```
e8/
├── data/                    # 資料檔案
│   ├── guangfu_overlay.gpkg # 光復地區覆蓋圖層
│   ├── shelters_hualien.gpkg # 花蓮避難所位置
│   ├── top5_bottlenecks.gpkg # 前5個瓶頸點
│   ├── mataian_detections.gpkg # 馬太安地區偵測結果
│   ├── impact_table.csv     # 影響統計表
│   └── shelter_risk_audit.json # 避難所風險審計
├── output/                  # 輸出結果
│   ├── 12_coverage_gap_map.png # 覆蓋缺口地圖
│   ├── 07_lake_mask.png     # 堰塞湖遮罩
│   ├── 08_landslide_threshold_grid.png # 崩塌閾值網格
│   ├── 09_debris_mask.png   # 土石流遮罩
│   └── 10_three_masks.png   # 三種遮罩組合圖
├── script/                  # 分析腳本
│   └── Week8-Student-Complete.ipynb # 主要分析筆記本
├── README.md                # 專案說明文件
└── .env                     # 環境變數（不上傳GitHub）
```

---

## 執行方式

1. 確認 `data/` 資料夾有所有必要的 `.gpkg` 和 `.csv` 檔案
2. 在 `e8/` 根目錄啟動 Jupyter：`jupyter notebook`
3. 執行 `script/Week8-Student-Complete.ipynb` 進行完整分析
4. 輸出結果將儲存至 `output/` 資料夾