# **Documentação Agendinha do GRAAC - WEB**

## **Sobre**
Esse arquivo servirá como um guia para ajudar a manter os projetos padronizados.

## **Padrão de Nomenclatura**

| Elemento | Padrão | Descrição |
|----------|--------|-----------|
| Variáveis | Camel Case | Letra inicial minúscula — Ex: `camelCase`, `variavelCamelCase` |
| Funções | Camel Case | Letra inicial minúscula — Ex: `camelCase`, `variavelCamelCase` |
| Arquivos → Componentes | Pascal Case | Letra inicial maiúscula — Ex: `PascalCase`, `VariavelPascalCase` |
| Arquivos → Páginas | Pascal Case | Letra inicial maiúscula — Ex: `PascalCase`, `VariavelPascalCase` |
| Arquivos → Restantes | Camel Case | Letra inicial minúscula — Ex: `camelCase`, `variavelCamelCase` |
| Idioma | Inglês (preferencial) | Português caso necessário |


## **Organização de Pastas**

| Categoria | Padrão / Valor | Descrição |
|-----------|----------------|-----------|
| Nomenclatura | Snake Case | Todas letras em minúsculo, palavras diferentes separadas por underline. <br>Ex: `snake_case`, `pasta_snake_case` |
| Nível de hierarquia | Caminho | Diretório raiz do projeto que contém as pastas principais |
---
```plaintext
raiz/

├── /components   → Componente é um bloco de código autocontido e reutilizável que encapsula uma parte específica da interface do usuário (UI) e toda a sua lógica associada.

├── /interfaces   → Guarda os modelos que um corpo/retorno de requisição, como se fosse um "contrato" de como deve ser a estrutura do objeto.

├── /middleware   → Códigos/funções que rodam antes de rodar uma página ou um grupo da mesma.

├── /pages        → Guarda todas as páginas individuais. Em outra análise, são um grupo de componentes que formam uma componente mais complexa.

├── /plugins      → Arquivos que permitem funcionalidades de terceiro que não são nativas do Vue, como o Vuetify. Elas adicionam funcionalidades no nível da aplicação.

├── /public       → Arquivos que não são modificados durante o processo de build. Geralmente guarda-se arquivos estáticos (vão manter o seu nome ou não serão modificados
diretamente durante o processo da aplicação), como imagens, arquivos de textos, ícones para a aba do navegador e outros arquivos multimídia.

├── /servers      → Usado para registrar handlers de API e servidor dentro do aplicativo. Um handler é uma função de evento que é executada quando uma chamada específica
e geralmente retorna algo (como endpoints de API ou algo relacionado ao lado do servidor).

├── /store        → Serve para configurar os stores, isto é, reutilizar a lógica de estado de um componente para vários. Usado com algum gerenciador de estado, como o Pinia.

├── /utils        → funções diversas que podem ser úteis nos componentes do Vue e que não estão diretamente ligadas com eles.

```
## **Padrão do Código**

|  Categoria  |  Diretriz | Observações |  
|-------------|-----------|------------- |
| Escrita | Preferencialmente em inglês  | Evite termos como `CadastroSystem` ou `AtendimentoState`. |   
| Comentários | Evite comentários | O código sempre precisa ser escrito para que sua rotina não precise de comentários. Se achar necessário, pode usar variáveis como `doSomethingLikeThis`, que possuem nomes grandes mas bem especificados. Para interfaces e classes criadas apenas como modelo, se necessário, use `JSDoc`. |  
| Identação | Quatro espaços ou um tab |   

## **Git**

| Tipo  | Nomenclatura  | Descrição  |
|-------|---------------|------------|
| Branch | `issue-(id)-(description)` | Sendo `id` o ID da issue criada e `description` uma breve descrição (4 ou 5 palavras no máximo, preferencialmente).<br>**Ex:** `issue-15-add-login-system` |
| Commit  | Conventional Commits:<br>`<tipo>: <descrição>`<br>Descrição em inglês, iniciando com verbo no presente simples |  <ul><li>`test`: indica qualquer tipo de criação ou alteração de códigos de teste.</li><li>`feat`: indica o desenvolvimento de uma nova feature ao projeto.</li><li>`refactor`: usado quando houver uma refatoração de código que não tenha qualquer tipo de impacto na lógica/regras de negócio do sistema.</li><li>`style`: empregado quando há mudanças de formatação e estilo do código que não alteram o sistema de nenhuma forma.</li><li>`fix`: utilizado quando há correção de erros que estão gerando bugs no sistema.</li><li>`chore`: indica mudanças no projeto que não afetam o sistema ou arquivos de testes. São mudanças de desenvolvimento.</li><li>`docs`: usado quando há mudanças na documentação do projeto.</li><li>`build`: utilizada para indicar mudanças que afetam o processo de build do projeto ou dependências externas.</li><li>`revert`: indica a reversão de um commit anterior.</li></ul> 🔗 [Conventional Commits v1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) |

## **Pull Request**

|  Categoria  | Diretriz / Padrão  | 
|-------------|--------------------|
| Descrição | Referencie sempre qual issue o PR está solucionando em sua descrição. Use `#(id)`, sendo id o id da issue. Pode-se usar `Closes #(id)` ou `Fecha #(id)`. Descrições de PR podem ser feitas em português ou inglês |
| Título | O título segue o padrão de `[issue-(id)] Título da issue` |
| Aprovação | Coordenador: **Guilherme Samuel** |

## **Boas Práticas**

1. Use `v-for` com a referência `:key=""`, para o Vue fazer com que a DOM fique mais eficiente.  
   **Não use `v-for` e `v-if` ao mesmo tempo.**

2. A função `data()` sempre deve retornar uma função.

3. Componentes declarados uma vez por página devem usar o prefixo `The` antes do nome do componente.

## **Método de trabalho**
  - Scrum
## **Frequência de reunião**
  - Se necessário, 1 reunião por semana para discutir pontos específicos do projeto da Agendinha
