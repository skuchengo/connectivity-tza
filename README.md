# Tanzania — Connectivity and Population · Connectivité et population

**Population-weighted connectivity indicators from Ookla® Speedtest Open Data and WorldPop**
**Indicateurs de connectivité pondérés par la population, à partir des données ouvertes Ookla® Speedtest et de WorldPop**

[![Dashboard](https://img.shields.io/badge/dashboard-live-00A86A)](./index.html)
![Licence](https://img.shields.io/badge/licence-CC%20BY--NC--SA%204.0-D49A00)
![Languages](https://img.shields.io/badge/langues-EN%20%7C%20FR-00704A)

African Development Bank · AU STATAFRIC — STG17.
Generated on 2026-09-30 for **Tanzania (TZA)**,
reference period **2026 Q2**. The dashboard is bilingual: use the EN / FR switch in
the top-right corner. *Le tableau de bord est bilingue : utilisez le sélecteur EN / FR en haut à droite.*

## Headline figures · Chiffres clés

| Indicator · Indicateur | Value · Valeur |
|---|---|
| Population (2025, WorldPop) | 69,099,125 |
| Median mobile download **per person** · Débit médian **par habitant** | **21.7 Mbps** |
| Median download per measured tile · Débit médian par carreau mesuré | 21.9 Mbps |
| Population ≥ 10 Mbps · Population ≥ 10 Mbit/s | 73.4% |
| Population measured · Population mesurée | 18.6% |
| Land area measured · Territoire mesuré | 0.27% |
| Connectivity Gini · Gini de connectivité | 0.574 |
| Median latency · Latence médiane | 31 ms |
| ADM2 units · Unités ADM2 | 170 |

## Contents · Contenu

| File | Description |
|---|---|
| `index.html` | Bilingual interactive dashboard · Tableau de bord interactif bilingue |
| `connectivity_ADM2_TZA_2026Q2.csv` | Indicators by administrative unit · Indicateurs par unité administrative |
| `connectivity_ADM2_TZA_2026Q2.geojson` | Same, with geometry · Idem, avec géométrie |
| `national_summary_TZA_2026Q2.csv` | National aggregates · Agrégats nationaux |
| `tiles_TZA_2026Q2.parquet` | Tile-level micro-file · Fichier détail au carreau |
| `settlement_TZA_2026Q2.csv` | Urban / peri-urban / rural · Urbain / périurbain / rural |
| `metadata.json` | Machine-readable provenance · Provenance lisible par machine |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Method · Méthode

**EN.** Ookla publishes quarterly performance tiles at Web-Mercator zoom 16 (≈611 m at the equator).
Tiles covering Tanzania were extracted directly from the global parquet files using a quadkey
range predicate, clipped to the national polygon on the tile centroid, and converted from kbps to
Mbps. Each tile was located in the WorldPop 2025 1km population
grid (Global 2 R2025A) by its centroid; the population of each grid cell was shared equally among the tiles it
contains, giving every tile a population weight. All headline speeds are **population-weighted
medians**. Coverage of measurement is the share of the national population living in a grid cell
that contains at least one measured tile. Settlement classes are a density proxy
(urban ≥ 1500 people/km², peri-urban ≥ 300, rural below).

**FR.** Ookla publie des carreaux de performance trimestriels au zoom 16 en projection Web-Mercator
(≈611 m à l'équateur). Les carreaux couvrant Tanzania ont été extraits directement des
fichiers parquet mondiaux au moyen d'un prédicat d'intervalle sur le quadkey, découpés sur le
polygone national selon le centroïde du carreau, puis convertis de kbit/s en Mbit/s. Chaque carreau
a été localisé dans la grille de population WorldPop 2025 1km
(Global 2 R2025A) ; la population de chaque cellule a été répartie à parts égales entre
les carreaux qu'elle contient, ce qui donne à chaque carreau un poids de population. Tous les débits
mis en avant sont des **médianes pondérées par la population**. La couverture de la mesure est la
part de la population nationale vivant dans une cellule contenant au moins un carreau mesuré. Les
classes d'habitat sont une approximation par la densité (urbain ≥ 1500 hab./km²,
périurbain ≥ 300, rural en dessous).

## Limitations · Limites

**EN.** (1) Speedtest measurements are user-initiated and self-selected: no probability sample, no
design weights. (2) Absence of measurement is not absence of service —
81% of the population lives in a cell with no test in the reference
quarter. (3) Device and tariff effects cannot be separated from network performance. (4) Only
0.27% of the land area is measured and tests are heavily concentrated, so
unweighted national averages are biased upward. (5) WorldPop is a modelled surface, not a census,
and is partly built from night-time lights. (6) Boundaries come from geoBoundaries, not from the
national mapping authority. (7) This is **experimental statistics**, not an official indicator,
unless validated against operator or survey data.

**FR.** (1) Les mesures Speedtest sont lancées par les utilisateurs et auto-sélectionnées : ni
échantillon probabiliste, ni pondération de sondage. (2) L'absence de mesure n'est pas l'absence de
service — 81 % de la population vit dans une cellule sans aucun
test sur le trimestre de référence. (3) Les effets du terminal et du forfait ne peuvent être séparés
de la performance du réseau. (4) Seuls 0.27 % du territoire sont mesurés
et les tests sont très concentrés : les moyennes nationales non pondérées sont biaisées vers le
haut. (5) WorldPop est une surface modélisée, pas un recensement, et repose en partie sur les
lumières nocturnes. (6) Les limites administratives proviennent de geoBoundaries, et non de
l'autorité cartographique nationale. (7) Il s'agit de **statistiques expérimentales**, et non d'un
indicateur officiel, tant qu'elles n'ont pas été validées contre des données d'opérateurs ou
d'enquête.

## Sources and licences · Sources et licences

- **Ookla® Speedtest Open Data** — <https://github.com/teamookla/ookla-open-data> — **CC BY-NC-SA 4.0**
- **WorldPop** 2025 (1km, Global 2 R2025A) — <https://www.worldpop.org> — CC BY 4.0
- **geoBoundaries** (gbOpen) — <https://www.geoboundaries.org> — CC BY 4.0

## Licence of this product · Licence de ce produit

Released under **CC BY-NC-SA 4.0**, inherited from the Ookla licence (share-alike).
**Non-commercial use only.** Ookla trademarks are the property of Ookla, LLC. This product is not
endorsed by or affiliated with Ookla.

*Diffusé sous licence **CC BY-NC-SA 4.0**, héritée de la licence Ookla (partage dans les mêmes
conditions). **Usage non commercial uniquement.** Les marques Ookla sont la propriété d'Ookla, LLC.
Ce produit n'est ni approuvé par Ookla ni affilié à Ookla.*

## Reproducing · Reproduire

Open the notebook `02-Lab-Ookla-Speedtest-Open-Data-and-WorldPop.ipynb`, set
`COUNTRY_ISO3 = "TZA"` in the configuration cell, and run all cells. It runs unchanged in
Google Colab, Kaggle and locally, and requires no API key.
