<img src="http://www.schematocode.com/ngx-logo.jpg" alt="logo" width="100%">

<img src="http://www.schematocode.com/screen.jpg" alt="generated screens" width="100%">

# ngx-schema-to-code

## 🌟Overview
Ngx-schema-to-code is an Angular Schematic designed to automate the creation of complete boilerplate code for 
CRUD (Create, Read, Update, Delete) operations. It uses a JSON Schema file as a blueprint to generate 
a fully functional user interface using Angular Material components. It allows to generate quick prototype for a web application for CURD operations.

It has used angular's latest features like standalone component, signal apis and zoneless application which will work with Angular 20 and above versions.  

It will create fast application prototype, which will be ready run state, without having any api implementation, with the help of json-server.  

It will create input form, grid / list with filter, services for CURD operations, routing, navigation, shared component and services etc.  

It will generate standalone code, no dependency on ngx-schema-to-code library after code generation. Generated code will fully readable and user can modify it his own way. 

Ngx-schema-to-code library is free to use and distribute. No restriction for generated code.  

## ✨Key Features
- **Automatic UI Generation:** It transforms a simple json schema into ready-to-use Angular application.
- **Angular Material Integration:** The generated code is pre-style and configure to work with Angular Material Library.
- **CURD Scaffolding:** It generates the necessary components and logic to handle basic database-like operations (creating, editing, viewing, deleting data) based on the schema definitions.
- **Boilerplate Reduction:** Its primary goal is to save developers time and speedily generate the application prototype.
- **Latest Angular Features:** It's used all stable latest features like standalone component, signal apis and zoneless application etc.
- **Restful API:** Its use restful API approach to implement services to call api.
- **Ready-to-Run:** Generated application is ready to run and test CURD functionality with json-server.

You can generate CURD code for new application or existing one. You can run it one or more times with same or 
different json schema.    
Ngx-schema-to-code will work on Angular 20, 21 and above versions.  

**While working with existing angular application keep backup first, it may be overwrite existing files and folders.**  

## ⚙️Installation

Install the angular cli
```bash
npm install -g @angular/cli
```
create an angular project
```bash
ng new my-project
```
go to my-project root folder and add angular material
```bash
cd my-project
ng add @angular/material
```
install angular material moment adapter 
If you have angular ^20.x.x use
```bash
npm install @angular/material-moment-adapter@20.2.14
```
else
```bash
npm install @angular/material-moment-adapter
```
Install json-server to test CURD operations.
```bash
npm install json-server --save-dev
```
Now add ngx-schema-to-code do not use ~~npm install ngx-schema-to-code~~
```bash
ng add ngx-schema-to-code
```
Remove the unwanted code from app.html, leave only **router-outlet** html tag.
    
## 💡How to Use

Create a json schema file as specified in [json-schema][json-schema] or you can copy [sample employee schema][employee-json], modify it, save in projects root folder.
```bash
ng generate ngx-schema-to-code:curd <fileName.extention>
```

run following script to start json server.
```bash
npm run api
```
open another terminal or command prompt and run the angular application.
```bash
ng serve --open
```
Add record using + add icom and test all CURD functionalities. Once your apis got implemented only change api url in services. We have use id (string) as primary key for entities, you need change it as per your database / api implemention.  

**Rule for create a json schema file.**
A json schema file can contains multiple entities with many properties.  
Only array and group type can have nested properties. Only one level nesting.  
Entity name, property name should be start with letters can contains letters, numbers and underscoure only, should not contain any spaces.  
inptuType **select, radio and array->checkbox** required to have a subproperty **options** or **optionValues**  or **source**.  
Subproperty(metadata) **dataType** is required.  
**inputType**, if not provided it will define on base of the datytype.  
**displayName**, will be use in grid / list, if not provided then auto generate it.  
**label**, will be use in input forms if not provided then displayName will be use.  

## 🪲 [Bug Reporting][bug-reporting]

## 📒 Documentation

  | Official site www.schematocode.com |  |
  |------------------------------------|--|
  | [Overview][overview] | [Installation][installation] |
  | [Json Schema][json-schema] | [How to Use][how-to-use] |
  | [Entity][entity] | [Property][property] |
  | [Primary/Unique Key][primary-key] | [Date Types][data-types] |
  | [Input Types][input-types] | [Properties][properties] |
  | [Api Integration][api-integration] | [Array][array] |
  | [Boolean][boolean] | [Checkbox][checkbox] |
  | [Checkbox Group][checkbox-group] | [Date][date] |
  | [Email][email] | [File][file] |
  | [Group][group] | [Image][image] |
  | [Number][number] | [Options][options] |
  | [Radio][radio] | [Select][select] |
  | [SlideToggle][slide-toggle] | [String][string] |
  | [Text][text] | [Textarea][textarea] |
  | [Validation][validation] | [Sample employee.json file][employee-json] |

[www.schematocode.com]: http://www.schematocode.com/
[overview]: http://www.schematocode.com/ngx-schema-to-code
[installation]: http://www.schematocode.com/ngx-schema-to-code/installation
[json-schema]: http://www.schematocode.com/ngx-schema-to-code/json-schema
[how-to-use]: http://www.schematocode.com/ngx-schema-to-code/how-to-use
[entity]: http://www.schematocode.com/ngx-schema-to-code/entity
[property]: http://www.schematocode.com/ngx-schema-to-code/property
[primary-key]: http://www.schematocode.com/ngx-schema-to-code/primary-key
[data-types]: http://www.schematocode.com/ngx-schema-to-code/data-types
[input-types]: http://www.schematocode.com/ngx-schema-to-code/input-types
[properties]: http://www.schematocode.com/ngx-schema-to-code/properties
[api-integration]: http://www.schematocode.com/ngx-schema-to-code/api-integration
[array]: http://www.schematocode.com/ngx-schema-to-code/array
[boolean]: http://www.schematocode.com/ngx-schema-to-code/boolean
[checkbox]: http://www.schematocode.com/ngx-schema-to-code/checkbox
[checkbox-group]: http://www.schematocode.com/ngx-schema-to-code/checkbox-group
[date]: http://www.schematocode.com/ngx-schema-to-code/date
[email]: http://www.schematocode.com/ngx-schema-to-code/email
[file]: http://www.schematocode.com/ngx-schema-to-code/file
[group]: http://www.schematocode.com/ngx-schema-to-code/group
[image]: http://www.schematocode.com/ngx-schema-to-code/image
[number]: http://www.schematocode.com/ngx-schema-to-code/number
[options]: http://www.schematocode.com/ngx-schema-to-code/options
[radio]: http://www.schematocode.com/ngx-schema-to-code/radio
[select]: http://www.schematocode.com/ngx-schema-to-code/select
[slide-toggle]: http://www.schematocode.com/ngx-schema-to-code/slide-toggle
[string]: http://www.schematocode.com/ngx-schema-to-code/string
[text]: http://www.schematocode.com/ngx-schema-to-code/text
[textarea]: http://www.schematocode.com/ngx-schema-to-code/textarea
[validation]: http://www.schematocode.com/ngx-schema-to-code/validation
[employee-json]: http://www.schematocode.com/ngx-schema-to-code/sample/employee-json
[bug-reporting]: https://github.com/ngx-schema-to-code/ngx-schema-to-code/issues
