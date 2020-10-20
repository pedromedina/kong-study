# Kong - Konga

Esse docker-compose executa alguns containers:

|Nome do serviço | Descrição                                            |
|----------------| -----------------------------------------------------|
|kong            |Api gateway kong                                      |
|kong-bootstrap  |Um container efêmero para inicializar o banco de dados|
|kong            |Uma GUI para a api de administração do Kong           |
|cassandra       |Banco de dados usado pelo Kong                        |
|api             |Uma api simples em python                             |


Para executar todos os serviços execute os passos abaixo:

1. Execute o comando `docker-compose up -d`
    
    Caso todos os serviços estajem rodando normalmente(verifique com `docker-compose ps`) é só acessar o konga na porta 1337 e se divertir, Se o kong não estiver rodando siga os próximos passos.

2. Se você chegou até aqui é provavel que o kong tenha ficado pronto antes do cassandra e não tenha conseguido executar as migrations para preparar o banco de dados, para corrigir isso execute `docker-compose up -d kong-bootstrap`, assim que o bootstrap terminar de rodar aguarde um pouco e o kong irá reiniciar normalmente.
