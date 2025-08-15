# devsignin

[![GitHub last commit](https://img.shields.io/github/last-commit/stanycruz/devsignin)](https://github.com/stanycruz/devsignin/commits/main)
[![GitHub issues](https://img.shields.io/github/issues/stanycruz/devsignin)](https://github.com/stanycruz/devsignin/issues)
[![GitHub license](https://img.shields.io/github/license/stanycruz/devsignin)](https://github.com/stanycruz/devsignin/blob/main/LICENSE)
[![CI](https://img.shields.io/badge/CI-GitHub%20Actions-informational?logo=github-actions&logoColor=white)](https://github.com/stanycruz/devsignin/actions)
[![TypeScript](https://badges.frapsoft.com/typescript/code/typescript.svg?v=101)](https://github.com/microsoft/TypeScript)
[![semantic-release](https://img.shields.io/badge/semantic--release-e10079?logo=semantic-release)](https://github.com/semantic-release/semantic-release)

_🔐 API de autenticação com NestJS, MongoDB e JWT_

---

## Install

```bash
npm install
```

## Features

- API RESTful com **NestJS** ⚡
- Conexão com **MongoDB** via Mongoose 🍃
- Autenticação **JWT** 🔑
- Hash de senha com **bcrypt** 🔒
- Validação de entrada com `class-validator` ✅
- Rotas protegidas com `@nestjs/passport` + `passport-jwt` 🛡️
- Estrutura modular escalável 📂

## Example

```http
# Login
POST /users/signin
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "123456"
}

# Cadastro
POST /users/signup
Content-Type: application/json

{
  "name": "Usuário",
  "email": "user@example.com",
  "password": "123456"
}
```

## Endpoints

| Método | Rota            | Protegida | Descrição               |
|-------:|-----------------|:---------:|-------------------------|
| POST   | `/users/signup` | ❌        | Cria um novo usuário    |
| POST   | `/users/signin` | ❌        | Autentica e retorna JWT |
| GET    | `/users`        | ✅        | Lista todos usuários    |

## Environment Variables

| Variável         | Descrição                               |
|------------------|-----------------------------------------|
| `MONGO_URI`      | URL de conexão com MongoDB              |
| `JWT_SECRET`     | Chave secreta para assinar tokens       |
| `JWT_EXPIRATION` | Expiração do token (ex.: `1h`, `15m`)   |
| `PORT`           | Porta da API (padrão `3000`)            |

## Development

Clone e execute localmente:

```bash
git clone https://github.com/stanycruz/devsignin
cd devsignin
npm install
npm run start:dev
```

**Start coding!** 🎉

## Contributing

Contribuições são bem-vindas!  
Abra uma *issue* ou envie um *pull request*.

