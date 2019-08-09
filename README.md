# dataprocessor_client (for Python)

## Installing (USE PYTHON3 FOR GODS SAKE)
```
pip install dataprocessor_client
```

## Usage

```
from dataprocessor_client import client
conn = client.connect()
q = "select percentile_99(measure) from city_sensors"
job_id = conn.sql(q, "city_sensors")
conn.process(job_id)
```

## Deploying new versions

**To install:**
```
pip install . --user --upgrade
```

**To package:**
```
python setup.py sdist bdist_wheel
```

**To upload do pypi:**
```
twine upload dist/*
```
