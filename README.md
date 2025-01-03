# Formulário de Inscrição

Este projeto é um formulário de inscrição simples desenvolvido com **React**, **TypeScript**, **Tailwind CSS** para estilização e **Vite** como bundler. O usuário pode se inscrever em uma newsletter fornecendo seu nome, e-mail e concordando com os termos. O formulário também valida os dados do usuário e exibe mensagens de erro caso algum campo obrigatório seja deixado em branco ou se o usuário não concordar com os termos.

## Tecnologias Utilizadas

- **React**: Framework JavaScript para construir a interface de usuário.
- **TypeScript**: Superset do JavaScript que adiciona tipagem estática.
- **Tailwind CSS**: Framework CSS para estilização, utilizado para um design responsivo e moderno.
- **Vite**: Bundler moderno e rápido para desenvolvimento e produção de aplicações web.

## Estrutura de Arquivos

- `src/components/Form.tsx`: Componente principal do formulário, onde a lógica de captura e validação de dados ocorre.
- `src/App.tsx`: Componente que renderiza o formulário de inscrição dentro de uma página.
- `src/utils/validate.ts`: Função de validação para os dados do formulário.
- `src/types/User.ts`: Definição do tipo `User` que representa os dados do formulário.

## Como Executar o Projeto

### Pré-requisitos

- **Node.js** (versão 14 ou superior)
- **npm** ou **yarn**

### Passos

1. Clone o repositório:
    ```bash
    git clone https://github.com/matteussaraujo/form_newsletter
    cd form_newsletter
    ```

2. Instale as dependências:
    ```bash
    npm install
    ```
    ou
    ```bash
    yarn install
    ```

3. Inicie o servidor de desenvolvimento com Vite:
    ```bash
    npm run dev
    ```
    ou
    ```bash
    yarn dev
    ```

4. Abra o navegador e acesse `http://localhost:5173` para visualizar o aplicativo.

### Tailwind CSS

O Tailwind CSS já está configurado no projeto. Ele é usado para a estilização dos componentes, garantindo um design limpo e responsivo. Caso queira personalizar a aparência do projeto, edite as classes do Tailwind nos componentes JSX.

## Descrição do Código

### `Form.tsx`

Este é o componente principal que renderiza o formulário de inscrição.

- **useState** é usado para gerenciar o estado dos campos `name`, `email`, `agree` e `errors`.
- O **handleSubmit** é responsável por capturar os dados do formulário, validar usando a função `validate`, e exibir as mensagens de erro se necessário. Se a validação passar, o formulário é resetado e uma mensagem de agradecimento é exibida.
- O formulário contém campos de entrada para o nome, e-mail e uma caixa de seleção para os termos.
- As mensagens de erro são mostradas ao lado dos campos, caso algum dado não passe na validação.

### `App.tsx`

O `App.tsx` renderiza o componente `Form` e envolve o formulário com um estilo e título. A página inclui uma breve descrição e um rodapé com uma mensagem de aviso sobre o envio de e-mails.

### `validate.ts`

Este arquivo contém a função `validate`, que recebe os dados do formulário e verifica se todos os campos obrigatórios estão preenchidos. Caso algum campo falhe na validação, é retornado um objeto de erro com mensagens correspondentes.

### `User.ts`

O arquivo `User.ts` define o tipo `User`, que é usado para tipar os dados do formulário. Ele contém as propriedades `name`, `email` e `agree`, que são todas opcionais.

## Como Funciona a Validação

A função `validate` verifica três campos:

1. **name**: Verifica se o nome não está vazio.
2. **email**: Verifica se o e-mail não está vazio.
3. **agree**: Verifica se o usuário concordou com os termos.

Se algum desses campos não for preenchido ou o usuário não concordar com os termos, uma mensagem de erro será exibida ao lado do campo correspondente.

## Conclusão

Este projeto demonstra um formulário simples com validação e feedback ao usuário. Ele foi configurado utilizando **Vite** para um ambiente de desenvolvimento rápido e otimizado, e **Tailwind CSS** para estilização. Você pode usá-lo como base para criar formulários de inscrição mais complexos em seus projetos React.

