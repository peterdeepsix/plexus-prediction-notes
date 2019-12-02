# plexus-prediction-notes

Berglas Setup
git clone https://github.com/jthegedus/firebase-gcp-examples/
cd firebase-gcp-examples/gcp-cloudrun-berglas/berglas-setup
chmod +x 01-bootstrap.sh 02-encrypt.sh
./01-bootstrap.sh
./02-encrypt.sh api-key supersecrettestapikey

Berglas Docker
COPY --from=gcr.io/berglas/berglas:latest /bin/berglas /bin/berglas
ENTRYPOINT exec /bin/berglas exec -- yarn start

Berglas Cloudbuild
"--set-env-vars",
"API_KEY=berglas://berglas-secrets-$PROJECT_ID/API_KEY",


ENV FILE
apiKey = @@@@@@@@@@@@
authDomain = @@@@@@@@@@@@,
databaseURL = @@@@@@@@@@@@,
projectId = @@@@@@@@@@@@,
storageBucket = @@@@@@@@@@@@,
messagingSenderId = @@@@@@@@@@@@,
appId = @@@@@@@@@@@@,
measurementId = @@@@@@@@@@@@

type = @@@@@@@@@@@@
project_id = @@@@@@@@@@@@
private_key_id = @@@@@@@@@@@@
private_key = @@@@@@@@@@@@
client_email = @@@@@@@@@@@@
client_id = @@@@@@@@@@@@
auth_uri = @@@@@@@@@@@@
token_uri = @@@@@@@@@@@@
auth_provider_x509_cert_url = @@@@@@@@@@@@
client_x509_cert_url = @@@@@@@@@@@@

