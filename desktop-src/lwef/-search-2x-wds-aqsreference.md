---
title: Sintassi di ricerca avanzata
description: La sintassi di query avanzata (AQS) viene usata da Microsoft Windows Desktop Search (WDS) per consentire a utenti e programmatori di definire e limitare meglio le ricerche.
ms.assetid: 8e55bd40-c7cf-44a6-bc18-24bc7a267779
ms.topic: article
ms.date: 05/19/2020
ms.openlocfilehash: 2daf552f8f750335abacea4b550f92bd71c91c9b2b688a387b035a8180a8b3dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601821"
---
# <a name="advanced-query-syntax"></a>Sintassi di ricerca avanzata

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows ricerca.](../search/-search-3x-wds-overview.md)

La sintassi di query avanzata (AQS) viene usata da Microsoft Windows Desktop Search (WDS) per consentire a utenti e programmatori di definire e limitare meglio le ricerche. L'uso di AQS è un modo semplice per restringere le ricerche e offrire set di risultati migliori. Le ricerche possono essere ristrette con i parametri seguenti:

-   Tipi di file: cartelle, documenti, presentazioni, immagini e così via.
-   Archivi file: database e percorsi specifici.
-   Proprietà del file: dimensioni, data, titolo e così via.
-   Contenuto del file: parole chiave come "risultati finali del progetto", "AQS", "scarpe blu in suede" e così via.

Inoltre, i parametri di ricerca possono essere combinati usando gli operatori di ricerca. Nella parte restante di questa sezione vengono illustrati la sintassi di query, i parametri e gli operatori e il modo in cui possono essere combinati per offrire risultati di ricerca mirati. Le tabelle descrivono la sintassi da usare con Servizi di distribuzione Windows, nonché le proprietà su cui è possibile eseguire query per ogni tipo di file visualizzato nella finestra dei risultati di Windows **Desktop Search.**

## <a name="desktop-search-syntax"></a>Sintassi di Desktop Search

Una query di ricerca può includere una o più parole chiave, con operatori booleani e criteri facoltativi. Questi criteri facoltativi possono restringere una ricerca in base a quanto segue:

-   Ambito o archivio dati in cui si trovano i file
-   Tipi di file
-   Proprietà gestite dei file

I criteri facoltativi, descritti più dettagliatamente di seguito, usano la sintassi seguente:

`<scope name>:<value>`

`<file kind>:<value>`

`<property name>:<value>`

Si supponga che un utente voglia cercare un documento contenente la frase "last quarter", creata da John o Johnne, e che l'utente abbia salvato nella cartella mydocuments. La query può essere simile alla seguente:

`"last quarter" author:(john OR joanne) foldername:mydocuments`

### <a name="scope-locations-and-data-stores"></a>Ambito: percorsi e archivi dati

Gli utenti possono limitare l'ambito delle ricerche a percorsi di cartelle o archivi dati specifici. Ad esempio, se si usano più account di posta elettronica e si vuole limitare una query a Microsoft Outlook o Microsoft Outlook Express, è possibile usare rispettivamente o `store:outlook` `store:oe` .



| Limitare la ricerca in base all'archivio dati | Uso              | Esempio                                  |
|-------------------------------|------------------|------------------------------------------|
| Desktop                       | desktop          | store:desktop                            |
| File                         | files            | store:files                              |
| Outlook                       | Outlook          | store:outlook                            |
| Outlook Express               | Oe               | store:oe                                 |
| Cartella specifica               | foldername o in | foldername:MyDocuments o in:MyDocuments |



 

Se è presente un gestore di protocollo per la ricerca per indicizzazione negli archivi personalizzati, ad esempio Lotus Notes, è possibile usare il nome dell'archivio o del gestore di protocollo per l'archivio. Ad esempio, se è stato implementato un gestore di protocollo per includere un archivio dati Lotus Notes come "notes", la sintassi della query sarà `store:notes` .

### <a name="common-file-kinds"></a>Tipi di file comuni

Gli utenti possono anche limitare le ricerche a tipi specifici di file, detti tipi di file. La tabella seguente elenca i tipi di file e offre esempi della sintassi usata per cercare questi tipi di file.



