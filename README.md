
# Tech Challenge - Product API

Microserviço responsável pela gestão de produtos da lanchonete digital.

**Observação:** Este repositório é parte da solução de arquitetura de software para o desafio Tech Challenge da Fiap, com outros microsserviços que compõe o sistema da lanchonete.

📚 Para mais detalhes sobre a solução e arquitetura de software completa, consulte nossa documentação [Repositório Overview](https://github.com/RenatoMartinsXrd/fiap-soat-tech-challenge-overview)

---

## 📦 Tecnologias Utilizadas

- Java 21 + Spring Boot
- PostgreSQL + Flyway
- Docker + Docker Compose
- Swagger (OpenAPI)
- Clean Architecture

---

## ▶️ Excutando a API Localmente

**Pré-requisitos:**
- Docker + Docker Compose
- (Opcional) Java 21 (caso queira rodar pela IDE)

**Passos:**

```bash
docker compose up --build
```

- API disponível em: http://localhost:8080

- PGAdmin: http://localhost:5050

---

### Acessando a documentação OpenAPI/Swagger

1. Abra o URL no seu navegador:

```sh
http://localhost:30080/swagger-ui/index.html
```

---

## 🔌 Endpoints Disponíveis

| Método | Rota           | Descrição                   |
|--------|----------------|-----------------------------|
| GET    | /products      | Lista todos os produtos     |
| GET    | /products/{id} | Retorna um produto específico |
| POST   | /products      | Cadastra um novo produto    |
| PUT    | /products/{id} | Atualiza um produto         |
| DELETE | /products/{id} | Remove um produto           |

> A documentação completa pode ser acessada via Swagger.

---

## 🧠 Arquitetura

Este microserviço adota o padrão **Clean Architecture**, com foco em separação de responsabilidades e independência tecnológica.

**Principais camadas:**

- **core**: Entidades, regras de negócio, casos de uso e contratos (ports)
- **adapters**: Controladores e mapeadores que traduzem o mundo externo para o domínio
- **frameworks**: Implementações específicas (REST, JPA, integrações externas)
- **shared**: Configurações globais e utilitários comuns

---

## 🧪 Testes

Os testes são realizados com **JUnit** e **Mockito** para garantir a qualidade do código.

### **Execução dos testes**

1. No diretório do repositório, execute o comando Maven para rodar os testes:

   ```bash
   mvn test
   ```

2. Para gerar o relatório de cobertura de testes com **Jacoco**, execute:

   ```bash
   mvn clean verify
   ```

3. A cobertura mínima exigida é de **80%**.

---

## 👥 Equipe

- Renato Martins - @RenatoMartinsXrd
- Daniel Quevedo - @dequevedo

---

