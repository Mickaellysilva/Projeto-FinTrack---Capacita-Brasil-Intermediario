# FinTrack

Sistema de controle de finanças pessoais desenvolvido em **Java**, com interface gráfica utilizando **JavaFX**, persistência de dados via **JDBC** e testes automatizados com **JUnit**.

## Sobre o Projeto

O FinTrack é uma aplicação desktop que permite ao usuário gerenciar suas finanças pessoais de forma simples e intuitiva.

Com ele é possível:

- Cadastrar receitas;
- Cadastrar despesas;
- Listar todas as transações;
- Remover transações;
- Consultar o saldo atual;
- Visualizar relatórios financeiros.

O projeto foi desenvolvido com o objetivo de aplicar conceitos de Programação Orientada a Objetos, Generics, JavaFX, JDBC e Testes de Software.

---

## Funcionalidades

### Gerenciamento de Transações

- Cadastro de receitas;
- Cadastro de despesas;
- Exclusão de transações;
- Listagem de transações;
- Cálculo automático do saldo.

### Interface Gráfica

- Tela principal com tabela de transações;
- Tela de cadastro de transações;
- Tela de relatório/saldo;
- Interface estilizada com CSS.

### Persistência de Dados

- Armazenamento das informações em banco de dados;
- Operações CRUD completas;
- Uso de PreparedStatement para maior segurança.

---

## Tecnologias Utilizadas

- Java
- JavaFX
- FXML
- Scene Builder
- CSS
- JDBC
- SQLite/MySQL
- JUnit 5

---

## Conceitos Aplicados

### Generics

Utilização de classes e métodos genéricos para promover reutilização de código:

```java
public class RepositorioGenerico<T> {
    private List<T> elementos = new ArrayList<>();
}
```

Recursos utilizados:

- `<T>`
- `<?>`
- `<? extends T>`
- `<? super T>`

### JavaFX

Componentes utilizados:

- Label
- TextField
- TextArea
- Button
- DatePicker
- CheckBox
- TableView
- VBox
- HBox
- GridPane
- BorderPane

### FXML + Scene Builder + CSS

- Separação entre interface e lógica;
- Controllers utilizando `fx:controller`;
- Desenvolvimento visual com Scene Builder;
- Estilização utilizando CSS.

### JDBC

Implementação de acesso ao banco de dados através de:

- Connection
- PreparedStatement
- ResultSet
- DAO (Data Access Object)

Tabela principal:

```sql
CREATE TABLE transacoes (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    data DATE NOT NULL,
    descricao VARCHAR(255),
    valor DECIMAL(10,2),
    tipo VARCHAR(20)
);
```

### JUnit

Testes automatizados para:

- Classe Transacao;
- RepositorioGenerico;
- TransacaoDAO;
- Cálculo de saldo;
- Inserção e remoção de registros.

---

## Estrutura do Projeto

```text
FinTrack/
├── src/
│   ├── model/
│   ├── dao/
│   ├── database/
│   ├── controller/
│   ├── service/
│   ├── view/
│   └── FinApp.java
│
├── resources/
│   └── style.css
│
├── test/
│   ├── TransacaoTest.java
│   ├── RepositorioGenericoTest.java
│   └── TransacaoDAOTest.java
│
└── README.md
```

---

## Como Executar

### Pré-requisitos

- Java JDK 17 ou superior
- JavaFX SDK
- IDE Java (IntelliJ IDEA, Eclipse ou NetBeans)
- Banco de dados configurado

### Passos

1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/fintrack.git
```

2. Abra o projeto na sua IDE.

3. Configure o JavaFX.

4. Configure a conexão com o banco de dados na classe `Conexao.java`.

5. Execute a classe principal:

```java
FinApp.java
```

---

## Executando os Testes

Execute os testes pela IDE ou utilizando Maven:

```bash
mvn test
```

---

## Objetivos de Aprendizagem

Este projeto foi desenvolvido para praticar:

- Programação Orientada a Objetos;
- Generics em Java;
- Desenvolvimento de interfaces gráficas com JavaFX;
- Integração com banco de dados utilizando JDBC;
- Padrão DAO;
- Testes automatizados com JUnit;
- Organização de projetos em camadas.

---

## Autora
Mickaelly;
Projeto acadêmico desenvolvido para fins de aprendizagem e aplicação prática dos conceitos estudados na disciplina.
