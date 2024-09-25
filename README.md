# elk-keycloak-poc
POC repo for integrating the ELK stack with Keycloak

### Prerequisiti
- Keycloak avviato (non incluso nel docker-compose.yml)
- Un realm creato e configurato su Keycloak

### Step 1 - Configurazione
- Modificare nel file `.env` 
  - le password di Elastic e Kibana
  - l'encryption key
  - la PWD, la cartella dove si trova la cartella `config/`
  - url e port di Keycloak

- Modificare nella cartella `config/` il file `oidc_client_secret.txt` inserendo il client secret preso da Keycloak

### Step 2 - Avvio
- Avviare tramite `docker-compose up -d`

### Conclusione
- Controllando il log di elasticsearch, si può notare che il realm specificato è stato disabilitato

![screenshoot1](https://github.com/user-attachments/assets/4ea46e33-cb6b-4d56-b909-4739fe36e44a)
![screenshoot2](https://github.com/user-attachments/assets/930c541e-4ca4-4359-9d3d-245b1a0ead69)
