# IonoScope

**Download (Google Play):**  
https://play.google.com/store/apps/details?id=com.ktf.ionoscope&hl=en_US  

**Source code:**  
https://github.com/kfilip10/ion-app.git

---

## Overview

IonoScope is an educational Android application designed to demonstrate real-time ionospheric measurements using dual-frequency GNSS data collected from commercial smartphones.

---

## What is IonoScope?

IonoScope uses raw dual-frequency GNSS measurements (L1/L5) to estimate ionospheric **Total Electron Content (TEC)** from signal transit delays.

It is intended as:

- An educational tool for learning about GNSS and the ionosphere  
- A platform to support instructional labs on ionospheric density  
- A low-cost method for persistent ionospheric sensing using static smartphones

---

## Smartphone Capabilities

Modern Android devices and APIs support **dual-frequency GNSS (L1/L5)** measurements.  
By comparing L1 and L5 signal transit times, the app estimates slant TEC through the ionosphere.

---

## App Architecture

- **Capacitor runtime** – Bundles and hosts the application components  
- **Java GNSS plugin (Android API)** – Accesses raw GNSS measurements  
- **SvelteKit** – UI for learning pages, settings, and measurements; backend for data analysis  
- **SQLite** – Local data storage and CSV export for sharing

---

## App Uses

- Classroom demonstrations  
- Guided labs on signal propagation and ionospheric density  
- Long-term passive data collection with low-cost devices

---

## Education Features

- Learning modules covering:
  - Ionosphere basics  
  - GNSS fundamentals  
  - Signal propagation and delay  
  - TEC calculation  
- Real-time GNSS data displays  
- Embedded figures and short quizzes (“check on learning”)

---

## Labs and Data Analysis

- Live signal statistics and filtering  
- Summary tables and simple graphs  
- CSV data export via standard phone sharing (email, Drive, etc.)  
- Sample lab worksheet linked within the app

---

## Data Collection

- Continuous GNSS measurement logging  
- Local storage in SQLite  
- Exportable datasets for external analysis

---

## Low-Cost Persistent Sensing

Currently being investigated for viability

1. Deploy an inexpensive Android phone with clear sky view, doesn't need a phone plan, just wifi access for data sharing.
2. Collect data for ~24 hours to estimate satellite biases  
3. Run multi-day logging sessions  
4. Visualize ionospheric density externally (e.g., GIS tools)  
5. Compare results to research-grade receivers

---

## Limitations

- Android only (no raw GNSS access on iOS)  
- No device-specific satellite bias corrections  
- Some satellites may produce negative TEC values  
- Requires newer dual-frequency GNSS phones  
- Small development team → slower update cadence

---

## What’s Next

**Short term**

- UI/UX improvements  
- Better data visualization  
- Integrate VTEC calculations

**Long term**

- Support additional GNSS constellations  
- Background persistent logging  
- Improved satellite bias handling  
- Automated export and mapping pipelines  
- Validation against research-grade receivers

---

## Resources

- Slides, sample lab worksheet, and sample datasets included in the project repository  
- GitHub: https://github.com/kfilip10/IonoScope  
- https://www.unoosa.org/documents/pdf/psa/activities/2022/ISWI2022/s6_02.pdf This is another handy slide deck that describes the concepts and calculations.
- https://www.swpc.noaa.gov/products/us-total-electron-content This is a NOAA product that describes real time TEC (total electron content) but also has some other links to describe the phenomenon.
- https://www.nature.com/articles/s41586-024-08072-x This idea was also implemented differently in an article in Nature. Here they aggregated data from phones to measure the TEC across large geographic areas. 
- https://gssc.esa.int/navipedia/index.php/Ionospheric_Delay This is a helpful source from the European Space Agency that describes the phenomenon in a little more detail. 

---

## Contact

Kevin T. Filip  
kfilip10@gmail.com
