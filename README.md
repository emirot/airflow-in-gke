# airflow-in-gke
Airflow in GKE

### How to lauch the config 

`kubectl create -f config/`

You will have to change the fernet key in the config map : 
```
python -c "from cryptography.fernet import Fernet; FERNET_KEY = Fernet.generate_key().decode(); print(FERNET_KEY)"
```

### Image used

All the hard work is done in this image : 

`https://github.com/puckel/docker-airflow`



TO DO : 
- Logs 
