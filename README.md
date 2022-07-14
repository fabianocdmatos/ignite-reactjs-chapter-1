# ignite-reactjs-chapter 1

Estudo de React JS desde o Início

---

### Aula 3 - Configurando Babel

---

- `Babel` ( https://babeljs.io/ )
- Conversor do código `Javascript` e `JSX` de uma maneira que todos os navegadores entendam.

  - Instalação apenas no ambiente `-D` desenvolvimento.
  - Em produção não precisa do `Babel`, o código vai ser convertido antes de subir a aplicação.

    - `npm install @babel/core -D` - biblioteca que contém todas as funcionalidades do `Babel`.
    - `npm install @babel/cli -D` - biblioteca para o `Babel` ser executado em linha de comando.
    - `npm install @babel/preset-env -D` - biblioteca que identifica qual ambiente a aplicação esta sendo executada para poder converter o `Javascript` e `JSX` da melhor maneira possível para o ambiente que vai ser instalado a aplicação.

  - Na pasta principal crie o arquivo `babel.config.js`
  - Dentro do arquivo adicione a configuração do `Babel`

    ```lang-js
    module.exports = {
      presets: [ '@babel/preset-env' ]
    }
    ```

  - Na pasta `src` crie o arquivo `index.js` e digite o código abaixo.:

    ```lang-js
    const user = {
        name: "Fabiano"
    };

    console.log(user.name);
    console.log(user.address?.street);
    ```

- Comando via bash para poder converter o `Javascript` e `JSX` de uma forma que os navegadores entendam.

  - `npx babel src/index.js --out-file dist/bundle.js`
  - com este comando vai ser gerado o `Javascript` de uma forma que os navegadores entendam, onde que `--out-file` vai ser o arquivo `JS` gerado com o códgo todo convertido.
  - de acordo com uma convenção a pasta `dist` e o arquivo `bundle.js` é meio que padrão para o desenvolvimento.
  - após executar o comando vai ser gerada a pasta `dist` com arquivo `bundle.js` onde em `bundle.js` vai estar o código `Javascript` convertido de uma forma que os navegadores entendam.

  - `**Obervação:** nunca vamos programar ou mexer nesta pasta dist e nem no arquivo bundle.js. Só apenas ao executar a aplicação e fazendo o build dela, automanticamente vai ser gerada esta pasta com o Javascript convertido de uma forma que os navegadores entendam.`

---

### Aula 02 - Criando estrutura do projeto

---

- Criar pasta do projeto

  - `ignite-reactjs-chapter-1`

- Inicializar o repositório dentro da pasta `ignite-reactjs-chapter-1`

  - `npm init -y` - Cria automanticamente o arquivo abaixo com as configurações corretas.
    - `package.json` - contem as configurações, informações e dependências do projeto.

- Instalando bibliotecas/dependências do projeto, a chamada e registros delas vão ser salvo no arquivo `package.json`.

  - `npm install react` ( https://www.npmjs.com/package/react ) - biblioteca principal em Javascript para o desenvolvimento de aplicações.
  - `npm install react-dom` ( https://www.npmjs.com/package/react-dom ) - biblioteca Javascript, interpretador/conversor de HTML para poder trabalhar React com Web. Comunicação do Javascript com o HTML.

- Estrutura de pastas e arquivos ( fazer a criação das pastas e arquivos abaixo começando na pasta principal )
  - `src` - pasta source onde vai conter todo código criado por você da aplicação
  - `public` - pasta onde vai ficar arquivos publicos da aplicação, arquivos que pode ser acessado de meios externos. ( ex.: favicon.ico, index.html, robot.txt, etc.)
    - `public/index.html` - arquivo `index.html` criado dentro da `public`.

---

### Aula 01 - Instalação e configuração do Ambiente para o desenvolvimento

---

- NodeJs ( https://nodejs.org/ )
- Git ( https://git-scm.com/ )
- VSCode ( https://code.visualstudio.com/ )
  - Extensões
    - Auto Close Tag
    - Color Highlighter
    - Dracula Official
    - ES7 React/Redux/GraphQL/React-Native snippets
    - ES7+ React/Redux/React-Native snippets
    - ESLint
    - GitLens — Git supercharged
    - GraphQL
    - Import Cost
    - JSX HTML <tags/>
    - PostCSS Language Support
    - Prettier - Code formatter
    - Tabnine AI Autocomplete for Javascript, Python, Typescr
    - Tailwind CSS IntelliSense
    - vscode-icons
    - vscode-styled-components
