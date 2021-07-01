---
description: In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti principali coinvolti in ognuna, viene illustrata la tempistica dell'attività di indicizzazione e vengono fornite alcune note per gli sviluppatori di terze parti che desiderano indicizzare gli archivi dati o i formati di file.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Processo di indicizzazione in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b819a056b9a3dd44ea799ee56ae6b2e87606f552
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119536"
---
# <a name="indexing-process-in-windows-search"></a>Processo di indicizzazione in Windows Search

In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti principali coinvolti in ognuna, viene illustrata la tempistica dell'attività di indicizzazione e vengono fornite alcune note per gli sviluppatori di terze parti che desiderano indicizzare gli archivi dati o i formati di file.

Questo argomento è organizzato come segue:

- [Panoramica](#overview)
- [Fase 1: Accodamento degli URL per l'indicizzazione](#stage-1-queuing-urls-for-indexing)
- [Fase 2: Ricerca per indicizzazione degli URL](#stage-2-crawling-urls)
- [Fase 3: Aggiornamento dell'indice](#stage-3-updating-the-index)
- [Come viene pianificata l'indicizzazione](#how-indexing-is-scheduled)
- [Note per gli implementatori](#notes-to-implementers)
- [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Windows Search supporta l'indicizzazione di proprietà e contenuto da file di formati di file diversi, ad esempio formati .doc o JPEG, e archivi dati, ad esempio le cassette postali file system o Windows Outlook. Esistono due tipi di indici: indici di valore che consentono l'applicazione di filtri e l'ordinamento in base all'intero valore di una proprietà e indici invertiti che indicizzano le parole all'interno di proprietà testuali o contenuto. Se si dispone di un formato di file personalizzato o di un archivio dati, è necessario comprendere in che modo Windows Search per ottenere correttamente gli elementi indicizzati.

Il processo di indicizzazione si verifica in tre fasi controllate da un componente Windows Search denominato gatherer. Nella prima fase, il gatherer aggiunge gli URL alle code. Gli URL identificano gli elementi da indicizzare e le code sono semplicemente elenchi di URL classificati in ordine di priorità. Nella seconda fase, il gatherer coordina altri componenti Windows Search e di terze parti per accedere agli elementi e raccogliere dati su di essi. Infine, nella terza fase, i dati raccolti vengono aggiunti all'indice.

Il diagramma seguente illustra i componenti principali e il flusso dei dati durante il processo di indicizzazione. Nella raccolta dei dati per l'indice sono coinvolti diversi componenti. Alcune di queste sono parte di Windows Search e altre provengono da applicazioni di terze parti. Se si dispone di un archivio dati o di un formato di file personalizzato, Windows Search si basa sul gestore del protocollo e sul filtro per l'accesso agli URL e la creazione di proprietà per l'indicizzazione. Windows Search componenti vengono visualizzati in blu e i componenti di terze parti sono visualizzati in verde.

![Diagramma che illustra l'interazione tra i componenti durante il processo di indicizzazione](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Fase 1: Accodamento degli URL per l'indicizzazione

Nella prima fase dell'indicizzazione, il gatherer raccoglie informazioni sugli aggiornamenti agli archivi dati, confronta le informazioni con l'ambito di ricerca per indicizzazione noto e quindi compila una coda di URL da attraversare per raccogliere i dati per l'indice. Per le origini non basate su notifiche, ad esempio unità FAT, il gatherer avvia periodicamente un attraversamento completo dell'ambito della ricerca per indicizzazione in modo che i dati nell'indice siano mantenuti aggiornati. Per origini come NTFS, è presente una sola ricerca per indicizzazione e tutto il resto viene gestito dalle notifiche dal journal delle modifiche [USN.](/windows/desktop/FileIO/change-journals) Non è inoltre disponibile alcuna ricerca per indicizzazione in Microsoft Outlook. Il diagramma seguente mostra una visualizzazione di alto livello del processo di accodamento per l'indicizzazione non per indicizzazione.

![diagramma che illustra il processo di query per l'indicizzazione non per indicizzazione](images/queuingurls.jpg)

Nella parte restante di questa sezione viene illustrato Windows Search gli URL di cui eseguire la ricerca per indicizzazione e vengono definiti alcuni termini importanti lungo il percorso.

**Ambito ricerca per indicizzazione**  L'ambito della ricerca per indicizzazione è un set di URL che Windows Search per raccogliere dati sugli elementi che l'utente vuole indicizzare per ricerche più veloci. Windows Search aggiunge alcuni URL all'ambito della ricerca per indicizzazione per impostazione predefinita, ad esempio i percorsi delle cartelle **Documenti** **e Immagini degli** utenti. Altri URL possono essere aggiunti da applicazioni di terze parti, utenti e Criteri di gruppo. Infine, sia gli utenti che Criteri di gruppo possono escludere in modo esplicito gli URL. Windows Search accetta tutti gli URL aggiunti e rimuove gli URL esclusi per determinare l'ambito della ricerca per indicizzazione. Questo è il working set di URL da cui inizia il lavoro del gatherer.

**Gatherer**  Gatherer è un componente Windows Search che raccoglie informazioni sugli URL nell'ambito della ricerca per indicizzazione e crea una coda di URL per l'indicizzatore per la ricerca per indicizzazione. Quando un elemento nell'ambito della ricerca per indicizzazione viene aggiunto, eliminato o aggiornato, il gatherer viene informato dal provider di notifiche dell'archivio dati. Esiste una ricerca per indicizzazione iniziale in cui il gatherer inizia in corrispondenza della radice dell'ambito della ricerca per indicizzazione. L'URL viene passato al gestore di protocollo e quindi all'oggetto [**IFilter appropriato.**](/windows/win32/api/filter/nn-filter-ifilter) Il filtro è in genere un'enumerazione di directory che produce più URL. Le notifiche sono in stato stabile. In genere, ogni archivio dati ha un proprio gestore di protocollo che fornisce queste notifiche. Ad esempio, nel file system locale, il journal delle modifiche [USN](/windows/desktop/FileIO/change-journals) funge da provider di notifiche per tutti gli URL nel protocollo file://. Analogamente, Microsoft Outlook funge da provider di notifiche per tutti gli URL nel mapi:// protocollo. Quando un utente riceve, sposta o elimina un messaggio di posta elettronica, Outlook notifica al gatherer lo stato modificato del messaggio di posta elettronica. Da queste notifiche, il gatherer crea code di indicizzazione di URL per la ricerca per indicizzazione.

**Indicizzazione delle code**  Le code di indicizzazione sono elenchi di URL che identificano gli elementi che devono essere indicizzati o indicizzati di nuovo. Il gatherer confronta gli URL ricevuti dai provider di notifiche con gli URL nell'ambito della ricerca per indicizzazione. Ogni URL dei provider di notifiche che rientra nell'ambito della ricerca per indicizzazione viene aggiunto a una coda che il gatherer usa per classificare in ordine di priorità gli URL da elaborare successivamente.

Sono disponibili tre code: notifiche con priorità alta, notifiche normali e ricerche per indicizzazione periodiche. La coda con priorità alta è per le notifiche che devono essere elaborate immediatamente. Ad esempio, quando un utente modifica la proprietà title di un elemento in Esplora risorse, la visualizzazione Esplora risorse deve essere aggiornata immediatamente dopo la modifica. La coda di notifica normale è per tutte le notifiche di modifica rimanenti. Le code di notifica vengono elaborate prima della coda di ricerca per indicizzazione perché è più probabile che gli elementi modificati siano di interesse per un utente. Il gatherer accede ai dati per gli URL in ogni coda nell'ordine FIFO (First In, First Out).

Per altre informazioni sull'assegnazione delle priorità e sulle API di gestione degli eventi introdotte in Windows 7, vedere Indicizzazione delle priorità e degli eventi del set di [righe in Windows 7.](indexing-prioritization-and-rowset-events.md) Per altre informazioni sulla gestione dell'ambito della ricerca per indicizzazione e sulle notifiche, vedere [Invio di notifiche di](-search-3x-wds-notifyingofchanges.md) modifica e Uso del [Gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Fase 2: Ricerca per indicizzazione degli URL

Nella seconda fase dell'indicizzazione, il gatherer esegue una ricerca per indicizzazione nelle code, accedendo agli archivi dati e recuperando i flussi di elementi. In primo luogo, il gatherer trova il gestore di protocollo appropriato per ogni URL. Quindi, il gatherer passa l'URL al gestore di protocollo. Il gestore di protocollo accede all'elemento e passa di nuovo i metadati dell'elemento al gatherer. Il gatherer usa i metadati per identificare il filtro corretto.

Il diagramma seguente mostra una visualizzazione di alto livello del processo di ricerca per indicizzazione degli URL. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![diagramma che illustra il processo di ricerca per indicizzazione degli URL e accesso agli elementi](images/crawlingqueues.jpg)

Nella parte restante di questa sezione viene descritto Windows Search gli elementi per l'indicizzazione e vengono illustrati i ruoli di ognuno dei componenti coinvolti.

**Gatherer**  Nella fase 2, la fase di ricerca per indicizzazione, il gatherer elabora gli URL nelle code, a partire dalla coda con priorità alta. Ogni URL viene esaminato per identificarne il protocollo. Il gatherer cerca quindi il gestore di protocollo registrato per il protocollo e crea un'istanza nel processo host del protocollo di ricerca.

**Host del protocollo di ricerca**  L'host del protocollo di ricerca è semplicemente un processo host boxed per i gestori di protocollo. In genere, Windows Search crea due processi host di questo tipo, uno che viene eseguito nel contesto di sicurezza del sistema e uno che viene eseguito nel contesto di sicurezza dell'utente. Questa separazione garantisce che i dati specifici di un utente non siano mai eseguiti nel contesto di sistema.

Windows Search usa anche il processo host per isolare un'istanza di un gestore di protocollo da altri processi o applicazioni. In questo modo, nessuna applicazione esterna può accedere a tale istanza specifica del gestore di protocollo e, se il gestore di protocollo ha esito negativo in modo imprevisto, viene interessato solo il processo di indicizzazione. Poiché il processo host esegue codice di terze parti (gestori di protocollo), Windows Search ricicla periodicamente il processo per ridurre al minimo il tempo necessario a un attacco riuscito per sfruttare le informazioni nel processo. Oltre a ciò, l'host del protocollo di ricerca non influisce sulla ricerca per indicizzazione degli URL o sull'indicizzazione degli elementi.

**Gestori di protocollo**  I gestori di protocollo forniscono l'accesso agli elementi in un archivio dati usando il protocollo dell'archivio dati. Ad esempio, il gestore del protocollo NTFS fornisce l'accesso ai file in un'unità locale usando il file:// sistema. Il gestore di protocollo sa come attraversare l'archivio dati, identificare gli elementi nuovi o aggiornati e inviare una notifica al gatherer. Quindi, quando inizia la ricerca per indicizzazione, il gestore del protocollo fornisce un oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) al gatherer per eseguire l'associazione al flusso sottostante dell'elemento e restituire i metadati dell'elemento, ad esempio le restrizioni di sicurezza e l'ora dell'ultima modifica.

> [!NOTE]  
> I gestori di protocollo non sono Windows Search componenti. sono componenti del protocollo e dell'archivio dati specifici a cui sono progettati per l'accesso. Se si dispone di un archivio dati personalizzato da indicizzare, è necessario implementare un gestore di protocollo. Per altre informazioni sui gestori di protocollo e su come implementarne uno, vedere [Sviluppo di gestori di protocollo.](-search-3x-wds-phaddins.md)

**Metadati e flusso**  Usando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore di protocollo, il gatherer identifica il filtro corretto per l'URL. Il gatherer analizza l'estensione del nome file dell'elemento e cerca il filtro registrato per tale estensione. Se il gatherer non riesce a trovare un filtro, Windows Search usa i metadati per derivare un set minimo di informazioni sulle proprietà di sistema (ad esempio System.ItemName) e aggiornare l'indice. In caso contrario, se il gatherer trova il filtro, inizia la terza fase dell'indicizzazione.

## <a name="stage-3-updating-the-index"></a>Fase 3: Aggiornamento dell'indice

Nella terza fase dell'indicizzazione, il gatherer crea un'istanza del filtro corretto per l'URL e inizializza il filtro con il flusso [**dell'oggetto IUrlAccessor.**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) Il filtro accede quindi all'elemento e restituisce il contenuto per l'indice. Se si dispone di un formato di file personalizzato, Windows Search si basa sul filtro per accedere agli URL e generare contenuto e proprietà per l'indicizzazione.

Il diagramma seguente mostra una visualizzazione di alto livello del processo di accesso ai dati. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![Diagramma che mostra i dati degli elementi generati per l'indice](images/filteringdata.jpg)

Nella parte restante di questa sezione viene descritto Windows Search ai dati degli elementi per l'indicizzazione e vengono illustrati i ruoli di ognuno dei componenti coinvolti.

**Gatherer**  All'inizio di questa fase, il ruolo del gatherer è creare un'istanza del filtro corretto per l'elemento e passarlo al flusso dell'elemento. Al termine di questa fase, il gatherer accetta il contenuto e le proprietà generati dal gestore del filtro e della proprietà e aggiorna l'indice.

**Filter Host**  L'host filtro è semplicemente un processo host per filtri e gestori di proprietà e ha uno scopo simile all'host del protocollo di ricerca. Il processo host isola i filtri e i gestori di proprietà dal resto del sistema per gli stessi motivi di sicurezza e stabilità per cui i processi host del protocollo di ricerca isolano i gestori di protocollo. Il processo host viene eseguito con diritti minimi (non può nemmeno accedere al file system) e viene occasionalmente riciclato per proteggersi dagli attacchi alla sicurezza. Windows Search monitora anche l'uso delle risorse in modo che, se un filtro utilizza troppe risorse, il processo host viene riciclato.

**Filtri**  I filtri sono componenti critici del processo di indicizzazione che generano informazioni sugli elementi per il gatherer. I filtri sono denominati in base all'interfaccia principale usata nella relativa implementazione, [**all'interfaccia IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e, di conseguenza, vengono talvolta definiti IFilter. Esistono due tipi di filtri: uno che interagisce con singoli elementi come i file e uno che interagisce con contenitori come le cartelle. Entrambi forniscono i dati per l'indice.

Usando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore di protocollo, il gatherer identifica il filtro corretto per un particolare URL e lo passa al flusso. Il gatherer identifica il filtro corretto tramite un gestore di protocollo o tramite l'estensione del nome file, il tipo MIME o l'identificatore di classe (CLSID). Se l'URL punta a un contenitore, il filtro genera le proprietà per il contenitore ed enumera gli elementi nel contenitore (URL figlio). Se l'URL punta a un elemento, il filtro restituisce il contenuto testuale, se la lettura delle proprietà e è più complessa rispetto ai gestori di proprietà. In genere, è consigliabile che i filtri emettono il contenuto dell'elemento mentre i gestori di proprietà generano le proprietà dell'elemento. Tuttavia, se il filtro deve funzionare con applicazioni meno recenti che non riconoscono i gestori di proprietà, è possibile implementare il filtro anche per generare proprietà.

> [!NOTE]  
> I filtri non sono Windows Search componenti. sono componenti correlati al formato di file o al contenitore specifico a cui sono progettati per l'accesso. Per altre informazioni sui filtri e su come implementarne uno per un formato di file o un contenitore personalizzato, vedere Procedure consigliate per la creazione di gestori di [filtri in Windows Search](-search-3x-wds-extidx-filters.md).

La tabella seguente elenca i risultati che il gatherer riceve da un filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e da un gestore delle proprietà ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante il processo di indicizzazione.

|                            | [**Ifilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Consenti scrittura**                | No                                 | Sì                                             |
| **Combinare contenuto e proprietà** | Sì                                | No                                              |
| **Multilingue**               | Sì                                | No                                              |
| **Creare collegamenti**                 | Sì                                | No                                              |
| **MIME**                       | Sì                                | No                                              |
| **Limiti del testo**            | Frase, paragrafo, capitolo       | Nessuno                                            |
| **Client/server**            | Entrambi                               | Client                                          |
| **Implementazione**             | Complex                            | Semplice                                          |

**Gestori di proprietà**  I gestori di proprietà sono componenti che leggono e scrivono proprietà per un particolare formato di file. Accedono agli elementi e generano proprietà per il gatherer nello stesso modo in cui vengono applicati i filtri per il contenuto. I gestori di proprietà sono più facili da implementare rispetto ai filtri. Se un formato di file basato su testo è molto semplice o si prevede che i file siano molto piccoli, il gestore delle proprietà può generare sia proprietà che contenuto.

> [!NOTE]  
> I gestori di proprietà non sono Windows Search componenti. sono componenti correlati al formato di file specifico a cui sono progettati per l'accesso. Per altre informazioni sui gestori di proprietà e su come implementarne uno per un formato di file personalizzato, vedere Sviluppo di gestori di proprietà [per Windows Search](-search-3x-wds-extidx-propertyhandlers.md).

**Proprietà** Windows Search fornisce un [sistema di proprietà](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) che include una grande libreria di proprietà. Qualsiasi proprietà può essere visualizzata in qualsiasi elemento in base a quanto definito dal gestore del filtro o della proprietà. Se si dispone di un formato di file personalizzato, è possibile eseguire il mapping delle proprietà del formato di file a queste proprietà di sistema ed è possibile creare nuove proprietà personalizzate. Quando il gestore di filtri o proprietà genera queste proprietà, il gatherer aggiorna l'indice in modo che gli utenti possano eseguire ricerche usando le proprietà. Per altre informazioni sulla creazione e la registrazione di proprietà personalizzate per un formato di file, vedere [Sistema di proprietà.](../properties/building-property-handlers.md)

**SystemIndex**  L'indice, denominato SystemIndex, archivia i dati indicizzati ed è composto da un archivio di proprietà e da indici sulle proprietà e sul contenuto per le proprietà degli elementi e un indice invertito per il contenuto testuale e le proprietà. Dopo che il gatherer ha aggiornato l'indice, è possibile eseguire query sull'indice Windows Search e altre applicazioni. Per altre informazioni sulle modalità di esecuzione di query sull'indice, vedere [Esecuzione di query sull'indice a livello di codice.](-search-3x-wds-qryidx-overview.md)

> [!NOTE]  
> Tenere presente che quando si registra nuovamente uno schema, le modifiche apportate agli attributi delle proprietà definite in precedenza potrebbero non essere rispettate dall'indicizzatore. La soluzione consiste nel ricompilare l'indice o nell'introdurre nuove proprietà che riflettano le modifiche anziché aggiornare quelle precedenti (scelta non consigliata). Per altre informazioni, vedere [Note to Implementers](#notes-to-implementers) in [Properties System Overview.](../properties/property-system-overview.md)

## <a name="how-indexing-is-scheduled"></a>Come viene pianificata l'indicizzazione

Quando Windows Search viene installato per la prima volta, esegue un'indicizzazione completa dell'ambito della ricerca per indicizzazione, sospendo durante i periodi di attività utente e I/O elevate. L'ambito di ricerca per indicizzazione predefinito è costituito dai percorsi predefiniti delle librerie, ad esempio **Documenti,** **Musica,** **Immagini** e **Video.** Le notifiche vengono elaborate anche prima del termine della ricerca per indicizzazione iniziale. In alcuni casi, il gatherer esegue una ricerca per indicizzazione degli URL dall'ambito completo della ricerca per indicizzazione. Queste ricerche per indicizzazione complete assicurano che i dati nell'indice siano nuovi. Ad esempio, se un provider di notifiche non riesce a inviare notifiche o se il servizio Windows Search viene terminato in modo imprevisto, il gatherer non sarà a conoscenza di elementi nuovi o modificati e non indicizza tali elementi. Esistono due tipi di origini: solo notifica e notifica abilitata. In entrambe le origini, il gatherer esegue inizialmente una ricerca per indicizzazione nell'indice. Dopo la ricerca per indicizzazione iniziale, le origini di sola notifica non eseguiranno mai di nuovo una ricerca per indicizzazione completa, a meno che non si sia verificato un errore, ad esempio il roll over del journal delle modifiche [USN.](/windows/desktop/FileIO/change-journals) Le origini abilitate per le notifiche eseguono una ricerca per indicizzazione incrementale all'avvio dell'indicizzatore, ma sono in ascolto delle notifiche durante l'esecuzione. NTFS e Microsoft Outlook sono solo notifiche. Internet Explorer e FAT sono abilitati per la notifica.

## <a name="notes-to-implementers"></a>Note per gli implementatori

La qualità dei dati nell'indice e l'efficienza del processo di indicizzazione dipendono in gran parte dall'implementazione del gestore di filtri e proprietà. Poiché il filtro viene chiamato ogni volta che un URL identifica il formato di file, il processo di indicizzazione può rallentare notevolmente se il filtro è inefficiente. Se il gestore delle proprietà non esegue correttamente il mapping di tutte le proprietà del file alle proprietà di sistema o non genera correttamente queste proprietà, i dati nell'indice non saranno corretti e le ricerche successive di tali proprietà restituiranno risultati non corretti. Se il gestore di filtri o proprietà ha esito negativo, l'indicizzatore non sarà in grado di indicizzare i dati.

Applicazioni e processi diversi da Windows Search si basano su gestori di protocollo, filtri e gestori di proprietà. Le implementazioni possono influire su tali applicazioni in modi che potrebbero non essere previsti. La [Windows Search sviluppo di](-search-developers-guide-entry-page.md) applicazioni fornisce consigli sulle scelte di progettazione e sul test di ognuno di questi componenti.

## <a name="related-topics"></a>Argomenti correlati

[Indicizzazione, esecuzione di query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)

[Elementi inclusi nell'indice](-search-indexing-process-overview.md)

[Processo di query in Windows Search](querying-process--windows-search-.md)

[Processo di notifica in Windows Search](-search-3x-wds-support.md)

[Requisiti di formattazione url](url-formatting-requirements.md)
