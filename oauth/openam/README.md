 docker run --name apicast-rhsso --rm -p 8082:8082 -p 8090:8090 \
 -v /home/sgutierr/development/3Scale/pocs/utils/oauth/openam/keycloak.lua:/opt/app-root/src/src/oauth/keycloak.lua:ro \
 -v /home/sgutierr/development/3Scale/pocs/utils/oauth/implicit/nginx.conf:/opt/app-root/src/conf/nginx.conf:ro \
 -e RHSSO_ENDPOINT=http://99f857a7.ngrok.io/openam/oauth2/3Scale/connect/jwk_uri \
 -e APICAST_MANAGEMENT_API=debug \
 -e APICAST_LOG_LEVEL=debug \
 -e APICAST_SERVICES=2555417737596 \
 -e THREESCALE_PORTAL_ENDPOINT=https://d817aa540dbd7a811904012539ed6a52@sgutierr-admin.3scale.net \
 quay.io/3scale/apicast:v3.0.0
