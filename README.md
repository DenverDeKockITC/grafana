# grafana

docker volume create grafana-storage


docker stop grafana-container && docker rm grafana-container && aws sso login && eval "$(aws configure export-credentials --profile jnr-dev --format env)" && docker run -d -p 3000:3000 \
--name grafana-container \
-v grafana-storage:/var/lib/grafana \
  -e AWS_ACCESS_KEY_ID=$AWS_ACCESS_KEY_ID \
  -e AWS_SECRET_ACCESS_KEY=$AWS_SECRET_ACCESS_KEY \
  -e AWS_SESSION_TOKEN=$AWS_SESSION_TOKEN \
  grafana/grafana

  
