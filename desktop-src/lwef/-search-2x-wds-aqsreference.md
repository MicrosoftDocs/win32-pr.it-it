---
title: Sintassi di ricerca avanzata
description: La sintassi di query avanzata (AQS) viene utilizzata da Microsoft Windows Desktop Search (WDS) per aiutare gli utenti e i programmatori a definire e restringere meglio le ricerche.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: bd00821e60c8d950a7ec384b62d7ff062066f224
ms.sourcegitcommit: 8bba855bfee06d018edb16c1af70fa4d4344445b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "106299497"
---
# <a name="advanced-query-syntax"></a>Sintassi di ricerca avanzata

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

La sintassi di query avanzata (AQS) viene utilizzata da Microsoft Windows Desktop Search (WDS) per aiutare gli utenti e i programmatori a definire e restringere meglio le ricerche. L'uso di AQS è un modo semplice per limitare le ricerche e fornire migliori set di risultati. È possibile limitare le ricerche con i parametri seguenti:

-   Tipi di file: cartelle, documenti, presentazioni, immagini e così via.
-   Archivi di file: database e percorsi specifici.
-   Proprietà file: dimensioni, data, titolo e così via.
-   Contenuto del file: parole chiave come "risultati del progetto", "AQS", "Blue Suede Shoes" e così via.

Inoltre, i parametri di ricerca possono essere combinati usando gli operatori di ricerca. Nella parte restante di questa sezione vengono illustrati la sintassi di query, i parametri e gli operatori e il modo in cui possono essere combinati per offrire risultati di ricerca mirati. Le tabelle descrivono la sintassi da utilizzare con WDS, nonché le proprietà su cui è possibile eseguire query per ogni tipo di file visualizzato nella finestra Risultati **ricerca desktop di Windows** .

## <a name="desktop-search-syntax"></a>Sintassi di ricerca desktop

Una query di ricerca può includere una o più parole chiave, con operatori booleani e criteri facoltativi. Questi criteri facoltativi possono restringere una ricerca basata sugli elementi seguenti:

-   Ambito o archivio dati in cui risiedono i file
-   Tipi di file
-   Proprietà gestite dei file

I criteri facoltativi, descritti in modo più dettagliato dopo, usano la sintassi seguente:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Si supponga che un utente desideri cercare un documento contenente la frase "ultimo trimestre", creato da John o Joanne, e che l'utente abbia salvato nella cartella documenti. La query potrebbe essere simile alla seguente:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Ambito: posizioni e archivi dati

Gli utenti possono limitare l'ambito delle proprie ricerche a percorsi di cartelle o archivi dati specifici. Se, ad esempio, si utilizzano più account di posta elettronica e si desidera limitare una query a Microsoft Outlook o Microsoft Outlook Express, è possibile `store:outlook` utilizzare `store:oe` rispettivamente o.



| Limita la ricerca per archivio dati | Uso              | Esempio                                  |
|-------------------------------|------------------|------------------------------------------|
| Desktop                       | desktop          | Archivio: desktop                            |
| File                         | files            | Archivio: file                              |
| Outlook                       | Outlook          | Archivio: Outlook                            |
| Outlook Express               | OE               | Archivio: OE                                 |
| Cartella specifica               | FolderName o in | FolderName: documenti o in: documenti |



 

Se si dispone di un gestore di protocollo per eseguire la ricerca per indicizzazione di archivi personalizzati, ad esempio Lotus Notes, è possibile usare il nome dell'archivio o del gestore del protocollo per l'archivio. Se, ad esempio, è stato implementato un gestore di protocollo per includere un archivio dati Lotus Notes come "note", la sintassi della query sarà `store:notes` .

### <a name="common-file-kinds"></a>Tipi di file comuni

Gli utenti possono anche limitare le proprie ricerche a specifici tipi di file, chiamati tipi di file. La tabella seguente elenca i tipi di file e offre esempi della sintassi usata per cercare questi tipi di file.



