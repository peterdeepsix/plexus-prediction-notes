# plexus-prediction-notes

Berglas Setup
git clone https://github.com/jthegedus/firebase-gcp-examples/
cd firebase-gcp-examples/gcp-cloudrun-berglas/berglas-setup
chmod +x 01-bootstrap.sh 02-encrypt.sh
./01-bootstrap.sh
./02-encrypt.sh “api-key” “super secret test api key”

Berglas Docker
COPY --from=gcr.io/berglas/berglas:latest /bin/berglas /bin/berglas
ENTRYPOINT exec /bin/berglas exec -- yarn start

Berglas Cloudbuild
"--set-env-vars",
"API_KEY=berglas://berglas-secrets-$PROJECT_ID/API_KEY", "API_KEY=berglas://berglas-secrets-$PROJECT_ID/API_KEY",
