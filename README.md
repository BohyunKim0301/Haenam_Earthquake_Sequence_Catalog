# 2020 Haenam Earthquake Catalog (1,345 Events)

This repository provides the earthquake catalog compiled in our study of the 2020 Haenam sequence.  
The catalog contains 1,345 events detected using the Maximum Filter Template Matching (MFTM) method.

---

## 📑 Table of Contents

- [File Description](#-file-description)
- [Column Description](#-column-description)
- [Data Completeness and Missing Values](#-data-completeness-and-missing-values)
- [Methods Summary](#-methods-summary)
- [Citation](#-citation)
- [License](#-license)
- [Contact](#-contact)

---

## 📁 File Description

**Haenam_2020_catalog_v1.0.csv**

Format: CSV (comma-separated values)  
Encoding: UTF-8  
Time standard: UTC  

---

## 📌 Column Description

| Column Name | Description | Unit |
|-------------|------------|------|
| evid | Event identification number | – |
| origin_time_mftm | Origin time determined by MFTM | UTC |
| cc_max | Maximum cross-correlation coefficient among all templates | – |
| template_origin_time | Origin time of the template with the highest cross-correlation coefficient | UTC |
| template_evid | Event ID of the template with the highest cross-correlation coefficient | – |
| Mw | Moment magnitude | – |
| M_rel | Relative magnitude estimated from amplitude ratios | – |
| origin_time_hypo | Origin time determined by hypoellipse | UTC |
| lat | Hypocenter latitude from hypoellipse | degree |
| lon | Hypocenter longitude from hypoellipse | degree |
| depth | Hypocenter depth from hypoellipse | km |
| rel_lat | Relative latitude from hypoDD relocation | m |
| rel_lon | Relative longitude from hypoDD relocation | m |
| rel_depth | Relative depth from hypoDD relocation | m |
| lat_kma | Latitude reported by KMA | degree |
| lon_kma | Longitude reported by KMA | degree |
| depth_kma | Depth reported by KMA | km |
| M_kma | Local Magnitude reported by KMA | - |

---
## 📊 Data Completeness and Missing Values

- **Magnitude information**
  - When spectral fitting was successful, the event has a reported **moment magnitude (Mw)**.
  - If moment magnitude could not be determined, the magnitude is provided as **relative magnitude (M_rel)** estimated from amplitude ratios.
  - In such cases, the unused magnitude field is recorded as `NaN`.

- **Absolute location (hypoellipse)**
  - Hypocentral parameters (`origin_time_hypo`, `lat`, `lon`, `depth_km`) are provided only for events successfully processed with hypoellipse.
  - Events without hypoellipse solutions contain `NaN` in these fields.

- **Relative relocation (hypoDD)**
  - Relative coordinates (`rel_lat_m`, `rel_lon_m`, `rel_depth_m`) are available only for events included in the hypoDD relocation.
  - Events not relocated by hypoDD contain `NaN` in these columns.
    
- **KMA catalog information**
  - Hypocentral parameters reported by the Korea Meteorological Administration (`lat_kma`, `lon_kma`, `depth_kma_km`, `M_kma`) are provided only for events catalogued in the KMA catalog.
  - Events not reported by KMA contain `NaN` in these fields.

- All missing values are represented as `NaN`.

---

## 🔎 Methods Summary

- Event detection: Maximum Filter Template Matching (MFTM)
- Absolute location: hypoellipse
- Relative relocation: hypoDD
- Magnitude estimation:
  - Moment magnitude (Mw) from S-wave spectral analysis
  - Relative magnitude (M_rel) from inter-event amplitude ratios

---

## 📖 Citation

If you use this catalog, please cite:

> [Full citation of your paper]

---

## 📜 License

Specify the license here (e.g., CC-BY 4.0).

---

## 📬 Contact

For questions regarding the dataset, please contact:  
[Bohyun Kim]  
[Chonnam National University, Department of Geological and Environmental Sciences, Seismological Lab]  
[kbobo51@jnu.ac.kr]

---
