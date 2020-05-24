
# Angular

## Introduction
Hello. Today I’ll tell you about one of the most popular and widespread framework Angular on the example of small application and try to persuade you to apply this powerful and extensively benefited  instrument in your practice.  

## What is Angular  
The name Angular derives simply from the fact that the HTML tags are enclosed by angle brackets.
Angular is a TypeScript-based open-source web application framework led by the Angular Team at Google.
It is designed specifically for creating dynamic web applications. With this framework, you can develop front-end based applications without having to use other plug-ins or frameworks. Angular is used to develop client-side applications, especially Single-Page applications. It has a series of features and tools that simplify the development of the applications themselves while simultaneously guaranteeing excellent performance results.  
As can be seen from the slide many  companies use Angular framework.
Companies that use Angular: Autodesk, MacDonald’s, UPS, Apple, Adobe, GoPro, YouTube, Paypal, Nike, Google, Telegram, etc.
Framework has official github repository(https://github.com/angular), where you can find the source files themselves, as well as some additional information.

## History  
The first version on Angular was released in 2010 with the name of “Angular JS”. The framework, a JavaScript-based was intended to decouple an application’s logic from DOM manipulation.
AngularJS became popular very quickly and received a lot of traction.  In 2016 Angular 2 was published. It’s no coincidence the framework received a new name: actually, it was fully re-written and redesigned, while many concepts were reconsidered. One of the main features of Angular 2 was the ability to develop for multiple platforms: web, mobile, and native desktop (whereas AngularJS has no mobile support out of the box). 
Also Angular is based on TypeScript while AngularJS is based on JavaScript. Angular has also benefits of ES6 like: lambda operators, iterators or reflection’s mechanism.
The current version of Angular 9 is released on February 6, 2020.  

## Architecture  
Each  Angular application is built in accordance with a specific architecture.  
The main building blocks are modules, components, templates, metadata, data binding, directives, services and dependency injection.  

# Modules  
Let’s consider the architecture of Angular on the example of this small real application, which displays 2 greetings and has plus and minus buttons to reduce and increase counter value.
One of the main features of Angular is modularity. The basic building blocks are NgModules, which provide a compilation context for components. 
An app always has at least a root module, that enables bootstrapping , and typically has many more feature modules. Other modules are linked from a root module in a process called import.  
A module is a mechanism to group components, directives, pipes and services that are related, in such a way that can be combined with other modules to create an application. Modules is used to speed up the complex app development.  
The most important properties of NgModule are imports, exports, providers, bootstrap, and declarations.
* Imports: external modules needed by the templates of this module
* Declarations: the components, directives, and pipes that belong to this NgModule
* Exports: the subset of declarations that should be visible and usable in the component templates of other NgModules.
* Providers: creators of services that this NgModule contributes to the global collection of services; they become accessible in all parts of the app 
* Bootstrap: main application view, called the root component, that hosts all other app views  

# Components  
One of the main architectural principles in Angular called Component-Based-Architecture is that an application should be composed of well encapsulated, loosely coupled components. 
Components define views (sets of screen elements) that Angular can choose among and modify according to the program logic and data. 
Any app should have at least one component, known as a root component that contains all other components.
Angular follows MVC pattern. (The Model-View-Controller (MVC)  is an architectural pattern that separates an application into three main logical components Model, View, and Controller. 
Controller does processing of data from view or model its logic. 
View is component visual representation.
Our application contains one root component called app.component. Its controller apply increment and decrement methods to change value of counter. 
App.component has two hello components.
Once we created a hello component. And then we can reuse it for similar tasks. Reusability is one of the main benefits of Angular. 
Other benefits of  component-based architecture:
* readability. Consistency in coding makes reading the code a piece of cake for new developers on an ongoing project, which adds to their productivity
* unit-test friendly. Being independent of each other, the components make unit testing much easier.
* maintainability. Decoupled components are replaceable with better implementations. Simply put, it enables efficient code maintenance and update  

# Metadata 
Component contains Metadata, which tells Angular about the process of a class. Also, metadata informs the Angular of the place to take the chief building blocks that need to be specified for the component.  
Selector: A CSS selector that tells Angular to create and insert an instance of this component wherever it finds the corresponding tag in template HTML. 
TemplateUrl: The module-relative address of this component's HTML template. Alternatively, you can provide the HTML template inline, as the value of the template property.  

# Template  
Template looks like regular HTML, except that it also contains Angular template syntax, which alters the HTML based on your app's logic and the state of app and DOM data. 
In general we can say that template is a  view of component.  

# Directive  
Angular components are not more than directives with templates. 
If you need a reusable element, write a component. Directives deal with manipulating DOM elements. You can write a directive once and reuse it wherever you need that behavior. Directive changes the appearance or behavior an existing element.
By replacing, adding, or removing the elements in DOM, Structural directives can simply modify the layouts. 
To modify the behavior or appearance of an existing element, Attribute directives are used.
In our example, we use structure directive *ngFor  to change display value of counter.  

# Data Binding  
Data Binding is the important concept of Angular.It allow us to define the communication between component and view. Data Binding is passed from component to view and from view to the component.
The following diagram shows the four forms of data binding markup.  
1.	Interpolation
Interpolation is a mechanism that allows the integration of defined string values into text within HTML tags and attribute assignments in the presentation layer (view). 
2.	Property binding
 Property binding is a one-way mechanism that lets you set the property of a view element. It involves updating the value of a property in the component and binding it to an element in the view template. 
3.	Event binding
This data binding type is when information flows from the view to the component when an event is triggered. The view sends the data from an event like the click of a button to be used to update the component. 
4.	Two-way data binding
Two-way binding is a mechanism where data flows both ways from the component to the view and back. The component and view are always in sync, and changes made on either end are immediately updated both ways. Two-way binding is commonly used when dealing with forms where the user input is used to update the component’s state and vice versa. 
In application the (click) event binding calls increment and decrement methods when the user clicks a button. The {{ name}} interpolation displays the name defined as Angular. The {{ item}} interpolation displays the value of counter.  

# Service  
Services allow sharing data and logic across components and encapsulate external interactions (HTTP requests). How component get access to the service? 

# Dependency injection  
Service can be injected into a component constructor. Injection is based on Dependency injection. DI is a coding pattern in which a class receives the instances of objects it needs (called dependencies) from an external source rather than creating them itself.
We use the service in order not to store the counter in the component, but to provide access to it from anywhere in the application. We inject the service into root component, giving the component access to counter value.  

# Advantages  
Let’s have a look at the main benefits that make Angular stand out.
1.	Its a component based framework which gives a clean structure for our application. Components can easily be replaced and decoupled as well as reused in other parts of an app. In addition, component independence makes it easy to test a web app and ensure that every component works seamlessly.
2. Angular is built with TypeScript, which in turn relies on JS ES6. TypeScript fully compiles to JavaScript, but helps to eliminate common mistakes when actually typing the code. While small JavaScript projects don’t require such an enhancement, the enterprise-scale applications challenge developers to make their code cleaner and verify its quality more often. TypeScript has better navigation, autocompletion, and refactoring services.
3. The platform-agnostic philosophy
Angular was developed with the mobile-first approach in mind. The idea is to share the codebase and ultimately the engineering skillset across the web, iOS, and Android applications. You have one framework for multiple platforms.
4. Great ecosystem of third-party components. 
The popularity of Angular has resulted in the appearance of thousands of additional tools and components that can be used in Angular apps. As a result, you can get additional functionality and productivity improvements.
If the average engineer gets lost, there’s always a tool to help solve a problem that pops up.
5. Angular command-line interface (CLI)
It is probably the most beloved feature for the majority of Angular developers. It automates the whole development process making app initialization, configuration, and development as easy as possible. We install Angular CLI with npm and then use shot commands for all manipulation in you project. It not only increases code quality but also greatly facilitates development.
6. Angular Elements. 
Starting with Angular 6, developers can easily add custom elements to any web app built with React, JQuery, Vue, or any other environment.
7. Ahead-of-time compiler.
Angular’s AOT compiler converts TypeScript and HTML into JavaScript during the build process. This means that code is compiled before the browser loads your web app so that it’s rendered much faster. 
8. Support by Google.  The developers of Angular confirmed that Google will support Angular on a long-term basis. Google plans to stick with the Angular ecosystem and further develop it, trying to hold the lead positions among front-end engineering tools.
9. Detailed documentation. Angular boasts detailed documentation where developers can find all necessary information without asking their colleagues. As a result, developers can quickly come up with technical solutions and resolve emerging issues.  

# Disadvantages  
Every tool has both strong and weak sides. Angular has the following imperfections:
* Hard to learn
Most developers claim that Angular is quite complex, which is why it can be difficult for newcomers. And even though the component-based architecture makes code more readable, it’s still difficult to manage and set dependencies between components. 
* Poor SEO options
Even though the Angular team does their utmost to make Angular SEO-friendly, lots of developers still complain about poor accessibility for search crawlers.  

# Conclusion  
One last thing worth mentioning is that sometimes using Angular for an app may be overkill. If you have a small or medium-sized project without any complex user interfaces and interactions, it may be a much better idea to stick with plain old JavaScript. But Angular is likely to become the main instrument for long-term and heavy-investment projects where a steep learning curve is compensated for by stability and ongoing tech support.




