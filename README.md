# PNAD COVID — Pipeline (Spark + SQL)

## Objetivo
Extrair, padronizar e analisar microdados da PNAD COVID (IBGE) para explorar
comportamentos na pandemia e sinalizar riscos de novo surto.

## Estrutura
- `data/raw`: fontes originais (.zip, dicionários .xls)
- `data/interim`: extrações temporárias (CSV/TXT)
- `data/processed`: dados limpos e padronizados
- `src/etl`: scripts de extração e transformação
- `notebooks`: exploração e análises

## Como rodar
```bash
python -m venv .venv && source .venv/bin/activate  # (Windows: .venv\Scripts\activate)
pip install -r requirements.txt

# 1) Extrair arquivos
python src/etl/extract.py --raw_dir data/raw --out_dir data/interim

# 2) Padronizar/limpar
python src/etl/transform.py --in_dir data/interim --out_dir data/processed

# 3) Abrir o Spark e rodar consultas (notebook 03_analises_spark_sql.ipynb)

