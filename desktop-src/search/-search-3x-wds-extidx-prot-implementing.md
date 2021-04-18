---
description: Alcune applicazioni archiviano gli elementi in database o tipi di file personalizzati.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Informazioni sui gestori di protocollo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306187"
---
# <a name="understanding-protocol-handlers"></a>Informazioni sui gestori di protocollo

Alcune applicazioni archiviano gli elementi in database o tipi di file personalizzati. Sebbene Windows Search possa indicizzare il nome e le proprietà del file, Windows non è in grado di conoscere il contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti nella shell di Windows. Creando un gestore di protocollo è possibile rendere disponibili questi elementi per l'indicizzazione. È inoltre possibile indicizzare un formato di file composto, ad esempio un file con estensione zip.

Questo argomento è organizzato nel modo seguente:

-   [Indicizzazione di archivi dati con gestori di protocollo](#indexing-data-stores-with-protocol-handlers)
    -   [Archivi dati della shell](#shell-data-stores)
    -   [Gestori del protocollo](#protocol-handlers)
    -   [Filtri e gestori di protocollo](#filters-and-protocol-handlers)
-   [Indicizzazione di un formato di file composto](#indexing-a-compound-file-format)
-   [Argomenti correlati](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indicizzazione di archivi dati con gestori di protocollo

Quando gli utenti devono eseguire ricerche in database legacy, archivi di posta elettronica o altre strutture di dati che non sono supportate da Windows Search, è necessario innanzitutto determinare se un gestore di protocollo esiste già per quell'archivio dati, ad esempio per l'uso con un'altra applicazione, ad esempio SharePoint Server. In tal caso, è possibile installare il gestore di protocollo nel sistema. I gestori del protocollo di ricerca di Windows utilizzano specifiche di progettazione simili a quelle di SharePoint Server e spesso possono essere utilizzati in modo interscambiabile.

Per ulteriori informazioni sulla distribuzione di Search Server 2008 con Office SharePoint Server 2007, vedere la pagina relativa alla ricerca [federata nel \[ server \] 2008](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Archivi dati della shell

Prima che uno sviluppatore di terze parti di nuovi formati di file e archivi dati possa visualizzare i formati e i negozi nei risultati della query in Esplora risorse, lo sviluppatore deve implementare un'origine dati della shell. Un'origine dati della shell è un componente usato per estendere lo spazio dei nomi della shell ed esporre gli elementi in un archivio dati. Un archivio dati è un repository di dati. Un archivio dati può essere esposto al modello di programmazione della shell come contenitore che usa un'origine dati della shell. Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo. Il gestore di protocollo implementa il protocollo per l'accesso a un'origine di contenuto nel formato nativo. Le interfacce [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) e [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) vengono utilizzate per implementare un gestore di protocollo personalizzato per espandere le origini dati che possono essere indicizzate.

Se si desidera che i risultati della query vengano visualizzati in Esplora risorse, è necessario implementare un'origine dati della shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query saranno a livello di codice (tramite OLE DB ad esempio) e interpretate dal codice dell'applicazione anziché dalla shell, uno spazio dei nomi della shell ancora preferito non è strettamente necessario.

> [!Note]  
> Un'origine dati della shell è talvolta nota come estensione dello spazio dei nomi della shell. Un gestore è talvolta noto come estensione della shell o gestore di estensione della shell.

 

Se si desidera che gli utenti visualizzano i risultati della ricerca in Esplora risorse, è necessario creare un gestore di protocollo e uno o più dei componenti aggiuntivi seguenti:

-   Gestore del menu di scelta rapida
-   Gestore icone
-   Un altro tipo di gestore di file

Per un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in [Windows Search come piattaforma di sviluppo](-search-3x-wds-development-ovr.md). Per informazioni sulla creazione di gestori, vedere [registrazione di estensioni della shell](../shell/reg-shell-exts.md), [menu di scelta rapida](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))e [gestori di tipi di file](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Gestori del protocollo

Se l'archivio dati è anche un contenitore, ad esempio una cartella di file system, è necessario implementare un filtro per enumerare gli URL nel contenitore. Se l'archivio dati contiene tipi di dati o di file diversi da uno dei tipi di file 200 supportati da Windows Search, è necessario implementare un filtro per accedere e indicizzare il contenuto degli elementi nell'archivio. Windows Search usa il gestore di protocollo e la tecnologia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) analoga a quella usata da SharePoint Server. Se sono già presenti filtri per un archivio specifico e un tipo di file installati nel sistema indicizzato, è possibile che Windows Search sia in grado di utilizzare le interfacce esistenti per indicizzare i dati.

Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md). Per informazioni concettuali sui gestori di filtri, vedere [sviluppo di gestori di filtri](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filtri e gestori di protocollo

I gestori di protocollo consentono all'indicizzatore di ricerca di Windows di accedere agli archivi dati, consentendo all'indicizzatore di eseguire la ricerca per indicizzazione dei nodi di un archivio dati ed estrarre le informazioni rilevanti da indicizzare. Windows Search, ad esempio, viene fornito con gestori di protocollo per gli archivi file system e per alcune versioni di entrambi gli archivi dati di Microsoft Outlook. Quando si indicizza la posta elettronica di Outlook, il gestore di protocollo esegue la ricerca per indicizzazione di tutti i messaggi in un set di cartelle di Outlook ed estrae informazioni da ogni messaggio e allegato. Queste informazioni vengono passate all'indicizzatore per l'inclusione nel catalogo di Windows Search.

Per panoramiche su Gestione cataloghi e gestione ambito ricerca per indicizzazione, vedere [utilizzo di gestione cataloghi](-search-3x-wds-mngidx-catalog-manager.md) e [utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indicizzazione di un formato di file composto

Un formato di file composto può essere indicizzato in modo che i singoli elementi nel file possano essere restituiti come singoli risultati. Un formato di file composto, ad esempio un file compresso con estensione zip, è essenzialmente un archivio dati e può essere considerato come tale, per finalità di indicizzazione. Nell'esempio seguente viene visualizzato un file con estensione zip nello spazio dei nomi file system (FILE://c:/test/test.zip) in cui sono presenti sia sottocartelle che singoli elementi.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

Il gestore del protocollo FILE rileva quando FILE://c:/test/test.zip modifiche monitorando file system log delle modifiche e richiamerà un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) registrato per i file con estensione zip in tale file quando il file viene modificato, ma non conosce la struttura interna del file con estensione zip.

È necessario informare l'indicizzatore che il formato di file composto è un archivio dati. È necessario fare in modo che i singoli elementi vengano indicizzati e recuperati come entità univoche. Dopo aver implementato un'origine dati della shell ed eseguito i passaggi seguenti, si disporrà di un gestore di protocollo che può elaborare ed esporre i dati da un formato di file composto (un file con estensione zip) come singoli elementi.

**Per informare l'indicizzatore che un file composto è un archivio dati:**

1.  Creare un gestore di protocollo (usando [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) o [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) per i file con estensione zip che hanno la possibilità di eseguire l'associazione al file di origine. Per ulteriori informazioni, vedere [installazione e registrazione dei gestori di protocollo](-search-3x-wds-ph-install-registration.md).

    Ad esempio, è possibile usare un percorso di escape del file con estensione zip come nome della cartella radice e quindi usare una sintassi della gerarchia come qualsiasi altro formato di file.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Usando i dati di esempio precedenti per c: \\ test \\test.zip, gli URL univoci sono i seguenti. Con questi URL, il gestore di protocollo dispone delle informazioni necessarie per eseguire l'associazione al file zip ed enumerare gli URL figlio, inclusi i file interni, in modo che possano essere associati e indicizzati dai filtri doc e txt.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Verificare che il gestore di protocollo soddisfi le due condizioni seguenti:
    -   Gli URL radice per un file con estensione zip devono creare PKEY \_ Search \_ IsClosedDirectory ([System. search. IsClosedDirectory](../properties/props-system-search-iscloseddirectory.md)) sugli URL che corrispondono agli URL del file con estensione zip radice. Ad esempio,. zip:///FILE:%2f%2f%2fc:%2ftest% 2ftest.zip/deve creare IsClosedDirectory = **true**. In questo modo l'indicizzatore indica che se la data in questo URL non è stata modificata, non è necessario elaborare alcun URL figlio.
    -   Ogni URL figlio per tale URL deve creare PKEY \_ Search \_ IsFullyContained ([System. search. IsFullyContained](../properties/props-system-search-isfullycontained.md)) sugli URL figlio dell'URL root. zip. Normalmente alla fine di una ricerca per indicizzazione incrementale, l'indicizzatore considera tutti gli URL non visitati come elementi che devono essere eliminati. Il file con estensione zip radice, tuttavia, non deve elaborare URL radice perché non è stato modificato nulla. La creazione di questa proprietà su **true** indica all'indicizzatore che se l'URL non è stato elaborato alla fine di una ricerca per indicizzazione incrementale, non deve essere eliminato. Verrà eliminato solo se l'elemento radice è stato modificato e non viene visitato.

Windows Search richiede una pagina iniziale per un protocollo per sapere quali URL eseguire la ricerca per indicizzazione in modo incrementale e quali URL devono essere ignorati quando vengono trovati. Non è tuttavia possibile iniziare con un URL per ogni file zip, perché non è noto dove si trova ogni file zip. Di conseguenza, l'URL della pagina iniziale del gestore del protocollo zip deve essere in grado di enumerare tutti gli elementi alla radice dei percorsi di escape di tutti i file con estensione zip. I file zip non sono necessariamente nel FILE: namespace e possono essere un URL di tipo MAPI che punta a un file con estensione zip come allegato, ad esempio.

**Per registrare una radice come pagina iniziale:**

1.  Registrare una radice, ad esempio zip:///, come pagina iniziale in modo che tutti i file con estensione zip partano, in effetti. Quando si elabora l'URL root. zip:, il gestore di protocollo deve generare l'elenco di URL figlio da emettere eseguendo una query su ricerca di Windows per tutti gli URL con System. FileExtension = ". zip".
2.  Eseguire l'escape degli URL per rimuovere le barre e restituirle come URL figlio. Una query di esempio per recuperare i tipi desiderati potrebbe avere un aspetto simile al seguente.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Quando Windows Search esegue periodicamente una ricerca per indicizzazione incrementale sull'URL radice. zip:///, è necessario rispecchiare l'elenco di URL che Windows Search sta già gestendo con URL. zip. Se un'eliminazione viene individuata nell'archivio nativo in cui è archiviato il file zip, non viene visualizzata nell'enumerazione e il ramo dell'albero nel file zip viene rimosso.
4.  Per eseguire il binding ai dati con estensione zip per un altro gestore di protocollo, è consigliabile passare attraverso la [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) per l'URL per l'associazione all'archiviazione dell'oggetto e non presupporre che si tratta sempre di un file. In questo modo si garantisce la flessibilità necessaria per lavorare con gli allegati negli archivi di posta elettronica, ad esempio.
5.  Quando si creano URL figlio per ogni file con estensione zip, è necessario usare PKEY \_ Search \_ UrlToIndexWithModificationTime ([System. search. UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md)) per passare pkey \_ DateModified ([System. DateModified](../properties/props-system-datemodified.md)) del file con estensione zip effettivo, in modo che l'indicizzatore indicizzazione del file con estensione zip solo se è stato modificato.

Per eseguire l'indicizzazione degli URL. zip immediatamente dopo la creazione o la modifica e non è necessario attendere la ricerca di una ricerca per indicizzazione incrementale per individuare il nuovo stato, è possibile monitorare il file system per le modifiche del file con estensione zip. Questo approccio, tuttavia, non funziona per altri archivi dati, ad esempio MAPI.

**Per indicizzare gli URL con estensione zip quando vengono creati o modificati:**

1.  Creare un filtro (e l'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) per il tipo di file zip. Per altre informazioni, vedere [sviluppo di gestori di proprietà per la ricerca di Windows](-search-3x-wds-extidx-propertyhandlers.md).
2.  Ogni volta che l'implementazione di [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) viene chiamata, è perché tale URL è stato individuato o modificato. Generare quindi un evento per l'URL. zip appropriato per l'URL di origine tramite l'interfaccia [**IGatherNotifyInline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) . Questa operazione consente di indicare immediatamente all'indicizzatore che sono presenti nuovi dati da indicizzare senza dover attendere la ricerca per indicizzazione incrementale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Aggiunta di icone e menu di scelta rapida](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Esempio di codice: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
