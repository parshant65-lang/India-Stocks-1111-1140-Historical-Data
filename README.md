# India-Stocks-1111-1140-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1111 to 1140)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1111-1140-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1111 to 1140)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1111 | `GANDHITUBE` | Gandhi Special Tubes Limited | `GANDHITUBE.NS` |
| 1112 | `GANECOS` | Ganesha Ecosphere Limited | `GANECOS.NS` |
| 1113 | `GANESHBE` | Ganesh Benzoplast Limited | `GANESHBE.NS` |
| 1114 | `GANESHCP` | Ganesh Consumer Products Limited | `GANESHCP.NS` |
| 1115 | `GANESHHOU` | GANESH HOUSING LIMITED | `GANESHHOU.NS` |
| 1116 | `GANGAFORGE` | Ganga Forging Limited | `GANGAFORGE.NS` |
| 1117 | `GANGESSECU` | Ganges Securities Limited | `GANGESSECU.NS` |
| 1118 | `GARFIBRES` | Garware Technical Fibres Limited | `GARFIBRES.NS` |
| 1119 | `GARUDA` | Garuda Construction and Engineering Limited | `GARUDA.NS` |
| 1120 | `GATECH` | GACM Technologies Limited | `GATECH.NS` |
| 1121 | `GATECHDVR` | GACM Technologies Limited | `GATECHDVR.NS` |
| 1122 | `GATEWAY` | Gateway Distriparks Limited | `GATEWAY.NS` |
| 1123 | `GAUDIUMIVF` | Gaudium IVF and Women Health Limited | `GAUDIUMIVF.NS` |
| 1124 | `GAYAHWS` | Gayatri Highways Limited | `GAYAHWS.NS` |
| 1125 | `GAYAPROJ` | Gayatri Projects Limited | `GAYAPROJ.NS` |
| 1126 | `GCSL` | Gretex Corporate Services Limited | `GCSL.NS` |
| 1127 | `GEECEE` | GeeCee Ventures Limited | `GEECEE.NS` |
| 1128 | `GEEKAYWIRE` | Geekay Wires Limited | `GEEKAYWIRE.NS` |
| 1129 | `GEMAROMA` | Gem Aromatics Limited | `GEMAROMA.NS` |
| 1130 | `GENCON` | Generic Engineering Construction and Projects Limited | `GENCON.NS` |
| 1131 | `GENESYS` | Genesys International Corporation Limited | `GENESYS.NS` |
| 1132 | `GENSOL` | Gensol Engineering Limited | `GENSOL.NS` |
| 1133 | `GENUSPAPER` | Genus Paper & Boards Limited | `GENUSPAPER.NS` |
| 1134 | `GENUSPOWER` | Genus Power Infrastructures Limited | `GENUSPOWER.NS` |
| 1135 | `GEOJITFSL` | Geojit Financial Services Limited | `GEOJITFSL.NS` |
| 1136 | `GERMAN` | German Green Steel and Power Limited | `GERMAN.NS` |
| 1137 | `GFLLIMITED` | GFL Limited | `GFLLIMITED.NS` |
| 1138 | `GHCL` | GHCL Limited | `GHCL.NS` |
| 1139 | `GHCLTEXTIL` | GHCL Textiles Limited | `GHCLTEXTIL.NS` |
| 1140 | `GICHSGFIN` | GIC Housing Finance Limited | `GICHSGFIN.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream GANDHITUBE 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1111-1140-Historical-Data/main/GANDHITUBE/1m/2026/10/GANDHITUBE_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
