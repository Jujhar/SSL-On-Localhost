C:\Program Files (x86)\Ampps\apache\conf

==***1***==
<hr>
set OPENSSL_CONF="c:\Program Files (x86)\Ampps\apache\conf\openssl.cnf"

==***2***==
<hr>
openssl req -config "c:\Program Files (x86)\Ampps\apache\conf\openssl.cnf" -new -out "c:\Program Files (x86)\Ampps\apache\conf\server.csr" -keyout "c:\Program Files (x86)\Ampps\apache\conf\server.pem"

==***3***==
<hr>
openssl rsa -in "c:\Program Files (x86)\Ampps\apache\conf\server.pem" -out "c:\Program Files (x86)\Ampps\apache\conf\server.key"

==***4***==
<hr>
openssl x509 -req -signkey "C:\Program Files (x86)\Ampps\apache\conf\server.key" -days 1024 -in "C:\Program Files (x86)\Ampps\apache\conf\server.csr" -out "C:\Program Files (x86)\Ampps\apache\conf\server.crt"
