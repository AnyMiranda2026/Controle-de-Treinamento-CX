# Controle de Treinamentos

Painel em HTML para registrar, consolidar e analisar os treinamentos realizados pelo time de CX.

## Como usar

Abra `index.html` em um navegador moderno. O painel permite:

- escolher diretamente qualquer mês do ano;
- adicionar, editar, salvar e bloquear treinamentos;
- digitar a duração em `HH:MM` ou em horas decimais;
- informar múltiplos módulos quando o treinamento for customizado;
- mesclar, mediante confirmação, treinamentos do mesmo cliente realizados em dias diferentes;
- importar registros históricos em massa por CSV;
- baixar o modelo oficial de importação;
- exportar os dados do mês para CSV;
- acompanhar treinamentos e horas por Recurso CX e por cliente no dashboard;
- imprimir a visão mensal.

Os registros são sincronizados pelo Firebase/Firestore e ficam disponíveis para todas as pessoas que acessam o mesmo link. O navegador também mantém uma cópia local para preservar o trabalho em caso de falha temporária de conexão.

Na primeira abertura da versão sincronizada, os dados históricos existentes neste navegador são migrados automaticamente para a base compartilhada.

## Layout da importação histórica

Use o arquivo [`docs/Layout_Importacao_Historico_v2.csv`](docs/Layout_Importacao_Historico_v2.csv) ou clique em **Baixar modelo** no painel.

Campos aceitos:

1. Data — obrigatória, em `DD/MM/AAAA` ou `AAAA-MM-DD`.
2. Datas adicionais — se houver, separadas por `|`.
3. Duração — exemplo: `02:30` ou `2,5`.
4. Cliente.
5. Módulos.
6. Módulos customizados — múltiplos valores separados por `|`.
7. Tipo.
8. Solicitação.
9. Local.
10. Link do Projeto ou Chamado (Wrike ou Fresh).
11. Envio da Pesquisa de Satisfação.
12. Recurso CX.
13. Observação.

Os registros importados entram salvos e bloqueados para edição.
