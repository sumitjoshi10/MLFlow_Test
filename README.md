# MLFlow_Test

## For Dagshub

MLFLOW URL = https://dagshub.com/sumit.joshi9818/MLFlow_Test.mlflow

Use the following code for dagshub and mlflow
```bash
import dagshub
dagshub.init(repo_owner='sumit.joshi9818', repo_name='MLFlow_Test', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

```
