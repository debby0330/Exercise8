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

## 執行方式

1. 確認 `data/` 資料夾有三個 `.gpkg` 檔案
2. 在 `e8/` 根目錄啟動 Jupyter：`jupyter notebook`
3. 依序執行 `Week8-Student.ipynb` 所有 cell