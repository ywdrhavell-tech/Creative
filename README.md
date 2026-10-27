# Creativa Flow Desk — versão com banco de dados

Aplicação reconstruída de forma independente com interface React/Vite, API Node.js/Express e banco SQLite persistente. Não é o código original do Base44; os arquivos fornecidos continham apenas a página de entrada, configuração de dependências e README, então a interface e o backend foram montados para entregar uma versão funcional equivalente.

## Requisitos
- Node.js 20.19+ (recomendado Node 22 LTS ou superior)
- npm

## Rodar no Windows / VS Code
1. Extraia o ZIP e abra a pasta no VS Code.
2. Abra o terminal nessa pasta.
3. Execute `npm install`.
4. Execute `npm run dev`.
5. Abra o endereço mostrado pelo Vite, normalmente `http://localhost:5173`.

A API inicia em `http://localhost:3001`; o banco é criado automaticamente em `data/creativa.db`.

## Funcionalidades
- Cadastro e exclusão de clientes.
- Cadastro e exclusão de serviços.
- Criação, listagem, exclusão e atualização de status de pedidos.
- Indicadores e relatório por status.
- Dados persistidos no SQLite, mesmo após fechar/atualizar o navegador.
- API REST em `/api` e endpoint de verificação `/api/health`.

## Rotas principais
- `GET/POST /api/clients`; `PUT/DELETE /api/clients/:id`
- `GET/POST /api/services`; `PUT/DELETE /api/services/:id`
- `GET/POST /api/orders`; `PATCH/DELETE /api/orders/:id`
- `GET /api/dashboard`; `GET /api/health`

## Observações
- O arquivo `data/creativa.db` é criado automaticamente no primeiro início. Faça cópias de segurança desse arquivo para preservar os dados.
- Para publicar na internet, hospede a API em um serviço Node compatível com armazenamento persistente e configure o frontend/API. O SQLite local não é automaticamente compartilhado entre computadores.
- Esta versão não possui login; não a exponha publicamente com dados pessoais sem implementar autenticação e autorização.
