keyclock command:

docker run -p 8081:8080 -e KEYCLOAK_ADMIN=admin KEYCLOAK_ADMIN_PASSWORD=admin --network msbank-network quay.io/keycloak/keycloak:18.0.0 start-dev

docker command:

docker run -d --name ms-gateway -p 8080:8080 -e EUREKA_SERVER=eureka-server -e KEYCLOAK_SERVER=mskeyclock -e KEYCLOAK_PORT=8080 --network msbank-network ms-gateway