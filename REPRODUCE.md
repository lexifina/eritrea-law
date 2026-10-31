# How this repository was made (Eritrea)

This file is written by the build on 2026-10-31, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| WIPO Lex: The Constitution of Eritrea (ER001), English text | <https://www.wipo.int/wipolex/en/legislation/details/8937> | 2026-10-30 | Official text of a law, exempt from copyright under Civil Code of the State of Eritrea (2015) Art. 1161; WIPO Lex is the host of the copy |
| Wikidata | <https://www.wikidata.org/wiki/Q986> | 2026-10-30 | CC0 1.0 |
| UN Treaty Collection (MTDSG status pages) | <https://treaties.un.org/> | 2026-10-29 | Facts only (treaty action, date, depositary); no text copied |
| UNHCR Refworld (publisher: National Legislative Bodies / National Authorities): Penal Code of the State of Eritrea (2015) | <https://www.refworld.org/docid/55a51ccc4.html> | 2026-10-31 | Official text of a law, exempt from copyright under Civil Code of the State of Eritrea (2015) Art. 1161; Refworld (UNHCR) is the host of the copy |
| UNHCR Refworld (publisher: National Legislative Bodies / National Authorities): Criminal Procedure Code of the State of Eritrea (2015) | <https://www.refworld.org/docid/55a51de04.html> | 2026-10-31 | Official text of a law, exempt from copyright under Civil Code of the State of Eritrea (2015) Art. 1161; Refworld (UNHCR) is the host of the copy |
| UNHCR Refworld (publisher: National Legislative Bodies / National Authorities): Civil Procedure Code of the State of Eritrea (2015) | <https://www.refworld.org/docid/55a51d914.html> | 2026-10-31 | Official text of a law, exempt from copyright under Civil Code of the State of Eritrea (2015) Art. 1161; Refworld (UNHCR) is the host of the copy |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution` | The Constitution of Eritrea (ratified 23 May 1997) | 1 | 1997-05-23 to 1997-05-23 |
| `legal-system` | Eritrea: legal system facts (Wikidata) | 2 | 1993-05-24 to 2026-10-30 |
| `treaties` | Treaty actions of Eritrea (UN Treaty Collection) | 23 | 1993-07-24 to 2025-01-06 |
| `penal-code` | Penal Code of the State of Eritrea (2015) | 1 | 2015-05-15 to 2015-05-15 |
| `criminal-procedure-code` | Criminal Procedure Code of the State of Eritrea (2015) | 1 | 2015-05-15 to 2015-05-15 |
| `civil-procedure-code` | Civil Procedure Code of the State of Eritrea (2015) | 1 | 2015-05-15 to 2015-05-15 |

The build made 39 commits:

| Commits | Kind |
| ---: | --- |
| 6 | first version of an act |
| 33 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-31.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 35 laws in the record.
- 63 tags.

## Dates

Each commit is dated at noon (Africa/Asmara) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: No date of entry into force is recorded: the Constitution was ratified on 23 May 1997 and, per the Government, has not been implemented. The ratification date is used as the version date. https://www.wipo.int/wipolex/en/legislation/details/8937

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `d20b4f606578bbfbd93f93f618dc887e37e2200660ea110507fde52e44714267` (1102194 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3d00541d258745461ab52b1b0cb4e1716a27a95d`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

29 versions of 6 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

A second build from the same corpus into an empty folder gave identical hashes for all 39 history commits and 63 tags (history tip `14cd90c0c60c956182ce53d9fb03cfdf1c03c2e3`).

## Decisions made by hand

- The Constitution was ratified by the Constituent Assembly on 23 May 1997 and has not been implemented; the version is dated by the ratification date because no entry-into-force date exists.
- Text source: the English PDF of the Constitution on WIPO Lex (an intergovernmental host), not an Eritrean government site, because no official online copy exists. Reuse rests on Civil Code of the State of Eritrea (2015), Art. 1161, which excludes official texts of a legislative nature from copyright and lets them be freely reproduced; the 1993 Provisional Civil Code, Art. 1651, said the same.
- Line wraps were joined into numbered paragraphs by the order of the numbers (1, 2, 3 and a, b, c); the PDF's own typesetting and spelling are kept.
- legal-system holds Wikidata facts (CC0); facts with a day-precision date are dated by it, the rest by the retrieval date 2026-10-30 as the oldest version available.
- treaties holds 30 multilateral treaties from the UN Treaty Collection status pages (retrieved 2026-10-29) to which Eritrea is a party or signatory, each action dated by its action date; coverage is limited to those selected status pages.
- Penal Code of the State of Eritrea (2015): one version dated 2015-05-15, the date of the Minister of Justice's foreword to the 2015 edition, credited to the Ministry of Justice as "oldest version available". By Art. 3 the Code comes into force on the date of its publication in the Gazette of Eritrean Laws, and the date of that Gazette issue is not in the source. The source records no later amendments.
- Penal Code of the State of Eritrea (2015): one unit per article (art-NNN) and one for the preamble; part, book, title, chapter and section headings are kept at the start of the article that follows them. Page numbers are left out and paragraphs running over a page break are joined. Typographic quotes are normalised to straight quotes. The five annexes (charts of graduated classes and of aggravating, mitigating and recidivism circumstances) are tables whose text layer does not keep their layout, so they are left out.
- Criminal Procedure Code of the State of Eritrea (2015): one version dated 2015-05-15, the date of the Minister of Justice's foreword to the 2015 edition, credited to the Ministry of Justice as "oldest version available". The Code states no date of its coming into force (Art. 4 refers only to "the day of its coming into force"), and the edition says "Published in June 2015". The source records no later amendments.
- Criminal Procedure Code of the State of Eritrea (2015): one unit per article (art-NNN); part, book, title, chapter and section headings are kept at the start of the article that follows them. Page numbers are left out and paragraphs running over a page break are joined. Typographic quotes are normalised to straight quotes.
- Civil Procedure Code of the State of Eritrea (2015): one version dated 2015-05-15, the date of the Minister of Justice's foreword to the 2015 edition, credited to the Ministry of Justice as "oldest version available". By Art. 1(1) the Code comes into force on the date of its publication in the Gazette of Eritrean Laws, and the date of that Gazette issue is not in the source. The source records no later amendments.
- Civil Procedure Code of the State of Eritrea (2015): one unit per article (art-NNN); part, book, title, chapter and section headings are kept at the start of the article that follows them. Page numbers are left out and paragraphs running over a page break are joined. Typographic quotes are normalised to straight quotes.

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- none
- none
- none
- none
