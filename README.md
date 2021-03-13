# SpringBootEcommerce

## Dependencies

Open the Maven tool window and run `Reimport All Maven Projects` to download project dependencies.

## Run

Navigate to `src/main/java/com/luv2code/ecommerce/SpringBootEcommerceApplication.java` and run main to spin up a server on http://localhost:8080/.

## APIs

Products: http://localhost:8080/api/product-category/1/products

* Product: http://localhost:8080/api/product-category{?page,size,sort}
* States: http://localhost:8080/api/states{?page,size,sort}
* Countries: http://localhost:8080/api/countries{?page,size,sort}
* Customers: http://localhost:8080/api/customers{?page,size,sort}
* Products: http://localhost:8080/api/products{?page,size,sort}
* Profile: http://localhost:8080/api/profile

# AngularEcommerce

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.3.18.

## Dependencies

Run `npm install` to download project dependencies.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Project Milestones

```gherkin
Angular Front End - Product List
Integrating Online Shop Template
Search for Products by Category
Search for Products by Category (Dynamic Search Component)
Search for Products by Keyword
Product Master-Detail View
Pagination
Shopping Cart Status Component
Shopping Cart Items CRUD
Checkout Form Layout
Checkout Form - Drop-Down Lists
Checkout Form - Validation
Checkout Form - Review Cart Totals
Checkout Form - Save the Order to Database - Backend
Checkout Form - Save the Order to Database - Frontend
Security - Login/Logout
Security - User Registration
Security - VIP Member Access -Protected Routes
Security - Handling BrowserRefresh
Refactoring
```

## Deploy to Heroku

1. Change `SPRING_PROFILES_ACTIVE` to `prod`.
1. Add the following to `package.json`.
```aidl
"heroku-postbuild": "ng build --prod && npm install -g http-server-spa",
"start": "http-server-spa dist/webapp index.html $PORT",
```
3. Add `baseUrl: 'http://localhost:8080/` to `environment.ts'`.
1. Add `baseUrl: 'https://emiller-ecommerce.herokuapp.com/'` to `environment.prod.ts`.
1. Change the `product.service.ts` to use `environment.baseUrl`.
1. run `ng build` in angular project root and copy the content of `dist` folder to `src/main/resources/static/`.
1. create Procfile (for maven): `web: java $JAVA_OPTS -Dserver.port=$PORT -jar target/*.jar`
1. Ensure you have `spring-boot-starter-web` present in dependencies. It has the embedded tomcat and is automatically configured to serve static content from the static folder.


* [Read this later](https://dasunpubudu.wordpress.com/2018/04/17/deploying-spring-angular-mast-stack-application-in-heroku/)
* [Deploy Spring and Angular to same Heroku](https://stackoverflow.com/questions/44831611/spring-boot-angular-2-heroku-deployment)


## ng generate Command

The ng generate command is used to generate and/or modify file based on schematic.

```
ng generate <schematic> [options]  
ng g <schematic> [options]  
ng g module environments/environment
```
### Parameter Explanation:
`<schematic >`: It specifies the schematic or collection:schematic which you want to generate. It can take one of the following sub-commands.

* appShell
* application
* class
* component
* directive
* enum
* guard
* interface
* library
* module
* pipe
* service
* serviceWorker
* universal

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
