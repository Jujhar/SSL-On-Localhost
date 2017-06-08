C:\Program Files (x86)\Ampps\apache\conf

set OPENSSL_CONF="c:\Program Files (x86)\Ampps\apache\conf\openssl.cnf"

openssl req -config "c:\Program Files (x86)\Ampps\apache\conf\openssl.cnf" -new -out "c:\Program Files (x86)\Ampps\apache\conf\server.csr" -keyout "c:\Program Files (x86)\Ampps\apache\conf\server.pem"

openssl rsa -in "c:\Program Files (x86)\Ampps\apache\conf\server.pem" -out "c:\Program Files (x86)\Ampps\apache\conf\server.key"

openssl x509 -req -signkey "C:\Program Files (x86)\Ampps\apache\conf\server.key" -days 1024 -in "C:\Program Files (x86)\Ampps\apache\conf\server.csr" -out "C:\Program Files (x86)\Ampps\apache\conf\server.crt"
