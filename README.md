# 🛰️ Surface Temperature Analysis Using Satellite Imagery

Computing and mapping Land Surface Temperature (LST) from satellite raster imagery with a geospatial Python stack.

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![rasterio](https://img.shields.io/badge/rasterio-Raster-brightgreen.svg)
![GeoPandas](https://img.shields.io/badge/GeoPandas-Vector-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

**🌐 Language:** English · [Türkçe](#-türkçe)

## 🌍 Overview

Satellites measure the thermal radiation leaving Earth's surface, which can be converted into **Land Surface Temperature** — a key indicator for urban heat islands, agriculture, drought and climate studies. This project reads satellite raster bands, derives surface temperature, and visualizes it over a geographic area.

## 📊 Data

Geospatial raster imagery (GeoTIFF bands, e.g. thermal/optical satellite data) plus optional vector layers (boundaries/regions) for context.

## 🧠 Approach

1. **Read rasters** — open GeoTIFF bands with `rasterio`, inspect metadata (CRS, resolution, extent).
2. **Compute LST** — apply band math / scaling to convert raw values into surface temperature.
3. **Geospatial context** — overlay vector boundaries with `geopandas`.
4. **Visualization** — render temperature maps with `rasterio.plot` and `matplotlib`, using `numpy` for array operations.

## 🛠️ Tech Stack

`Python` · `rasterio` · `geopandas` · `numpy` · `matplotlib`

## ▶️ How to Run

```bash
pip install rasterio geopandas numpy matplotlib
jupyter notebook SurfaceTemperatureAnalysisUsingSatelliteImagery.ipynb
```

Provide the raster (and any vector) files at the paths set in the notebook, then run the cells.

---

<a name="-türkçe"></a>
## 🇹🇷 Türkçe

### Genel Bakış
Uydular, Dünya yüzeyinden çıkan termal ışımayı ölçer; bu da **Yüzey Sıcaklığına (LST)** dönüştürülebilir — kentsel ısı adaları, tarım, kuraklık ve iklim çalışmaları için kilit bir gösterge. Bu proje uydu raster bantlarını okur, yüzey sıcaklığını hesaplar ve bir coğrafi alan üzerinde görselleştirir.

### Veri
Coğrafi raster görüntüler (GeoTIFF bantları, ör. termal/optik uydu verisi) ve bağlam için isteğe bağlı vektör katmanları (sınırlar/bölgeler).

### Yaklaşım
1. **Raster okuma** — GeoTIFF bantları `rasterio` ile açılır, üst veri (CRS, çözünürlük, kapsam) incelenir.
2. **LST hesabı** — bant matematiği / ölçekleme ile ham değerler yüzey sıcaklığına çevrilir.
3. **Coğrafi bağlam** — `geopandas` ile vektör sınırlar bindirilir.
4. **Görselleştirme** — `rasterio.plot` ve `matplotlib` ile sıcaklık haritaları çizilir; dizi işlemleri için `numpy`.

### Teknolojiler
`Python` · `rasterio` · `geopandas` · `numpy` · `matplotlib`

### Çalıştırma
```bash
pip install rasterio geopandas numpy matplotlib
jupyter notebook SurfaceTemperatureAnalysisUsingSatelliteImagery.ipynb
```
Raster (ve varsa vektör) dosyalarını notebook'taki yollara koy ve hücreleri çalıştır.
