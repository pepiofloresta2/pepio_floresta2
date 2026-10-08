# Melhorias v16 — Comunidade São Pio

## Alterações
- Recibo de dízimo agora identifica a comunidade como **Comunidade São Pio** e mostra a Diocese de Criciúma, sem repetir o nome da paróquia.
- Relatório para impressão fica mais limpo: esconde os cards de resumo e a tabela de movimentação mensal, mantendo as listas de entradas por categoria/forma, despesas por categoria e lançamentos detalhados.
- Removido CPF das telas de cadastro, ficha e lista de dizimistas. A coluna antiga da planilha é mantida por compatibilidade, mas não é mais usada pela interface.
- Campo **Documento Nº** no lançamento financeiro, para NF nas saídas e recibo/documento nas entradas.
- Campo opcional para número do recibo ao registrar o dízimo mensal; esse número é guardado no lançamento e pode aparecer no recibo impresso.
- Agrupamento de entradas no relatório usa nomes sem travessão, por exemplo “Dízimo Dinheiro” e “Dízimo PIX”.

## Publicação
1. Substitua os arquivos do projeto no repositório GitHub pela versão deste ZIP.
2. No Google Apps Script, atualize o arquivo `Apps-Script-Code.gs`.
3. Em **Implantar → Gerenciar implantações**, edite a implantação existente, escolha **Nova versão** e clique em **Implantar**.
4. Não execute `setup()`, pois essa função apaga as abas e os dados da planilha.
