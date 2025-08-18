
# Minimal Hyperledger Fabric 2.5 App using Fabric CA

## Quickstart

```bash
cd network/scripts
bash startFabric.sh 


## Initial Structure
fabric-app-v2.5/
├── config/
│   └── configtx.yaml
├── network/
│   ├── docker-compose.yaml
│   ├── ca/
│   │   ├── ca.org1.example.com.yaml
│   ├── scripts/
│   │   ├── registerEnroll.sh
│   │   └── startFabric.sh
├── chaincode/
│   └── basic/
│       └── chaincode.go
└── README.md


# Generate TLS cert and key for the CA (self-signed)
openssl req -new -x509 -days 365 -nodes \
  -out ca/tls-cert.pem \
  -keyout ca/tls-key.pem \
  -config openssl-ca.cnf



sudo chown -R $USER:$USER .

sudo chown -R $USER:$USER ../../organizations