| Per limitare il tipo di file:       | Uso              | Esempio                        |
|---------------------------------|------------------|--------------------------------|
| Tutti i tipi di file                  | tutto       | Tipo: tutto                |
| Comunicazioni                  | (DIP) interno   | Tipo: comunicazioni            |
| Contatti                        | contatti         | Kind: contatti                  |
| Posta elettronica                          | email            | Tipo: posta elettronica                     |
| Conversazioni di messaggistica immediata | messaggistica immediata               | Tipo: im                        |
| Riunioni                        | riunioni         | Tipo: riunioni                  |
| Attività                           | attività            | Tipo: attività                     |
| Note                           | di HDInsight            | Kind: note                     |
| Documenti                       | docs             | Tipo: docs                      |
| Documenti di testo                  | text             | Kind: testo                      |
| Fogli di calcolo                    | fogli     | Tipo: fogli di calcolo              |
| Presentazioni                   | presentazioni    | Tipo: presentazioni             |
| Musica                           | music            | Kind: musica                     |
| Immagini                        | pics             | Kind: pics                      |
| Video                          | videos           | Kind: video                    |
| Cartelle                         | cartelle          | Kind: cartelle                   |
| Nome cartella                     | FolderName o in | FolderName: docs o in: docs |
| Preferiti                       | Preferiti        | Kind: Preferiti                 |
| Programmi                        | programmi         | Kind: programmi                  |



 

### <a name="boolean-operators"></a>Operatori booleani

È possibile combinare le parole chiave di ricerca e le proprietà del file per ampliare o restringere una ricerca con gli operatori. Nella tabella seguente vengono illustrati gli operatori comuni utilizzati in una query di ricerca.



| Parola chiave/simbolo  | Esempio                                              | Funzione                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | sicurezza sociale<br/>                        | Trova elementi che contengono *Social*, ma non di *sicurezza*.<br/>                                              |
|                 | sicurezza sociale<br/>                           | Trova elementi che contengono *Social Network* e *sicurezza*.<br/>                                              |
| OR              | social networking o sicurezza<br/>                         | Trova elementi che contengono *Social* networking o *sicurezza*.<br/>                                                    |
| Virgolette | "Social Security"<br/>                          | Trova gli elementi che contengono la frase esatta *sulla sicurezza sociale*.<br/>                                        |
| Parentesi     | (Social Security)<br/>                          | Trova gli elementi che contengono *Social* e *Security* in qualsiasi ordine.<br/>                                      |
| >            | Data: >11/05/04<br/> Dimensioni: >500<br/>  | Trova gli elementi con una data successiva al 11/05/04. <br/> Trova elementi con una dimensione maggiore di 500 byte.<br/> |
| <            | Data: <11/05/04 <br/> Dimensioni: <500<br/> | Trova gli elementi con una data precedente alla 11/05/04. <br/> Trova elementi con una dimensione inferiore a 500 byte.<br/>   |
| ..              | Data: 11/05/04.. 11/10/04<br/>                    | Trova gli elementi con una data che inizia il 11/05/04 e termina con 11/10/04.<br/>                               |



 

> [!Note]
>
> Gli operatori **not** e **or** devono essere in lettere maiuscole e non possono essere combinati in un'unica query (ad esempio, `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Proprietà booleane

Alcuni tipi di file consentono agli utenti di cercare i file usando le proprietà booleane, come descritto nella tabella seguente.



