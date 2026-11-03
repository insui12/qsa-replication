# Surviving Quantum Mutants from QuCheck and Muskit Archives: Equivalent Builds, Input Limitations and Lost Histogram Information

Seojin Choi and Geunseok Yang (corresponding author: gsyang@hknu.ac.kr)
Department of Computer Science and Engineering, Hankyong National University

Replication files for the manuscript.

| File | Content | SHA-256 |
|---|---|---|
| `QSA_SQJ_manuscript.pdf` | Manuscript | `6f187aa133664e669ed409b7ccf0e08232a26fa8e736475fe62ef0e33812b7a7` |
| `QSA_SQJ_Online_Resource_1.pdf` | Online Resource 1: full tables and supporting analyses | `970efa246034eeb6bf46e9e5c553229cf37afd28c83e1e7ffc967392863a0efe` |
| `QSA_SQJ_Online_Resource_2.zip` | Online Resource 2: data, code and reproduction package ([release asset](https://github.com/insui12/qsa-replication/releases/tag/v1.0)) | `985ae8054d73cae1116699c6a9303a53d97e4d86b32f469dd0f543216d208a00` |
| `QSA_SQJ_latex_source.tar.gz` | LaTeX source of the manuscript | `c8807a7417b08aa603af0d1d53ec3c4aba245063a2e334426e36ad007ffc4347` |

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
