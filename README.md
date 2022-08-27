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
 - pasta com as dependências do projeto, módulos externos 

pasta src 
 - pasta onde se encontra toda a aplicação 

pasta e2e
 - pasta onde se encontram os testes da aplicação 

### Pasta SRC

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

## Módulos e Componentes  

### Introdução 

Funcionammento do angular: o angular funciona através de módulos e componentes, são os itens principais do angular. Então, obrigatóriamente, uma aplicação angular deverá conter no minímo um módulo e um componente. Toda vez que uma aplicação angular é iniciada o arquivo é chamado e executado.
Um componente no angular sempre é composto por um arquivo typescript, um arquivo html e um arquivo css, podendo também ter um arquivo spec.ts que é um aruivo de testes. 
app.componente.ts: comportamento.
app.componente.html: visualização. 
app.componente.css: falhas de estilos. 


````ts 

//importação do angular core, módulo enablePodroMode para trabalhar em produção 
import { enableProdMode } from '@angular/core';

// importação do @angular/platform-browser-dynamic, módulo  platformBrowserDynamic 
// para trablhar com diversas plataformas(o angular é agnóstico, roda nativo em outras plataformas)
import { platformBrowserDynamic } from '@angular/platform-browser-dynamic';


// importação módulo raiz 
import { AppModule } from './app/app.module';

// importação das variáveis de ambiente 
import { environment } from './environments/environment';

// utilizando módulo 
if (environment.production) {
  enableProdMode();
}

//realizar carregamento de uma plataforma 
platformBrowserDynamic()

    //iniciar aplicação carregando um módulo, nocaso o modulo padrão(raiz)
  .bootstrapModule(AppModule)
  .catch(err => console.error(err));

````

Módulo app.module.ts 

````ts
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';

//MetaData 
//Decorador
@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})

//exportando, tornando classe publica 
export class AppModule { }

````

## Radando aplicação 

````bash 
ng serve
````
rodar e abrir o braswer

````bash
ng server -o
````

## Variáveis e Tipos 

criando variável 
````ts
public todos: any[] = [];
````

## Exibindo dados na tela 

## Variáveis angular

### ngIf

````html
<button *ngIf="!todo.done">Concluir</button> |
    <button *ngIf="todo.done">Refazer</button> |
````
## Removendo um item 
