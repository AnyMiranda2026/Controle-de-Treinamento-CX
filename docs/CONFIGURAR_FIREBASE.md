# Configuração do histórico compartilhado

Projeto Firebase: `controle-de-treinamentos-cx`

## Firestore

- Edição: Standard.
- Região: `southamerica-east1` (São Paulo).
- Modo inicial: produção.
- Publicar o conteúdo do arquivo `firestore.rules` na aba **Firestore > Regras**.

## Autenticação

Em **Authentication > Sign-in method**, habilitar o provedor **Anônimo**.

Em **Authentication > Settings > Authorized domains**, adicionar:

`anymiranda2026.github.io`

O painel entra anonimamente no Firebase. Assim, qualquer pessoa que receba o link pode consultar e atualizar a base compartilhada sem criar uma senha. As regras impedem acesso sem uma sessão válida do Firebase.

## Migração

Na primeira abertura após a publicação, os registros existentes no `localStorage` são enviados ao Firestore. Depois disso, todos os navegadores recebem atualizações em tempo real.
