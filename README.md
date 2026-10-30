---
license: cc-by-nc-4.0
pretty_name: "Texas Oil & Gas Production and County Mineral Appraisal Summary (1993–2026)"
language:
- en
tags:
- oil-and-gas
- texas
- energy
- railroad-commission-of-texas
- mineral-rights
- open-data
size_categories:
- n<1K
configs:
- config_name: counties
  data_files: texas_counties_1993_2026.csv
- config_name: operators
  data_files: texas_top_100_operators.csv
---

# Texas Oil & Gas Production and County Mineral Appraisal Summary (1993–2026)

Oil and gas production for all 254 Texas counties from January 1993 through August 2026, and the 100 largest Texas operators of
the latest 12 months, compiled by [Royalty Clerk](https://royaltyclerk.com) from the Railroad Commission of Texas's public production reports
(65,182,259 monthly lease reports since 1993) and the mineral appraisal rolls of 143 Texas counties.

Data through **August 2026** (RRC production reports run about two months behind, and recent months still gain late reports).
Built 2026-10-30.

## Files

| File | Rows | What |
|---|---:|---|
| [`texas_counties_1993_2026.csv`](texas_counties_1993_2026.csv) | 254 | Every Texas county: cumulative oil and gas 1993–2026, peak year, last 12 months, producing leases, mineral roll accounts |
| [`texas_top_100_operators.csv`](texas_top_100_operators.csv) | 100 | The 100 operators with the most oil-equivalent over the last 12 months |
| `README.md` | | This file: columns, summary tables, and how RRC lease numbers, disposition codes and roll decimals work |
| [`historic_estate_and_family_leases_by_county.md`](historic_estate_and_family_leases_by_county.md) | | Leases named for estates, heirs, trusts and ranches, by county, with first report year (a finding aid for heirs and family historians) |
| `LICENSE`, `CITATION.cff`, `zenodo.json` | | License text, citation and repository metadata |

## `texas_counties_1993_2026.csv`

| Column | Meaning |
|---|---|
| `county` | County name |
| `fips` | 5-digit FIPS code (48 + county) |
| `rrc_county_no` | The Railroad Commission's 3-digit county code |
| `rrc_districts` | RRC production districts that include the county |
| `oil_bbl_1993_2026` | Oil and condensate reported by the county's leases, January 1993 to August 2026, barrels |
| `gas_mcf_1993_2026` | Casinghead gas and gas-well gas over the same months, thousand cubic feet (mcf) |
| `peak_year` | The complete calendar year (1993–2025) with the most oil-equivalent (oil + gas / 6); blank when nothing was reported |
| `peak_year_boe` | Oil-equivalent barrels in the peak year |
| `oil_bbl_last_12m`, `gas_mcf_last_12m` | The 12 months to August 2026 |
| `active_leases` | Leases the latest RRC data shows as producing: volume reported in at least one of the latest 3 months |
| `mineral_roll_accounts` | Accounts on the county's newest mineral appraisal roll loaded by Royalty Clerk; blank when not loaded |
| `mineral_roll_year` | Tax year of that roll |
| `county_url` | The county's page, with monthly trends, top leases, operators, fields and drilling permits |

## `texas_top_100_operators.csv`

| Column | Meaning |
|---|---|
| `rank` | By `boe_last_12m` |
| `operator` | Operator name as filed with the RRC (title-cased) |
| `rrc_operator_no` | RRC operator number (Form P-5). One company can file under several numbers; this list is by number |
| `active_leases` | Producing leases the operator runs now |
| `counties_active` | Counties with at least one of those leases |
| `oil_bbl_last_12m`, `gas_mcf_last_12m` | Production reported under the operator's number in the 12 months to August 2026 |
| `boe_last_12m` | Oil + gas / 6 |
| `share_of_texas_boe_pct` | Percent of all Texas oil-equivalent over the same months |
| `flared_vented_pct` | Gas reported under disposition code 4 (vented or flared) as a percent of all gas disposed of, on the leases it runs now |
| `operator_url` | The operator's page: leases, counties, fields, permits and where its gas went |
| `report_card_url` | The operator's report card (output, leases gained and lost, buyers, permits), when it has enough public signals for one |

## Summary tables

### Texas counties by cumulative oil-equivalent, January 1993 to August 2026

| # | County | Oil (million bbl) | Gas (billion cubic feet) | Peak year | Producing leases |
|---:|---|---:|---:|---:|---:|
| 1 | [Midland](https://royaltyclerk.com/texas/counties/midland-county-tx) | 2,349.2 | 7,889.2 | 2025 | 3,547 |
| 2 | [Reeves](https://royaltyclerk.com/texas/counties/reeves-county-tx) | 1,790.7 | 10,652.2 | 2025 | 4,472 |
| 3 | [Webb](https://royaltyclerk.com/texas/counties/webb-county-tx) | 288.7 | 17,692.1 | 2025 | 6,466 |
| 4 | [Martin](https://royaltyclerk.com/texas/counties/martin-county-tx) | 2,009.3 | 4,649.2 | 2025 | 3,874 |
| 5 | [Loving](https://royaltyclerk.com/texas/counties/loving-county-tx) | 1,457.5 | 6,061.0 | 2025 | 2,725 |
| 6 | [Karnes](https://royaltyclerk.com/texas/counties/karnes-county-tx) | 1,529.7 | 4,322.6 | 2019 | 2,541 |
| 7 | [Upton](https://royaltyclerk.com/texas/counties/upton-county-tx) | 1,288.5 | 5,028.7 | 2025 | 2,727 |
| 8 | [Panola](https://royaltyclerk.com/texas/counties/panola-county-tx) | 65.4 | 12,176.3 | 2022 | 4,581 |
| 9 | [Tarrant](https://royaltyclerk.com/texas/counties/tarrant-county-tx) | 0.4 | 9,885.6 | 2012 | 3,447 |
| 10 | [Pecos](https://royaltyclerk.com/texas/counties/pecos-county-tx) | 620.2 | 6,058.1 | 1994 | 1,362 |

### Texas counties by oil-equivalent, 12 months to August 2026

| # | County | Oil (million bbl) | Gas (billion cubic feet) | Producing leases |
|---:|---|---:|---:|---:|
| 1 | [Midland](https://royaltyclerk.com/texas/counties/midland-county-tx) | 238.9 | 1,028.5 | 3,547 |
| 2 | [Martin](https://royaltyclerk.com/texas/counties/martin-county-tx) | 258.5 | 803.6 | 3,874 |
| 3 | [Reeves](https://royaltyclerk.com/texas/counties/reeves-county-tx) | 167.1 | 1,163.8 | 4,472 |
| 4 | [Loving](https://royaltyclerk.com/texas/counties/loving-county-tx) | 171.1 | 699.3 | 2,725 |
| 5 | [Webb](https://royaltyclerk.com/texas/counties/webb-county-tx) | 21.5 | 1,298.3 | 6,466 |
| 6 | [Upton](https://royaltyclerk.com/texas/counties/upton-county-tx) | 111.5 | 482.6 | 2,727 |
| 7 | [Reagan](https://royaltyclerk.com/texas/counties/reagan-county-tx) | 74.8 | 538.7 | 2,173 |
| 8 | [Howard](https://royaltyclerk.com/texas/counties/howard-county-tx) | 79.5 | 415.2 | 2,159 |
| 9 | [Culberson](https://royaltyclerk.com/texas/counties/culberson-county-tx) | 47.7 | 587.3 | 1,180 |
| 10 | [Karnes](https://royaltyclerk.com/texas/counties/karnes-county-tx) | 77.6 | 242.1 | 2,541 |

### Top 10 Texas operators, 12 months to August 2026

| # | Operator | Producing leases | Oil (million bbl) | Gas (billion cubic feet) | Share of Texas BOE | Flared or vented |
|---:|---|---:|---:|---:|---:|---:|
| 1 | [Pioneer Natural Res. USA, Inc.](https://royaltyclerk.com/texas/operators/pioneer-natural-res-usa-inc-665748) | 4,137 | 227.7 | 820.3 | 8.48% | 0.31% |
| 2 | [Diamondback E&P LLC](https://royaltyclerk.com/texas/operators/diamondback-e-p-llc-217012) | 3,847 | 220.6 | 860.6 | 8.47% | 1.55% |
| 3 | [EOG Resources, Inc.](https://royaltyclerk.com/texas/operators/eog-resources-inc-253162) | 3,665 | 83.0 | 620.2 | 4.34% | 0.23% |
| 4 | [Anadarko E&P Onshore LLC](https://royaltyclerk.com/texas/operators/anadarko-e-p-onshore-llc-020528) | 1,239 | 83.9 | 326.9 | 3.22% | 0.06% |
| 5 | [BPX Operating Company](https://royaltyclerk.com/texas/operators/bpx-operating-company-085408) | 1,440 | 51.6 | 453.6 | 2.96% | 0.13% |
| 6 | [XTO Energy Inc.](https://royaltyclerk.com/texas/operators/xto-energy-inc-945936) | 1,525 | 55.4 | 352.7 | 2.66% | 0.17% |
| 7 | [Apache Corporation](https://royaltyclerk.com/texas/operators/apache-corporation-027200) | 1,581 | 56.7 | 300.2 | 2.48% | 1.02% |
| 8 | [Chevron U. S. A. Inc.](https://royaltyclerk.com/texas/operators/chevron-u-s-a-inc-148113) | 641 | 44.0 | 313.8 | 2.24% | 0.13% |
| 9 | [Burlington Resources O & G Co LP](https://royaltyclerk.com/texas/operators/burlington-resources-o-g-co-lp-109333) | 1,114 | 57.1 | 218.1 | 2.18% | 0.10% |
| 10 | [Cog Operating LLC](https://royaltyclerk.com/texas/operators/cog-operating-llc-166150) | 1,248 | 52.6 | 201.8 | 2.01% | 0.15% |

### Texas by year, 1993–2026

Every lease with a county on file, including offshore state-waters areas.

| Year | Oil (million bbl) | Gas (billion cubic feet) | Oil-equivalent (million bbl) |
|---:|---:|---:|---:|
| 1993 | 612.5 | 5,608.6 | 1,547.3 |
| 1994 | 581.5 | 5,670.5 | 1,526.6 |
| 1995 | 552.2 | 5,664.3 | 1,496.2 |
| 1996 | 539.0 | 5,832.7 | 1,511.1 |
| 1997 | 530.9 | 5,812.4 | 1,499.6 |
| 1998 | 499.4 | 5,785.3 | 1,463.6 |
| 1999 | 445.5 | 5,566.7 | 1,373.3 |
| 2000 | 438.5 | 5,717.3 | 1,391.3 |
| 2001 | 420.6 | 5,791.7 | 1,385.9 |
| 2002 | 405.8 | 5,691.5 | 1,354.3 |
| 2003 | 400.7 | 5,779.8 | 1,364.0 |
| 2004 | 392.7 | 5,980.4 | 1,389.5 |
| 2005 | 392.6 | 5,988.4 | 1,390.7 |
| 2006 | 392.5 | 6,310.5 | 1,444.2 |
| 2007 | 391.2 | 6,868.8 | 1,536.0 |
| 2008 | 405.9 | 7,693.9 | 1,688.2 |
| 2009 | 399.3 | 7,570.2 | 1,661.0 |
| 2010 | 426.9 | 7,455.5 | 1,669.5 |
| 2011 | 529.7 | 7,809.0 | 1,831.2 |
| 2012 | 725.5 | 8,049.4 | 2,067.1 |
| 2013 | 928.3 | 8,190.3 | 2,293.4 |
| 2014 | 1,160.2 | 8,547.0 | 2,584.7 |
| 2015 | 1,262.7 | 8,671.2 | 2,707.9 |
| 2016 | 1,170.5 | 8,058.3 | 2,513.6 |
| 2017 | 1,277.3 | 7,962.4 | 2,604.3 |
| 2018 | 1,613.1 | 8,926.8 | 3,100.9 |
| 2019 | 1,864.8 | 10,205.4 | 3,565.7 |
| 2020 | 1,774.8 | 10,241.5 | 3,481.7 |
| 2021 | 1,746.2 | 10,518.8 | 3,499.4 |
| 2022 | 1,873.4 | 11,450.0 | 3,781.7 |
| 2023 | 2,008.3 | 12,345.4 | 4,065.9 |
| 2024 | 2,078.3 | 12,910.5 | 4,230.0 |
| 2025 | 2,092.8 | 13,621.9 | 4,363.1 |
| 2026 (to August) | 1,304.3 | 9,135.1 | 2,826.8 |

Royalty Clerk's statewide view: [Texas oil and gas by county](https://royaltyclerk.com/texas).

## How the Texas records work

### Railroad Commission lease numbers

The Railroad Commission of Texas (RRC) files oil and gas production by *lease*, and it numbers oil and gas differently:

- **Oil leases** carry a lease number written as **5 digits** with leading zeros (`00002` to `71534` so far). Each district
  office hands out its own numbers, so the same number turns up in several districts: 34,093 of the 66,678 oil lease numbers on record are used in more than one district, some in as many as 10.
  An oil lease is therefore identified by **district + lease number** (for example district 08, lease 41234).
- **Gas production is reported well by well**, each well under its own **RRC gas ID**, written as **6 digits**
  (`000011` to `302264` so far). A gas "lease" in RRC production data is a single well.
  None of the 207,882 gas IDs on record appears in more than one district, so in practice a gas ID is unique statewide.
- The two ranges overlap as numbers: oil lease 41234 and gas ID 041234 are different properties. Always keep the type (oil or
  gas) with the number. Royalty Clerk's page addresses end in `-g` for gas wells for that reason.

Every lease reported since January 1993:

| Type | Written as | Numbers on record | Lowest | Highest |
|---|---|---:|---:|---:|
| Oil lease | 5 digits | 146,571 | 00002 | 71534 |
| Gas well | 6 digits | 207,882 | 000011 | 302264 |

Oil counts are district + number pairs; gas counts are gas IDs.

**Districts.** The RRC has 13 production districts: `01` to `06`, `6E`, `7B`, `7C`, `08`, `8A`, `09` and `10` (no plain 07). The RRC's own
data files code them as numbers (`6E` = 07, `7B` = 08, `7C` = 09, `08` = 10, `8A` = 11, `09` = 13, `10` = 14), so a raw district
code of `08` in a data file is not district 08. County appraisal rolls print the RRC number in their own formats, often without
the district or the type, which is why matching a roll account to a lease needs both.

Leases by district: oil leases and gas wells reported since 2020, how many of those are producing now (volume in the latest
three months), and leases last reported before 2020.

| District | Oil leases | Gas wells | Producing now | Reported only 1993-2019 |
|---|---:|---:|---:|---:|
| 01 | 8,725 | 9,642 | 14,269 | 7,997 |
| 02 | 4,101 | 6,560 | 6,369 | 13,386 |
| 03 | 6,569 | 4,816 | 5,934 | 16,411 |
| 04 | 1,304 | 15,717 | 10,031 | 19,593 |
| 05 | 1,099 | 6,919 | 6,019 | 2,730 |
| 06 | 2,765 | 20,069 | 14,387 | 9,386 |
| 08 | 30,649 | 11,525 | 29,506 | 12,896 |
| 09 | 7,964 | 22,425 | 19,556 | 13,385 |
| 10 | 3,581 | 16,349 | 12,401 | 8,113 |
| 6E | 1,044 | 0 | 761 | 561 |
| 7B | 5,505 | 5,696 | 5,171 | 13,992 |
| 7C | 9,551 | 15,318 | 17,787 | 9,099 |
| 8A | 4,961 | 308 | 3,520 | 3,872 |

### Form PR disposition codes

Each month the operator files a production report (Form PR) that says how much oil and gas each lease produced and where it went
(its *disposition*), one code per destination. The codes are public and are the closest public record of what was sold.
Royalty is normally figured on gas sold to a transmission line (code 2) or a processing plant (code 3); code 1 and code 4 gas
was not sold.

Share of all Texas gas disposed of, by code, September 2025 to August 2026:

| Gas code | Meaning | What happened | Share |
|---|---|---|---:|
| 1 | Lease or field fuel use | Burned on the lease; not sold | 2.41% |
| 2 | Transmission line | Sold into a pipeline with no further processing | 45.46% |
| 3 | Processing plant | Delivered to a gas plant that strips natural gas liquids (reported on Form R-3) | 50.87% |
| 4 | Vented or flared | Released or burned; not sold (Statewide Rule 32) | 0.85% |
| 5 | Gas lift | Sent back down a well to lift oil | 0.17% |
| 6 | Repressure / pressure maintenance | Injected to hold reservoir pressure | 0.24% |
| 7 | Carbon black plant | Rare in current reports | 0.00% |
| 8 | Other | Any other use the operator reports | 0.00% |

Oil and condensate disposition over the same months:

| Oil code | Meaning | Share |
|---|---|---:|
| 0 | Pipeline | 81.97% |
| 1 | Truck | 17.84% |
| 2 | Tank car or barge | 0.00% |
| 3 | Net oil from tank cleaning | 0.00% |
| 4 | Circulating oil | 0.00% |
| 5 | Lost or stolen (spills, fires, theft) | 0.00% |
| 6 | Sedimentation (BS&W from tank cleaning) | 0.00% |
| 7 | Other (stock adjustment, lease use, etc.) | 0.01% |
| 8 | Skim liquid hydrocarbons (charged back by a disposal system, Form P-18) | 0.17% |
| 9 | Scrubber oil (charged back by a gas plant, Form R-3) | 0.00% |

Explained for owners: [Railroad Commission disposition codes explained](https://royaltyclerk.com/learn/rrc-disposition-codes-explained).

### County mineral roll decimals

Texas taxes producing minerals as real property. Each appraisal district (CAD) values the oil and gas leases in its county every
year, as of January 1, usually from the lease's production and the Comptroller's average prices (Texas Tax Code §23.175), and
splits each lease's value among its owners. Every owner's share is an **account** on the county's mineral roll, with:

- an **interest type**: royalty (RI), overriding royalty (ORRI) or working interest (WI);
- a **decimal interest**: the owner's share of the lease's production revenue; and
- an **appraised value**: roughly the lease's value times that decimal (a working interest also carries its share of costs).

A royalty decimal is a product of fractions. An owner of one quarter of the minerals under a tract leased at a 3/16 royalty owns
0.25 × 0.1875 = **0.046875** of that tract's production; if the tract is 40% of a pooled unit, the decimal on the unit becomes
0.046875 × 0.40 = **0.01875**. Each county's roll covers only the part of a lease inside that county, and districts round
decimals differently, so the roll decimal can differ from the operator's division order decimal; so can the January 1 date or a
unit change since.

Decimals on the newest roll of the 143 counties in this release:

| Interest type | Accounts | Decimal 0 to 1 | Above 1 | 10th pct | Median | 90th pct | Exactly 1/8 | 3/16 | 1/5 | 1/4 |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| Royalty interest (RI) | 4,767,097 | 4,764,492 | 1,705 | 0.000016 | 0.000349 | 0.007560 | 5,832 | 805 | 1,140 | 4,858 |
| Overriding royalty (ORRI) | 620,281 | 619,980 | 227 | 0.000030 | 0.000769 | 0.012518 | 861 | 18 | 24 | 78 |
| Working interest (WI) | 130,619 | 130,294 | 325 | 0.727000 | 0.768817 | 0.875000 | 31 | 25 | 14 | 14 |
| Other / not typed | 1,268,724 | 228,465 | 29,754 | 0.001465 | 0.040804 | 0.425260 | 231 | 43 | 89 | 184 |

Percentiles use decimals from 0 to 1 only; a decimal above 1 cannot be a share of a lease, so those accounts are counted
separately. In the royalty row, the exact fractions are the common lease royalty rates (1/8, 3/16, 1/5, 1/4), held by an owner of all the
minerals in a tract; most royalty accounts are much smaller shares of those.

Explained for owners: [What your decimal interest means](https://royaltyclerk.com/learn/what-your-decimal-interest-means).

## Method and caveats

- **Source.** Production comes from the RRC's Production Data Query bulk download (one row per lease per month, as filed by the
  operator; months with no filed report are left out, not counted as zero). 1993–2019 were loaded once from the download dated
  2026-09-18; 2020 on are refreshed every month when the RRC posts a new one (this release: 2026-10-20).
- **Counties.** The RRC reports by lease, not by county. Each lease is counted in one county: for 1993–2019, the county where
  most of its wells are; from 2020, the lease's primary county. A lease that spans a county line is counted once.
- **Not in the county file:** offshore state-waters areas (26.1 million bbl of oil and 1.07 billion mcf of gas since 1993, in the yearly table) and leases with no county on file (60,499 bbl and 295,065 mcf, in neither); together 0.27% of all Texas oil-equivalent since 1993.
- **Oil** includes condensate from gas wells; **gas** includes casinghead gas from oil leases. **BOE** uses 6 mcf = 1 barrel.
- **Latest months grow.** Operators file late and amend; the newest two or three months gain volume in later releases.
- **Operators** are RRC operator numbers. A merger shows up as leases moving from one number to another, not as one combined
  history. Production follows the number on each monthly report; active leases and flaring follow the operator that runs the
  lease now.
- **Mineral rolls** cover the 143 counties whose appraisal districts publish a roll Royalty Clerk loads; the others are blank.
  Some districts list lease equipment and other industrial property on the same roll, and those accounts are counted too.
- 230 of the 254 counties reported oil or gas production at some point since 1993.

## Sources

- Railroad Commission of Texas, [Production Data Query](https://webapps.rrc.texas.gov/PDQ/home.do) and [data sets available for download](https://www.rrc.texas.gov/resource-center/research/data-sets-available-for-download/).
- County appraisal district mineral rolls, as each district publishes them (one roll per county and tax year).
- Royalty Clerk, [Texas oil and gas by county](https://royaltyclerk.com/texas), [operators](https://royaltyclerk.com/texas/operators) and [operator report cards](https://royaltyclerk.com/texas/operators/report-cards): the pages behind each row, with monthly detail.

## License

The files in this package are released under the [Creative Commons Attribution-NonCommercial 4.0 International](https://creativecommons.org/licenses/by-nc/4.0/) license (CC BY-NC 4.0). You may copy,
share, chart and adapt them for non-commercial purposes, including research, teaching and journalism, as long as you credit
Royalty Clerk and link to https://royaltyclerk.com. For commercial use, contact support@royaltyclerk.com.

This license covers only the files in this package. It grants no rights to the rest of royaltyclerk.com, whose data stays under
its [terms](https://royaltyclerk.com/terms#data-license): quoting individual figures with a link is welcome; scraping and bulk copying are not. The underlying
RRC production reports and appraisal rolls are public records, available from those agencies.

## How to cite

> Royalty Clerk (2026). *Texas Oil & Gas Production and County Mineral Appraisal Summary (1993–2026)* (data through August 2026). https://royaltyclerk.com/texas
