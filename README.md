# 📅 Agendador de Horários API

API REST desenvolvida com Java e Spring Boot para gerenciamento de agendamentos de serviços.

O sistema permite cadastrar, consultar, atualizar e remover agendamentos, além de validar conflitos de horários automaticamente.

---

## 🚀 Tecnologias Utilizadas

- Java
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL
- Maven
- Lombok

---

## 📌 Funcionalidades

- Cadastro de agendamentos
- Consulta de agendamentos por data
- Atualização de agendamentos
- Remoção de agendamentos
- Validação de horários já ocupados
- Persistência de dados com JPA

---

## 📂 Estrutura do Projeto

```bash
src/main/java/br/com/larissa/agendador_horarios
│
├── controller
│   └── AgendamentoController.java
│
├── infrastructure
│   ├── entity
│   │   └── Agendamento.java
│   └── repository
│       └── AgendamentoRepository.java
│
├── service
│   └── AgendamentoService.java
│
└── AgendadorHorariosApplication.java
```

---


## 🔗 Endpoints

### ➕ Criar agendamento

```http
POST /agendamentos
```

### 🔍 Buscar agendamento por data

```http
GET /agendamentos?data=2026-05-20
```

### ✏️ Atualizar agendamento

```http
PUT /agendamentos
```

### ❌ Remover agendamento

```http
DELETE /agendamentos
```

---

## 📥 Exemplo de Requisição

```json
{
  "servico": "Corte de cabelo",
  "profissional": "Carlos",
  "dataHoraAgendamento": "2026-05-20T14:00:00",
  "cliente": "Larissa",
  "telefoneCliente": "11999999999"
}
```

---

## ⚙️ Regras de Negócio

- Não permite agendamentos duplicados no mesmo horário.
- Validação de disponibilidade de horário antes da criação do agendamento.
- Cada agendamento registra data de criação automaticamente.

---

## ▶️ Como Executar

### Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/agendador-horarios.git
```

### Configure o banco de dados

No arquivo `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/agendador
spring.datasource.username=SEU_USUARIO
spring.datasource.password=SUA_SENHA
```

### Execute a aplicação

Rodando a classe:

```bash
AgendadorHorariosApplication.java
```

---

## 🧪 Testes

Os endpoints podem ser testados utilizando:

- Postman
- Insomnia

---

## 📚 Conceitos Praticados

Este projeto foi desenvolvido para praticar:

- Desenvolvimento de APIs REST
- CRUD completo
- Spring Boot
- Spring Data JPA
- Arquitetura em camadas
- Injeção de dependência
- Regras de negócio
- Persistência de dados
- Organização de projetos backend

---

