---
description: In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti primari interessati, viene illustrato il tempo di indicizzazione dell'attività e vengono fornite alcune note per gli sviluppatori di terze parti che desiderano indicizzare gli archivi dati o i formati di file.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: Processo di indicizzazione in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87867d5925cd53b237092435bbc9d16428418b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750402"
---
# <a name="indexing-process-in-windows-search"></a>Processo di indicizzazione in Windows Search

In questo argomento vengono descritte le tre fasi del processo di indicizzazione e i componenti primari interessati, viene illustrato il tempo di indicizzazione dell'attività e vengono fornite alcune note per gli sviluppatori di terze parti che desiderano indicizzare gli archivi dati o i formati di file.

Questo argomento è organizzato nel modo seguente:

- [Overview](#overview)
- [Fase 1: accodamento degli URL per l'indicizzazione](#stage-1-queuing-urls-for-indexing)
- [Fase 2: ricerca per indicizzazione degli URL](#stage-2-crawling-urls)
- [Fase 3: aggiornamento dell'indice](#stage-3-updating-the-index)
- [Modalità di pianificazione dell'indicizzazione](#how-indexing-is-scheduled)
- [Note per gli implementatori](#notes-to-implementers)
- [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Windows Search supporta l'indicizzazione di proprietà e contenuto da file di formati di file diversi, ad esempio formati doc o JPEG e archivi dati, ad esempio le cassette postali di file system o Windows Outlook. Esistono due tipi di indici: indici di valore che consentono di filtrare e ordinare in base all'intero valore di una proprietà e indici indici che indicizzano parole all'interno di contenuto o proprietà testuali. Se si dispone di un formato di file personalizzato o di un archivio dati, è necessario comprendere il modo in cui gli indici di ricerca di Windows vengono indicizzati correttamente.

Il processo di indicizzazione si verifica in tre fasi controllate da un componente di ricerca di Windows denominato Gatherer. Nella prima fase, il Gatherer aggiunge gli URL alle code. Gli URL identificano gli elementi da indicizzare e le code sono semplicemente elenchi di URL con priorità. Nella seconda fase, il Gatherer coordina altri componenti di Windows Search e di terze parti per accedere agli elementi e raccoglierne i dati. Infine, nella terza fase, i dati raccolti vengono aggiunti all'indice.

Il diagramma seguente illustra i componenti principali e il flusso di dati tramite il processo di indicizzazione. Per la raccolta dei dati per l'indice sono necessari diversi componenti. Alcune di queste sono parte della ricerca di Windows e alcune provengono da applicazioni di terze parti. Se si dispone di un archivio dati personalizzato o di un formato di file, la ricerca di Windows si basa sul gestore di protocollo e sul filtro per l'accesso agli URL e la creazione di proprietà per l'indicizzazione. I componenti di Windows Search sono visualizzati in blu e i componenti di terze parti sono visualizzati in verde.

![diagramma che mostra l'interazione tra i componenti durante il processo di indicizzazione](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Fase 1: accodamento degli URL per l'indicizzazione

Nella prima fase dell'indicizzazione, il Gatherer raccoglie informazioni sugli aggiornamenti agli archivi dati, confronta tali informazioni con l'ambito di ricerca per indicizzazione noto e quindi compila una coda di URL da attraversare per raccogliere i dati per l'indice. Per le origini non basate sulla notifica, ad esempio le unità FAT, il Gatherer avvia periodicamente un attraversamento completo dell'ambito della ricerca per indicizzazione, in modo che i dati nell'indice rimangano aggiornati. Per le origini, ad esempio NTFS, esiste una sola ricerca per indicizzazione e tutte le altre operazioni vengono gestite dalle notifiche del [Journal delle modifiche USN](/windows/desktop/FileIO/change-journals). Non esiste neanche una ricerca per indicizzazione di Microsoft Outlook. Nel diagramma seguente viene illustrata una visualizzazione di alto livello del processo di Accodamento per l'indicizzazione non di ricerca per indicizzazione.

![diagramma che illustra il processo di query per l'indicizzazione non di ricerca per indicizzazione](images/queuingurls.jpg)

Nella parte restante di questa sezione viene illustrato come Windows Search determini quali URL eseguire la ricerca per indicizzazione e definisce alcuni termini importanti lungo il percorso.

**Ambito di ricerca per indicizzazione**  L'ambito di ricerca per indicizzazione è costituito da un set di URL che vengono attraversati dalla ricerca di Windows per raccogliere dati sugli elementi che l'utente desidera indicizzare per ricerche più veloci. Per impostazione predefinita, Windows Search aggiunge alcuni URL all'ambito di ricerca per indicizzazione, ad esempio i percorsi delle cartelle di **documenti** e **Immagini** degli utenti. È possibile aggiungere altri URL da applicazioni di terze parti, utenti e Criteri di gruppo. Infine, sia gli utenti che Criteri di gruppo possono escludere in modo esplicito gli URL. Windows Search accetta tutti gli URL aggiunti e rimuove gli URL esclusi per determinare l'ambito di ricerca per indicizzazione. Si tratta dell'working set degli URL da cui il Gatherer inizia il lavoro.

**Raccolta**  Il Gatherer è un componente di ricerca di Windows che raccoglie informazioni sugli URL nell'ambito della ricerca per indicizzazione e crea una coda di URL per l'indicizzatore per la ricerca per indicizzazione. Quando viene aggiunto, eliminato o aggiornato un elemento nell'ambito della ricerca per indicizzazione, il Gatherer riceve una notifica dal provider di notifiche dell'archivio dati. Viene avviata una ricerca per indicizzazione iniziale in corrispondenza della radice dell'ambito della ricerca. L'URL viene passato al gestore di protocollo e quindi all' [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)appropriato. Il filtro è in genere un'enumerazione di directory che produce più URL. Le notifiche sono lo stato stabile. In genere, ogni archivio dati dispone di un proprio gestore di protocollo che fornisce queste notifiche. Ad esempio, nel file system locale, il [Journal delle modifiche USN](/windows/desktop/FileIO/change-journals) funge da provider di notifiche per tutti gli URL nel protocollo file://. Analogamente, Microsoft Outlook funge da provider di notifiche per tutti gli URL nel protocollo mapi://. Quando un utente riceve, sposta o Elimina la posta elettronica, Outlook notifica al Gatherer lo stato modificato del messaggio di posta elettronica. Da queste notifiche, il Gatherer crea le code di indicizzazione degli URL per eseguire la ricerca per indicizzazione.

**Indicizzazione di code**  Le code di indicizzazione sono elenchi di URL che identificano gli elementi che devono essere indicizzati o reindicizzati. Il Gatherer confronta gli URL ricevuti dai provider di notifiche agli URL nell'ambito della ricerca per indicizzazione. Ogni URL dei provider di notifiche che rientra nell'ambito della ricerca per indicizzazione viene aggiunto a una coda utilizzata dal raccoglitore per definire le priorità degli URL da elaborare successivamente.

Sono disponibili tre code: le notifiche con priorità alta, le notifiche normali e le ricerche periodiche. La coda con priorità alta è destinata alle notifiche che devono essere elaborate immediatamente. Ad esempio, quando un utente modifica la proprietà title di un elemento in Esplora risorse, è necessario aggiornare la visualizzazione Esplora risorse immediatamente dopo la modifica. La normale coda di notifica è per tutte le notifiche di modifica rimanenti. Le code di notifica vengono elaborate prima della coda di ricerca per indicizzazione perché gli elementi modificati sono più probabili per un utente. Il Gatherer accede ai dati degli URL in ogni coda in ordine First in, First out (FIFO).

Per altre informazioni sulla definizione delle priorità e sulle API per gli eventi introdotte in Windows 7, vedere [indicizzazione delle priorità e eventi del set di righe in Windows 7](indexing-prioritization-and-rowset-events.md). Per ulteriori informazioni sulla gestione e sulle notifiche degli ambiti di ricerca, vedere la pagina relativa alla [fornitura di notifiche di modifica](-search-3x-wds-notifyingofchanges.md) e [all'utilizzo di gestione ambito ricerca](-search-3x-wds-extidx-csm.md)

## <a name="stage-2-crawling-urls"></a>Fase 2: ricerca per indicizzazione degli URL

Nella seconda fase dell'indicizzazione, il Gatherer esegue la ricerca per indicizzazione nelle code, accedendo agli archivi dati e recuperando i flussi di elementi. In primo luogo, il Gatherer trova il gestore di protocollo appropriato per ogni URL. Quindi, il Gatherer passa l'URL al gestore del protocollo. Il gestore di protocollo accede all'elemento e passa di nuovo i metadati dell'elemento al Gatherer. Il raccoglitore usa i metadati per identificare il filtro corretto.

Il diagramma seguente mostra una visualizzazione di alto livello del processo di ricerca di URL. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![diagramma che illustra il processo di ricerca per indicizzazione degli URL e accesso agli elementi](images/crawlingqueues.jpg)

Nella parte restante di questa sezione viene descritto il modo in cui Windows Search accede agli elementi per l'indicizzazione e spiega i ruoli di ognuno dei componenti interessati.

**Raccolta**  Nella fase 2, la fase di ricerca per indicizzazione, il Gatherer elabora gli URL nelle code, a partire dalla coda con priorità alta. Ogni URL viene esaminato per identificare il protocollo. Il raccoglitore cerca quindi il gestore di protocollo registrato per quel protocollo e ne crea un'istanza nel processo host del protocollo di ricerca.

**Host del protocollo di ricerca**  L'host del protocollo di ricerca è semplicemente un processo host boxed per i gestori del protocollo. In genere, la ricerca di Windows crea due processi host, uno che viene eseguito nel contesto di sicurezza del sistema e uno che viene eseguito nel contesto di sicurezza dell'utente. Questa separazione garantisce che i dati specifici di un utente non vengano mai eseguiti nel contesto di sistema.

Windows Search USA inoltre il processo host per isolare un'istanza di un gestore di protocollo da altri processi o applicazioni. In questo modo, nessuna applicazione esterna può accedere a tale istanza specifica del gestore di protocollo e, se il gestore del protocollo non riesce in modo imprevisto, solo il processo di indicizzazione è interessato. Poiché il processo host esegue codice di terze parti (gestori di protocollo), Windows Search ricicla periodicamente il processo per ridurre al minimo il tempo per cui un attacco riuscito deve sfruttare le informazioni nel processo. Oltre a questo, l'host del protocollo di ricerca non influisce sulla ricerca di URL o sull'indicizzazione di elementi.

**Gestori di protocollo**  I gestori di protocollo forniscono l'accesso agli elementi in un archivio dati usando il protocollo dell'archivio dati. Il gestore di protocollo NTFS, ad esempio, consente di accedere ai file in un'unità locale usando il protocollo file://. Il gestore di protocollo sa come attraversare l'archivio dati, identificare gli elementi nuovi o aggiornati e inviare una notifica al Gatherer. Quindi, quando inizia la ricerca per indicizzazione, il gestore di protocollo fornisce un oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) al Gatherer per eseguire l'associazione al flusso sottostante dell'elemento e restituire i metadati dell'elemento, ad esempio le restrizioni di sicurezza e l'ora dell'Ultima modifica.

> [!NOTE]  
> I gestori di protocollo non sono componenti di Windows Search; sono componenti del protocollo specifico e dell'archivio dati a cui sono progettati per l'accesso. Se si vuole indicizzare un archivio dati personalizzato, è necessario implementare un gestore di protocollo. Per altre informazioni sui gestori di protocollo e su come implementarne uno, vedere [sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md).

**Metadati e flusso**  Utilizzando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore di protocollo, il Gatherer identifica il filtro corretto per l'URL. Il raccoglitore analizza l'estensione del nome di file dell'elemento e cerca il filtro registrato per tale estensione. Se il gatherer non è in grado di trovare un filtro, Windows Search USA i metadati per derivare un set minimo di informazioni sulle proprietà di sistema, ad esempio System. ItemName, e aggiorna l'indice. In caso contrario, se il raccoglitore trova il filtro, inizia la terza fase dell'indicizzazione.

## <a name="stage-3-updating-the-index"></a>Fase 3: aggiornamento dell'indice

Nella terza fase dell'indicizzazione, il Gatherer crea un'istanza del filtro corretto per l'URL e inizializza il filtro con il flusso dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) . Il filtro accede quindi all'elemento e restituisce il contenuto per l'indice. Se si dispone di un formato di file personalizzato, Windows Search si basa sul filtro per accedere agli URL ed emettere contenuto e proprietà per l'indicizzazione.

Nel diagramma seguente viene illustrata una visualizzazione di alto livello del processo di accesso ai dati. Questa fase include un notevole coordinamento e comunicazione tra i componenti.

![diagramma che mostra i dati dell'elemento emessi per l'indice](images/filteringdata.jpg)

Nella parte restante di questa sezione viene descritto il modo in cui Windows Search accede ai dati degli elementi per l'indicizzazione e spiega i ruoli di ognuno dei componenti interessati.

**Raccolta**  All'inizio di questa fase, il ruolo del Gatherer è creare un'istanza del filtro corretto per l'elemento e passargli il flusso dell'elemento. Alla fine di questa fase, il Gatherer acquisisce il contenuto e le proprietà generati dal gestore di filtro e proprietà e aggiorna l'indice.

**Filtra host**  L'host del filtro è semplicemente un processo host per i filtri e i gestori di proprietà e offre uno scopo simile all'host del protocollo di ricerca. Il processo host isola i filtri e i gestori delle proprietà dal resto del sistema per gli stessi motivi di sicurezza e stabilità che i processi host del protocollo di ricerca isolano i gestori del protocollo. Il processo host viene eseguito con diritti minimi (non può neanche accedere al file system) ed è occasionalmente riciclato per proteggersi da attacchi alla sicurezza. Windows Search monitora inoltre l'utilizzo delle risorse in modo che, se un filtro utilizza troppe risorse, il processo host viene riciclato.

**Filtri**  I filtri sono componenti fondamentali del processo di indicizzazione che emettono informazioni sugli elementi per il Gatherer. I filtri vengono denominati in base all'interfaccia principale utilizzata nella relativa implementazione, l'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) e, di conseguenza, vengono talvolta definiti IFilters. Esistono due tipi di filtri: uno che interagisce con singoli elementi, ad esempio file, e uno che interagisce con contenitori come le cartelle. Entrambi forniscono i dati per l'indice.

Utilizzando i metadati restituiti dall'oggetto [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) del gestore di protocollo, il Gatherer identifica il filtro corretto per un URL specifico e lo passa al flusso. Il raccoglitore identifica il filtro corretto tramite un gestore di protocollo o mediante l'estensione del nome file, il tipo MIME o l'identificatore di classe (CLSID). Se l'URL punta a un contenitore, il filtro emette le proprietà per il contenitore ed enumera gli elementi nel contenitore (URL figlio). Se l'URL punta a un elemento, il filtro restituisce il contenuto testuale, se la lettura delle proprietà e sono più complesse rispetto ai gestori di proprietà. In genere, è consigliabile che i filtri creino il contenuto dell'elemento mentre i gestori delle proprietà emettono le proprietà degli elementi. Tuttavia, se il filtro deve funzionare con le applicazioni meno recenti che non riconoscono i gestori delle proprietà, è possibile implementare il filtro per creare anche proprietà.

> [!NOTE]  
> I filtri non sono componenti di Windows Search; sono componenti correlati al formato di file specifico o al contenitore a cui sono progettati per l'accesso. Per ulteriori informazioni sui filtri e su come implementarne uno per un contenitore o un formato di file personalizzato, vedere [procedure consigliate per la creazione di gestori di filtri in Windows Search](-search-3x-wds-extidx-filters.md).

Nella tabella seguente sono elencati i risultati che il Gatherer riceve da un filtro ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) e da un gestore di proprietà ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) durante il processo di indicizzazione.

|                            | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| Consenti scrittura                | No                                 | Sì                                             |
| Combinare contenuto e proprietà | Sì                                | No                                              |
| Multilingue               | Sì                                | No                                              |
| Creare collegamenti                 | Sì                                | No                                              |
| MIME                       | Sì                                | No                                              |
| Limiti del testo            | Frase, paragrafo, capitolo       | nessuno                                            |
| Client/server            | Entrambi                               | Client                                          |
| Implementazione             | Complex                            | Semplice                                          |

**Gestori di proprietà**  I gestori di proprietà sono componenti che leggono e scrivono le proprietà per un formato di file specifico. Accedono agli elementi ed emettono proprietà per il Gatherer nello stesso modo in cui i filtri eseguono il contenuto. I gestori di proprietà sono più facili da implementare rispetto ai filtri. Se un formato di file basato su testo è molto semplice o si prevede che i file siano di dimensioni molto ridotte, il gestore delle proprietà può emettere sia proprietà che contenuto.

> [!NOTE]  
> I gestori di proprietà non sono componenti di Windows Search; sono componenti correlati al formato di file specifico per cui sono progettati per l'accesso. Per altre informazioni sui gestori di proprietà e su come implementarne uno per un formato di file personalizzato, vedere [sviluppo di gestori di proprietà per la ricerca di Windows](-search-3x-wds-extidx-propertyhandlers.md).

**Proprietà** di Windows Search fornisce un [sistema di proprietà](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) che include una raccolta di proprietà di grandi dimensioni. Qualsiasi proprietà può essere visualizzata in qualsiasi elemento come definito dal gestore di filtri o proprietà. Se si dispone di un formato di file personalizzato, è possibile eseguire il mapping delle proprietà del formato di file a queste proprietà di sistema ed è possibile creare nuove proprietà personalizzate. Quando il gestore di filtro o proprietà emette queste proprietà, il Gatherer aggiorna l'indice in modo che gli utenti possano eseguire ricerche usando le proprietà. Per altre informazioni sulla creazione e la registrazione di proprietà personalizzate per un formato di file, vedere [sistema di proprietà](../properties/building-property-handlers.md).

**SystemIndex**  L'indice, denominato SystemIndex, archivia i dati indicizzati ed è costituito da un archivio delle proprietà e dagli indici delle proprietà e del contenuto per le proprietà degli elementi e da un indice invertito per le proprietà e il contenuto testuale. Quando il Gatherer aggiorna l'indice, l'indice può essere sottoposto a query da Windows Search e da altre applicazioni. Per ulteriori informazioni su come eseguire query sull'indice, vedere [esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md).

> [!NOTE]  
> Tenere presente che quando si registra di nuovo uno schema, le modifiche apportate agli attributi delle proprietà definite in precedenza potrebbero non essere rispettate dall'indicizzatore. La soluzione consiste nel ricompilare l'indice o introdurre nuove proprietà che riflettono le modifiche anziché aggiornare quelle meno recenti (scelta non consigliata). Per ulteriori informazioni, vedere la [Nota relativa agli implementatori](#notes-to-implementers) nella [Panoramica del sistema Properties](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Modalità di pianificazione dell'indicizzazione

Quando Windows Search viene installato per la prima volta, viene eseguita un'indicizzazione completa dell'ambito di ricerca per indicizzazione, che viene sospesa durante i periodi di elevata attività di I/O e dell'utente. L'ambito di ricerca per indicizzazione predefinito è costituito da percorsi di libreria predefiniti, ad esempio **documenti**, **musica**, **Immagini** e **video**. Le notifiche vengono elaborate anche prima del completamento della ricerca per indicizzazione iniziale. Occasionalmente, il Gatherer esegue la ricerca per indicizzazione degli URL dall'ambito completo. Queste ricerche per indicizzazione complete assicurano che i dati nell'indice siano aggiornati. Se, ad esempio, un provider di notifiche non riesce a inviare notifiche o se il servizio Windows Search viene terminato in modo imprevisto, il gatherer non avrà alcuna conoscenza degli elementi nuovi o modificati e non eseguirà l'indicizzazione di questi elementi. Esistono due tipi di origini: solo notifica e notifica abilitata. In entrambe le origini, il Gatherer esegue inizialmente la ricerca per indicizzazione nell'indice. Dopo la ricerca per indicizzazione iniziale, le origini di sola notifica non eseguono mai una ricerca per indicizzazione completa, a meno che non si verifichi un errore, ad esempio il rollforward del [Journal delle modifiche USN](/windows/desktop/FileIO/change-journals) . Le origini abilitate per le notifiche eseguono una ricerca per indicizzazione incrementale quando l'indicizzatore viene avviato, ma in ascolto delle notifiche durante l'esecuzione. NTFS e Microsoft Outlook sono solo notifiche. Internet Explorer e FAT sono abilitati per le notifiche.

## <a name="notes-to-implementers"></a>Note per gli implementatori

La qualità dei dati nell'indice e l'efficienza del processo di indicizzazione dipendono in gran parte dall'implementazione del gestore delle proprietà e del filtro. Poiché il filtro viene chiamato ogni volta che un URL identifica il formato di file, il processo di indicizzazione può rallentare notevolmente se il filtro non è efficiente. Se il gestore delle proprietà non esegue correttamente il mapping di tutte le proprietà del file alle proprietà di sistema o non emette correttamente queste proprietà, i dati nell'indice non saranno corretti e le ricerche successive verranno restituiti risultati non corretti. Se il gestore di filtro o di proprietà ha esito negativo, l'indicizzatore non sarà in grado di indicizzare i dati.

Le applicazioni e i processi diversi dalla ricerca di Windows si basano sui gestori di protocollo, i filtri e i gestori di proprietà. Le implementazioni possono influire su tali applicazioni in modi che potrebbero non essere previsti. La [Guida allo sviluppo di Windows Search](-search-developers-guide-entry-page.md) fornisce consigli sulle scelte di progettazione e sul test di ognuno di questi componenti.

## <a name="related-topics"></a>Argomenti correlati

[Indicizzazione, query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)

[Contenuto dell'indice](-search-indexing-process-overview.md)

[Esecuzione di query sul processo in Windows Search](querying-process--windows-search-.md)

[Processo di notifica in Windows Search](-search-3x-wds-support.md)

[Requisiti per la formattazione degli URL](url-formatting-requirements.md)
