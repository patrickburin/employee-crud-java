# 💼 CRUD de Gestão de Funcionários

Este é um projeto backend de gerenciamento de funcionários. Foi desenvolvido com Quarkus e Java, conectados a um banco de dados MySQL.

---

# 💼 Employee Management CRUD

This is a backend project for managing employees. It was developed using Quarkus and Java, connected to a MySQL database.

---

## 🚀 Tecnologias Utilizadas | Technologies Used

### Backend

- **Java 17**: Linguagem de programação moderna e versátil | Modern and versatile programming language
- **Quarkus**: Framework Java voltado a performance e cloud-native | Java framework focused on performance and cloud-native applications
- **Jakarta REST (JAX-RS)**: Para criação de APIs RESTful | For building RESTful APIs
- **Hibernate ORM com Panache**: ORM simplificado para persistência com JPA | Simplified ORM for persistence with JPA

### Banco de Dados | Database

- **MySQL**: Banco de dados relacional | Relational database
- **MySQL Workbench**: Interface visual opcional para administração do banco | Optional visual interface for database management

---

## ⚙️ Requisitos para Executar Localmente | Requirements to Run Locally

### Backend

- Java 17 ou superior | Java 17 or higher
- Maven instalado (ou usar o `./mvnw` incluso no projeto) | Maven installed (or use the included `./mvnw`)
- MySQL Server rodando localmente (porta 3306 por padrão) | MySQL Server running locally (port 3306 by default)
- Banco de dados `company` criado manualmente ou via MySQL Workbench | Database `company` created manually or via MySQL Workbench

---

## 📁 Estrutura do Projeto | Project Structure

```
crud-funcionarios/
├── backend/     # Projeto Quarkus (API Java) | Quarkus project (Java API)
```

---

## 🔧 Como Rodar o Projeto Localmente | How to Run the Project Locally

### 1. Clone o Repositório | Clone the Repository

```bash
git clone https://github.com/patrickburin/employee-crud-java.git

```

### 2. Configure o Banco de Dados | Set Up the Database

No seu MySQL (pode usar o Workbench ou terminal), crie o banco:  
In your MySQL (you can use Workbench or terminal), create the database:

```sql
CREATE DATABASE company;
```

O Quarkus irá criar as tabelas automaticamente na primeira execução.  
Quarkus will automatically create the tables on first run.

### 3. Backend (API com Quarkus)

```bash
cd backend
./mvnw quarkus:dev
```

---

## ✅ Funcionalidades do Sistema | System Features

- 📋 Listagem de funcionários cadastrados | List registered employees
- ✏️ Edição de dados com validações | Edit employee data with validation
- ➕ Cadastro de novos funcionários | Register new employees
- 🗑️ Exclusão de funcionários | Delete employees
- ✅ Validação completa de campos (campos obrigatórios, CPF, valores positivos) | Full field validation (required fields, CPF, positive values)

---

## 🧪 Sugestões de Testes | Test Suggestions

- Tente adicionar um CPF que já está cadastrado (deve retornar erro do backend)  
  Try adding a CPF that is already registered (should return a backend error)
- Tente salvar sem preencher todos os campos obrigatórios  
  Try saving without filling all required fields
- Informe valores negativos em "salário" ou "carga horária" (deve bloquear)  
  Enter negative values for "salary" or "workload" (should be blocked)
- Teste a edição e observe o toast de sucesso  
  Edit an employee and observe the success feedback
- Apague um registro e veja a atualização da tabela em tempo real  
  Delete a record and see the list update in real time
