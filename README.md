# India-Stocks-691-720-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 691 to 720)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-691-720-Historical-Data/
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

## 📦 Constituents (691 to 720)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 691 | `ASTRAZEN` | AstraZeneca Pharma India Limited | `ASTRAZEN.NS` |
| 692 | `ASTRON` | Astron Paper & Board Mill Limited | `ASTRON.NS` |
| 693 | `ATALREAL` | Atal Realtech Limited | `ATALREAL.NS` |
| 694 | `ATAM` | Atam Valves Limited | `ATAM.NS` |
| 695 | `ATL` | Allcargo Terminals Limited | `ATL.NS` |
| 696 | `ATLANTAA` | ATLANTAA LIMITED | `ATLANTAA.NS` |
| 697 | `ATLANTAELE` | Atlanta Electricals Limited | `ATLANTAELE.NS` |
| 698 | `ATLASCYCLE` | Atlas Cycles (Haryana) Limited | `ATLASCYCLE.NS` |
| 699 | `ATULAUTO` | Atul Auto Limited | `ATULAUTO.NS` |
| 700 | `AUGMONT` | Augmont Enterprises Limited | `AUGMONT.NS` |
| 701 | `AURIONPRO` | Aurionpro Solutions Limited | `AURIONPRO.NS` |
| 702 | `AURUM` | Aurum PropTech Limited | `AURUM.NS` |
| 703 | `AURUS` | AURUS GEM CORPORATION LIMITED | `AURUS.NS` |
| 704 | `AUSOMENT` | Ausom Enterprise Limited | `AUSOMENT.NS` |
| 705 | `AUSTENG` | Austin Engineering Company  Limited | `AUSTENG.NS` |
| 706 | `AUTOAXLES` | Automotive Axles Limited | `AUTOAXLES.NS` |
| 707 | `AUTOIND` | Autoline Industries Limited | `AUTOIND.NS` |
| 708 | `AVADHSUGAR` | Avadh Sugar & Energy Limited | `AVADHSUGAR.NS` |
| 709 | `AVALON` | Avalon Technologies Limited | `AVALON.NS` |
| 710 | `AVANCE` | Avance Technologies Limited | `AVANCE.NS` |
| 711 | `AVANTEL` | Avantel Limited | `AVANTEL.NS` |
| 712 | `AVG` | AVG Logistics Limited | `AVG.NS` |
| 713 | `AVL` | Aditya Vision Limited | `AVL.NS` |
| 714 | `AVONMORE` | Avonmore Capital & Management Services Limited | `AVONMORE.NS` |
| 715 | `AVROIND` | AVRO INDIA LIMITED | `AVROIND.NS` |
| 716 | `AVTNPL` | AVT Natural Products Limited | `AVTNPL.NS` |
| 717 | `AWFIS` | Awfis Space Solutions Limited | `AWFIS.NS` |
| 718 | `AWHCL` | Antony Waste Handling Cell Limited | `AWHCL.NS` |
| 719 | `AXISCADES` | AXISCADES Technologies Limited | `AXISCADES.NS` |
| 720 | `AXITA` | Axita Cotton Limited | `AXITA.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ASTRAZEN 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-691-720-Historical-Data/main/ASTRAZEN/1m/2026/10/ASTRAZEN_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
