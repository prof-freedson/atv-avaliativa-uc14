# Repositório sobre a realização da atividade avaliativa da unidade curricular 14: Codificar acesso a webservices e recursos de sistemas móveis

A atividade consiste no desenvolvimento de uma API usando Node.js para o recebimento de requisições de comprovação de uso de recursos de câmera, GPS e rede de internet (wi-fi ou redes móveis) através de uma aplicação com React Native e Expo.

## Para o desenvolvimento da API, tem-se os seguintes requisitos:
- a API poderá ter somente o arquivo da aplicação principal;
- usar as linguagens JavaScript ou TypeScript;
- receber requisições e enviar dados em JSON;
- criar arquivo de variáveis de ambiente para a API;
- usar o banco de dados serverless PostgreSQL da Neon para o armazenamento das requisições vindas da aplicação React Native;
- instalar os pacotes para criação de servidor HTTP para envio e recebimento de requisições, conexão com banco de dados PostgreSQL da Neon e disponibilidade de uso da API para fontes externas;
- implementar endpoints para receber as requisições de cada recurso do dispositivo móvel(câmera, GPS e rede de internet) e de acesso dados dados de cada recurso;
- receber da câmera os seguintes dados: 
```json
{
    "fotoBase64": "string-longa-base-64",
    "cameraFoto": "frontal",
    "dataHoraFoto": "date" //data e hora da requisição  
}
```
> **Observação:** para `"fotoBase64"`, receber uma string longa em base64, sendo que a aplicação em React Native enviará a foto já no formato informado; para `"cameraFoto"`, receber o valor "frontal" ou "traseira".
- receber do GPS os seguintes dados: 
```json
{
    "latitude": "0.156846",
    "longitude": "25.58544",
    "dataHoraLocalizacao": "date" //data e hora da requisição
}
```
- receber da rede de internet os seguintes dados: 
```json
{
    "ipRede": "123.456.789.012",
    "tipoRede": "wi-fi",
    "dataHoraRede": "date" //data e hora da requisição
}
```
> **Observação:** para a leitura ou acesso aos dados do uso dos recursos do dispositivo móvel(câmera, GPS e rede de internet), o formato JSON pode ser o mesmo do recebimento.
- o envio das respostas da API para cada requisição deve ser uma mensagem de sucesso ou erro, a critério da equipe, e que deve ser consumida na aplicação React Native;

## Para o desenvolvimento da aplicação React Native, tem-se os seguintes requisitos:
- usar React Native e Expo;
- usar a linguagem TypeScript;
- criar arquivo de variáveis de ambiente para a API;
- usar o roteamento para navegação entre as telas da aplicação;
- instalar e configurar a aplicação para o uso dos recursos do dispositivo móvel(câmera, GPS e rede de internet);
- instalar os pacotes de roteamento da aplicação e de requisição de dados para API's;
- implementar uma tela inicial que permita ao usuário selecionar a interface para cada requisição de cada recurso do dispositivo móvel(câmera, GPS e rede de internet);
- utilizar somente os estilos usando o Stylesheet;

## Para o cumprimento da realização da atividade avaliativa, tem-se os seguintes requisitos:
- cada equipe deverá criar uma pasta para cada parte do sistema: `api` e `app`;
- realizar o fork do repositório do GitHub;
- enviar até a data limite da atividadeuma pull request para o repositório do GitHub com a contribuição de cada membro da equipe;
- os dados de conexão com o banco de dados PostgreSQL da Neon devem ser armazenados em variáveis de ambiente e será fornecidos pelo professor em breve;

## Observações finais:
- cada membro da turma fará parte da equipe mediante sorteio realizado em sala de aula. O resultado do sorteio fará parte do repositório do GitHub;
- a aplicação React Native deverá ser usada e testada através do aplicativo Expo Go. A API deverá ser usada ou inicializada localmente e testada através de qualquer cliente API (Thunder Client, Postman, Imsomnia, Postman, Hopscotch, etc);
- cada equipe deverá realizar contrbuições individuais, além de manter o espírito de colaboração, compartilhamento e ajuda mutua;