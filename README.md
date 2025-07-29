# BSSDH_2025_workshop_data
Data for workshops in [Baltic Summer School of Digital Humanities 2025](https://www.digitalhumanities.lv/bssdh/2025/about/)

**Repository:** https://github.com/LNB-DH/BSSDH_2025_workshop_data


## CORPUS OVERVIEW


1. SOURCE MATERIAL
------------------

| Periodical | Details |
|------------|---------|
| "Rigasche Zeitung" (RZei) (1918–1919) | - **Data file:** `Rigasche_Zeitung_1918_1919.zip`<br>- **Download:** https://github.com/LNB-DH/BSSDH_2025_workshop_data/blob/main/data/Rigasche_Zeitung_1918_1919.zip<br>- Morning newspaper, intermittently published from 1778 to 1919 in Riga.<br>- Language: German (Fraktur script)<br>- Once the most popular morning paper in the Baltic provinces of the Russian Empire.<br>- Covered general political and economic news in Riga, the Baltics, the Russian Empire, and internationally.<br>- Historical context: World War I, Latvian War of Independence.<br>- Link: https://periodika.lv/#periodicalMeta:234;-1<br>- More info: https://enciklopedija.lv/skirklis/163962 |
| "Latvian Economic Review" (LERQ) (1936–1940) | - **Data file:** `Latvian_Economic_Review_1936_1940.zip`<br>- **Download:** https://github.com/LNB-DH/BSSDH_2025_workshop_data/blob/main/data/Latvian_Economic_Review_1936_1940.zip<br>- Full title: "Latvian Economic Review: A quarterly review of trade, industry and agriculture".<br>- Language: English (modern)<br>- Published by the Latvian Chamber of Commerce and Industry (established 1934).<br>- Focused on cross-border representation of Latvian economy during the Great Depression, increasing state control, push for autarky, and start of WWII.<br>- Link: https://periodika.lv/#periodicalItem:620 |

2. CORPUS INFORMATION
----------------------

| Metric | RZei | LERQ |
|--------|------|------|
| Token Count (words) | 5.37 million | 0.5 million |
| Issue Count | 359 issues | 18 issues |
| Segment (article) Count | 33,124 | 5,510 |
| Language | German | English |
| Script | Fraktur | Modern |

Filename Structure:
-------------------
Format: [periodical][year][volume#*][issue#]_[page#]_[[plaintext]]_[segment#]

Example: `lerq1936s01n02_031_plaintext_s17.txt`
         → 17th segment from LERQ, Issue 2, 1936, page 31.

*Volume value in corpus is one in all cases.

3. METHODOLOGY
---------------

| Step | Description |
|------|-------------|
| 3.1. Source Access | Digitised issues obtained from the National Library of Latvia (https://periodika.lv/) |
| 3.2. Processing & OCR | CCS docWORKS & ABBYY FineReader 9.0<br>- LERQ has better OCR quality than RZei<br>- No further data cleaning/normalization |
| 3.3. Metadata Added | Fields: title, author, uri<br>- Author info available in:<br>&nbsp;&nbsp;&nbsp;&nbsp;LERQ: 4 cases (0.95%)<br>&nbsp;&nbsp;&nbsp;&nbsp;RZei: 325 cases (7.05%)<br>- Title availability:<br>&nbsp;&nbsp;&nbsp;&nbsp;LERQ: 95.7%, RZei: 99.15%<br>- URI coverage: 100% for both<br>- URIs point to LNB DOM system |

