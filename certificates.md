# Certificates

## Add Password to PFX
openssl pkcs12 -in cert.pfx -out temp.pem -nodes
openssl pkcs12 -export -out cert.pfx -in tmp.pem 
