# Controle de Dizimistas da Comunidade

Versão adaptada do projeto enviado para uso paroquial.

## Funcionalidades principais
- Cadastro de dizimistas com número de cadastro, nome, CPF, endereço, telefone e observações.
- Controle mensal de contribuições, com data, valor e forma de pagamento (PIX/dinheiro e demais formas).
- Ficha individual com histórico e recibo imprimível/Salvar em PDF.
- Movimento de caixa, entradas/saídas, relatórios e exportação CSV.
- Dados sincronizados pela API do Google Apps Script/Google Sheets configurada em `src/config.js`.

## Antes de publicar
1. Faça backup da planilha vinculada à API.
2. Atualize o projeto Apps Script com `Apps-Script-Code.gs` e publique uma nova versão da implantação.
3. A aba `Residents` agora utiliza as colunas `id, name, house, phone, email, notes, exempt, paidMonths, created_date, monthlyPaymentIds, cadastro, cpf`. Não execute `setup()` na planilha com dados reais: ele apaga e recria as abas. Faça a migração das colunas manualmente ou numa cópia de teste.
4. Confirme os valores padrão da aba `Settings` (`associacao`, `taxaMensal`, `responsavel`).
5. Atualize `API_URL` em `src/config.js` com a URL da implantação que você efetivamente publicou.
6. Instale dependências (`npm install`) e gere a versão de produção (`npm run build`).

O login foi mantido para proteger dados pessoais como CPF e o histórico de contribuições.
