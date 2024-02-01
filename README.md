# MVP
Model View Presenter

![mvp-clean](https://github.com/NrupParikh/MVP/assets/108717119/68400355-3881-40e7-9e2f-1f099a19cf81)


### Why
- Seperation of Concern
- Easy to test each layer

- Presentation Layer > UseCase (Model) > Domain Layer (Handle request comes from Presentation and retrive data from Data Layer) > Data Layer (DB or API Singletons)
- UI > UserCase > Domain >Data [ db or API ]

### For What

- Presentation Layer : Know about UI , Android Related
- Domain Layer : Know about Plain Java object. Bussiness entity
- Data Layer : DB and API Related

### Dependancy
- Presentation Layer depend on Domain Layer, Domain Layer depend on Data Layer
- It is transitive. Means, Presentation Layer know about Domain Layer, Domain Layer know about Data Layer but Data Layer don't know about Domain Layer and Domain Layer don't know about Presentation Layer

- We make request from Presentation Layer. Ex. button click
- It go to Domain layer then Data layer and get data from it and pass back to our UI
- Presenter handle everything in background using AsyncTask or RxJava  (Asyncronous) and post on UI
- Model called as UseCase or Interactor, which represent app related bussiness case. Not to domain specific.
- Domain layer handle the request comes from Presentaiton layer and return the data read from Datra Layer
- Data layer contains DB or API related singletons

### Reference

https://www.youtube.com/watch?v=btyF_Zl7uAk
