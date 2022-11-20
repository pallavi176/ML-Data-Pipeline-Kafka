# confluent-kafka-python


This repo help us to know how to publish and consume data to and from kafka confluent in json format.

Step 1: Create a conda environment
```
conda --version
```

Step2: Create  a conda environment
```
conda create -p mlproj1 python==3.8 -y
```

Step3:
```
conda activate mlproj1/
```
OR

```bash
conda create --prefix ./env python=3.8 -y
```

```bash
conda activate ./env
```
OR
```bash
source activate ./env
```

Step4:
```
pip install -r requirements.txt
```

Below repo help you to obtain requried credentials
```
https://github.com/Big-Data-01/confluent-tutorial.git
```


Cluster Environment Variable
```
API_KEY
API_SECRET_KEY
BOOTSTRAP_SERVER
```


Schema related Environment Variable
```
SCHEMA_REGISTRY_API_KEY
SCHEMA_REGISTRY_API_SECRET
ENDPOINT_SCHEMA_URL
```
Data base related Environment Variable
```
MONGO_DB_URL
```

## Update the credential in .env file and run below command to run your application in docker container


Create .env file in root dir of your project if it is not available
paste the below content and update the credentials
```
API_KEY=xxxxxxx
API_SECRET_KEY=xxxxxxxxxxxx
BOOTSTRAP_SERVER=xxxxxxxx
SCHEMA_REGISTRY_API_KEY=xxxxxxx
SCHEMA_REGISTRY_API_SECRET=xxxxxxxxxxxxxx
ENDPOINT_SCHEMA_URL=xxxxxxxx
MONGO_DB_URL=xxxxxxxxxxxxxx
```

Build docker image
```
docker build -t data-pipeline:lts .
```

For linux or mac
Run docker image
```
docker run -it -v $(pwd)/logs:/logs  --env-file=$(pwd)/.env data-pipeline:lts
```

Git repo commands
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/pallavi176/ML-Data-Pipeline-Kafka.git
git push -u origin main
```

git restore --staged <file_name>
