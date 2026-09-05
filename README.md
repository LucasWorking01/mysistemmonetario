# BaseFynanci — Controle Financeiro Pessoal

Um sistema simples, bonito e 100% offline para você registrar suas entradas e
saídas de dinheiro, organizar tudo por mês e dia, e acompanhar para onde seu
dinheiro está indo — sem precisar de internet, login ou planilhas.

Funciona bem tanto no computador quanto no celular: no celular, a navegação
fica numa barra inferior (como um app nativo) e há um botão flutuante (+)
para adicionar um lançamento rapidamente.

## Como usar

1. Extraia o arquivo `.zip`.
2. Dê duplo clique em **`index.html`**. Ele abre no seu navegador (Chrome,
   Edge, Firefox...) e funciona como um programa normal.
3. Pronto — pode começar a usar. Não precisa instalar nada.

> Dica: crie um atalho do `index.html` na área de trabalho para acessar mais rápido.

## O que o sistema faz

### 1. Lançamentos
Aba principal para registrar cada movimentação financeira:

- **Tipo**: Entrada ou Saída
- **Data**: dia exato do lançamento
- **Categoria**: predefinida de acordo com o tipo (veja lista abaixo)
- **Descrição**: ex. "Jantar de aniversário", "Salário de setembro"
- **Valor**: em reais (R$)

Os lançamentos aparecem automaticamente **agrupados por mês e, dentro do mês,
por dia**, como um livro-caixa. Você pode editar ou excluir qualquer
lançamento clicando nos ícones que aparecem ao passar o mouse sobre a linha.

**Categorias de saída (gastos):**
Alimentação · Transporte · Moradia · Saúde · Educação · Lazer · Compras ·
Contas e Serviços · Outros

**Categorias de entrada (dinheiro recebido):**
Salário · Freelancer · Investimentos · Presente · Outros

### 2. Relatório
Um levantamento completo do mês selecionado:

- Total de entradas, total de saídas e saldo do mês
- Gastos por categoria (com barra de porcentagem)
- Entradas por categoria
- Gráfico dos últimos 6 meses (entradas x saídas)
- Tabela detalhada com o total e a quantidade de lançamentos por categoria

Use as setas ao lado do nome do mês para navegar entre períodos.

### 3. Observações
Uma aba livre para anotações — metas do mês, lembretes, ou o contexto de um
gasto específico. A data é opcional.

## Banco de dados integrado

Todos os seus dados ficam salvos automaticamente no seu computador, usando o
**IndexedDB** do navegador — um banco de dados embutido, sem precisar de
servidor, internet ou instalação. Ao fechar e abrir o arquivo novamente, seus
lançamentos e observações continuam lá.

**Importante:**
- Os dados ficam vinculados ao navegador que você usou para abrir o arquivo.
  Sempre acesse pelo mesmo navegador (e, se possível, sem apagar os dados de
  navegação) para não perder as informações.
- Por segurança, use o botão **Exportar** (no menu lateral) de tempos em
  tempos para salvar um backup em `.json`. Se precisar trocar de computador
  ou de navegador, use o botão **Importar** para restaurar tudo.

## Estrutura do projeto

```
financas/
├── index.html   → aplicativo completo (interface + banco de dados)
└── README.md    → este arquivo
```

Todo o sistema — visual, lógica e banco de dados — está contido em um único
arquivo `index.html`, o que torna o programa fácil de guardar, copiar ou
levar para outro computador em um pendrive, por exemplo.

## Privacidade

Nenhuma informação sai do seu computador. Não há envio de dados para
servidores externos, contas de usuário ou rastreamento — tudo roda
localmente, direto no seu navegador.
