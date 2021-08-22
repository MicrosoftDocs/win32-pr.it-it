---
description: In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti principali coinvolti in ognuna, viene illustrato il tempo di attività di indicizzazione e vengono fornite alcune note per sviluppatori di terze parti che vogliono indicizzare i propri archivi dati o formati di file.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Processo di indicizzazione nella Windows ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5f69306834c001a122a18087205d64b6164d51618226fe0e0fb735f7f5b905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095022"
---
# <a name="indexing-process-in-windows-search"></a>Processo di indicizzazione nella Windows ricerca

In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti principali coinvolti in ognuna, viene illustrato il tempo di attività di indicizzazione e vengono fornite alcune note per sviluppatori di terze parti che vogliono indicizzare i propri archivi dati o formati di file.

Questo argomento è organizzato come segue:

- [Overview](#overview)
- [Fase 1: Accodamento di URL per l'indicizzazione](#stage-1-queuing-urls-for-indexing)
- [Fase 2: Ricerca per indicizzazione di URL](#stage-2-crawling-urls)
- [Fase 3: Aggiornamento dell'indice](#stage-3-updating-the-index)
- [Come viene pianificata l'indicizzazione](#how-indexing-is-scheduled)
- [Note per gli implementatori](#notes-to-implementers)
- [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Windows La ricerca supporta l'indicizzazione di proprietà e contenuto da file di formati di file diversi, ad esempio formati .doc o jpeg, e archivi dati, ad esempio le cassette postali file system o Windows Outlook dati. Esistono due tipi di indici: indici di valori che consentono il filtro e l'ordinamento in base all'intero valore di una proprietà e indici invertiti che indicizzano le parole all'interno di proprietà testuali o contenuto. Se si dispone di un formato di file o di un archivio dati personalizzato, è necessario comprendere Windows indici di ricerca per ottenere gli elementi indicizzati correttamente.

Il processo di indicizzazione si verifica in tre fasi controllate da un Windows di ricerca denominato gatherer. Nella prima fase, il gatherer aggiunge URL alle code. Gli URL identificano gli elementi da indicizzare e alle code viene semplicemente assegnata la priorità agli elenchi di URL. Nella seconda fase, il gatherer coordina altri Windows di ricerca e componenti di terze parti per accedere agli elementi e raccogliere dati su di essi. Infine, nella terza fase i dati raccolti vengono aggiunti all'indice.

Il diagramma seguente illustra i componenti principali e il flusso dei dati tramite il processo di indicizzazione. Nella raccolta dei dati per l'indice sono coinvolti diversi componenti. Alcune di queste sono parte della ricerca Windows e altre provengono da applicazioni di terze parti. Se si dispone di un archivio dati o di un formato di file personalizzato, Windows Ricerca si basa sul gestore del protocollo e sul filtro per accedere agli URL ed emettere proprietà per l'indicizzazione. Windows I componenti di ricerca sono visualizzati in blu e i componenti di terze parti sono visualizzati in verde.

![Diagramma che illustra l'interazione tra i componenti durante il processo di indicizzazione](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Fase 1: Accodamento di URL per l'indicizzazione

Nella prima fase dell'indicizzazione, il gatherer raccoglie informazioni sugli aggiornamenti agli archivi dati, confronta le informazioni con l'ambito di ricerca per indicizzazione noto e quindi compila una coda di URL da attraversare per raccogliere dati per l'indice. Per le origini non basate su notifiche, ad esempio unità FAT, il gatherer avvia periodicamente un attraversamento completo dell'ambito di ricerca per indicizzazione in modo che i dati nell'indice siano mantenuti aggiornati. Per origini come NTFS, è presente una sola ricerca per indicizzazione e tutto il resto viene gestito dalle notifiche dal journal delle modifiche [USN.](/windows/desktop/FileIO/change-journals) Non è inoltre disponibile alcuna ricerca per indicizzazione di Microsoft Outlook. Il diagramma seguente illustra una visualizzazione di alto livello del processo di accodamento per l'indicizzazione non sottoposta a ricerca per indicizzazione.

![Diagramma che illustra il processo di query per l'indicizzazione non sottoposta a ricerca per indicizzazione](images/queuingurls.jpg)

La parte restante di questa sezione illustra Windows ricerca determina quali URL eseguire la ricerca per indicizzazione e definisce alcuni termini importanti lungo il percorso.

**Ambito della ricerca per indicizzazione**  L'ambito della ricerca per indicizzazione è un set di URL che Windows ricerca attraversa per raccogliere dati sugli elementi che l'utente vuole indicizzato per ricerche più veloci. Windows La ricerca aggiunge alcuni URL all'ambito della ricerca per indicizzazione per impostazione predefinita, ad esempio i percorsi delle cartelle **Documenti** e Immagini **degli** utenti. Altri URL possono essere aggiunti da applicazioni di terze parti, utenti e Criteri di gruppo. Infine, sia gli utenti che Criteri di gruppo possono escludere in modo esplicito gli URL. Windows La ricerca accetta tutti gli URL aggiunti e rimuove gli URL esclusi per determinare l'ambito della ricerca per indicizzazione. Questa è la working set di URL da cui il gatherer inizia il proprio lavoro.

**Gatherer**  Il gatherer è un Windows di ricerca che raccoglie informazioni sugli URL all'interno dell'ambito di ricerca per indicizzazione e crea una coda di URL per l'indicizzatore per la ricerca per indicizzazione. Quando un elemento nell'ambito della ricerca per indicizzazione viene aggiunto, eliminato o aggiornato, il gatherer viene informato dal provider di notifiche dell'archivio dati. Esiste una ricerca per indicizzazione iniziale in cui il gatherer inizia in corrispondenza della radice dell'ambito di ricerca per indicizzazione. L'URL viene passato al gestore del protocollo e quindi [**all'oggetto IFilter appropriato.**](/windows/win32/api/filter/nn-filter-ifilter) Il filtro è in genere un'enumerazione di directory che produce più URL. Le notifiche sono lo stato fisso. In genere, ogni archivio dati dispone di un gestore di protocollo che fornisce queste notifiche. Ad esempio, nel file system locale, il journal delle modifiche [USN](/windows/desktop/FileIO/change-journals) funge da provider di notifiche per tutti gli URL nel file:// locale. Analogamente, Microsoft Outlook funge da provider di notifiche per tutti gli URL nel mapi:// protocollo. Quando un utente riceve, sposta o elimina messaggi di posta elettronica, Outlook al gatherer lo stato modificato del messaggio di posta elettronica. Da queste notifiche, il gatherer crea code di indicizzazione di URL per la ricerca per indicizzazione.

**Code di indicizzazione**  Le code di indicizzazione sono elenchi di URL che identificano gli elementi che devono essere indicizzati o indicizzati di nuovo. Il gatherer confronta gli URL ricevuti dai provider di notifiche con gli URL nell'ambito della ricerca per indicizzazione. Ogni URL dei provider di notifiche che rientra nell'ambito della ricerca per indicizzazione viene aggiunto a una coda che il gatherer usa per classificare in ordine di priorità gli URL da elaborare successivamente.

Sono disponibili tre code: notifiche con priorità alta, notifiche normali e ricerche per indicizzazione periodiche. La coda con priorità alta è per le notifiche che devono essere elaborate immediatamente. Ad esempio, quando un utente modifica la proprietà title di un elemento in Windows Explorer, la visualizzazione Windows Explorer deve essere aggiornata immediatamente dopo la modifica. La coda di notifica normale è per tutte le notifiche di modifica rimanenti. Le code di notifica vengono elaborate prima della coda di ricerca per indicizzazione perché è più probabile che gli elementi modificati siano di interesse per un utente. Il gatherer accede ai dati per gli URL in ogni coda nell'ordine FIFO (First In, First Out).

Per altre informazioni sull'assegnazione delle priorità e sulle API di gestione degli eventi introdotte in Windows 7, vedere Indicizzazione della priorità e degli eventi del set di [righe in Windows 7](indexing-prioritization-and-rowset-events.md). Per altre informazioni sulla gestione dell'ambito di ricerca per indicizzazione e sulle notifiche, vedere [Fornire notifiche di modifica](-search-3x-wds-notifyingofchanges.md) e Usare [il](-search-3x-wds-extidx-csm.md)Gestione ambito ricerca per indicizzazione .

## <a name="stage-2-crawling-urls"></a>Fase 2: Ricerca per indicizzazione di URL

Nella seconda fase dell'indicizzazione, il gatherer esegue la ricerca per indicizzazione nelle code, accedendo agli archivi dati e recuperando i flussi di elementi. In primo luogo, il gatherer trova il gestore di protocollo appropriato per ogni URL. Quindi, il gatherer passa l'URL al gestore del protocollo. Il gestore di protocollo accede all'elemento e passa i metadati dell'elemento al gatherer. Il gatherer usa i metadati per identificare il filtro corretto.

Il diagramma seguente mostra una visualizzazione di alto livello del processo di ricerca per indicizzazione degli URL. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![diagramma che illustra il processo di ricerca per indicizzazione di URL e accesso agli elementi](images/crawlingqueues.jpg)

La parte restante di questa sezione descrive Windows ricerca accede agli elementi per l'indicizzazione e illustra i ruoli di ognuno dei componenti coinvolti.

**Gatherer**  Nella fase 2, la fase di ricerca per indicizzazione, il gatherer elabora gli URL nelle code, a partire dalla coda con priorità alta. Ogni URL viene esaminato per identificarne il protocollo. Il gatherer cerca quindi il gestore di protocollo registrato per il protocollo e crea un'istanza nel processo host del protocollo di ricerca.

**Host del protocollo di ricerca**  L'host del protocollo di ricerca è semplicemente un processo host boxed per i gestori di protocollo. In genere, Windows ricerca crea due processi host di questo tipo, uno eseguito nel contesto di sicurezza del sistema e uno eseguito nel contesto di sicurezza dell'utente. Questa separazione garantisce che i dati specifici di un utente non siano mai eseguiti nel contesto di sistema.

Windows La ricerca usa anche il processo host per isolare un'istanza di un gestore di protocollo da altri processi o applicazioni. In questo modo, nessuna applicazione esterna può accedere a tale istanza specifica del gestore del protocollo e, se il gestore del protocollo ha esito negativo in modo imprevisto, viene interessato solo il processo di indicizzazione. Poiché il processo host esegue codice di terze parti (gestori di protocollo), Windows Ricerca ricicla periodicamente il processo per ridurre al minimo il tempo necessario a un attacco riuscito per sfruttare le informazioni nel processo. Oltre a questo, l'host del protocollo di ricerca non influisce sulla ricerca per indicizzazione degli URL o sull'indicizzazione degli elementi.

**Gestori di protocollo**  I gestori di protocollo forniscono l'accesso agli elementi in un archivio dati usando il protocollo dell'archivio dati. Ad esempio, il gestore del protocollo NTFS fornisce l'accesso ai file in un'unità locale usando file:// protocollo. Il gestore del protocollo sa come attraversare l'archivio dati, identificare gli elementi nuovi o aggiornati e inviare una notifica al gatherer. Quando inizia la ricerca per indicizzazione, il gestore del protocollo fornisce quindi un oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) al gatherer per eseguire l'associazione al flusso sottostante dell'elemento e restituire i metadati dell'elemento, ad esempio restrizioni di sicurezza e ora dell'ultima modifica.

> [!NOTE]  
> I gestori di protocollo non sono Windows di ricerca; sono componenti del protocollo e dell'archivio dati specifici a cui sono progettati per l'accesso. Se si dispone di un archivio dati personalizzato da indicizzare, è necessario implementare un gestore di protocollo. Per altre informazioni sui gestori di protocollo e su come implementarne uno, vedere [Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md).

**Metadati e flusso**  Usando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore del protocollo, il gatherer identifica il filtro corretto per l'URL. Il gatherer analizza l'estensione del nome file dell'elemento e cerca il filtro registrato per tale estensione. Se il gatherer non riesce a trovare un filtro, ricerca Windows usa i metadati per derivare un set minimo di informazioni sulle proprietà di sistema (ad esempio System.ItemName) e aggiorna l'indice. In caso contrario, se il gatherer trova il filtro, inizia la terza fase dell'indicizzazione.

## <a name="stage-3-updating-the-index"></a>Fase 3: Aggiornamento dell'indice

Nella terza fase dell'indicizzazione, il gatherer crea un'istanza del filtro corretto per l'URL e inizializza il filtro con il flusso [**dall'oggetto IUrlAccessor.**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) Il filtro accede quindi all'elemento e restituisce il contenuto per l'indice. Se si ha un formato di file personalizzato, Windows ricerca si basa sul filtro per accedere agli URL e generare contenuto e proprietà per l'indicizzazione.

Il diagramma seguente illustra una visualizzazione di alto livello del processo di accesso ai dati. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![diagramma che mostra i dati degli elementi generati per l'indice](images/filteringdata.jpg)

La parte restante di questa sezione descrive Windows ricerca accede ai dati degli elementi per l'indicizzazione e illustra i ruoli di ognuno dei componenti coinvolti.

**Gatherer**  All'inizio di questa fase, il ruolo del gatherer è creare un'istanza del filtro corretto per l'elemento e passarlo al flusso dell'elemento. Al termine di questa fase, il gatherer accetta il contenuto e le proprietà generate dal gestore di filtri e proprietà e aggiorna l'indice.

**Filtrare l'host**  L'host del filtro è semplicemente un processo host per i filtri e i gestori delle proprietà e ha uno scopo simile all'host del protocollo di ricerca. Il processo host isola i filtri e i gestori delle proprietà dal resto del sistema per gli stessi motivi di sicurezza e stabilità per cui i processi host del protocollo di ricerca isolano i gestori di protocollo. Il processo host viene eseguito con diritti minimi (non può neanche accedere al file system) e viene occasionalmente riciclato per la protezione da attacchi alla sicurezza. Windows La ricerca monitora anche l'uso delle risorse in modo che, se un filtro utilizza troppe risorse, il processo host viene riciclato.

**Filtri**  I filtri sono componenti critici del processo di indicizzazione che generano informazioni sugli elementi per il gatherer. I filtri sono denominati in base all'interfaccia principale usata nell'implementazione, [**all'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e di conseguenza vengono talvolta definiti filtri IFilter. Esistono due tipi di filtri: uno che interagisce con singoli elementi come i file e uno che interagisce con contenitori come cartelle. Entrambi forniscono dati per l'indice.

Usando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore del protocollo, il gatherer identifica il filtro corretto per un URL specifico e lo passa al flusso. Il gatherer identifica il filtro corretto tramite un gestore di protocollo o in base all'estensione del nome file, al tipo MIME o all'identificatore di classe (CLSID). Se l'URL punta a un contenitore, il filtro genera proprietà per il contenitore ed enumera gli elementi nel contenitore (URL figlio). Se l'URL punta a un elemento, il filtro restituisce il contenuto testuale, se la lettura delle proprietà e è più complessa rispetto ai gestori di proprietà. In genere, è consigliabile che i filtri emettono il contenuto dell'elemento mentre i gestori delle proprietà emettono le proprietà dell'elemento. Tuttavia, se il filtro deve funzionare con applicazioni meno recenti che non riconoscono i gestori delle proprietà, è possibile implementare il filtro anche per generare proprietà.

> [!NOTE]  
> I filtri non sono Windows di ricerca. sono componenti correlati al formato di file o al contenitore specifico a cui sono progettati per l'accesso. Per altre informazioni sui filtri e su come implementarne uno per un contenitore o un formato di file personalizzato, vedere [Procedure consigliate](-search-3x-wds-extidx-filters.md)per la creazione di gestori filtri in Windows Ricerca .

Nella tabella seguente sono elencati i risultati ricevuti dal gatherer da un filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e dal gestore delle proprietà ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante il processo di indicizzazione.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Consenti scrittura**                | No                                 | Sì                                             |
| **Combinare contenuto e proprietà** | Sì                                | No                                              |
| **Multilingue**               | Sì                                | No                                              |
| **Creare collegamenti**                 | Sì                                | No                                              |
| **MIME**                       | Sì                                | No                                              |
| **Limiti del testo**            | Frase, paragrafo, capitolo       | Nessuno                                            |
| **Client/server**            | Entrambe                               | Client                                          |
| **Implementazione**             | Complex                            | Semplice                                          |

**Gestori delle proprietà**  I gestori delle proprietà sono componenti che leggono e scrivono proprietà per un formato di file specifico. Accedono agli elementi e generano proprietà per il gatherer nello stesso modo in cui vengono applicati i filtri per il contenuto. I gestori di proprietà sono più facili da implementare rispetto ai filtri. Se un formato di file basato su testo è molto semplice o si prevede che i file siano molto piccoli, il gestore delle proprietà può generare sia proprietà che contenuto.

> [!NOTE]  
> I gestori delle proprietà non sono Windows di ricerca; sono componenti correlati al formato di file specifico a cui sono progettati per l'accesso. Per altre informazioni sui gestori delle proprietà e su come implementarne uno per un formato di file personalizzato, vedere [Developing Property Handlers for Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Proprietà** Windows ricerca fornisce un [sistema di proprietà](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) che include una grande libreria di proprietà. Qualsiasi proprietà può essere visualizzata in qualsiasi elemento in base a quanto definito dal gestore del filtro o della proprietà. Se si ha un formato di file personalizzato, è possibile eseguire il mapping delle proprietà del formato di file a queste proprietà di sistema ed è possibile creare nuove proprietà personalizzate. Quando il gestore di filtri o proprietà genera queste proprietà, il gatherer aggiorna l'indice in modo che gli utenti possano eseguire ricerche usando le proprietà. Per altre informazioni sulla creazione e la registrazione di proprietà personalizzate per un formato di file, vedere [Sistema di proprietà](../properties/building-property-handlers.md).

**SystemIndex**  L'indice, denominato SystemIndex, archivia i dati indicizzati ed è costituito da un archivio delle proprietà e da indici sulle proprietà e sul contenuto per le proprietà dell'elemento e da un indice invertito per il contenuto testuale e le proprietà. Dopo che il gatherer ha aggiornato l'indice, è possibile eseguire query sull'indice Windows ricerca e altre applicazioni. Per altre informazioni su come eseguire query sull'indice, vedere [Esecuzione di query sull'indice a livello di codice.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Tenere presente che quando si registra nuovamente uno schema, le modifiche apportate agli attributi delle proprietà definite in precedenza potrebbero non essere rispettate dall'indicizzatore. La soluzione consiste nel ricompilare l'indice o nell'introdurre nuove proprietà che riflettano le modifiche anziché aggiornare quelle precedenti (scelta non consigliata). Per altre informazioni, vedere [Note per gli implementatori](#notes-to-implementers) in [Panoramica del sistema delle proprietà](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Come viene pianificata l'indicizzazione

Quando Windows ricerca viene installata per la prima volta, esegue un'indicizzazione completa dell'ambito della ricerca per indicizzazione, sospendo durante i periodi di attività di I/O e utente elevate. L'ambito di ricerca per indicizzazione predefinito è costituito dai percorsi predefiniti della libreria, ad esempio **Documenti**, **Musica**, **Immagini** e **Video**. Le notifiche vengono elaborate anche prima del termine della ricerca per indicizzazione iniziale. In alcuni casi, il gatherer esegue la ricerca per indicizzazione degli URL dall'ambito completo della ricerca per indicizzazione. Queste ricerche per indicizzazione complete garantiscono che i dati nell'indice siano nuovi. Ad esempio, se un provider di notifiche non riesce a inviare notifiche o se il Windows servizio di ricerca viene terminato in modo imprevisto, il gatherer non ha conoscenza di elementi nuovi o modificati e non indicizza questi elementi. Esistono due tipi di origini: solo notifica e notifica abilitata. In entrambe le origini, il gatherer esegue inizialmente la ricerca per indicizzazione dell'indice. Dopo la ricerca per indicizzazione iniziale, le origini di sola notifica non eseguiranno mai di nuovo una ricerca per indicizzazione completa a meno che non si sia verificato un errore, ad esempio il roll over del journal delle modifiche [USN.](/windows/desktop/FileIO/change-journals) Le origini abilitate per le notifiche eseguono una ricerca per indicizzazione incrementale all'avvio dell'indicizzatore, ma sono in ascolto delle notifiche durante l'esecuzione. NTFS e Microsoft Outlook solo notifiche. Internet Explorer e FAT sono abilitati per la notifica.

## <a name="notes-to-implementers"></a>Note per gli implementatori

La qualità dei dati nell'indice e l'efficienza del processo di indicizzazione dipendono in gran parte dall'implementazione del filtro e del gestore delle proprietà. Poiché il filtro viene chiamato ogni volta che un URL identifica il formato di file, il processo di indicizzazione può rallentare notevolmente se il filtro non è efficiente. Se il gestore delle proprietà non esegue correttamente il mapping di tutte le proprietà del file alle proprietà di sistema o non genera correttamente queste proprietà, i dati nell'indice non saranno corretti e le ricerche successive di tali proprietà restituiranno risultati non corretti. Se il gestore del filtro o della proprietà ha esito negativo, l'indicizzatore non sarà in grado di indicizzare i dati.

Le applicazioni e i processi diversi Windows ricerca si basano su gestori di protocollo, filtri e gestori di proprietà. Le implementazioni possono influire su tali applicazioni in modi che potrebbero non essere previsti. La [Windows per lo sviluppo della](-search-developers-guide-entry-page.md) ricerca fornisce consigli sulle scelte di progettazione e sul test di ognuno di questi componenti.

## <a name="related-topics"></a>Argomenti correlati

[Indicizzazione, query e notifiche nella ricerca Windows ricerca](-search-3x-wds-included-in-index.md)

[Elementi inclusi nell'indice](-search-indexing-process-overview.md)

[Processo di query nella Windows ricerca](querying-process--windows-search-.md)

[Processo di notifica nella Windows ricerca](-search-3x-wds-support.md)

[Requisiti di formattazione url](url-formatting-requirements.md)
