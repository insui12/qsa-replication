# Surviving Quantum Mutants from QuCheck and Muskit Archives: Equivalent Builds, Input Limitations and Lost Histogram Information

Seojin Choi and Geunseok Yang (corresponding author: gsyang@hknu.ac.kr)
Department of Computer Science and Engineering, Hankyong National University

Replication files for the manuscript.

| File | Content | SHA-256 |
|---|---|---|
| `QSA_SQJ_manuscript.pdf` | Manuscript | `54be8e9b6f5e8c407842d28e4abf60e2cf7f913cecbf53a48cca370fb070afa9` |
| `QSA_SQJ_Online_Resource_1.pdf` | Online Resource 1: full tables and supporting analyses | `a87d4c6dbb7e285eeeada802ffe84a8e46daa30b8ef1124366e1bf634643375c` |
| `QSA_SQJ_Online_Resource_2.zip` | Online Resource 2: data, code and reproduction package ([release asset](https://github.com/insui12/qsa-replication/releases/tag/v1.1)) | `f43f593686e088a0da0871fe904ffffc797e14623d704b6dcee6a36f7d81ed8b` |
| `QSA_SQJ_latex_source.tar.gz` | LaTeX source of the manuscript | `36f795c37be24c2b8ba323c6b2d8ca005dfe030bfa0f525ba39481a79f5e9bea` |

Online Resource 2 (86 MB) is attached to release `v1.1`.
Check a download with `sha256sum <file>`.

## Reproduce

Requires Linux x86-64 and Python 3.11. Inside the unpacked `package/` directory of Online Resource 2:

```
python3.11 -m venv .venv
.venv/bin/python -m pip install --only-binary=:all: --require-hashes -r reproduction_env/requirements-hashed.txt
PATH="$PWD/.venv/bin:$PATH" bash reproduce.sh
```

Installation fetches the pinned NumPy and SciPy wheels from PyPI and checks their SHA-256 hashes; the reproduction itself runs offline.
The script recomputes every number in the manuscript and ends with `PAPER NUMBERS IDENTICAL` and `PASS`.
`package/README.md` describes the contents.

## Licence

Authors' own code: Apache-2.0. Authors' own data and documents: CC BY 4.0. Full texts are in `LICENSE`.
Third-party material keeps its upstream licence and attribution: QuCheck (MIT) and Muskit texts are in `package/LICENSES/` of Online Resource 2; the LaTeX class and style files carry their own licence notices; NumPy and SciPy are installed from PyPI under their own licences.
