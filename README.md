# Kong - Konga

Esse docker-compose executa alguns containers:

1. Kong
2. Konga(Uma GUI para a api de administração do Kong)
3. Cassandra(Banco de dados usado pelo Kong)
4. Uma api em python que tem apenas a rota '/books'

Para rodar o Kong e o Konga(Dashboar para kong) basta rodar o comando `docker-compose up -d`
