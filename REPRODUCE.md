# How this repository was made (Nasarawa State)

This file is written by the build on 2026-11-01, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| Nasarawa State Government: Laws as gazetted (PDF) | <https://nasarawastate.gov.ng/> | 2026-11-01 | Laws of Nasarawa State as published in the Nasarawa State of Nigeria Gazette, from the copies the Nasarawa State Government publishes at nasarawastate.gov.ng. Official texts of a legislative nature are not eligible for copyright: Copyright Act, 2022 (Nigeria), s. 3(b). |
| Nasarawa State Government: Laws as gazetted (PDF) | <https://nasarawastate.gov.ng/> | 2026-11-01 | Laws of Nasarawa State as published in the Nasarawa State of Nigeria Gazette, from the copies the Nasarawa State Government publishes at nasarawastate.gov.ng. Official texts of a legislative nature are not eligible for copyright: Copyright Act, 2022 (Nigeria), s. 3(b). |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `nagis-law-2017` | Nasarawa Geographic Information Service (NAGIS) Law, 2017 (Legal Notice No. 83 of 2017) | 1 | 2017-05-21 to 2017-05-21 |
| `nagis-amendment-law-2020` | Nasarawa Geographic Information Service (Amendment) Law, 2020 (Legal Notice No. 20 of 2020) | 1 | 2020-05-21 to 2020-05-21 |
| `nida-law-2021` | Nasarawa State Investment and Development Agency Law (Legal Notice No. 3 of 2021) | 1 | 2020-10-15 to 2020-10-15 |

The build made 3 commits:

| Commits | Kind |
| ---: | --- |
| 3 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-11-01.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 3 laws in the record.
- 6 tags.

## Dates

Each commit is dated at noon (Africa/Lagos) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Each Law here states its own commencement, and its version is dated by it; no general rule is applied. https://nasarawastate.gov.ng/

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `6f716b99a30eb4380a122384a623668457139b829406076a65d7b940d2146197` (113521 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `900da0d33bfd1ef455267fb4dcef7961fd5acc9c`, `check.py` `5d719354ea4c62d240c93d2cae446307d81d9e81`, `on.py` `aff48cf1b68d50c7ba8f399ca32261871c301824`.
- Python 3.14.4; git version 2.53.0.

## Checks

3 versions of 3 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- NAGIS Law 2017 is dated 2017-05-21: section 1 says it "shall come into force on 21st day of May 2017", the day the Governor assented.
- NAGIS (Amendment) Law 2020 is dated 2020-05-21: section 1 says it "shall be deemed to have come into effect on the 21st day of May 2020", the day the Governor assented.
- Each Law is one version: the text as enacted, credited to the Law itself (first_law) and dated by its commencement. Later amendments are not in this record.
- One file per section. The title lines printed before the enacting formula are "000-title", the enacting formula (where printed) is "001-enacting-formula", and schedules follow the sections. Each section's heading is its printed margin note (or, where there is none, "Section N") and stands as the file's first line; it is not part of the checked text.
- The text layer is read with line positions: running heads, page numbers and margin notes are set apart by their place on the page, and the pieces of one printed row are joined left to right. Lines wrapped by the printer are joined into one paragraph per line; a new paragraph starts at a section number, a bracketed (sub)paragraph letter or number, a quoted definition, a Part heading or a schedule heading. A Part heading printed after a section is placed at the head of the next section. Typing errors in the source stay as printed.
- NIDA Law 2021 is dated 2020-10-15: section 1 says it "shall come into operation on the 15th day of October, 2020", the day the Governor assented; it was gazetted on 21 January 2021.
- Each Law is one version: the text as enacted, credited to the Law itself (first_law) and dated by its commencement. Later amendments are not in this record.
- One file per section. The title lines printed before the enacting formula are "000-title", the enacting formula (where printed) is "001-enacting-formula", and schedules follow the sections. Each section's heading is its printed margin note (or, where there is none, "Section N") and stands as the file's first line; it is not part of the checked text.
- The text layer is read with line positions: running heads, page numbers and margin notes are set apart by their place on the page, and the pieces of one printed row are joined left to right. Lines wrapped by the printer are joined into one paragraph per line; a new paragraph starts at a section number, a bracketed (sub)paragraph letter or number, a quoted definition, a Part heading or a schedule heading. A Part heading printed after a section is placed at the head of the next section. Typing errors in the source stay as printed.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none: the text is the PDF text layer, parsed by rules; no model wrote or corrected legal text.
- none: the text is the PDF text layer, parsed by rules; no model wrote or corrected legal text.
