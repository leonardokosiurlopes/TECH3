pnad-covid/
├─ data/
│  ├─ raw/                # zips originais + dicionários .xls
│  ├─ interim/            # arquivos extraídos (CSV/TXT) sem limpeza
│  └─ processed/          # dados limpos/curados
├─ notebooks/
│  ├─ 01_extracao_validacao.ipynb
│  ├─ 02_limpeza_padronizacao.ipynb
│  └─ 03_analises_spark_sql.ipynb
├─ src/
│  ├─ etl/
│  │  ├─ extract.py
│  │  ├─ transform.py
│  │  └─ utils.py
│  └─ analytics/
│     └─ queries.sql
├─ env/                   # (opcional) configs locais
├─ README.md
├─ requirements.txt
├─ .gitignore
└─ .gitattributes         # se usar Git LFS
