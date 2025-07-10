# **Documentação VApt - WEB**

## **Sobre**
Esse arquivo servirá como um guia para ajudar a manter os projetos padronizados.

## **Padrão de Nomenclatura**

| Categoria |Padrão | Regras |
|-----------|-------|--------|
| **Variáveis** | `camelCase` | Primeiro nome inicia com letra minúscula, os seguintes com maiúscula sem separação o por espaços (ex: `variavelExemplo`, `camelCase`) |
| **Funções/Métodos** | `camelCase` | Mesmo padrão de variáveis (`variavelExemplo`, `camelCase`) |
| **Classes (Bloco principal)** | **Metodologia BEM** | Separação de nomes com hífen (ex: `class-example`) |
| **Classes (Elementos)** | **Metodologia BEM** | Bloco principal + dois underlines + elemento (ex: `class-example__element`) |
| **Arquivos -> componentes** | `PascalCase` | Todos nomes se iniciam em letras maiúscula, sem separação por espaços (ex: `PascalCase`, `ArquivoComponente`) |
| **Arquivos -> static** | `PascalCase` ou minúsculo | Todos nomes se iniciam em letras maiúscula, sem separação por espaços (ex: `PascalCase`, `ArquivoComponente`), caso tenha apenas um nome mantenha em minúsculo |
| **Arquivos -> restantes** | `kebab-case` | Todos nomes se iniciam em litras minúsculas, com separação por hífen (ex: `kebab-case`, `arquivo-exemplo`) |
| **Idioma** | Inglês ou Português | - |

## **Organização de Pastas**

| Categoria    | Padrão     | Observações |
|--------------|------------|-------------|
| Nomenclatura | Snake Case | Todas letras em minúsculo, palavras separadas por underline.<br>Ex: `snake_case`, `pasta_snake_case` |
| Exceções | - | Pastas para configuração de testes e GitHub. |
| Idioma | Inglês | - |
---
```plaintext
raiz/
├── /assets                       → O diretório contém arquivos não compilados, como arquivos stylus ou sass, imagens ou fontes.
│   ├── /images                   → Imagens sobre a codelab
│   ├── /js                       → Arquivo JSON para itens do admin
│   └── /service                  → Local para iniciar a API

├── /components                   → Contém os componentes .vue, que compõem partes da interface do usuario (UI) e sua lógica associada em sua página e podem ser reutilizados e importados
em sua páginas e layouts.
│   └── /admin                    → Contém os componentes para admin
│       ├── __test__              → Arquivos para armazenar os testes de /components/admin
│       │   └── __snapshots__     → Armazenam o snapshots para testes do /components/admin
│   └── __test__                  → Arquivos para armazenar os testes de /components
│       └── __snapshots__         → Armazenam o snapshots para testes dos /componentes

├── /layout                       → Reponsável por alterar a aparência da aplicação Nuxt, podendo ter layouts distintos para desktop e mobile

├── /pages                        → Contem as views e rotas da aplicação. Nuxt ira ler todos arquivos .vue e configurar o Vue Router
│   └── /admin                    → Aplicações para o admin
│       ├── __tests__             → Arquivos para armazenar os testes de /admin
│       │   └── __snapshots__     → Armazenam o snapshots para testes dos /pages/admins 
│   └── __tests__                 → Arquivos para armazenar os testes de /pages
│       └── __snapshots__         → Armazenam o snapshots para testes de /pages

├── /plugins                      → Contém plugins JavaScript que sera executado antes de instanciar a aplicação raiz do Vue.js. Também o local para adicionar plugins do vue, funções ou
constantes

├── /static                        → Contém os arquivos estáticos, mapeados para /

├── /store                         → Contém os arquivos store. Ao criar um arquivo neste diretório, o Vuex é ativado automaticamente. Tendo como função reutilizar a lógica de estado de
um componente para vários

├── /test                          → Local para iniciar e configurar o jest

├── /.github                       → Pasta que não afeta diretamente a aplicação, mas sua interação com o GitHub
│   ├── /workflows                 → Armazena os arquivos .yaml para automações do GitHub Actions
│   └── ISSUE_TEMPLATE             → Armazena o template para a issue do repositório
```

## **Padrão do Código**

|  Categoria | Diretriz  | Descrição |   
|------------|-----------|-----------|
| Escrita      | Inglês  | - | 
| Comentários  | - | Breve descrição do que cada parte do método faz. Escrita em português | 

**Identação:**<br>
**HTML** -> Quebra de linha para blocos como ``<template>``, ``<div>``, ``<button>``.
Para cada nivel de alinhamento insira dois espaços em relação ao bloco pai.
Abrir e fechar os blocos na mesma profundidade.
```html
<div>  
  <button>  
  </button>  
</div>  
```
**CSS** -> Quebra de linha para classes.
dentro da classe inserir dois espaços cada linha de estilo, quebras de linhas para separação .
Caso tenha subclasses duas quebras de linha e siga o padrão anterior.
Abrir e fechar os blocos no mesmo nivel de identação
```css
.div{
 .button{
 }
}
```
**Script** -> Quebra de linha para o método
Dentro do método inserir dois espaços e quebras de linhas para cada linha de código.
Para condicionais, laços de repetições ou chamar outros métodos repita o padrão anterior.
Abrir e fechar blocos no mesmo nivel de identação.
```
method() {
 code...
 if(){
 code..
 }
}
```

## **Git**

| Tipo  | Nomenclatura  | Descrição  |
|-------|---------------|------------|
| Branch  | `issue-(id)` | Sendo id um valor numérico inteiro Ex: issue-15 |
| Commit  | Conventional Commits:<br>`<tipo>: <descrição>`<br>Descrição em inglês, iniciando com verbo no presente simples  |  <ul><li>`test`: indica qualquer tipo de criação ou alteração de códigos de teste.</li><li>`feat`: indica o desenvolvimento de uma nova feature ao projeto.</li><li>`refactor`: usado quando houver uma refatoração de código que não tenha qualquer tipo de impacto na lógica/regras de negócio do sistema.</li><li>`style`: empregado quando há mudanças de formatação e estilo do código que não alteram o sistema de nenhuma forma.</li><li>`fix`: utilizado quando há correção de erros que estão gerando bugs no sistema.</li><li>`chore`: indica mudanças no projeto que não afetam o sistema ou arquivos de testes. São mudanças de desenvolvimento.</li><li>`docs`: usado quando há mudanças na documentação do projeto.</li><li>`build`: utilizada para indicar mudanças que afetam o processo de build do projeto ou dependências externas.</li><li>`revert`: indica a reversão de um commit anterior.</li></ul> 🔗 [Conventional Commits v1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) |

## **Pull Request**

|  Categoria  | Diretriz / Padrão  | 
|-------------|--------------------|
| Descrição | Breve descrição de que o PR estará implementando ou resolvendo, podem ser feitas em português. |
| Título | Nome da issue (branch) entre colchetes + descrição da implementação |
| Aprovação | Coordenador do projeto ou pessoa também relacionada à task |