# Bolsa de Valores - Sistema Distribuído com gRPC e NestJS

Este projeto implementa um sistema de bolsa de valores distribuído utilizando o framework NestJS com gRPC para comunicação entre microserviços. O sistema gerencia ordens de compra e venda de ações e suporta operações em tempo real, como criação, consulta e atualização de ordens.

## Funcionalidades

- **Cadastro de Ordens**: Envia uma ordem de compra ou venda de ações para ser processada.
- **Consulta de Ordens**: Consulta ordens existentes com base no ID da ordem ou ID da conta.
- **Atualização de Ordens**: Atualiza o status de uma ordem existente.
- **Remoção de Ordens**: Remove uma ordem existente do sistema.

## Tecnologias Utilizadas

- **NestJS**: Framework Node.js para construção de aplicações do lado do servidor.
- **gRPC**: Framework RPC para comunicação eficiente entre microserviços.
- **Protobuf**: Formato de serialização de dados para comunicação entre serviços.
- **ValidationPipe**: Validação e transformação de dados de entrada.

## Estrutura do Projeto

- **`src/`**: Código fonte da aplicação.
  - **`orders/`**: Módulo de ordens.
    - **`orders.controller.ts`**: Controlador para gerenciar requisições relacionadas a ordens.
    - **`orders.service.ts`**: Serviço para lógica de negócio e manipulação de ordens.
    - **`proto/`**: Definições dos serviços e mensagens gRPC.
      - **`orders.proto`**: Arquivo de definição dos serviços gRPC.
  - **`main.ts`**: Arquivo de entrada para a aplicação, configuração do microserviço gRPC.
  - **`validation-exception.filter.ts`**: Filtro global para tratamento de exceções de validação.

## Configuração

## Instalação e Configuração

Esta seção orienta sobre como preparar e executar o projeto Bolsa de Valores em sua máquina local. 

### Clonando o Repositório

Primeiro, clone o repositório do projeto para sua máquina local:

```bash
git clone https://github.com/username/projeto-bolsa-valores.git

cd projeto-bolsa-valores

npm install
```
### Compilando o Projeto
```bash
npm run build
```
#### Configuração do Ambiente
```bash
MONGO_URI=mongodb://localhost:27017/bolsa-valores
PORT=3000
```

### Executando a Aplicação
```bash
npm run start:dev
```