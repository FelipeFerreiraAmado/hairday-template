# 💇‍♀️ Painel de Agendamentos HairDay

Este repositório apresenta um painel de agendamentos desenvolvido para um salão de cabeleireiros, focado em gerenciar horários de forma eficiente e intuitiva.

## ✨ Visão Geral

O sistema permite que clientes agendem horários para manhã, tarde e noite, por dia do mês e ano. Uma vez que um horário é agendado, ele se torna indisponível para outros agendamentos, garantindo a exclusividade. Os agendamentos são persistidos através de uma API local, assegurando que os dados não sejam perdidos ao recarregar a página.

## 📸 Screenshots do Frontend

*Adicione aqui as imagens do frontend da aplicação. Exemplo:*

<!-- ![Descrição da Imagem 1](./caminho/para/imagem1.png) -->
<!-- ![Descrição da Imagem 2](./caminho/para/imagem2.png) -->

## 🛠️ Tecnologias Utilizadas

[![My Skills](https://skillicons.dev/icons?i=html,css,js,nodejs,webpack,babel,dayjs,json )](https://skillicons.dev )

- **HTML, CSS, JavaScript**: Para a estrutura, estilização e lógica de front-end do painel.
- **Node.js**: Utilizado para organizar as bibliotecas e pacotes do projeto.
- **Webpack**: Empacotador de módulos para otimização e compilação do código.
- **Babel**: Transpilador de JavaScript para garantir compatibilidade com diferentes navegadores.
- **Day.js**: Biblioteca leve para manipulação de datas e horas.
- **json-server**: Ferramenta para criar uma API REST falsa rapidamente, utilizada para persistir os agendamentos no arquivo `server.json`.

## 🚀 Como Usar

Para configurar e executar o projeto localmente, você precisará rodar dois servidores simultaneamente: um para a API de agendamentos e outro para a aplicação front-end. Siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/FelipeFerreiraAmado/hairday-template.git
    ```
2.  **Navegue até o diretório do projeto:**
    ```bash
    cd hairday-template
    ```
3.  **Instale as dependências:**
    ```bash
    npm install
    ```
4.  **Inicie o JSON Server (API de Agendamentos ):**
    ```bash
    npm run server
    ```
    *Certifique-se de que o `json-server` esteja rodando na porta `3333` para que a aplicação possa se comunicar com a API. Este servidor gerencia a persistência dos agendamentos no arquivo `server.json`.*

5.  **Em um novo terminal, inicie o Webpack (Aplicação Front-end):**
    ```bash
    npm run dev
    ```
    *Este comando irá compilar os arquivos JavaScript e CSS e iniciar um servidor de desenvolvimento, que geralmente roda em `http://localhost:3000`.*

6.  **Acesse a Aplicação no Navegador:**
    Abra seu navegador e acesse `http://localhost:3000` para visualizar o painel de agendamentos.

## 💡 Funcionalidades

-   **Visualização de Horários**: Painel intuitivo que exibe horários disponíveis para agendamento.
-   **Agendamento por Período**: Possibilidade de agendar horários nos períodos da manhã, tarde e noite.
-   **Seleção de Data**: Escolha do dia e ano para o agendamento.
-   **Indisponibilidade Automática**: Horários agendados são automaticamente marcados como indisponíveis.
-   **Persistência de Dados**: Agendamentos são salvos em um arquivo `server.json` via API, garantindo que os dados não sejam perdidos ao recarregar a página.

## 🌐 Endpoints da API (json-server )

O `json-server` cria automaticamente endpoints RESTful com base no arquivo `server.json`. Para este projeto, os principais endpoints são:

-   **`GET /appointments`**: Retorna todos os agendamentos.
-   **`GET /appointments/:id`**: Retorna um agendamento específico pelo ID.
-   **`POST /appointments`**: Cria um novo agendamento.
    -   **Corpo da Requisição (JSON)**:
        ```json
        {
          "date": "YYYY-MM-DD",
          "time": "HH:MM",
          "clientName": "Nome do Cliente"
        }
        ```
-   **`PUT /appointments/:id`**: Atualiza um agendamento existente pelo ID.
    -   **Corpo da Requisição (JSON)**:
        ```json
        {
          "date": "YYYY-MM-DD",
          "time": "HH:MM",
          "clientName": "Novo Nome do Cliente"
        }
        ```
-   **`DELETE /appointments/:id`**: Exclui um agendamento pelo ID.

## 🔮 Melhorias Futuras

-   Implementação de autenticação e autorização para acesso ao painel.
-   Integração com um banco de dados real (e.g., PostgreSQL, MongoDB) para maior escalabilidade e robustez.
-   Funcionalidades de notificação para clientes e cabeleireiros.
-   Interface de usuário mais rica e responsiva para dispositivos móveis.
-   Adição de serviços e profissionais múltiplos.

## 🤝 Contribuição

Contribuições são sempre bem-vindas! Se você tem ideias para melhorar este projeto, sinta-se à vontade para:

1.  Fazer um fork do repositório.
2.  Criar uma nova branch (`git checkout -b feature/sua-feature`).
3.  Fazer suas alterações e commit (`git commit -m \'Adiciona nova feature\'`).
4.  Enviar para a branch (`git push origin feature/sua-feature`).
5.  Abrir um Pull Request.

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
