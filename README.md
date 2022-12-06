# Istio claim based routing

Create JWKS and JWT token using the `gen-jwt.py` script provided by Istio.

## Create JWT token for `details-v1`

    ./gen-jwt.py key.pem -jwks=./details-v1-jwks.json --expire=3153600000 --iss=testing@tetrate.io --aud=details-v1 --claims=group:bookinfo > v1-details.jwt

## Create JWT token for `details-v2`

    ./gen-jwt.py key.pem -jwks=./details-v2-jwks.json --expire=3153600000 --iss=testing@tetrate.io --aud=details-v2 --claims=group:bookinfo > v2-details.jwt