| Per limitare in base al tipo di file:       | Uso              | Esempio                        |
|---------------------------------|------------------|--------------------------------|
| Tutti i tipi di file                  | Tutto       | kind:everything                |
| Comunicazioni                  | (DIP) interno   | kind:communications            |
| Contatti                        | contatti         | kind:contacts                  |
| Posta elettronica                          | email            | kind:email                     |
| Conversazioni di Instant Messenger | Im               | kind:im                        |
| Riunioni                        | Riunioni         | kind:meetings                  |
| Attività                           | attività            | kind:tasks                     |
| Note                           | di HDInsight            | kind:notes                     |
| Documenti                       | docs             | kind:docs                      |
| Documenti di testo                  | text             | kind:text                      |
| Fogli di calcolo                    | Fogli     | kind:spreadsheets              |
| Presentazioni                   | presentazioni    | kind:presentations             |
| Musica                           | music            | kind:music                     |
| Immagini                        | Foto             | kind:pics                      |
| Video                          | videos           | kind:videos                    |
| Cartelle                         | cartelle          | kind:folders                   |
| Nome cartella                     | foldername o in | foldername:mydocs o in:mydocs |
| Preferiti                       | Preferiti        | kind:favorites                 |
| Programmi                        | programmi         | kind:programs                  |



 

### <a name="boolean-operators"></a>Operatori booleani

Le parole chiave di ricerca e le proprietà dei file possono essere combinate per ampliare o restringere una ricerca con operatori. Nella tabella seguente vengono illustrati gli operatori comuni usati in una query di ricerca.



| Parola chiave/simbolo  | Esempio                                              | Funzione                                                                                                       |
|-----------------|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| NOT             | social NOT security<br/>                        | Trova gli elementi che contengono *social*, ma non *la sicurezza*.<br/>                                              |
|                 | sicurezza sociale<br/>                           | Trova gli elementi che contengono *social* e *sicurezza.*<br/>                                              |
| OR              | social or security<br/>                         | Trova gli elementi che contengono *social network* o *security.*<br/>                                                    |
| Virgolette | "sicurezza sociale"<br/>                          | Trova gli elementi che contengono la frase esatta *social security.*<br/>                                        |
| Parentesi     | (sicurezza sociale)<br/>                          | Trova gli elementi che contengono *social* network *e sicurezza* in qualsiasi ordine.<br/>                                      |
| >            | date:>05/11/04<br/> size:>500<br/>  | Trova gli elementi con una data successiva al 05/11/04. <br/> Trova gli elementi con dimensioni maggiori di 500 byte.<br/> |
| <            | date:<05/11/04 <br/> size:<500<br/> | Trova gli elementi con una data precedente al 05/11/04. <br/> Trova gli elementi con dimensioni inferiori a 500 byte.<br/>   |
| ..              | date:11/05/04..11/10/04<br/>                    | Trova gli elementi con una data che inizia il 05/11/04 e termina il 10/11/04.<br/>                               |



 

> [!Note]
>
> Gli operatori **NOT** **e OR** devono essere in maiuscolo e non possono essere combinati in una query ( ad esempio `social OR security NOT retirement` ).

 

### <a name="boolean-properties"></a>Proprietà booleane

Alcuni tipi di file consentono agli utenti di cercare file usando proprietà booleane, come descritto nella tabella seguente.



| Proprietà       | Esempio                   | Funzione                                                                                                        |
|----------------|---------------------------|-----------------------------------------------------------------------------------------------------------------|
| is:attachment  | report is:attachment      | Trova gli elementi con allegati che contengono *report*. Uguale a `isattachment:true`.                           |
| isonline:      | report isonline:true      | Trova gli elementi online che contengono il *report*.                                                         |
| è ricorrente:   | report isrecurring:true   | Trova gli elementi ricorrenti che contengono *report*.                                                       |
| isflagged:     | report isflagged:true     | Trova gli elementi contrassegnati (ad esempio Review, Follow up) e che contengono *report*.                       |
| Isdeleted:     | report isdeleted:true     | Trova gli elementi contrassegnati come eliminati (Cestino o Elementi eliminati, ad esempio) e che contengono *report*. |
| Iscompleted:   | report iscompleted:false  | Trova gli elementi che non sono contrassegnati come completi e che contengono *report*.                                        |
| hasattachment: | report hasattachment:true | Trova gli elementi *contenenti report* e allegati                                                          |
| hasflag:       | report hasflag:true       | Trova gli elementi *contenenti report* e con flag.                                                                |



 

### <a name="dates"></a>Date

Oltre a eseguire ricerche in date e intervalli di date specifici usando gli operatori descritti in precedenza, AQS consente valori di data relativi (ad esempio , o ) e valori di giorno (ad esempio o ) e di `today` `tomorrow` mese ( `next week` `Tuesday` `Monday..Wednesday` `February` ).



| Relativo a:    | Esempio di sintassi                                                                                                                         | Risultato                                                                                                                                                                                                                                                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Giorno             | date:today<br/> date:tomorrow<br/> date:yesterday<br/>                                                               | Trova gli elementi con la data odierna.<br/> Trova gli elementi con la data di domani.<br/> Trova gli elementi con la data di ieri. <br/>                                                                                                                                                                                                                     |
| Settimana/mese/anno | date:this week<br/> date:last week<br/> date:next month<br/> date:past month<br/> date:coming year <br/> | Trova gli elementi con una data che rientra nella settimana corrente.<br/> Trova gli elementi con una data che rientra nella settimana precedente.<br/> Trova gli elementi con una data che rientra nella settimana successiva.<br/> Trova gli elementi con una data che rientra nel mese precedente.<br/> Trova gli elementi con una data che rientra nell'anno successivo. <br/> |



 

