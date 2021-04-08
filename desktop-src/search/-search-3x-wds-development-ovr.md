---
description: Per indicizzare il contenuto e le proprietà dei nuovi formati di file e degli archivi dati, è necessario estendere la ricerca di Microsoft Windows con i componenti aggiuntivi.
ms.assetid: 04ddcd97-c358-44d2-9092-a035436c50c9
title: Windows Search come piattaforma di sviluppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19041ac23c90006cc2f1b2f6146cb20a6b972fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750442"
---
# <a name="windows-search-as-a-development-platform"></a>Windows Search come piattaforma di sviluppo

Per indicizzare il contenuto e le proprietà dei nuovi formati di file e degli archivi dati, è necessario estendere la ricerca di Microsoft Windows con i componenti aggiuntivi.

Prima che uno sviluppatore di terze parti di nuovi formati di file e archivi dati possa visualizzare i formati e i negozi nei risultati della query in Esplora risorse, lo sviluppatore deve eseguire le tre operazioni seguenti:

-   Implementare un'origine dati della Shell per estendere lo spazio dei nomi della shell.
-   Esporre gli elementi in un archivio dati (se aggiungono un nuovo archivio dati, perché sarebbe necessario indicizzare).
-   Sviluppare un gestore di protocollo in modo che Windows Search possa accedere ai dati per l'indicizzazione.

Questo argomento è organizzato nel modo seguente:

