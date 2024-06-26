### Generating Private Key and CSR
```
openssl req -new -newkey rsa:2048 -nodes -keyout server.key -out server.csr
```

### Generating Self Signed Certs
```
openssl req -x509 -new -nodes -key server.key -sha256 -days 365 -out server.crt
```

### Encrypting File
```
openssl enc -aes-256-cbc -salt -in file.txt -out file.enc
```

### Decrypting File
```
openssl enc -aes-256-cbc -d -in file.enc -out file.dec
```

### Check Certificate Expiration Date
```
openssl x509 -in server.crt -noout -text
```
Not Before and Not After fields in the output to check the validity period of the certificate