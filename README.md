# Desapega Senac ♻️

[![PHP](https://img.shields.io/badge/PHP-8.0-777BB4?style=flat&logo=php&logoColor=white)](https://www.php.net/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Kotlin](https://img.shields.io/badge/Kotlin-Android-7F52FF?style=flat&logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Marketplace local de anúncios de produtos novos e usados — conectando compradores e vendedores da comunidade Senac de forma simples, segura e direta.

---

## 🌟 Sobre o Projeto

O **Desapega Senac** é um marketplace de classificados no estilo OLX, desenvolvido como projeto acadêmico no Senac. A plataforma permite que usuários anunciem produtos novos ou usados, entrem em contato com vendedores e gerenciem seus próprios anúncios — tudo por meio de um aplicativo Android integrado a uma API RESTful em PHP.

O foco é na simplicidade da experiência: qualquer pessoa da comunidade consegue publicar um anúncio em poucos passos e encontrar o que procura com facilidade.

### ✨ Principais Funcionalidades

- **Anúncios de Produtos:** Publique itens novos ou usados com fotos, descrição, preço e condição.
- **Gestão de Conta:** Cadastro, login e gerenciamento do perfil do anunciante.
- **Catálogo Navegável:** Explore e filtre os anúncios disponíveis diretamente pelo app.
- **Controle de Anúncios:** Edite ou remova seus próprios anúncios a qualquer momento.
- **Aplicativo Android:** Interface mobile nativa para anunciar e buscar produtos com agilidade.

---

## 🛠️ Tech Stack

| Camada | Tecnologias |
|--------|-------------|
| **Backend** | PHP 8.0, PDO |
| **Banco de Dados** | MySQL 8.0 |
| **Mobile** | Android SDK, Kotlin, Gradle |
| **Segurança** | CORS, Prepared Statements |
| **Build** | Android Studio, Gradle |

---

## 📋 Pré-requisitos

- **PHP** 8.0 ou superior
- **MySQL** 8.0 ou superior
- **Composer** (gerenciamento de dependências PHP)
- **Android Studio** (para compilar e executar o app)
- **JDK** 11 ou superior

---

## 🚀 Instalação

```bash
# Clone o repositório
git clone https://github.com/seu-usuario/desapega-senac.git
cd desapega-senac

# Instale as dependências PHP
composer install
```

### Configuração do Banco de Dados

1. Crie um banco de dados MySQL:
   ```sql
   CREATE DATABASE desapega_senac;
   ```

2. Importe o schema (se disponível):
   ```bash
   mysql -u root -p desapega_senac < database/schema.sql
   ```

3. Configure as credenciais do banco nos arquivos `cadastrar_usuario.php` e `login.php`:
   ```php
   $host = 'localhost';
   $dbname = 'desapega_senac';
   $user = 'seu_usuario';
   $pass = 'sua_senha';
   ```

### Executando o App Android

1. Abra a pasta `app/` no **Android Studio**.
2. Sincronize o projeto com o Gradle.
3. Execute em um emulador ou dispositivo físico.

---

## 💻 Como Usar

### API — Endpoints Disponíveis

| Ação | Arquivo |
|------|---------|
| Cadastrar usuário | `cadastrar_usuario.php` |
| Login | `login.php` |
| Listar anúncios | `listagem/produtos.php` |
| Publicar anúncio | `listagem/incluir_produto.php` |
| Editar anúncio | `listagem/editar_produto.php` |
| Remover anúncio | `listagem/excluir_produto.php` |

### Aplicativo Android

Após criar sua conta e fazer login, o app permite:
- Publicar anúncios de produtos novos ou usados com fotos e descrição.
- Navegar pelo catálogo de anúncios da comunidade.
- Gerenciar (editar ou excluir) seus próprios anúncios.

---

## 📂 Estrutura do Projeto

```
desapega-senac/
├── cadastrar_usuario.php        # Endpoint de cadastro de usuário
├── login.php                    # Endpoint de autenticação
├── listagem/
│   ├── produtos.php             # Listagem de anúncios
│   ├── incluir_produto.php      # Publicação de anúncio
│   ├── editar_produto.php       # Edição de anúncio
│   └── excluir_produto.php      # Remoção de anúncio
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── AndroidManifest.xml
│   │   │   ├── res/
│   │   │   │   └── xml/
│   │   │   │       └── network_security_config.xml
│   │   │   └── java/
│   │   └── test/
│   └── build.gradle.kts
├── settings.gradle.kts
└── build.gradle.kts
```

---

## 🔐 Segurança

- **Prepared Statements:** Todas as queries ao banco utilizam PDO com prepared statements, eliminando riscos de SQL Injection.
- **CORS:** Configurado para restringir origens permitidas nas requisições à API.
- **Autenticação:** Operações sensíveis (publicar, editar, excluir) exigem login válido.

---

## 🤝 Contribuições

Contribuições são bem-vindas! Se você encontrar um bug ou tiver uma sugestão de melhoria, abra uma *issue* ou envie um *pull request*.

1. Faça um `fork` do projeto.
2. Crie uma nova *branch* (`git checkout -b feature/sua-feature`).
3. Realize suas alterações e faça o commit (`git commit -m 'feat: Adiciona nova funcionalidade'`).
4. Envie para o repositório remoto (`git push origin feature/sua-feature`).
5. Abra um *Pull Request*.

---

## 📄 Licença

Este projeto é distribuído sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 📬 Contato

Desenvolvido por **Gabriel Barreto**.

- **E-mail:** [gabrielprozds@gmail.com](mailto:gabrielprozds@gmail.com)
