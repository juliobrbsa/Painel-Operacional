## Painel Operacional

Painel Operacional Policial para Incremento de Roleplay em Servidores de GTA RP

Este projeto foi inicialmente desenvolvido para simular o sistema de gestão operacional do **1° Batalhão de Polícia de Choque ROTA**, mas é totalmente modular e pode ser adaptado para qualquer corporação dentro do cenário de Roleplay (RP).

-----

### 🌟 Funcionalidades

O painel oferece um sistema completo para gerenciamento de dados operacionais e simulação de rotinas policiais, incluindo:

  * **Autenticação de Usuário:** Login por ID Funcional (convertido para e-mail interno, ex: [ID]@rota.mil) utilizando Firebase Authentication.
  * **Gestão de Relatórios (RSO):** Formulário detalhado (rota_rso.html) para preenchimento de Relatórios de Serviço Operacional, com campos para cronologia, patrulha, apreensões (armas, drogas, dinheiro, veículos) e observações.
  * **Salvar Rascunho:** Opção de salvar um relatório como rascunho utilizando Firestore.
  * **Dashboard Interativo:** Visão geral (rota_dashboard.html) com métricas de relatórios, ocorrências, detidos e mortes.
  * **Análise de Dados:** Gráficos com tendências diárias, ranking de oficiais e apreensões por tipo (utilizando Chart.js).
  * **Controle de Acesso (Roles):** Sistema de permissão **oficial** e **comando**, que gerencia a visibilidade de abas (ex: Administração) e dados.
  * **Administração:** Aba dedicada para gerenciar usuários (funções/nomes) e pesquisar todos os relatórios da corporação (apenas para usuários com role comando).

### 🛠️ Tecnologias Utilizadas

Este projeto é construído como uma *landing page* estática, utilizando o JavaScript para integrar-se com o Firebase:

  * **Frontend:** HTML5, CSS puro e JavaScript.
  * **Design:** Tailwind CSS (carregado via CDN) para um design moderno e responsivo.
  * **Banco de Dados/Backend:** Google Firebase (Auth e Firestore).
  * **Visualização de Dados:** Chart.js para a geração de gráficos dinâmicos no dashboard.

### ⚙️ Firebase

Para que o sistema funcione corretamente, você deve configurar o seu projeto no Firebase e atualizar as credenciais em **todos os arquivos HTML (index.html, rota_rso.html, rota_dashboard.html)** onde a variável firebaseConfig é definida.

1.  **Crie um Projeto no Firebase:**

2.  **Habilite Serviços:**

      * **Authentication:** Habilite o método de login por **Email/Senha**.
      * **Firestore Database:** Crie um banco de dados e defina as regras de segurança adequadas (o sistema espera coleções para relatórios e dados de usuário).

3.  **Regras Iniciais no Firebase:** Para que um usuário possa entrar e ser reconhecido com a role comando ou oficial, ele deve ser cadastrado manualmente no Authentication.

### 🔄 Adaptação para Outras Corporações

Para adaptar o sistema para uma nova corporação (ex: PMESP, Polícia Civil, etc.):

1.  **Textos:** Edite todos os textos e títulos nos arquivos HTML (ex: mudar "1° BPChq ROTA" para o seu batalhão.).
2.  **Imagens:** Substitua o arquivo BrasãoROTA.png pelo logo da sua corporação.
