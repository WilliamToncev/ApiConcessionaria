# Concessionária API

  Uma API desenvolvida em Java com Spring Boot para gerenciar a loja virtual de uma rede de concessionárias, possibilitando o cadastro de usuários, veículos, compras e cartões de crédito. Esta aplicação foi projetada para ser escalável, segura e compatível com aplicações web e mobile.

## Funcionalidades
### Cadastro e Autenticação
  •	Cadastro de usuários com:
  •	Nome, sobrenome, CPF, celular, email, senha e aceite dos termos de uso.
  •	Login com email e senha.
  •	Recuperação de senha por email (futuro).

### Gerenciamento de Veículos
  •	Listagem de veículos cadastrados com:
  •	Nome, marca, placa, características gerais e ficha técnica.
  •	Busca de veículos por placa.

### Compras
  •	Realização de compras de veículos com:
  •	Dados do cartão de crédito (número, titular, bandeira, CPF/CNPJ, vencimento e código de segurança).
  •	Salvamento do cartão de crédito para compras futuras.
  •	Registro de compras realizadas para consulta posterior.

### Concessionárias
  •	Listagem e busca de concessionárias com:
  •	Nome, endereço, telefone e site.

### Tecnologias Utilizadas
  •	Linguagem: Java 17
  •	Framework: Spring Boot
  •	Banco de Dados: H2 (para testes) ou PostgreSQL
  •	Segurança: Spring Security com BCrypt para criptografia de senhas
  •	Documentação: Swagger/OpenAPI (futuro)
  •	Testes: JUnit 5 e MockMvc (futuro)

## Estrutura do Projeto
### Entidades
  •	User: Representa os usuários do sistema.
  •	Vehicle: Representa os veículos disponíveis para compra.
  •	Card: Representa os cartões de crédito dos usuários.
  •	Purchase: Registra as compras realizadas.
  •	Concessionaria: Representa as concessionárias cadastradas no sistema.

### Repositórios
Interfaces que gerenciam o acesso ao banco de dados, como:
  •	UserRepository
  •	VehicleRepository
  •	CardRepository
  •	PurchaseRepository
  •	ConcessionariaRepository

### Serviços
Camadas de lógica de negócio para:
  •	Gerenciar usuários (UserService)
  •	Listar e buscar veículos (VehicleService)

### Controladores
Endpoints REST para:
  •	Cadastro e consulta de usuários (/api/users)
  •	Listagem e busca de veículos (/api/vehicles)

## Instalação e Configuração
### Pré-requisitos
  •	Java 17 ou superior
  •	Maven
  •	Banco de dados PostgreSQL (opcional)

### Passos
  1.	Clone o repositório:
  2.	git clone https://github.com/seu-usuario/concessionaria-api.git
      cd concessionaria-api
  3.	Configure o banco de dados no arquivo application.properties ou application.yml.
  4.	Execute o projeto:
      mvn spring-boot:run
  5.	Acesse a aplicação em http://localhost:8080.

## Endpoints Principais
### Usuários
  •	Registrar Usuário: POST /api/users/register
  •	Buscar Usuário por Email: GET /api/users/email/{email}

### Veículos
  •	Listar Veículos: GET /api/vehicles
  •	Buscar Veículo por Placa: GET /api/vehicles/placa/{placa}

### Melhorias Futuras
  •	Implementar Swagger para documentação detalhada da API.
  •	Adicionar endpoints para gerenciamento de compras e cartões.
  •	Criar testes automatizados para validação das funcionalidades.
  •	Otimizar a segurança com autenticação JWT.

### Contribuições
Contribuições são bem-vindas! Siga os passos abaixo:
1.	Faça um fork do repositório.
2.	Crie uma branch para suas modificações: git checkout -b minha-feature.
3.	Envie suas alterações: git push origin minha-feature.
4.	Abra um Pull Request.