| Proprietà       | Esempio                   | Funzione                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| è: allegato  | report: allegato      | Trova gli elementi con allegati che contengono il *report*. Uguale a `isattachment:true`.                           |
| IsOnline      | report di linea: true      | Trova gli elementi online e che contengono il *report*.                                                         |
| IsRecurring   | IsRecurring report: true   | Trova gli elementi che sono ricorrenti e che contengono il *report*.                                                       |
| con flag:     | flag di segnalazione: true     | Trova gli elementi contrassegnati (revisione, completamento, ad esempio) e che contengono il *report*.                       |
| IsDeleted     | report da eliminare: true     | Trova gli elementi contrassegnati come eliminati (ad esempio, cestino o elementi eliminati) e che contengono *report*. |
| IsCompleted   | il report è stato completato: false  | Trova gli elementi che non sono contrassegnati come completi e che contengono il *report*.                                        |
| hasattachment: | HasAttachment report: true | Trova gli elementi contenenti il *report* e con allegati                                                          |
| HasFlag       | HasFlag report: true       | Trova gli elementi contenenti il *report* e i flag.                                                                |



 

### <a name="dates"></a>Date

Oltre a eseguire ricerche su date e intervalli di date specifici usando gli operatori descritti in precedenza, AQS consente valori relativi alla data, ad esempio `today` , `tomorrow` o, e al `next week` giorno (come `Tuesday` o `Monday..Wednesday` ) e ai valori month ( `February` ).



| Relativo a:    | Esempio di sintassi                                                                                                                         | Risultato                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Giorno             | Data: oggi<br/> Data: domani<br/> Data: ieri<br/>                                                               | Trova gli elementi con la data odierna.<br/> Trova gli elementi con la data di domani.<br/> Trova gli elementi con la data di ieri. <br/>                                                                                                                                                                                                                     |
| Settimana/mese/anno | Data: settimana corrente<br/> Data: Ultima settimana<br/> Data: mese successivo<br/> Data: ultimo mese<br/> Data: anno prossimo <br/> | Trova gli elementi con una data che rientra nella settimana corrente.<br/> Trova gli elementi con una data che rientra nella settimana precedente.<br/> Trova gli elementi con una data che rientra nella settimana successiva.<br/> Trova gli elementi con una data che rientra nel mese precedente.<br/> Trova gli elementi con una data che rientra nell'anno imminente. <br/> |



 

## <a name="properties-by-file-kind"></a>Proprietà per tipo di file

Gli utenti possono cercare proprietà specifiche di diversi tipi di file. Alcune proprietà, ad esempio le dimensioni dei file, sono comuni a tutti i file, mentre altre sono limitate a un tipo specifico. Il numero di diapositive, ad esempio, è specifico per le presentazioni. Nelle tabelle seguenti vengono elencate le proprietà in base al tipo di file.

### <a name="file-kind-everything"></a>Tipo di file: tutto

Si tratta di proprietà comuni a tutti i tipi di file. Per includere tutti i tipi di file in una query, la sintassi è:

`kind:everything <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà       | Uso                      | Esempio                        |
|----------------|--------------------------|--------------------------------|
| Titolo          | titolo, soggetto o informazioni  | title: "trimestrale Financial"    |
| Stato         | status                   | stato: completato                |
| Data           | data                     | Data: Ultima settimana                 |
| Data modifica  | DateModified o modificato | modificato: Ultima settimana             |
| Importanza     | importanza o priorità   | importanza: elevata                |
| Dimensione           | size                     | Dimensioni: > 50                   |
| Eliminata        | eliminata o eliminata     | con eliminazione: true                 |
| Allegato  | associazione             | alconnessione: true              |
| A             | a o toName             | a: Bob                         |
| Cc             | CC o ccname             | CC: John                        |
| Company        | company                  | società: Microsoft              |
| Location       | posizione                 | Località: "sala riunioni 102" |
| Category       | category                 | Categoria: business              |
| Parole chiave       | keywords                 | Parole chiave: "proiezioni delle vendite"   |
| Album          | album                    | album: "Fly by Night"           |
| Nome file      | nome file o file         | nome file: Resume              |
| Genre          | genre                    | genere: Rock                     |
| Autore         | autore o             | autore: "Stephen King"          |
| Persone         | utenti o con           | con: (Sonja o David)          |
| Cartella         | cartella, in o percorso    | cartella: download               |
| Estensione file | EXT o fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Attachment

Si tratta di proprietà comuni agli allegati. Per limitare la ricerca solo agli allegati, la sintassi è:

`kind:attachment <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà | Uso            | Esempio                  |
|----------|----------------|--------------------------|
| Persone   | utenti o con | persone: John o con: John |



 

