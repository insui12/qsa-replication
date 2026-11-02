# Diagnosing Undetected Quantum Mutants: Equivalence, Input Contracts and Oracle Statistics

Seojin Choi and Geunseok Yang (corresponding author: gsyang@hknu.ac.kr)
Department of Computer Science and Engineering, Hankyong National University

Replication files for the manuscript.

| File | Content | SHA-256 |
|---|---|---|
| `QSA_SQJ_manuscript.pdf` | Manuscript | `5cc047fe0c0624e5ab56453bc6497037530f4174c9797baf3c2d04b900793109` |
| `QSA_SQJ_Online_Resource_1.pdf` | Online Resource 1: full tables and supporting analyses | `548b8d215877c15f4cdd2aeb73e10f866466571a8e1492b0bd5b27f3ecfdde1e` |
| `QSA_SQJ_Online_Resource_2.zip` | Online Resource 2: data, code and reproduction package ([release asset](https://github.com/insui12/qsa-replication/releases/tag/v1.0)) | `6e20654944798e7a7a7a8b2b4dbf991d752854c964c993e59ceca28eb560fb46` |
| `QSA_SQJ_latex_source.tar.gz` | LaTeX source of the manuscript | `fed5efc608b7f9d2a49a2bd6e5d064c096be40473f57f1c9a64c167748b0612e` |

Online Resource 2 (139 MB) is attached to release `v1.0` because it exceeds the GitHub file size limit.
Check a download with `sha256sum <file>`.

## Reproduce

Requires Linux x86-64 and Python 3.11. Inside the unpacked `package/` directory of Online Resource 2:

```
python3.11 -m venv .venv
.venv/bin/python -m pip install --no-index --find-links reproduction_env/wheels numpy==1.26.4 scipy==1.17.1
PATH="$PWD/.venv/bin:$PATH" bash reproduce.sh
```

The script recomputes every number in the manuscript and ends with `PAPER NUMBERS IDENTICAL` and `PASS`.
`package/README.md` describes the contents.

## Licence

Authors' own code: Apache-2.0. Authors' own data and documents: CC BY 4.0. Full texts are in `LICENSE`.
Third-party material keeps its upstream licence and attribution: QuCheck (MIT) and Muskit texts are in `package/LICENSES/` of Online Resource 2; the numpy and scipy wheels and the LaTeX class and style files carry their own licence notices.