-   [Per iniziare](#getting-started)
-   [Panoramica degli scenari di sviluppo della ricerca](#overview-of-search-development-scenarios)
    -   [Aggiunta di un nuovo archivio dati](#adding-a-new-data-store)
    -   [Aggiunta di un nuovo formato di file](#adding-a-new-file-format)
    -   [Utilizzo dei risultati di Windows Search](#consuming-windows-search-results)
-   [Panoramica dei gestori](#overview-of-handlers)
-   [Linee guida del programma di installazione del componente aggiuntivo](#add-in-installer-guidelines)
-   [Nota per gli implementatori](#note-to-implementers)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="getting-started"></a>Introduzione

Prima di iniziare a creare un'applicazione Windows Search, tenere presente che il modo migliore per eseguire questa operazione consiste nell'usare un'origine dati della shell. Un'origine dati della shell estende lo spazio dei nomi della shell ed espone gli elementi in un archivio dati. Gli elementi nell'archivio dati possono quindi essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo. Questo approccio indiretto per l'accesso a Windows Search mediante l'implementazione di un'origine dati Shell è preferibile perché consente l'accesso alle funzionalità complete della shell. In questo modo si garantisce un'esperienza utente ragionevole.

Se si desidera che i risultati della query vengano visualizzati in Esplora risorse, è necessario implementare un'origine dati della shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query saranno programmatiche (tramite OLE DB ad esempio) e interpretate dal codice dell'applicazione invece che dalla shell, lo spazio dei nomi della shell è comunque preferibile ma non obbligatorio.

Un gestore di protocollo è necessario per Windows per ottenere informazioni sul contenuto dei file, ad esempio elementi nei database o tipi di file personalizzati. Sebbene Windows Search possa indicizzare il nome e le proprietà del file, Windows non è in grado di conoscere il contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti nella shell di Windows. Implementando un gestore di protocollo personalizzato, è possibile esporre questi elementi. Per un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, vedere [Cenni preliminari sui gestori](#overview-of-handlers).

## <a name="overview-of-search-development-scenarios"></a>Panoramica degli scenari di sviluppo della ricerca

Gli scenari di sviluppo più comuni in ricerca di Windows sono i seguenti:

-   [Aggiunta di un nuovo archivio dati](#adding-a-new-data-store)
-   [Aggiunta di un nuovo formato di file](#adding-a-new-file-format)
-   [Utilizzo dei risultati di Windows Search](#consuming-windows-search-results)

### <a name="adding-a-new-data-store"></a>Aggiunta di un nuovo archivio dati

È necessario un archivio dati della Shell per Windows Search solo se si sta aggiungendo un nuovo archivio dati da indicizzare. Un archivio dati è un repository di dati che possono essere esposti al modello di programmazione della shell come contenitore usando un'origine dati della shell. Gli elementi in un archivio dati possono quindi essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo. Il gestore di protocollo implementa il protocollo per l'accesso a un'origine di contenuto nel formato nativo. Le interfacce [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2) vengono utilizzate per implementare un gestore di protocollo personalizzato per espandere le origini dati che possono essere indicizzate. Per informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="adding-a-new-file-format"></a>Aggiunta di un nuovo formato di file

Se si aggiunge un nuovo formato di file personalizzato, è necessario sviluppare un gestore di filtro o un gestore di proprietà, ma non entrambi. Un filtro è un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Apre i file di un tipo di file specifico e filtra le proprietà e i blocchi di testo per l'indicizzatore. I filtri sono associati ai tipi di file, come indicato dalle estensioni dei nomi di file, dai tipi MIME o dagli identificatori di classe (CLSID). Sebbene un filtro sia in grado di gestire più tipi di file, ogni tipo di file funziona con un solo filtro.

Un gestore proprietà converte i dati archiviati in un file in uno schema strutturato riconosciuto da e accessibile da Esplora risorse, Windows Search e altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà in e da un file. I dati tradotti includono la visualizzazione dettagli, infotip, il riquadro dettagli, le pagine delle proprietà e così via. Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. È necessario un gestore proprietà per eseguire le operazioni seguenti:

-   Mostra le proprietà degli elementi non indicizzati nell'interfaccia utente.
-   Supporto per la scrittura di proprietà.

### <a name="consuming-windows-search-results"></a>Utilizzo dei risultati di Windows Search

Le sezioni seguenti descrivono diversi modi per l'utilizzo dei risultati di Windows Search:

-   [Esecuzione di query sui dati](#querying-data)
-   [Esecuzione di query su archivi dati remoti (ricerca federata)](#querying-remote-data-stores-federated-search)
-   [Indicizzazione di file ed elementi](#indexing-files-and-items)
-   [Indicizzazione di un archivio dati](#indexing-a-data-store)
-   [Gestione del processo di indicizzazione](#managing-the-indexing-process)
-   [Integrazione del sistema di proprietà di Windows con le applicazioni di Windows Search](#integrating-the-windows-property-system-with-windows-search-applications)

### <a name="querying-data"></a>Esecuzione di query su dati

Gli sviluppatori che scrivono applicazioni su Windows Search combinato e il sistema di proprietà Windows possono accedere ai file e agli elementi indipendentemente dall'applicazione o dal tipo di file. Esistono due modi per accedere alle applicazioni ai dati dell'indicizzatore:

-   Le applicazioni comunicano direttamente con OLE DB inviando query di Windows Search Structured Query Language (SQL) al provider di OLE DB Windows Search per recuperare i risultati. Le query possono essere costruite manualmente o usando l'interfaccia [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) per generare le parole chiave di ricerca SQL da e la sintassi di query avanzata (AQS).
-   Le applicazioni utilizzano il livello della shell. Il vantaggio del livello della shell è che supporta anche altre origini, ad esempio grep. Tuttavia, lo svantaggio è che non tutte le funzionalità dell'indicizzatore sono disponibili.

Un'altra opzione consiste nell'usare i protocolli search-ms://e search://, che eseguono ricerche basate su URL visualizzate tramite Esplora risorse. Questa opzione consente lo sviluppo più chiaro ma non restituisce risultati o selezioni utente dalla visualizzazione risultati all'applicazione chiamante. Inoltre, analogamente ad altri protocolli, le applicazioni di ricerca di terze parti possono assumere i protocolli search-ms://e search://se le applicazioni sono conformi al set di funzionalità richiesto. Per altre informazioni sull'esecuzione di query, vedere [esecuzione di query nel processo di ricerca di Windows](querying-process--windows-search-.md) ed [esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md).

### <a name="querying-remote-data-stores-federated-search"></a>Esecuzione di query su archivi dati remoti (ricerca federata)

In Windows 7 e versioni successive, la ricerca federata offre un nuovo provider di ricerca che esegue query negli archivi dati remoti tramite server Web, tramite il protocollo [OpenSearch](https://github.com/dewitt/opensearch) ed enumera i risultati come feed RSS o Atom XML. I connettori di ricerca sono giunzioni dello spazio dei nomi che simulano il comportamento delle cartelle tramite un provider di ricerca. Per ulteriori informazioni sulla Federazione di ricerca negli archivi dati remoti in Windows 7, vedere [ricerca federata in Windows](-search-federated-search-overview.md).

### <a name="indexing-files-and-items"></a>Indicizzazione di file ed elementi

Il contenuto indicizzato è basato sul file e sui tipi di dati supportati tramite i componenti aggiuntivi inclusi nella ricerca di Windows e le regole di inclusione ed esclusione predefinite per le cartelle nel file system. Ad esempio, i filtri inclusi in ricerca finestre supportano più di 200 tipi di dati comuni, inclusi Microsoft Office documenti, posta elettronica Microsoft Outlook (insieme al gestore del protocollo MAPI), file di testo normale, HTML e molti altri. Per un elenco completo dei tipi di file supportati in modo nativo, vedere [che cosa è incluso nell'indice](-search-3x-wds-included-in-index.md).

L'indice può essere esteso con gestori di proprietà e filtri per esporre il contenuto e le proprietà dei nuovi formati di file nell'indice e in Esplora risorse. I filtri sono un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Esistono due tipi di filtri: uno che interagisce con singoli elementi, ad esempio i file e uno che interagisce con i contenitori, ad esempio le cartelle. I filtri sono multiscopo in quanto supportano la suddivisione in blocchi di dati, contenuto di testo, alcune proprietà e più lingue.

Al contrario, i gestori delle proprietà hanno uno scopo più specifico: esporre le proprietà dei tipi di file specifici identificati dalle estensioni di file. Un gestore di proprietà per un tipo di file può abilitare le proprietà Get e set e può enumerare le proprietà associate al tipo di file. A differenza dei filtri, i gestori di proprietà non supportano il mandrino di dati o il contenuto di testo e i gestori di proprietà non hanno modo di indicare la lingua in cui si trova una proprietà di testo, a meno che non supportino la scrittura delle proprietà.

### <a name="indexing-a-data-store"></a>Indicizzazione di un archivio dati

L'indice può essere esteso con i gestori di protocollo per fornire l'accesso agli archivi dati proprietari. Ad esempio, i file e gli elementi contenuti in archivi dati non di file System, ad esempio database e archivi di posta elettronica, richiedono un gestore di protocollo per eseguire il mapping da un URL a un flusso. I gestori di protocollo possono anche determinare facoltativamente i filtri corretti da usare per l'estrazione di informazioni da un flusso. I filtri enumerano gli URL dell'archivio dati. Gli elementi vengono quindi indicizzati singolarmente tramite il filtro e/o il gestore di proprietà appropriati. Per ulteriori informazioni, vedere [estensione dell'indice](-search-3x-wds-extidx-overview.md).

### <a name="managing-the-indexing-process"></a>Gestione del processo di indicizzazione

Gli sviluppatori di applicazioni possono controllare l'ambito e la frequenza dell'indicizzazione di Windows Search usando varie interfacce di gestione. Queste interfacce includono funzionalità per aggiungere e rimuovere le directory di cui l'indicizzatore Cerca le modifiche, notificare manualmente l'indice delle modifiche ai dati, verificare lo stato dell'indicizzatore e forzare nuovamente l'indicizzazione di alcuni o tutti i dati. Per altre informazioni, vedere [Managing the index](-search-3x-wds-mngidx-overview.md).

### <a name="integrating-the-windows-property-system-with-windows-search-applications"></a>Integrazione del sistema di proprietà di Windows con le applicazioni di Windows Search

Il sistema di proprietà di Windows è un sistema di lettura/scrittura estendibile di definizioni dei dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell. Il sistema di proprietà di Windows in Windows Vista e versioni successive consente di archiviare e recuperare metadati per gli elementi della shell. Un elemento della shell è costituito da qualsiasi singolo contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto. Una proprietà è una singola parte di metadati associata a un elemento della shell. I valori delle proprietà vengono espressi come una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Viene incluso un elenco completo di proprietà comuni per diversi tipi di elemento comuni, ad esempio foto, musica, documenti, messaggi, contatti e file. Gli sviluppatori possono anche introdurre le proprie proprietà sulla piattaforma se nessuna proprietà esistente soddisfa le proprie esigenze. Per ulteriori informazioni sull'integrazione di applicazioni con il sistema di proprietà di Windows, vedere [sviluppo di gestori di proprietà](-search-3x-wds-extidx-propertyhandlers.md).

## <a name="overview-of-handlers"></a>Panoramica dei gestori

Un gestore è un oggetto Component Object Model (COM) che fornisce la funzionalità per un elemento della shell. La maggior parte delle origini dati della Shell offre un sistema estensibile per l'associazione di gestori agli elementi. Ad esempio, la cartella file system usa il sistema di associazione per cercare i gestori per un tipo di file specifico. Per ogni tipo di file è necessario un gestore specifico. Per il tipo di file Adobe Acrobat. pdf è necessario un gestore di filtri, ad esempio, per il formato di file doc è necessario un altro gestore di filtro e così via.

Gestori diversi hanno alcune comunanze. In Windows Vista e versioni successive, tutti i gestori devono usare una delle interfacce seguenti per inizializzare il gestore: [**IInitializeWithStream**](/windows/win32/api/propsys/nn-propsys-iinitializewithstream), [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)o [**IItinitializeWithFile**](/windows/win32/api/propsys/nn-propsys-iinitializewithfile).

Nella tabella seguente sono elencate le attività di alto livello per gli sviluppatori, il tipo di gestore necessario per ogni attività e viene fornito un collegamento alle informazioni concettuali su come eseguire ogni attività.



| Attività                                                                                                                                                            | Gestore                          | Informazioni concettuali                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accesso alle proprietà di un file per l'indicizzazione                                                                                                                 | Gestore proprietà                 | [Sviluppo di gestori di proprietà](-search-3x-wds-extidx-propertyhandlers.md)<br/> [Proprietà definite dal sistema per formati di file personalizzati](-shell-systemdefinedpropertiesforfileformats.md)<br/> |
| Aggiunta di formati degli Appunti per l'oggetto dati ([**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)) di un elemento (gli oggetti dati vengono utilizzati negli scenari di trascinamento della selezione e di copia e incolla). | Gestore dell'oggetto dati              | [Creazione di gestori di dati](/previous-versions/windows/desktop/legacy/cc144163(v=vs.85))                                                                                                                                                          |
| Aggiunta di verbi per un elemento comunemente visualizzato in un menu di scelta rapida                                                                                         | Gestore del menu di scelta rapida            | [Creazione di gestori di menu di scelta rapida](../shell/context-menu-handlers.md)<br/> [Personalizzazione di un menu di scelta rapida tramite verbi dinamici](../shell/shortcut-menu-using-dynamic-verbs.md)<br/>                         |
| Associazione di un tipo di file a un'icona specifica                                                                                                                    | Gestore icone                     | [Creazione di gestori di icone](../shell/how-to-create-icon-handlers.md)                                                                                                                                                          |
| Creazione di finestre delle proprietà con le immagini e i controlli dell'interfaccia utente che consentono l'interazione personalizzata con un tipo di file                                                          | Gestore della finestra delle proprietà           | [Gestori della finestra delle proprietà](/previous-versions/windows/desktop/legacy/cc144106(v=vs.85))                                                                                                                                                    |
| Abilitazione di un tipo di elemento per supportare scenari di trascinamento della selezione e di copia e incolla                                                                                         | Gestore di trascinamento                     | [Trasferimento di oggetti Shell con trascinamento della selezione e degli Appunti](/previous-versions/windows/desktop/legacy/bb776905(v=vs.85))                                                                                                                      |
| Estrazione di blocchi di proprietà Text e Document per l'indicizzazione                                                                                                  | Gestore filtro                   | [Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)                                                                                                                                           |
| Indicizzazione di un nuovo tipo di file                                                                                                                                        | Gestore di filtro, gestore proprietà | [Sviluppo di gestori di filtri](-search-ifilter-conceptual.md)<br/> [Sviluppo di gestori di proprietà](-search-3x-wds-extidx-propertyhandlers.md)<br/>                                          |
| Indicizzazione del contenuto di un archivio dati                                                                                                                           | Protocol handler                 | [Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)                                                                                                                                            |
| Visualizzazione in anteprima di una visualizzazione semplificata dell'elemento della shell nel riquadro di anteprima di Esplora risorse                                                                             | Gestore di anteprime                  | [Gestori di anteprime](../shell/preview-handlers.md)                                                                                                                                                             |
| Fornire il testo popup quando si passa il mouse su un oggetto dell'interfaccia utente                                                                                                      | Gestore della finestra popup                  | [Creazione di gestori di estensioni della shell](../shell/handlers.md) (personalizzazione infotip)                                                                                                                            |
| Fornire un'immagine statica per rappresentare un elemento della shell                                                                                                              | Gestore anteprime                | [Gestori di anteprime](/previous-versions/windows/desktop/legacy/cc144118(v=vs.85))                                                                                                                                                        |



 

Nella tabella seguente sono elencati i gestori e le interfacce per l'implementazione di ogni tipo di gestore.



| Gestore                | Interfacce                                                                                                                                                                                                                                                                                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestore di trascinamento           | [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget), [**IDropTargetHelper**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-idroptargethelper), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                      |
| Gestore dell'oggetto dati    | [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject), [ **IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)                                                                                                                                                                                                                                                                                                  |
| Gestore filtro         | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)<br/>                                                                                                                                                                                                                                                                                                                             |
| Gestore icone           | [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)<br/> Facoltativo: [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)<br/>                                                                                                                                                                                                                                 |
| Gestore della finestra popup        | [**IQueryInfo**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                                                                                                                                                                                                                                                                                                                                        |
| Gestore di anteprime        | [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)                                                                                                                                                                                                                                                                                                                              |
| Gestore proprietà       | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                                           |
| Protocol handler       | [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), [**ISearchProtocol**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol), [**IUrlAccessor**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor)<br/> Facoltativo: [**ISearchProtocol2**](/windows/win32/api/Searchapi/nn-searchapi-isearchprotocol2), [**IUrlAccessor2**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor2), [**IUrlAccessor3**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor3), [**IUrlAccessor4**](/windows/win32/api/Searchapi/nn-searchapi-iurlaccessor4)<br/> |
| Gestore della finestra delle proprietà | [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit), [ **IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)                                                                                                                                                                                                                                                                              |
| Gestore del menu di scelta rapida  | [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu), [**IExplorerCommand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iexplorercommand), [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)                                                                                                                                                                                                                                          |
| Gestore anteprime      | [**IThumbnailProvider**](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider)                                                                                                                                                                                                                                                                                                                        |



 

> [!Note]  
> Un gestore di proprietà è talvolta kown come gestore di metadati. Un'origine dati della shell è talvolta nota come estensione dello spazio dei nomi della shell. Un gestore di tipi di file è talvolta noto come gestore di estensione della shell o estensione della shell.

 

Per ulteriori informazioni sulla creazione di gestori, vedere [creazione di gestori di estensioni shell](../shell/handlers.md). Per ulteriori informazioni sulle proprietà, vedere [Windows Property System](../properties/windows-properties-system.md).

## <a name="add-in-installer-guidelines"></a>Linee guida del programma di installazione del componente aggiuntivo

Quando si crea un programma di installazione di un componente aggiuntivo, attenersi alle seguenti linee guida:

-   Il programma di installazione deve usare il programma di installazione EXE o MSI.
-   È necessario fornire le note sulla versione.
-   È necessario creare una voce di installazione **applicazioni** per ogni componente aggiuntivo installato.
-   Il programma di installazione deve assumere tutte le impostazioni del registro di sistema per il tipo di file o l'archivio specifico che il componente aggiuntivo corrente riconosce.
-   Se un componente aggiuntivo precedente viene sovrascritto, il programma di installazione deve inviare una notifica all'utente.
-   Se un componente aggiuntivo più recente ha sovrascritto un componente aggiuntivo precedente, l'utente deve essere in grado di ripristinare la funzionalità del componente aggiuntivo precedente e renderlo di nuovo il componente aggiuntivo predefinito per quel tipo di file o archivio.

## <a name="note-to-implementers"></a>Nota per gli implementatori

Prima di creare un gestore di filtro o di proprietà, gli sviluppatori devono considerare quanto segue:

-   Questi gestori sono estensioni in-process caricate in processi che non si controllano, ad esempio il processo del daemon di filtri, Esplora risorse (ricerca grep) e host di terze parti come Windows Mail.
-   È necessario scrivere codice sicuro sufficientemente solido da gestire forme arbitrariamente danneggiate del formato di file creato per attaccare il sistema.
-   Il componente aggiuntivo non deve perdere risorse che genereranno problemi per i processi host.
-   Il componente aggiuntivo non deve arrestarsi in modo anomalo perché questo arresterà in modo anomalo anche i processi host e rallenterà il processo di filtraggio.
-   Poiché questi gestori vengono eseguiti in un processo di sistema in background, devono essere eseguiti rapidamente con un minimo di CPU e I/O utilizzati per soddisfare i requisiti di prestazioni del sistema.

Quindi, questi componenti aggiuntivi devono essere scritti dagli sviluppatori con esperienza nella creazione di codice a livello di sistema.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sulla creazione di un'origine dati della shell, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).
-   Per le origini dati che devono usare l'oggetto della visualizzazione cartella di sistema (DefView) predefinito della shell, vedere [Implementing a Folder View](../lwef/nse-folderview.md), [**SHCreateShellFolderView**](/windows/win32/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview) Function e [**SFV \_ create**](/windows/win32/api/shlobj_core/ns-shlobj_core-sfv_create) structure. Le origini dati che usano l'oggetto di visualizzazione della cartella di sistema (DefView) predefinito della shell devono implementare il set di interfacce seguente: [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IShellFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder2), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder), [**IPersistFolder2**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2)e (facoltativamente) [**IPersistFolder3**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3). Se l'implementazione di **IShellFolder** non utilizza **SHCreateShellFolderView** per creare il DefView, è possibile che sia necessario [**IFolderView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifolderview)per l'oggetto visualizzazione Shell.
-   [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) è l'interfaccia principale per i consumer dell'origine dati della shell nota come DBFolder. Per ulteriori informazioni su DBFolder, vedere la descrizione dell'analisi STR \_ \_ con \_ proprietà costante nelle chiavi di [**stringa del contesto di binding**](../shell/str-constants.md). Vedere anche [array di associazioni](/previous-versions/windows/desktop/legacy/ee872122(v=vs.85)) e [**IPropertySystem:: GetPropertyDescriptionListFromString**](/windows/win32/api/propsys/nf-propsys-ipropertysystem-getpropertydescriptionlistfromstring).
-   Per informazioni su OLE DB, vedere [Cenni preliminari sulla programmazione OLE DB](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Per informazioni sul provider di dati di .NET Framework per OLE DB, vedere la documentazione [dello spazio dei nomi System. Data. OleDb](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .
-   Per bacheche dei messaggi supportati dalla community sulle tecnologie di ricerca, vedere la pagina relativa alla [ricerca nei forum](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads) MSDN su Windows.
-   Per esempi di codice correlati, vedere [esempi di codice di Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Lingue supportate da Windows Search](-search-3x-wds-language-support.md)
</dt> <dt>

[Uso di codice gestito con i dati della shell e Windows Search](-search-3x-wds-managed-code.md)
</dt> <dt>

[Guida per gli sviluppatori di Windows Search](-search-developers-guide-entry-page.md)
</dt> </dl>

 

 
