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

## Decode a x509 certificate
```
openssl x509 -in cert.crt -text
```

The `cert.crt` file is usually armored as follows

```
-----BEGIN CERTIFICATE-----
MIIFYDCC
```

## Convert a x509 certificate into DER format

This might be used to add a self signed CA cert to a windows certificate store

```
openssl x509 -pubkey -outform der -in ./root.pem -out ./root.cer
```
