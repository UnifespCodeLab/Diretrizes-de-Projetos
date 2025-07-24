# **Documentação IBEapp**

## **Sobre**
Esse arquivo servirá como um guia para ajudar a manter os projetos padronizados.

## **Padrão de Nomenclatura**

| Elemento | Padrão | Descrição |
|----------|--------|-----------|
| Variáveis | Snake Case | Letra inicial minúsula - Ex: `snake_case`, `variavel_snake_case` |
| Funções | Snake Case | Letra inicial minúsula -- Ex: `snake_case`, `variavel_snake_case` |
| Arquivos → Componentes | Pascal Case | Letra inicial maiúscula — Ex: `PascalCase`, `VariavelPascalCase` |
| Arquivos → Pages | Pascal Case | Letra inicial maiúscula — Ex: `PascalCase`, `VariavelPascalCase` |
| Arquivos → Restantes | Nomes em minúsculo  | Todas as letras em minúsculo |
| Idioma | Inglês (preferencial) | Português caso necessário |


## **Organização de Pastas**

| Categoria | Padrão / Valor | Descrição |
|-----------|----------------|-----------|
| Nomenclatura | Nomes em minúsuclo | Todas as letras em minúsculo. |
| Nível de hierarquia | Caminho | Descrição |
---
```plaintext
raiz/
├── /docs                   → Armazena diagramas do projeto
├── /public                 → Arquivos que não são modificados durante o processo de build.  
                             Geralmente guarda-se arquivos estáticos (vão manter o seu nome ou não serão modificados diretamente durante o processo da aplicação),  
                             como imagens, arquivos de textos, ícones para a aba do navegador e outros arquivos multimídia.
├── /src                    → Armazena todo o código-fonte da aplicação
│   ├── /assets             → Armazena arquivos não compilados como recursos visuais e estáticos
│   ├── /components         → Componente é um bloco de código autocontido e reutilizável que encapsula uma parte específica da interface do usuário (UI)  
                             e toda a sua lógica associada
│   ├── /layouts            → Armazena elementos de estrutura de página
│   ├── /pages              → Guarda todas as páginas individuais.  
                             Em outra análise, são um grupo de componentes que formam uma componente mais complexa
│   ├── /routes             → Armazenar o mapeamento das páginas para rotas
│   ├── /services           → Comunicação entre o Backend e Frontend
│   └── /util               → Funções reutilizáveis e genéricas, sem dependência visual

```
## **Padrão do Código**

|  Categoria  |  Diretriz | Observações |  
|-------------|-----------|------------- |
| Escrita | Preferencialmente em inglês  | 
Mas, mantendo em português palavras com relação direta às regras de negócio: Postagem, Comentario, Bairro, Categoria. |   
| Comentários | Breve descrição de cada função, metodo e classe. Outros comentários caso necessário. | Exemplo: Descrição da função, metodo ou classe |  
| Identação | Quatro espaços ou um tab |   

## **Git**

| Tipo  | Nomenclatura  | Descrição  |
|-------|---------------|------------|
| Branch | issue-XXXX | sendo XXXX o numero da issue criada |
| Commit  | Conventional Commits:<br>`<tipo>: <descrição>`<br>Descrição em inglês, iniciando com verbo no presente simples |  <ul><li>`test`: indica qualquer tipo de criação ou alteração de códigos de teste.</li><li>`feat`: indica o desenvolvimento de uma nova feature ao projeto.</li><li>`refactor`: usado quando houver uma refatoração de código que não tenha qualquer tipo de impacto na lógica/regras de negócio do sistema.</li><li>`style`: empregado quando há mudanças de formatação e estilo do código que não alteram o sistema de nenhuma forma.</li><li>`fix`: utilizado quando há correção de erros que estão gerando bugs no sistema.</li><li>`chore`: indica mudanças no projeto que não afetam o sistema ou arquivos de testes. São mudanças de desenvolvimento.</li><li>`docs`: usado quando há mudanças na documentação do projeto.</li><li>`build`: utilizada para indicar mudanças que afetam o processo de build do projeto ou dependências externas.</li><li>`revert`: indica a reversão de um commit anterior.</li></ul> 🔗 [Conventional Commits v1.0.0](https://www.conventionalcommits.org/en/v1.0.0/) |

## **Pull Request**

|  Categoria  | Diretriz / Padrão  | 
|-------------|--------------------|
| Descrição | Breve descrição de que o PR estará implementando ou resolvendo, podem ser feitas em português. |
| Título | O título segue o padrão de `[issue-(id)] Título da issue` |
| Aprovação | Coordenador do projeto |

## **Boas Práticas**

1.  Coordenador do projeto


