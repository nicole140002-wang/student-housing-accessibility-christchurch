# International Student Family Housing Site Selection in Christchurch

This project implements a **GIS-based spatial accessibility model** to identify suitable housing areas for international student families with primary school-aged children, who do not own private vehicles in Christchurch, New Zealand.  

Developed as part of the **GISC412 course (2025)** at the University of Canterbury.

---

## 🧭 Objectives
- Build a reproducible spatial analysis framework for housing site selection.
- Evaluate accessibility to **primary schools, University of Canterbury, and bus stops**.
- Generate composite suitability maps highlighting top residential zones.

---

## 📊 Data & Methods
- **Data sources**: Stats NZ (SA2, meshblock), OpenStreetMap (road network, schools, bus stops), Wikipedia (school list).  
- **Tools**: Python (GeoPandas, OSMnx, NetworkX, Pandas, Matplotlib, Contextily), Jupyter Notebook.  
- **Workflow**:
  1. Extract and clean open-source data.
  2. Build pedestrian network (1.2 m/s walking speed).
  3. Compute **network-based isochrones** (UC 40 min, schools 15 min, bus stops 15 min).
  4. Overlay and weight suitability (Schools 0.50, UC 0.35, Bus 0.15).
  5. Classify into five levels (Very Low → Very High).
  6. Produce final maps and SA2-based summaries.

---

## 🗺 Results

### UC Accessibility (0–40 min walk)
![](figures/uc_accessibility.png)

### Primary School Accessibility (0–15 min walk)
![](figures/primary_school_accessibility.png)

### Bus Stop Accessibility (0–15 min walk)
![](figures/bus_accessibility.png)

### Composite Suitability Map
![](figures/composite_suitability.png)

Top high-suitability areas: **Jellie Park, Ilam North, Fendalton**, with smaller clusters in Avonhead and Riccarton.

---

## 📂 Repository Structure
明白啦 👍。你这段内容其实就是 **仓库 README.md 里的 “目录结构 + 使用说明”** 部分。我帮你排版整理成一份规范的 Markdown，可以直接复制粘贴到 GitHub 仓库的 `README.md` 中。

---

# 📂 Repository Structure

```
notebooks/   → Jupyter notebooks (Python analysis)
report/      → Final PDF report
figures/     → Maps and charts
outputs/     → Spatial outputs (GeoPackage/CSV)
data/        → Sample datasets (small extracts only)
```

---

# 🔧 How to Reproduce

1. Clone this repository:

   ```bash
   git clone https://github.com/yourusername/student-housing-accessibility-christchurch.git
   cd student-housing-accessibility-christchurch
   ```

2. Open the main notebook in Jupyter:

   ```
   notebooks/GISC412_ProjectCode_WenjuanWang_submit.ipynb
   ```

3. Install dependencies (using conda):

   ```bash
   conda install geopandas osmnx contextily matplotlib networkx
   ```

4. Run cells step by step
   *(note: replace data paths if using your own datasets).*

---

# 📄 License

MIT License – feel free to use and adapt, with citation.

---

# ✍️ Citation

Wang, W. (2025). *International Student Family Housing Site Selection: A Spatial Accessibility Analysis in Christchurch*.
University of Canterbury, GISC412.

---