## <a name="properties-by-file-kind"></a>Proprietà per tipo di file

Gli utenti possono cercare proprietà specifiche di tipi di file diversi. Alcune proprietà, ad esempio le dimensioni del file, sono comuni a tutti i file, mentre altre sono limitate a un tipo specifico. Il numero di diapositive, ad esempio, è specifico per le presentazioni. Le tabelle seguenti elencano queste proprietà in base al tipo di file.

### <a name="file-kind-everything"></a>Tipo di file: Tutto

Si tratta di proprietà comuni a tutti i tipi di file. Per includere tutti i tipi di file in una query, la sintassi è:

`kind:everything <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà       | Uso                      | Esempio                        |
|----------------|--------------------------|--------------------------------|
| Titolo          | title, subject o about  | title:"Quarterly Financial"    |
| Stato         | status                   | status:complete                |
| Data           | data                     | date:last week                 |
| Data modifica  | datemodified o modified | modified:last week             |
| Importanza     | priorità o priorità   | importance:high                |
| Dimensione           | size                     | size:> 50                   |
| Eliminata        | eliminato o eliminato     | isdeleted:true                 |
| Allegato  | isattachment             | isattachment:true              |
| Per             | to o toname             | to:bob                         |
| Cc             | cc o ccname             | cc:john                        |
| Company        | company                  | company:Microsoft              |
| Località       | posizione                 | location:"Conference Room 102" |
| Category       | category                 | category:Business              |
| Parole chiave       | keywords                 | keywords:"proiezioni di vendita"   |
| Album          | Album                    | album:"Fly by Night"           |
| Nome file      | nome file o file         | filename:MyResume              |
| Genre          | genre                    | genre:rock                     |
| Autore         | author o by             | author:"Stephen King"          |
| Persone         | persone o con           | with:(sonja o david)          |
| Cartella         | cartella, in o percorso    | cartella:download               |
| Estensione file | ext o fileext           | ext:.txt                       |



 

### <a name="attachment"></a>Attachment

Si tratta di proprietà comuni agli allegati. Per limitare la ricerca solo agli allegati, la sintassi è:

`kind:attachment <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà | Uso            | Esempio                  |
|----------|----------------|--------------------------|
| Persone   | persone o con | people:john o with:john |



 

### <a name="contacts"></a>Contatti

Si tratta di proprietà comuni ai contatti. Per limitare la ricerca solo ai contatti, la sintassi è:

`kind:contacts <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà              | Uso                 | Esempio                            |
|-----------------------|---------------------|------------------------------------|
| Posizione             | jobtitle            | jobtitle:CFO                       |
| Indirizzo di messaggistica immediata            | imaddress           | imaddress:john\_doe@msn.com        |
| Telefono dell'assistente     | assistantsphone     | assistantsphone:555-3323           |
| Nome dell'assistente        | assistantname       | assistantname:Paul                 |
| Profession            | Professione          | plumb:plumber                 |
| Nome alternativo              | nickname            | nome alternativo:Tex                       |
| Coniuge                | Coniuge              | taser:Debbie                      |
| Città aziendale         | businesscity        | businesscity:Seattle               |
| Codice postale aziendale  | businesspostalcode  | businesspostalcode:98006           |
| Attività home page    | businesshomepage    | businesshomepage:www.microsoft.com |
| Numero di telefono di callback | callbackphonenumber | callbackphonenumber:555-555-2121   |
| Telefono dell'auto             | Carphone            | carphone:555-555-2121              |
| Children              | figli            | children:Timmy                     |
| Nome            | firstname           | firstname:John                     |
| Cognome             | lastname            | lastname:Doe                       |
| Home fax              | homefax             | homefax:555-555-2121               |
| Nome del responsabile        | managersname        | managersname:John                  |
| Cercapersone                 | pager               | pager:555-555-2121                 |
| Telefono ufficio        | businessphone       | businessphone:555-555-2121         |
| Telefono abitazione            | homePhone           | homephone:555-555-2121             |
| Cellulare          | Mobilephone         | mobilephone:555-555-2121           |
| Office                | office              | office:sample                      |
| Anniversario           | Anniversario         | anniversary:1/1/06                 |
| Data di nascita              | Compleanno            | 1/1/06                    |
| Pagina Web              | Sito web             | webpage:www.microsoft.com          |



 

> [!Note]
>
> Telefono i numeri vengono indicizzati come immessi. Ad esempio, se un utente non ha incluso un codice paese o area geografica quando immette il numero di telefono, gli utenti non saranno in grado di individuare un contatto se si esegue una ricerca con il codice paese o area geografica nel numero di telefono.

 

### <a name="communications"></a>Comunicazioni

Si tratta di proprietà comuni alle comunicazioni. Per limitare la ricerca solo alle comunicazioni, la sintassi è:

`kind:communications <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà       | Uso                           | Esempio                         |
|----------------|-------------------------------|---------------------------------|
| Da           | da o libreria             | from:john                       |
| Ricevuto       | ricevuto o inviato              | sent:yesterday                  |
| Oggetto        | oggetto o titolo              | subject:"Quarterly Financial"   |
| Ha un allegato | hasattachments, hasattachment | hasattachment:true              |
| Allegati    | allegati o allegati     | attachment:presentation.ppt     |
| Bcc            | bcc, bccname o bccaddress    | bcc:dave                        |
| Indirizzo Cc     | ccaddress o cc               | ccaddress:john\_doe@outlook.com |
| Flag di follow-up | flag di followup                  | followupflag:2                  |
| Data di scadenza       | duedate o due                | due:last week                   |
| Read           | read o isread                | is:read                         |
| Operazione completata   | Iscompleted                   | is:completed                    |
| Incompleto     | incompleto o isincomplete    | is:incomplete                   |
| Ha un flag       | hasflag o isflagged          | has:flag                        |
| Durata       | duration                      | duration:> 50                |



 