### <a name="contacts"></a>Contatti

Si tratta di proprietà comuni ai contatti. Per limitare la ricerca solo ai contatti, la sintassi è:

`kind:contacts <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà              | Uso                 | Esempio                            |
|-----------------------|---------------------|------------------------------------|
| Posizione             | jobtitle            | JobTitle: CFO                       |
| Indirizzo IM            | imindirizzo           | imindirizzo: Giorgio\_doe@msn.com        |
| Telefono dell'assistente     | assistantsphone     | assistantsphone: 555-3323           |
| Nome assistente        | AssistantName consente       | AssistantName: Paul                 |
| Profession            | professione          | professione: idraulico                 |
| Nome alternativo              | nickname            | nome alternativo: Tex                       |
| Coniuge                | coniuge              | sposo: Debbie                      |
| Città del business         | businesscity        | businesscity: Seattle               |
| Codice postale aziendale  | businesspostalcode  | businesspostalcode: 98006           |
| home page aziendali    | businesshomepage    | BusinessHomePage: www. Microsoft. com |
| Numero di telefono di callback | callbackphonenumber | callbackphonenumber: 555-555-2121   |
| Telefono auto             | Carphone            | Carphone: 555-555-2121              |
| Children              | figli            | elementi figlio: Timmy                     |
| Nome            | firstname           | Nome: John                     |
| Cognome             | lastname            | Cognome: Doe                       |
| Fax Home              | homefax             | homefax: 555-555-2121               |
| Nome del Manager        | ManagerName        | ManagerName: John                  |
| Cercapersone                 | pager               | cercapersone: 555-555-2121                 |
| Telefono ufficio        | BusinessPhone       | BusinessPhone: 555-555-2121         |
| Telefono abitazione            | homePhone           | HomePhone: 555-555-2121             |
| Cellulare          | mobilephone         | mobilephone: 555-555-2121           |
| Office                | office              | Office: esempio                      |
| Dell'anniversario           | dell'anniversario         | anniversario: 1/1/06                 |
| Data di nascita              | compleanno            | compleanno: 1/1/06                    |
| Pagina Web              | pagina Web             | pagina Web: www. Microsoft. com          |



 

> [!Note]
>
> I numeri di telefono vengono indicizzati come immessi. Se, ad esempio, un utente non include un paese o un codice di area quando immette il numero di telefono, gli utenti non saranno in grado di individuare un contatto in caso di ricerca con il codice paese o area nel numero di telefono.

 

### <a name="communications"></a>Comunicazioni

Si tratta di proprietà comuni alle comunicazioni. Per limitare la ricerca solo alle comunicazioni, la sintassi è:

`kind:communications <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà       | Uso                           | Esempio                         |
|----------------|-------------------------------|---------------------------------|
| Da           | da o dall'organizzatore             | da: Giorgio                       |
| Ricevuto       | ricevute o inviate              | Inviato: ieri                  |
| Oggetto        | oggetto o titolo              | oggetto: "trimestrale Financial"   |
| Con allegato | HasAttachments, HasAttachment | HasAttachment: true              |
| Allegati    | allegati o allegati     | attachment:presentation.ppt     |
| Bcc            | Ccn, bccname o bccaddress    | Ccn: Dave                        |
| Indirizzo CC     | ccaddress o CC               | ccaddress: Giorgio\_doe@outlook.com |
| Flag di completamento | followupflag                  | followupflag: 2                  |
| Scadenza       | DueDate o scadenza                | scadenza: Ultima settimana                   |
| Lettura           | lettura o lettura                | is: Read                         |
| Completato   | IsCompleted                   | è: completato                    |
| Incompleto     | Incomplete o incomplete    | is: incompleto                   |
| Con flag       | HasFlag o con contrassegno          | con: Flag                        |
| Duration       | duration                      | Durata: > 50                |



 

