# bookStore
O processo de cadastro envolve três camadas principais:

Frontend (React Native) → coleta os dados do usuário;
Backend (API Node.js) → valida e processa os dados;
Banco de Dados (MongoDB) → armazena as informações;

Fluxo de Funcionamento o usuário preenche formulário (username, email, password) o react Native envia requisição (POST /signup), backend recebe os dados passa pela validação dos campos depois verifica se o usuário já existe, usa a criptografada e a senha é salva no mongoDB. A resposta pode vir de certo ou errado para o usuário.

O frontend (React Native) coleta os dados do formulário e envia para o backend via requisição HTTP. O backend (Node.js + Express) tem a função de validar, trava e salvar os dados. O banco de dados amarzena as senhas quando salvas pelo criptografada. 
Exemplo de documento:
"_id": "123456", 
"username": "usuario123",
"email": "usuario@email.com" e
"password": "$2b$10$hashseguro..."

Práticas essenciais de senguração de armazenamento de dados:
Nunca armazenar senha em texto puro,
Utilizar hashing com bcrypt,
Validar entrada de dados,
Usar HTTPS em produção e
Não retornar senha nas respostas da API.

O mais seguro seria:
mail válido,
Senha com no mínimo 6 caracteres e
Username único (opcional).

