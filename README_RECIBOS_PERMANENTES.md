# Recibos permanentes da prestação de contas

Esta versão salva os recibos emitidos na aba `StatementReceipts` da planilha vinculada ao Apps Script. A aba é criada automaticamente na leitura, sem limpar ou recriar as demais abas.

- O número do recibo é gerado no formato `AAAAMM-001` e fica imutável após a primeira emissão.
- Emitir novamente a mesma categoria/forma no mesmo período atualiza o valor no registro existente, mantendo o número.
- Alterações de valor são acrescentadas ao campo `history` para rastreabilidade.
- A aba Prestação de contas mostra os recibos salvos e permite reimprimir.

## Atualização
1. Atualize os arquivos do front-end no GitHub.
2. Copie `Apps-Script-Code.gs` para o projeto Apps Script.
3. Implante uma nova versão da implantação existente.
4. Não execute `setup()`: ela limpa as abas. A aba de recibos é criada automaticamente pelo aplicativo.
5. Entre no app, acesse Relatórios > Prestação de contas e emita um recibo de teste.