### <a name="calendar"></a>Calendario

Si tratta di proprietà comuni ai calendari. Per limitare la ricerca solo ai calendari, la sintassi è:

`kind:calendar <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà  | Uso                      | Esempio          |
|-----------|--------------------------|------------------|
| Periodica | ricorrente o IsRecurring | is: ricorrente     |
| Organizzatore | libreria, da o da    | libreria: Debbie |



 

### <a name="documents"></a>Documenti

Si tratta di proprietà comuni ai documenti. Per limitare la ricerca solo ai documenti, la sintassi è:

`kind:documents <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà          | Uso             | Esempio                       |
|-------------------|-----------------|-------------------------------|
| Commenti          | comments        | Commenti: "necessità revisione finale" |
| Ultimo salvataggio     | LastSavedBy     | LastSavedBy: Giorgio              |
| Gestione documenti  | documentmanager | documentmanager: Giorgio          |
| Numero revisione   | RevisionNumber  | RevisionNumber: 1.0.3          |
| Formato documento   | DocumentFormat  | documentformat: MIMETYPE       |
| Data ultima stampa | datelastprinted | datelastprinted: Ultima settimana     |



 

### <a name="presentation"></a>Presentazione

Si tratta di proprietà comuni alle presentazioni. Per limitare la ricerca solo alle presentazioni, la sintassi è:

`kind:presentation <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà    | Uso        | Esempio           |
|-------------|------------|-------------------|
| Conteggio diapositive | slidecount | SlideCount: >20 |



 

### <a name="music"></a>Musica

Si tratta di proprietà comuni ai file musicali. Per limitare la ricerca solo alla musica, la sintassi è:

`kind:music <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà | Uso                | Esempio                  |
|----------|--------------------|--------------------------|
| Velocità in bit | bitrate, velocità      | velocità in bit: 192              |
| Artista   | artista, da o da | artista: John Singer       |
| Duration | duration           | Durata: 3               |
| Album    | album              | album: "Greatest Hits"    |
| Genre    | genre              | genere: Rock               |
| Track    | track              | Track: 12                 |
| Year     | anno               | anno: > 1980 < 1990 |



 

### <a name="picture"></a>Immagine

Si tratta di proprietà comuni alle immagini. Per limitare la ricerca solo alle immagini, la sintassi è:

`kind:picture <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà     | Uso         | Esempio               |
|--------------|-------------|-----------------------|
| Marca fotocamera  | cameramake  | cameramake: esempio     |
| Modello di fotocamera | CameraModel | CameraModel: esempio    |
| Dimensioni   | dimensions  | Dimensioni: 8X10       |
| Orientamento  | orientation | orientamento: orizzontale |
| Data di inizio   | DateTaken   | DateTaken: ieri   |
| Larghezza        | width       | Larghezza: 1600            |
| Altezza       | altezza      | Altezza: 1200           |



 

### <a name="video"></a>Video

Si tratta di proprietà comuni ai video. Per limitare la ricerca solo ai video, la sintassi è:

`kind:video <property>:<value>`

dove `<property>` è una proprietà elencata di seguito ed `<value>` è il termine di ricerca specificato dall'utente.



| Proprietà | Uso           | Esempio                                |
|----------|---------------|----------------------------------------|
| Nome     | nome, oggetto | Nome: "famiglia Vacation to the Beach 05" |
| Interno      | EXT, fileext  | ext:.avi                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Tipi percepiti](-search-2x-wds-perceivedtype.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> <dt>

[Chiamata di WDS dalla riga di comando](-search-2x-wds-fromcommandline.md)
</dt> <dt>

[Chiamata di WDS da pagine Web](-search-2x-wds-browserhelpobject.md)
</dt> </dl>

 

 





