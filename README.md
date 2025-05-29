# 🏠 Controle de Financiamento Pessoal

Bem-vindo à sua ferramenta pessoal e completa para gerenciamento de financiamentos imobiliários! Este sistema foi desenhado para ajudar você a organizar e acompanhar todos os pagamentos, metas financeiras, contribuições de múltiplos pagantes e o impacto de reajustes como o INCC, tudo de forma simples e diretamente no seu navegador.

## ✨ Visão Geral

Adquirir um imóvel envolve diversos custos e etapas de pagamento que podem se tornar complexos de gerenciar, especialmente quando há mais de uma pessoa contribuindo ou diferentes tipos de despesas (entrada, parcelas, taxas, impostos, reajustes). Esta ferramenta centraliza todas essas informações, oferecendo clareza sobre:

* **O que foi pago:** Registre cada desembolso e saiba exatamente para onde seu dinheiro foi.
* **O que falta pagar:** Acompanhe pagamentos pendentes e seus vencimentos.
* **Quem pagou o quê:** Defina as contribuições individuais para cada pagamento.
* **Progresso em Metas:** Cadastre grandes objetivos financeiros (como o valor total da entrada, ITBI, custos de cartório) e veja o quanto já foi amortizado.
* **Impacto de Reajustes:** Analise o efeito do INCC sobre o valor de suas parcelas.
* **Relatórios Detalhados:** Obtenha insights sobre seus gastos e a participação de cada envolvido.

Toda a gestão é feita localmente no seu navegador, utilizando o `localStorage` para guardar seus dados de forma privada e acessível a qualquer momento no mesmo navegador.

## 🚀 Principais Funcionalidades

A ferramenta é organizada em abas intuitivas:

* 📊 **Dashboard (Resumo):**
    * Visão geral e instantânea do status financeiro: Total efetivamente pago, total lançado, total pendente, e progresso geral dos lançamentos.
    * Acompanhamento da sua principal meta financeira cadastrada, com saldo devedor e progresso.
    * Lista dos próximos vencimentos para você não perder nenhum prazo.

* 🎯 **Metas:**
    * Cadastre grandes objetivos financeiros (ex: "Entrada do Imóvel", "Pagamento ITBI Total", "Custos de Cartório").
    * Defina o valor total para cada meta.
    * Acompanhe o valor já pago e o saldo devedor de cada meta.
    * Marque uma meta como principal para destaque no Dashboard.
    * Edite ou remova metas conforme necessário.

* 👥 **Pagantes:**
    * Gerencie as pessoas que participam dos pagamentos.
    * Adicione ou edite pagantes informando Nome Completo e Apelido.
    * *Observação:* Diferente de versões anteriores, o percentual de participação não é mais fixo por pagante, mas sim definido individualmente em cada lançamento de pagamento.

* 💸 **Pagamentos:**
    * O coração da ferramenta! Registre todos os seus pagamentos.
    * **Adicionar/Editar Pagamentos:** Informe tipo, descrição, valor total, data de vencimento.
    * **Distribuição de Contribuições:** Se houver mais de um pagante cadastrado, você poderá (e deverá) especificar quanto cada pagante contribuiu para o valor total daquele pagamento específico. A soma das contribuições deve bater com o valor total do pagamento.
    * **Vincular a Metas:** Associe pagamentos a metas financeiras cadastradas para abater o saldo devedor da meta correspondente.
    * **Marcar como Pago:** Indique quais contribuições individuais dentro de um pagamento foram efetivadas. O status geral do pagamento (Pago, Parcial, Pendente, Atrasado) é atualizado automaticamente.
    * **Visualizar Porcentagem de Contribuição:** Em cada pagamento rateado, veja claramente qual a porcentagem da contribuição de cada pagante em relação ao valor total daquele lançamento.

* 📈 **Reajuste INCC (Analisador):**
    * Entenda o impacto de reajustes em parcelas específicas.
    * Informe o "Valor Original da Parcela" e o "Valor Pago da Parcela com INCC".
    * A ferramenta calculará o valor (R$) e o percentual (%) do reajuste aplicado sobre aquela parcela.
    * Mantenha um histórico dessas análises.

* 📄 **Relatórios:**
    * **Relatório Geral Aprimorado:**
        * Resumo financeiro completo: total efetivamente pago, total lançado, pendências.
        * Visão agregada de todas as metas: valor total, total amortizado, saldo devedor e progresso.
        * Distribuição dos gastos efetivos por tipo de pagamento (Sinal, ITBI, Juros, etc.), mostrando o quanto cada tipo representa do total pago.
    * **Relatório por Pagante:**
        * Veja o total que cada pagante contribuiu.
        * Detalhe das contribuições de cada pagante por tipo de pagamento.
        * (Futuramente, poderá incluir detalhamento por meta).

* 💾 **Dados (Exportar/Importar):**
    * **Exportar Dados:** Faça backup de todos os seus dados (pagantes, pagamentos, metas, histórico INCC) em um arquivo JSON.
    * **Importar Dados:** Restaure seus dados a partir de um arquivo JSON previamente exportado. **Atenção:** A importação sobrescreve todos os dados existentes no navegador!

## 🛠️ Como Usar

1.  **Acesso:** Simplesmente abra o arquivo `financiamento.html` (ou o nome que você deu ao arquivo principal) em qualquer navegador de internet moderno (Chrome, Firefox, Edge, Safari).
2.  **Primeiros Passos (Sugestão):**
    * Acesse a aba **"Pagantes"** e cadastre todas as pessoas que contribuirão para os pagamentos.
    * Vá para a aba **"Metas"** e cadastre os grandes objetivos financeiros do seu financiamento (ex: Valor total da Entrada, Custo total do ITBI). Marque uma como principal se desejar vê-la no Dashboard.
    * Comece a lançar seus pagamentos na aba **"Pagamentos"**, detalhando as contribuições de cada pagante e vinculando os pagamentos às metas correspondentes.
3.  **Navegação:** Utilize os botões no topo da página para navegar entre as diferentes seções.
4.  **Salvamento:** Todos os dados são salvos automaticamente no `localStorage` do seu navegador. Não há necessidade de um botão "Salvar" geral para a aplicação.

## ⚠️ Dicas Importantes

* **Backups são Essenciais:** Utilize a funcionalidade de "Exportar Dados" (na aba "Dados") regularmente para criar backups do seu progresso. Guarde o arquivo JSON em um local seguro.
* **Dados Locais:** Lembre-se que os dados são armazenados apenas no navegador que você está utilizando. Eles não são sincronizados automaticamente entre diferentes computadores ou navegadores. Se você limpar o cache do seu navegador ou os dados de sites, poderá perder as informações, daí a importância do backup.
* **Importação de Dados:** Ao importar dados, os dados atuais no navegador serão completamente substituídos. Tenha certeza antes de confirmar a importação.

## 🔧 Aspectos Técnicos (Para Curiosos)

* **Tecnologias:** A ferramenta é construída utilizando HTML, CSS puro e JavaScript Vanilla (sem frameworks externos).
* **Armazenamento:** `localStorage` do navegador.
* **Ícones:** Font Awesome.
* **Design:** Responsivo, adaptando-se a diferentes tamanhos de tela.

---

Esperamos que esta ferramenta seja extremamente útil na sua jornada de financiamento imobiliário! Qualquer dúvida ou sugestão, anote para futuras melhorias.
