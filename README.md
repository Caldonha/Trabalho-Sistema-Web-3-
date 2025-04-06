# 🛒 Sistema de Compras Coletivas com Laravel

Este projeto é um sistema web desenvolvido utilizando **Laravel 11 + Sail (Docker)** para facilitar o gerenciamento de grupos de compras coletivas. Nele, usuários podem criar ou participar de grupos para realizar pedidos de forma compartilhada, proporcionando economia e eficiência.

---

## 🚀 Tecnologias Utilizadas

- **Laravel 11**
- **PHP 8.2**
- **Laravel Sail (Docker)**
- **MySQL**
- **Composer**

---

## 🧱 Estrutura do Banco de Dados

O banco de dados possui as seguintes tabelas principais:

| Tabela          | Descrição                                       |
|-----------------|-------------------------------------------------|
| `users`         | Cadastro dos usuários do sistema                |
| `grupos`        | Grupos de compras coletivas criados pelos usuários |
| `produtos`      | Produtos disponíveis em cada grupo              |
| `pedidos`       | Pedidos realizados pelos usuários               |
| `participacaos` | Relação muitos-para-muitos entre usuários e grupos |

---

## 🔁 Relacionamentos

- **Usuário** pode realizar **múltiplos pedidos**.
- **Grupo** pode conter **vários produtos**.
- **Produto** pertence a **um grupo específico**.
- **Pedido** está relacionado a **um usuário e a um produto**.
- Relacionamento **muitos-para-muitos** entre **usuários e grupos**, gerenciado pela tabela intermediária `participacaos`.

---

## 📊 Diagrama do Banco de Dados

O diagrama completo do banco, exibindo as tabelas e seus relacionamentos, encontra-se disponível no repositório:

📎 `![image](https://github.com/user-attachments/assets/ca31a63d-d85b-4697-bd7c-d3e9ec670486)
`

---

## ⚙️ Como Executar o Projeto

Siga os passos abaixo para executar localmente:

1. **Clone o repositório:**

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

2. **Entre na pasta do projeto:**

```bash
cd coletiva-app
```

3. **Inicie os containers com Laravel Sail:**

```bash
./vendor/bin/sail up -d
```

4. **Execute as migrations para criar as tabelas:**

```bash
./vendor/bin/sail artisan migrate
```

5. **Acesse o projeto pelo navegador:**

```
http://localhost:8080
```

---

## 📦 Observações Importantes

- A pasta `vendor/` não está incluída no repositório, pois será automaticamente criada quando você executar o Laravel Sail pela primeira vez. Isso mantém o repositório leve e evita problemas com tamanho máximo permitido.

---

## 👨‍💻 Autor

**Desenvolvido por:** [Vitor Hugo Caldonha Leme]  
**Curso:** Desenvolvimento Web 3  
**Instituição:** [REGES]

