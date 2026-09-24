# Laboratorio 7 - Spark MLlib sobre la ENEIC

CC3084 Data Science, Universidad del Valle de Guatemala, Semestre II 2026.
Fernando Rueda (23748) y Fernando Hernández (23645).

Análisis exploratorio, segmentación con KMeans y regresión con Spark 3.5 (`pyspark.ml`)
sobre las bases de Personas de la ENEIC del INE: los cuatro trimestres de 2025 para
desarrollo y el primer trimestre de 2026 para la evaluación final.

## Ejecución

Requiere Java 17 y Python 3.10+.

```
python3.10 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
export JAVA_HOME=$(/usr/libexec/java_home -v 17)
jupyter nbconvert --to notebook --execute --inplace notebooks/lab7.ipynb
```

El notebook descarga las bases del sitio del INE a `data/raw/` si no existen y guarda los
conjuntos preparados en `data/processed/` como Parquet. La carpeta `data/` no se versiona.
