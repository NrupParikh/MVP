### What is software Architecture
- About what the system does, what we are buiding
- High level abstraction of Software Design
- Represent biger picture
- Choice of frameworks, standards and High level principals
  
### What is Software Design
- About how we are building
- Smaller picture
- How to plan and structure your code, how to implement

### What is Clean Architecture
- Seperation of concerns
- It is Multi Layered
- It is Independent of framework, database, Layers, Interfaces
- It is testable by Layers
- They are testable
- Dependecy are from Lower level to Higher level only
- Ex. Presentation depend on Domain, Domain dependent on Data Layer. Data Layer depend on Modules. But not reversable.
  
# MVP
Model View Presenter

![mvp-clean](https://github.com/NrupParikh/MVP/assets/108717119/68400355-3881-40e7-9e2f-1f099a19cf81)


### Clean Architecture Layers

![clean_architecture_layers](https://github.com/NrupParikh/MVP/assets/108717119/1b1e5f28-f21b-49b3-b22a-5f64ba998279)

### Clean Architecture

![clean_architecture](https://github.com/NrupParikh/MVP/assets/108717119/dfe069bc-4f3c-4957-a50d-5840bed9a160)


### Why to use MVP ?
- Seperation of Concern
- Easy to test each layer

- Presentation Layer > UseCase (Model) > Domain Layer (Handle request comes from Presentation and retrive data from Data Layer) > Data Layer (DB or API Singletons)
- UI > UserCase > Domain >Data [ db or API ]

### Which Layer For What in MVP Clean Architecture?

- Presentation Layer : Know about UI , Android Related.  UI / View / Fragment / Activity (java or Kotlin class)
  - Presenter handle everything in background using (RxJava or AsyncTask) and transfer output on UI
  - Model (UseCase or Interactor) : Represent application specific flow. Not for domain. What the presentation layer does.
- Domain Layer : Know about Plain Java object. Bussiness entity. Handle request comes from Presentation Layer. Fetch data from Data Layer and pass to Presentation Layer.
- Data Layer : DB and API Related. Has singleton classes.
- Each layer can have Test case (Seperation of Concern)
  
### Dependancy of Layers
- Presentation Layer depend on Domain Layer, Domain Layer depend on Data Layer
- It is transitive. Means, Presentation Layer know about Domain Layer, Domain Layer know about Data Layer but Data Layer don't know about Domain Layer and Domain Layer don't know about Presentation Layer

### How it works?
- We make request from Presentation Layer. Ex. button click
- It go to Domain layer then Data layer and get data from it and pass back to our UI
- Presenter handle everything in background using AsyncTask or RxJava  (Asyncronous) and post on UI
- Model called as UseCase or Interactor, which represent app related bussiness case. Not to domain specific.
- Domain layer handle the request comes from Presentaiton layer and return the data read from Datra Layer
- Data layer contains DB or API related singletons
- Each layer can have Test class to run seperately

### Reference

https://www.youtube.com/watch?v=btyF_Zl7uAk
