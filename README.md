# 🛰️ Surface Temperature Analysis Using Satellite Imagery

Computing **Land Surface Temperature** from a **Landsat 9** thermal scene and mapping it with a geospatial Python stack.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![rasterio](https://img.shields.io/badge/rasterio-Raster-brightgreen.svg)
![GeoPandas](https://img.shields.io/badge/GeoPandas-Vector-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## 🌍 Overview

Satellites carry thermal sensors that measure the radiation leaving Earth's surface. This project turns a raw **Landsat 9 thermal band** into actual **Land Surface Temperature (LST)** in °C and maps it — a core technique for urban heat islands, agriculture, drought and climate studies.

## 📊 Data

A **Landsat 9 Collection-2 Level-2** thermal scene: `LC09_L2SP_044034_20221213_..._ST_B10.TIF` (band **ST_B10**), ~**7671 × 7791 pixels**, **UTM zone 10N**, captured **13 Dec 2022**.

## 🧠 Approach

1. **Read raster** — open the GeoTIFF band with `rasterio` and inspect its profile (CRS, size, nodata).
2. **Mask NoData** — mask out 0 / nodata pixels with a masked NumPy array.
3. **Convert to temperature** — apply the Landsat scale factor (`0.00341802`) and offset (`149.0`) to get Kelvin, then subtract 273.15 for **Celsius**.
4. **Result** — across this scene the surface temperature ranges roughly **−19.3 °C to +26.4 °C**.
5. **Visualize** — render the temperature map with `matplotlib` (and `geopandas` for vector context).

## 🛠️ Tech Stack

`Python` · `rasterio` · `geopandas` · `numpy` · `matplotlib`

## ▶️ How to Run

```bash
pip install rasterio geopandas numpy matplotlib
jupyter notebook SurfaceTemperatureAnalysisUsingSatelliteImagery.ipynb
```

Provide the Landsat thermal band (`ST_B10`) GeoTIFF at the path set in the notebook, then run the cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Uydular, Dünya yüzeyinden çıkan ışımayı ölçen termal sensörler taşır. Bu proje, ham bir **Landsat 9 termal bandını** gerçek **Yüzey Sıcaklığına (LST)** (°C) çevirir ve haritalar — kentsel ısı adaları, tarım, kuraklık ve iklim çalışmaları için temel bir teknik.

### Veri
Bir **Landsat 9 Collection-2 Level-2** termal sahnesi: `LC09_L2SP_044034_20221213_..._ST_B10.TIF` (**ST_B10** bandı), ~**7671 × 7791 piksel**, **UTM zone 10N**, **13 Aralık 2022** tarihli.

### Yaklaşım
1. **Raster okuma** — GeoTIFF bandı `rasterio` ile açılır, profili (CRS, boyut, nodata) incelenir.
2. **NoData maskeleme** — 0 / nodata pikselleri maskelenmiş NumPy dizisiyle dışlanır.
3. **Sıcaklığa çevirme** — Landsat ölçek faktörü (`0.00341802`) ve ofset (`149.0`) uygulanarak Kelvin elde edilir, ardından 273.15 çıkarılarak **Celsius**.
4. **Sonuç** — bu sahnede yüzey sıcaklığı yaklaşık **−19.3 °C ile +26.4 °C** arasında değişir.
5. **Görselleştirme** — sıcaklık haritası `matplotlib` ile çizilir (`geopandas` vektör bağlam için).

### Teknolojiler
`Python` · `rasterio` · `geopandas` · `numpy` · `matplotlib`

### Çalıştırma
```bash
pip install rasterio geopandas numpy matplotlib
jupyter notebook SurfaceTemperatureAnalysisUsingSatelliteImagery.ipynb
```
Landsat termal bandı (`ST_B10`) GeoTIFF dosyasını notebook'taki yola koy ve hücreleri çalıştır.
