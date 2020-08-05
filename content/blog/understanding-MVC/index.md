---
title: Understanding MVC
date: "2020-08-05T10:48:06.750Z"
description: ""
---

MVC stands for Model-View-Controller. The Model View Controller pattern is an architectural design pattern commonly used in software development for several reasons.
One of which is that it promotes separation of concerns between each part.

### Model

The Model is concerned with handling data concerns, specifically the data and the CRUD operations that will be performed on the data.
These operations are Create, Read, Update and Delete operations. It speaks only with the controller from which it gets data operation requests.
The model does not necessarily have to interface with an actual database, but it __*has*__ to manage the data, since it is concerned with the data access layer in the architecture.

### View

The View is the presentation layer. It is concerned with displaying or presenting data to the user and receiving user interactions as well.
The view is not aware of the Model, in fact it doesn't need to know that it exists. It only receives data to be displayed from the controller and displays that to the user.
It also receives input from the user via user interactions and it relays this to the Controller.

### Controller

The Controller handles receiving user requests and deciding what to do with them. Its primary responsibility is to interface between the model and the view.
It receives user input from the view and it is responsible for doing something with that input, for instance if the user has requested to see a list of patients in a hospital management system,
then the controller receives this request from the view and "asks" the model for the required data, this data is subsequently operated on and passed back to the View in a form that the View understands.

## Benefits of MVC

In general, the View and the Model are independent of themselves and do not necessarily need to know that either of them exists. They don't even need to know their inner workings.
The Controller is the only piece that is aware of both of them and acts as a middle man.
This means that each layer in the architecture is responsible for one function and one function only. Also the MVC pattern prevents tight coupling within the application,
since each part is independent of the other. For instance, the model doesn't even need to know the view exists and vice versa.

The key benefits of the MVC pattern is that it:

- promotes the Single Responsibility Principle
- ensures separation of concerns
- prevents tight coupling between constituent parts of the application

## Conclusion

MVC is not a framework, it is a design pattern. MVC is almost everywhere, and it is a design pattern that is heavily employed in designing the architecture of client facing applications and modern web application frameworks.
It is so common that almost every UI library employs some form of MVC architecture - think Ember, Vue, Angular, React.
The truth about the MVC pattern is that it is a pattern and can be used in any kind of application, even command-line applications.

Since MVC is a pattern, it is often adapted to suit specific use cases. Nothing is set in stone and depending on individual application specific implementation,
it is possible to see different variations of the MVC pattern.
