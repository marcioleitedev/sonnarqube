# ✅ SonarQube com PostgreSQL via Docker Compose

Este projeto fornece uma configuração simples para rodar o **SonarQube** com banco de dados **PostgreSQL** usando **Docker Compose**, ideal para análise estática de código localmente ou em um ambiente de desenvolvimento.

---

## 📌 Pré-requisitos
- [Docker](https://www.docker.com/get-started) instalado  
- [Docker Compose](https://docs.docker.com/compose/install/) instalado  

---

## 🚀 Como rodar
1. **Clone este repositório**:
   ```bash
   git clone https://github.com/seu-usuario/sonarqube-docker.git
   cd sonarqube-docker
   ```

2. **Suba os containers**:
   ```bash
   docker-compose up -d
   ```

3. **Acesse a interface do SonarQube**:
   ```
   http://localhost:9000
   ```

---

## 🔑 Credenciais padrão
- **SonarQube**:
  - Usuário: `admin`
  - Senha: `admin`

- **PostgreSQL**:
  - Host: `db`
  - Database: `sonar`
  - Usuário: `sonar`
  - Senha: `sonar`

---

## 🗂 Estrutura do projeto
```
├── docker-compose.yml   # Arquivo principal para subir os containers
└── README.md            # Este arquivo
```

---

## 📦 Volumes
O projeto utiliza **volumes nomeados** para persistência:
- `sonarqube_data`
- `sonarqube_extensions`
- `sonarqube_logs`
- `postgresql_data`

---

## 🛠 Comandos úteis
- **Ver logs**:
  ```bash
  docker-compose logs -f sonarqube
  ```
- **Parar os containers**:
  ```bash
  docker-compose down
  ```
- **Remover tudo (containers + volumes)**:
  ```bash
  docker-compose down -v
  ```

---

## ⚙️ Configurações adicionais
- Porta SonarQube: `9000`
- Banco PostgreSQL: `5432`

Se quiser modificar usuário, senha ou nome do banco, altere as variáveis no `docker-compose.yml`.

---

## ✅ Tecnologias utilizadas
- **[SonarQube LTS](https://www.sonarsource.com/products/sonarqube/)**
- **[PostgreSQL 15](https://www.postgresql.org/)**
- **[Docker](https://www.docker.com/)**
- **[Docker Compose](https://docs.docker.com/compose/)**

---

## 📜 Licença
Este projeto é distribuído sob a licença MIT.
