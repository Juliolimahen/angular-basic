# angular-basic

## Instalando o Angular
````bash
npm install -g @angular/cli@7.2.2
```` 
## Criando primeiro projeto 
````bash 
ng new todo
````

## Entendendo a estrutura do projeto 

tslint.json 
 - arquivo de intelisense typescript 

tsconfig.json
 - arquivo de configuração do typescript

package.json
 - arquivo com as dependências do projeto

package-lock.json
 - aquivo local com as dependências do projeto

angular.json 
 - arquivo com as configurações do angular 

.gitignore 
 - arquivo com define o que não será enviado para git 

editorconfig
 - arquivo de consfigurações do editor(vscode)

pasta node_modules
 - pasta com as dependências do projeto 

pasta src 
 - pasta onde se encontra toda a aplicação 

pasta e2e
 - pasta onde se encontram os testes da aplicação 

## SRC

tslint.json 
 - arquivo de intelisense typescript 

tsconfig.app.json
 - arquivo de configuração da aplicação 

tsconfig.spec.json
 - arquivo de configuração de test da aplicação 

test.ts
 - arquivo responsável por carregar os testes 

styles.css 
 - estilo da aplicação como um todo (css da aplicação)

polyfills.ts
 - arquivo responsável por carregar os módulos da aplicação 

main.ts
 - arquivo princípal, toda vez que à aplicação for iniciada esse arquivo será chamado  

karma.conf.js
 - arquivo que executa os códigos 

index.html 
 - página de entrada 

favicon.ico 
 - arquivo do ícone da aplicação 

brawserlist 
 - arquivo responsável por dar compatibilidade aos CSSs (para brawser antigos, pricípalmente)

past environments 
 - onde serão armazenadas as variáveis de ambiente (produção ou desensvolvimento)

pasta assets
 - pasta onde ficam os utilitários, imagens e css adicionais   

pasta app 
 - pasta princípal, onde fica nossos módulos, nossos components 