# Certificates

## Add Password to PFX
```
openssl pkcs12 -in cert.pfx -out tmp.pem -nodes
openssl pkcs12 -export -out cert.pfx -in tmp.pem 
```

## Get Expiration Date
```
openssl s_client -connect stackoverflow.com:443 -servername stackoverflow.com| openssl x509 -enddate -noout
```
