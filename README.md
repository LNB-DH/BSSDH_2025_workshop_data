# BSSDH_2025_workshop_data
Data for workshops in (Baltic Summer School of Digital Humanities 2025)[https://www.digitalhumanities.lv/bssdh/2025/about/]



=======================================================================
                           CORPUS OVERVIEW
=======================================================================

1. SOURCE MATERIAL
------------------

+----------------------------+---------------------------------------------------------+
| Periodical                 | Details                                                 |
+----------------------------+---------------------------------------------------------+
| "Rigasche Zeitung" (RZei)  | - Morning newspaper, intermittently published from      |
| (1918–1919)                |   1778 to 1919 in Riga.                                 |
|                            | - Language: German (Fraktur script)                     |
|                            | - Once the most popular morning paper in the Baltic     |
|                            |   provinces of the Russian Empire.                      |
|                            | - Covered general political and economic news in Riga,  |
|                            |   the Baltics, the Russian Empire, and internationally. |
|                            | - Historical context: World War I, Latvian War of       |
|                            |   Independence.                                         |
|                            | - Link: https://periodika.lv/#periodicalMeta:234;-1     |
|                            | - More info: https://enciklopedija.lv/skirklis/163962   |
+----------------------------+---------------------------------------------------------+
| "Latvian Economic Review"  | - Full title: "Latvian Economic Review: A quarterly     |
| (LERQ) (1936–1940)         |   review of trade, industry and agriculture".           |
|                            | - Language: English (modern)		               |
|                            | - Published by the Latvian Chamber of Commerce and      |
|                            |   Industry (established 1934).                          |
|                            | - Focused on cross-border representation of Latvian     |
|                            |   economy during the Great Depression, increasing       |
|                            |   state control, push for autarky, and start of WWII.   |
|                            | - Link: https://periodika.lv/#periodicalItem:620        |
+----------------------------+---------------------------------------------------------+

2. CORPUS INFORMATION
----------------------

+------------------------+-----------------------------+
| Metric                 | RZei         | LERQ         |
+------------------------+-----------------------------+
| Token Count (words)    | 5.37 million | 0.5 million  |
| Issue Count            | 359 issues   | 18 issues    |
| Segment (article) Count| 33,124       | 5,510        |
| Language               | German       | English      |
| Script                 | Fraktur      | Modern       |
+------------------------+-----------------------------+

Filename Structure:
-------------------
Format: [periodical][year][volume#*][issue#]_[page#]_[[plaintext]]_[segment#]

Example: `lerq1936s01n02_031_plaintext_s17.txt`
         → 17th segment from LERQ, Issue 2, 1936, page 31.

*Volume value in corpus is one in all cases.

3. METHODOLOGY
---------------

+----------------------------------------------------------------------------+
| Step                        | Description                                  |
+-----------------------------+----------------------------------------------+
| 3.1. Source Access          | Digitised issues obtained from the National  |
|                             | Library of Latvia (https://periodika.lv/)    |
+-----------------------------+----------------------------------------------+
| 3.2. Processing & OCR       | CCS docWORKS & ABBYY FineReader 9.0          |
|                             | - LERQ has better OCR quality than RZei      |
|                             | - No further data cleaning/normalization     |
+-----------------------------+----------------------------------------------+
| 3.3. Metadata Added         | Fields: title, author, uri                   |
|                             | - Author info available in:                  |
|                             |     LERQ: 4 cases (0.95%)                    |
|                             |     RZei: 325 cases (7.05%)                  |
|                             | - Title availability:                        |
|                             |     LERQ: 95.7%, RZei: 99.15%                |
|                             | - URI coverage: 100% for both                |
|                             | - URIs point to LNB DOM system               |
+----------------------------------------------------------------------------+

