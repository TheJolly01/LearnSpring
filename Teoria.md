# SPRING

## INTRODUZIONE
Spring è un framework open source nato con l'intento di gestire la complessità nello sviluppo di applicazioni enterprise
È un framwork leggeto e facile da integrare con altri framework esistenti. In più offre vari strumenti atti a gestire l'intera complessità di un progetto software.
Offre un approccio molto semplificato alla maggior parte dei problemi ricorrenti nello sviluppo software.

Uno dei principali vantaggi di Spring è quello di poter escludere le parti del framweork non necessarie all'applicazione, grazie all'architettura modulare di Spring, composta da 5 livelli

- Core Container
- Data Access/Integration
- Spring AOP
- Web
- Testing

### Core Container
Rappresenta la parte principale di Spring e sopra di esso è costruito tutto il framework.

#### Moduli

I moduli <b>Core</b> e <b>Beans</b> sono responsabili delle funzionalità di Inversion Of Control (IoC) e Dependency Injection, e hanno come compito la creazione, gestione e manipolazione di oggetti di qualsiasi natura, che vengono detti beans.

Il modulo <b>context</b> estende i servizi basilari del Core aggiungendo funzionalità tipiche di un moderno framework

Il modulo <b>Expression Language</b> fornisce un potente linguaggio per interrogare e modificare oggetti a runtime.

### Data Access/Integration
Fornisce un livello di astrazione per l'accesso ai dati mediante tecnologie eterogenee tra loro. Questo modulo tende a nascondere la complessità delle API di accesso ai dati, semplificando ed uniformando quelle che sono le problematiche legate alla gestione delle connessioni, delle transazioni e delle eccezzioni.

### Spring AOP
Aggiunge al framework la funzionalità della programamzione <b>Aspect Oriented</b>. Offre dunque un modo nuovo di programmare che porta notevoli vantaggi in tutte quelle operazioni che sono trasversali tra più oggetti.

### Web
È responsabile delle caratteristiche Web del framework. Oltre alle funzionalità basilari, per la creazione di applicazioni Web, questo livello mette a disposizione un'implementazione del pattern MVC realizzando lo Spring MVC Framework, configurabile attraverso delle Strategy, può operare sia in contesti servlet che portlet e può essere utilizzato con numerose tecnologie di view.

### Testing
Un'altra delle caratteristiche di Spring è il supporto al testing. Questo livello mette a disposizione un ambiente molto potente per il test delle componenti Spring, grazie anche alla sua integrazione con JUnit e TestNG e alla presenza di Mock objects per il testing del codice in isolamento.


## Introduzione a IoC
IoC è l'acrononimo di Inversion of Control, ed è un principio architettetturale basato sul concetto di invertire il controllo del flusso di sistema (Control Flow) rispetto alla programmazione tradizionale. Questo principio è molto utilizzato nei framework e ne rappresneta una delle caratteristiche basilari che li distingue dalle API.

Normalmente la logica di tale flusso è definita esplicitamente dallo sviluppatore, mentre IoC inverte il control flow facendo in modo che sia il framework ad occuparsi di questi aspetti. Questo principio è anche conosciuto come Hollywood Principle ("Non chiamarci, ti chiameremo noi")

## Dependency Injection
L'idea alla base della DI è quella di avere un componente esterno (assembler) che si occupa della creazione degli oggetti e delle loro relative dipendenze e di assemblarle mediante l'utilizzo dell'injection.
Esistono 3 forme di injection:
- Constructor Injection, dove la dipendenza viene iniettata tramite l'argomento del costruttore
- Setter Injection, dove la dipendenza viene inettatta tramite metodo set
- Interface Injection che si basa sul mapping tra interfaccia e relativa implementazione

La DI può essere realizzata in molteplici modi, come utilizzo di una factory.

### Container
Un modo migliore per poter lavorare con la DI è quello di utilizzare come assembler un IoC Container in grado di compiere operazionio di injection
Un container è un componente esterno che si prende carico di una serie di compiti esonerando così lo svliluppatore dal preoccuparsene. Uno IoC Container non è altro che un container specializzato nella DI, che è in grado di compiere opportune operazioni di injection

## IoC Container
Fornisce un contesto altamente configurabile per la creazione e risoluzione delle dipendenze che qui vengono chiamati bean (NON SONO I JAVA BEAN)

In Spring un bean non deve aderire a nessun tipo di contratto e può essere rappresentato da una qualunque classe Java

IoC è realizzato da due interfacce:
- BeanFactory, che definisce le funzionalità di base per la gestione dei bean
- ApplicationContext, che estende queste funzionalita basilari aggiungendone altre tipicamente enterprise come ad esempio la gestione degli eventi, l'internazionalizzazione e l'integrazione con AOP