### <a name="calendar"></a>Calendario

Si tratta di proprietà comuni ai calendari. Per limitare la ricerca solo ai calendari, la sintassi è:

`kind:calendar <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà  | Uso                      | Esempio          |
|-----------|--------------------------|------------------|
| Periodica | ricorrente o ricorrente | is:recurring     |
| Organizzatore | organizzatore, da o da    | organizzatore:debbie |



 

### <a name="documents"></a>Documenti

Si tratta di proprietà comuni ai documenti. Per limitare la ricerca solo ai documenti, la sintassi è la seguente:

`kind:documents <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà          | Uso             | Esempio                       |
|-------------------|-----------------|-------------------------------|
| Commenti          | comments        | comments:"needs final review" |
| Ultimo salvataggio da     | lastsavedby     | lastsavedby:john              |
| Gestione documenti  | documentmanager | documentmanager:john          |
| Numero di revisione   | revisionnumber  | revisionnumber:1.0.3          |
| Formato del documento   | documentformat  | documentformat:MIMETYPE       |
| Data ultima stampa | datelastprinted | datelastprinted:last week     |



 

### <a name="presentation"></a>Presentazione

Si tratta di proprietà comuni alle presentazioni. Per limitare la ricerca solo alle presentazioni, la sintassi è:

`kind:presentation <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà    | Uso        | Esempio           |
|-------------|------------|-------------------|
| Conteggio scorrimenti | slidecount | slidecount:>20 |



 

### <a name="music"></a>Musica

Si tratta di proprietà comuni ai file musicali. Per limitare la ricerca solo alla musica, la sintassi è:

`kind:music <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà | Uso                | Esempio                  |
|----------|--------------------|--------------------------|
| Velocità in bit | velocità in bit, velocità      | velocità in bit:192              |
| Artista   | artista, da o da | artista:John Esere       |
| Durata | duration           | durata:3               |
| Album    | Album              | album:"greatest hits"    |
| Genre    | genre              | genre:rock               |
| Track    | track              | track:12                 |
| Year     | anno               | year:> 1980 < 1990 |



 

### <a name="picture"></a>Immagine

Si tratta di proprietà comuni alle immagini. Per limitare la ricerca solo alle immagini, la sintassi è:

`kind:picture <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà     | Uso         | Esempio               |
|--------------|-------------|-----------------------|
| Fotocamera make  | cameramake  | cameramake:sample     |
| Modello di fotocamera | cameramodel | cameramodel:sample    |
| Dimensioni   | dimensions  | dimensioni:8X10       |
| Orientamento  | orientation | orientamento:orizzontale |
| Data di inizio   | datetaken   | datetaken:yesterday   |
| Larghezza        | width       | width:1600            |
| Altezza       | altezza      | height:1200           |



 

### <a name="video"></a>Video

Si tratta di proprietà comuni ai video. Per limitare la ricerca solo ai video, la sintassi è:

`kind:video <property>:<value>`

dove `<property>` è una proprietà elencata di seguito e è il termine di ricerca specificato `<value>` dall'utente.



| Proprietà | Uso           | Esempio                                |
|----------|---------------|----------------------------------------|
| Nome     | name, subject | name:"Family Vacation to the Beach 05" |
| Interno      | ext, fileext  | ext:.avi                               |



 

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

 

 





