# azure-lab
Repositório de estudo de Azure

Este projeto foi desenvolvido como parte de um aprendizado inicial sobre integração de aplicações Python com serviços do Azure. Ele consiste em um sistema de cadastro de produtos utilizando Streamlit para a interface, Azure Blob Storage para armazenamento de imagens e MySQL no Azure para o banco de dados.

Pontos de Aprendizado
1. Integração com Azure Blob Storage
O que é?
O Azure Blob Storage é um serviço de armazenamento de objetos na nuvem, ideal para armazenar grandes quantidades de dados não estruturados, como imagens e vídeos.

2. Uso de Variáveis de Ambiente
O que aprendemos?
Como configurar uma Connection String para acessar o Blob Storage.
Como fazer upload de arquivos (imagens) para um container no Blob Storage.
Como gerar URLs públicas para acessar os arquivos armazenados.

3. Uso de Variáveis de Ambiente
O que é?
Variáveis de ambiente são usadas para armazenar informações sensíveis, como credenciais de acesso, fora do código-fonte.

O que aprendemos?
Como usar a biblioteca python-dotenv para carregar variáveis de ambiente de um arquivo .env.
A importância de manter informações sensíveis, como chaves de acesso e senhas, fora do código.

4. Conexão com Banco de Dados MySQL no Azure
O que é?
O MySQL no Azure é um serviço gerenciado que permite hospedar bancos de dados MySQL na nuvem.
O que aprendemos?
Como configurar o servidor MySQL no Azure para aceitar conexões externas.
Como usar a biblioteca pymysql para conectar-se ao banco de dados e executar comandos SQL.
A importância de configurar corretamente o firewall do Azure para permitir conexões do IP local.

5. Tratamento de Erros
O que é?
O tratamento de erros é essencial para identificar e lidar com problemas durante a execução do programa.
O que aprendemos?
Como capturar erros específicos, como pymysql.MySQLError, para exibir mensagens amigáveis ao usuário.
Como usar try-except para evitar que o programa quebre em caso de falhas.

6. Uso do Streamlit
O que é?
O Streamlit é uma biblioteca Python que facilita a criação de interfaces web interativas para aplicações de dados.
O que aprendemos?
Como criar formulários simples para entrada de dados.
Como exibir imagens e informações formatadas na interface.
Como usar botões para acionar funções específicas, como salvar ou listar produtos.
8. Boas Práticas de Desenvolvimento
O que aprendemos?
A importância de organizar o código em funções reutilizáveis, como upload_blob e insert_product.
Como usar mensagens de sucesso e erro para melhorar a experiência do usuário.
A necessidade de validar entradas do usuário antes de processá-las.


Como Executar o Projeto
1-Pré-requisitos
Python 3.8 ou superior instalado.
Conta no Azure com um Blob Storage e MySQL configurados.
Biblioteca streamlit, azure-storage-blob, pymysql e python-dotenv instaladas.

2 - Configuração
Crie um arquivo .env com as seguintes variáveis:
BLOB_CONNECTION_STRING=<sua_connection_string>
BLOB_CONTAINER_NAME=<nome_do_container>
BLOB_ACCOUNT_NAME=<nome_da_conta>
SQL_SERVER=<servidor_mysql>
SQL_DATABASE=<nome_do_banco>
SQL_USER=<usuario>
SQL_PASSWORD=<senha>

3 - Executar o Projeto
No terminal, execute
streamlit run main.py

4 - Acessar a Interface
Abra o navegador e acesse o endereço exibido no terminal (geralmente http://localhost:8501).

Desafios Enfrentados: 
- Configuração do Firewall no Azure: Foi necessário permitir o IP público da máquina local para conectar ao MySQL.
- Erros de Timeout: Ajustamos o parâmetro connect_timeout para evitar desconexões durante consultas longas.
- Upload de Imagens: Aprendemos a lidar com erros ao fazer upload de arquivos para o Blob Storage.
  
