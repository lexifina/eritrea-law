# Eritrea: law history in git

The law of Eritrea as a git history: one file per provision, one commit per law on the day it took effect, and the law that made each change as the commit's author. `git blame` names the law behind every paragraph; `git log` lists every change; picking a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law).

## What this repository holds

The Constitution of Eritrea as ratified by the Constituent Assembly on 23 May 1997, in English, the language of the copy used. It has never been brought into effect, so it is a record of a ratified text, not of the law in force. Beside it are the Penal Code, the Criminal Procedure Code and the Civil Procedure Code of 2015, in the English text of the Ministry of Justice edition, and two fact-only acts: legal-system facts from Wikidata (CC0) and Eritrea's treaty actions from the UN Treaty Collection.

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `constitution/` | The Constitution of Eritrea: preamble and Articles 1 to 59 | 1 | As ratified on 23 May 1997 (never brought into effect) |
| `penal-code/` | Penal Code of the State of Eritrea (2015): preamble and Articles 1 to 396 (the five annex charts are not included) | 1 | Oldest version available, dated 15 May 2015 (the Minister of Justice's foreword) |
| `criminal-procedure-code/` | Criminal Procedure Code of the State of Eritrea (2015): Articles 1 to 197 | 1 | Oldest version available, dated 15 May 2015 (the Minister of Justice's foreword) |
| `civil-procedure-code/` | Civil Procedure Code of the State of Eritrea (2015): Articles 1 to 501 | 1 | Oldest version available, dated 15 May 2015 (the Minister of Justice's foreword) |
| `legal-system/` | Legal system facts from Wikidata | 2 | Facts as of 30 October 2026 |
| `treaties/` | Treaty actions of Eritrea: signature, ratification, accession (UN Treaty Collection) | 23 | Each action on its own date, 1993 to 2025 |

## Source

Facts: Wikidata (https://www.wikidata.org/wiki/Q986, CC0 1.0) and the UN Treaty Collection (https://treaties.un.org/; facts only, no treaty text), retrieved 29-30 October 2026.

Constitution text: WIPO Lex, The Constitution of Eritrea (ER001), English PDF (https://www.wipo.int/wipolex/en/legislation/details/8937), retrieved 30 October 2026. WIPO Lex is an intergovernmental host; the Eritrean Government publishes no official online copy, so WIPO Lex is the source of the bytes.

Penal Code, Criminal Procedure Code and Civil Procedure Code text: the English PDFs of the Ministry of Justice's 2015 editions as published on Refworld by UNHCR (https://www.refworld.org/docid/55a51ccc4.html, https://www.refworld.org/docid/55a51de04.html and https://www.refworld.org/docid/55a51d914.html), retrieved 31 October 2026. Refworld is the host of the copies; the Eritrean Government publishes no official online copy.

Terms: the Civil Code of the State of Eritrea (2015), Article 1161, provides: "Official texts of a legislative, administrative or judicial nature shall not be subject to the provisions of this Title. They may be freely reproduced." (the 1993 Provisional Civil Code, Art. 1651, said the same).

## Dates

`constitution` has one version, dated **23 May 1997**, the day the Constituent Assembly ratified the Constitution. No date of entry into force exists because the Constitution has not been implemented. The commit is credited to the Constitution itself. `legal-system` and `treaties` are dated by the Wikidata fact's own date where it has one, otherwise by the retrieval date (30 October 2026) as the oldest version available, and by the day of each treaty action. `penal-code`, `criminal-procedure-code` and `civil-procedure-code` each have one version dated **15 May 2015**, the date of the Minister of Justice's foreword to the edition, credited to the Ministry of Justice as the oldest version available: the Penal Code and the Civil Procedure Code come into force on their publication in the Gazette of Eritrean Laws (Art. 3 and Art. 1(1)), and that date is not in the copy used.

## How it is checked

Every version is read back from git on the day it took effect and on the day before (`tools/check_repo.py`) and must match `corpus.json`; results are in `REPRODUCE.md`.

## What "author" means

The author of a commit is the law (or, for facts, the retrieval) that made the change, with an e-mail address that cannot exist (`<law key>@wipo.invalid`). The committer is always Lexifina.

## Limits

- The Constitution has no amendments; treaties come from a selected set of UN Treaty Collection pages, not every treaty. Of the 2015 codes, the Civil Code is not yet included (no copy with a usable text layer was found), and neither is the Eritrean Gazette.
- In the three codes, part, book, title and chapter headings are kept at the start of the article that follows them, page numbers are left out, and typographic quotes are made straight.
- The PDF's own typesetting and spelling are kept; line wraps are joined into numbered paragraphs.
