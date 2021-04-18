---
description: Il sistema di proprietà di Windows è un sistema di lettura/scrittura estendibile di definizioni dei dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Panoramica del sistema di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab3a17eacdbaa9a5d0255004ba544b7c3f7ff2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310106"
---
# <a name="property-system-overview"></a>Panoramica del sistema di proprietà

Il sistema di proprietà di Windows è un sistema di lettura/scrittura estendibile di definizioni dei dati che fornisce un modo uniforme per esprimere i metadati sugli elementi della shell. Il sistema di proprietà di Windows in Windows Vista e versioni successive consente di archiviare e recuperare metadati per gli elementi della shell. Un elemento della shell è costituito da qualsiasi singolo contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto. Una proprietà è una singola parte di metadati associata a un elemento della shell. I valori delle proprietà vengono espressi come una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Questo argomento è organizzato nel modo seguente:

-   [Introduzione](#introduction)
-   [Scenari di sviluppo](#development-scenarios)
-   [Proprietà e Windows Search](#properties-and-windows-search)
-   [Nota per gli implementatori](#note-to-implementers)
-   [Documentazione del sistema di proprietà di Windows](#windows-property-system-documentation)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Le proprietà vengono identificate in modo univoco in base al nome canonico (ad esempio `System.Document.LastAuthor` ) e alla chiave della proprietà (ad esempio `PKEY_Document_LastAuthor` ). Una chiave di proprietà (PKEY) è la parte del nome di una coppia nome-valore costituita da un PKEY/PROPVARIANT o da una stringa/PROPVARIANT, in cui la stringa è il nome canonico del PKEY (ad esempio `System.Document.LastAuthor` ). Un PKEY è una definizione che indica al sistema di proprietà tutto ciò che è necessario conoscere sulla proprietà, mentre il valore è un'istanza effettiva della proprietà. Un PKEY contiene internamente un formatID e propID.

Una singola proprietà è costituita dalle tre parti seguenti:

-   Nome canonico, ad esempio `System.Music.Artist` .
-   Descrizione dello schema, specificata nel formato di file XML con estensione propdesc ed espressa a livello di codice tramite [**IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Valore, ad esempio il nome di un cantante.

La descrizione dello schema è costituita da informazioni sulla proprietà, ad esempio il nome della proprietà, il tipo di dati, i vincoli, le informazioni sul modo in cui la proprietà interagisce con le visualizzazioni e il sistema di ricerca e così via. Il nome e la descrizione dello schema sono definiti a livello globale e sono gli stessi per tutti gli elementi e i tipi. Un valore è specifico di un singolo elemento. Ovvero, la `System.Music.Artist` proprietà è sempre definita come stringa multivalore, ma può avere un valore diverso (o nessun valore) per ogni elemento.

Un gestore proprietà converte i dati archiviati in un file in uno schema strutturato riconosciuto da e accessibile da Esplora risorse, Windows Search e altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file. I dati tradotti vengono esposti a livello di codice e visualizzati all'utente tramite Esplora risorse in diversi contesti, tra cui la visualizzazione dettagli, infotip, il riquadro dei dettagli, le pagine delle proprietà e così via. Ogni gestore di proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. Gli sviluppatori devono implementare un gestore di proprietà che produce e utilizza il formato nativo del tipo di file, ad esempio. jpg o. png, oppure utilizza l'In-Memory archivio delle proprietà, che produce e utilizza il formato binario MS-PROPSTORE.

Il sistema di proprietà di Windows crea un modello di dati astratto che fornisce un livello di astrazione dai singoli formati di file. Il modello di dati astratto fornito dal sistema di proprietà di Windows è un metodo per la lettura e la scrittura di un set estensibile di valori denominati associati a un elemento della shell. L'espressione valore è flessibile, supporta molti tipi di dati ed è estendibile, abilitando i dati arbitrari (**\_ BLOB VT**) e gli oggetti da esprimere come valore.

A causa dell'astrazione, è possibile eseguire una query sugli attributi o sui metadati di qualsiasi elemento. Esempi di elementi che possono essere estratti includono Microsoft Office documenti, tag ID3 e AutoCAD e altro software proprietario di terze parti. Analogamente, se si dispone di un file con estensione JPEG, è possibile usare i codec. jpeg e EXIF per leggere i byte del file per individuare le dimensioni dell'immagine. Se invece si dispone di un file con estensione png, è necessario disporre di un codec diverso e di codice diverso. L'utilizzo del sistema di proprietà di Windows evita questo tipo di problema. Se si implementa un nuovo tipo di file, è possibile inserire l'astrazione uniforme offerta dal sistema di proprietà di Windows e specificare la modalità di utilizzo dei metadati. Per questi motivi, è sempre preferibile usare la piattaforma comune fornita dal sistema di proprietà di Windows.

## <a name="development-scenarios"></a>Scenari di sviluppo

Le proprietà sono espresse dai producer e dagli utenti. In questo contesto, i producer sono gli inventori delle proprietà nel sistema di proprietà di Windows e gli utenti sono applicazioni (e i relativi sviluppatori) che utilizzano le informazioni sulle proprietà di questo sistema. Nella tabella seguente vengono indicati gli utilizzi di e dei partecipanti al sistema di proprietà di Windows.



| Uso del sistema di proprietà di Windows                                                                                                                                                                                            | Partecipante |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Un blocco predefinito che fornisce un registro estensibile di descrizioni delle proprietà, un'implementazione di archivio delle proprietà in memoria e i servizi per l'associazione ai gestori di proprietà, alla conversione di tipi e alla serializzazione degli archivi delle proprietà. | Consumer    |
| Applicazioni che desiderano leggere e scrivere le proprietà in modo astratto.                                                                                                                                                       | Consumer    |
| Inventori di proprietà che definiscono nuove proprietà per il sistema di proprietà definendo schemi di proprietà personalizzati e sviluppando i propri gestori di proprietà.                                                                          | Producer    |
| Proprietari del formato di file che desiderano consentire l'accesso alle proprietà archiviate nei formati di file personalizzati.                                                                                                                           | Producer    |



 

I consumer utilizzano proprietà, schemi e gestori di proprietà esistenti. Le proprietà disponibili per l'utilizzo includono le proprietà di lettura/scrittura dai gestori di proprietà per i tipi di file supportati e possono includere anche alcune proprietà personalizzate. Gli schemi disponibili includono almeno lo schema del sistema e talvolta anche altri. Un consumer può creare un'applicazione per utilizzare i metadati e creare una vista basata sull'artista, indipendentemente dalle cartelle in cui sono archiviati gli elementi. La gerarchia di cartelle di file è irrilevante. Ad esempio, è possibile specificare tutti gli elementi del brano da un particolare cantante senza preoccuparsi della posizione di tali elementi. Questo complesso scenario end-to-end non è limitato al sistema di proprietà di Windows, ma prevede diversi componenti, ad esempio le cartelle indicizzazione e ricerca.

Gli inventori di proprietà o gli sviluppatori di terze parti sono produttori del sistema di proprietà di Windows. Quando si prepara la definizione di una nuova proprietà, controllare innanzitutto il set di proprietà definite da Windows. Se ne viene trovato uno che soddisfi le proprie esigenze, del tipo e della semantica corrispondenti all'uso necessario, usare tale proprietà e non inventarne una nuova. Se si definisce una nuova proprietà personalizzata, provare a ottenere un accordo con altri sviluppatori che desiderano utilizzarlo e pubblicare il risultato del presente contratto in modo che possano partecipare alla community degli utenti di tale proprietà.

I produttori possono sfruttare le funzionalità di Esplora risorse di Windows. Se, ad esempio, si sta scrivendo un nuovo formato di immagine e si implementa un gestore di proprietà, il nuovo formato di file diventa disponibile in Esplora risorse. Gli utenti possono quindi contrassegnare le proprie fotografie e trasformare la propria raccolta di fotografie in base a qualsiasi proprietà nel sistema di proprietà di Windows. In realtà, qualsiasi operazione eseguita da shell con le proprietà, gli sviluppatori di terze parti possono eseguire nelle proprie applicazioni. Sono inclusi il raggruppamento, l'ordinamento, l'esecuzione di query e la visualizzazione delle proprietà complete. L'esperienza utente fornita da Esplora risorse può essere ampiamente implementata da terze parti con API disponibili pubblicamente. Esplora risorse può essere sostituito o esteso con queste API.

Dal punto di vista di un'applicazione che usa il modello di dati della shell, esiste una vasta gamma di scenari che implicano l'uso del sistema di proprietà di Windows. Le applicazioni di gestione del supporto sono un esempio importante. Gli scenari di sistema di proprietà principali includono scenari come la lettura della proprietà keyword di una fotografia o l'impostazione della proprietà DateTaken. Esempi di scenari di integrazione end-to-end abilitati dal sistema di proprietà di Windows, ma che richiedono la funzione di diversi altri componenti, includono la visualizzazione di tutte le immagini o la ricerca di un documento che contiene una parola chiave.

## <a name="properties-and-windows-search"></a>Proprietà e Windows Search

Le proprietà servono sia Producer che consumer quando si interfacciano con la ricerca di Windows e l'indicizzazione. Windows Search include una cache di valori di proprietà utilizzati nell'implementazione di Windows servizio di ricerca (WSS). Questi valori di proprietà possono essere sottoposti a query a livello di codice tramite il provider di OLE DB di ricerca di Windows o tramite [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query. Windows Search raccoglie e archivia le proprietà generate dai gestori di filtro o dai gestori di proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

> [!Note]  
> Tenere presente che quando si registra nuovamente uno schema, le modifiche apportate agli attributi delle proprietà definite in precedenza potrebbero non essere rispettate dall'indicizzatore. La soluzione consiste nel ricompilare l'indice o introdurre nuove proprietà che riflettono le modifiche anziché aggiornare quelle meno recenti (scelta non consigliata). Per ulteriori informazioni, vedere la [Nota sugli implementatori](#note-to-implementers) più avanti in questo argomento.

 

Ad esempio, uno sviluppatore che crea un'applicazione multimediale vuole mostrare agli utenti dell'applicazione tutta la musica disponibile da un particolare artista. L'applicazione fornirà all'utente un elenco di artisti disponibili e quindi genererà un elenco di tutte le musiche disponibili dall'artista selezionato dall'utente. Oppure un utente finale potrebbe voler eseguire una query per? Artist: Beethoven? ed essere esposto all'elenco completo delle proprietà disponibili nel corso della ricerca. Questo esempio prevede l'uso dello spazio dei nomi della shell, dei gestori di proprietà e/o dell'esecuzione di query sull'indice tramite uno dei seguenti elementi:

-   Origine dati della shell.
-   Provider OLE DB.
-   Un file di ricerca salvato (. search-ms) usato per avviare una query passando al file di ricerca in Esplora risorse o il binding a [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) a livello di codice.

> [!Note]  
> Sebbene la `System.Kind` proprietà non partecipi a questo scenario di applicazione multimediale, può essere usata per compilare una query che restituisce tutti i file. search-ms in un determinato ambito.

 

Il modo migliore per accedere alle API di ricerca e creare applicazioni Windows Search consiste nell'usare un'origine dati della shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) è un componente che consente di creare istanze dell'origine dati della cartella di ricerca, ovvero un tipo di origine dati "virtuale" fornita dalla shell che può eseguire query su altre origini dati nello spazio dei nomi della shell ed enumerare i risultati. Questa operazione può essere eseguita utilizzando l'indicizzatore o enumerando e ispezionando manualmente gli elementi negli ambiti specificati.

Gli sviluppatori di terze parti possono creare applicazioni che utilizzano i dati nell'indice tramite query a livello di codice e possono estendere i dati nell'indice per i tipi di file e di elemento personalizzati che devono essere indicizzati da ricerca di Windows. Se si desidera visualizzare i risultati della query in Esplora risorse, è necessario implementare un'origine dati della shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query saranno programmatiche (tramite OLE DB ad esempio) e interpretate dal codice dell'applicazione? invece che dalla shell, lo spazio dei nomi della shell è comunque preferibile ma non obbligatorio. Un gestore di protocollo è necessario per Windows per ottenere informazioni sul contenuto dei file, ad esempio elementi nei database o tipi di file personalizzati. Sebbene Windows Search possa indicizzare il nome e le proprietà del file, Windows non contiene informazioni sul contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti nella shell di Windows. Implementando un gestore di protocollo personalizzato, è possibile esporre questi elementi. Per un elenco di gestori identificato dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in [Windows Search come piattaforma di sviluppo](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Un'origine dati della shell è talvolta nota come estensione dello spazio dei nomi della shell. Un gestore è talvolta noto come estensione della shell o gestore di estensione della shell.

 

## <a name="note-to-implementers"></a>Nota per gli implementatori

A causa di potenziali problemi che l'indicizzatore potrebbe avere quando si utilizza lo schema del sistema di proprietà, è fondamentale definire gli attributi in modo accurato e strategico per il primo rilascio dello schema. Eventuali modifiche apportate agli attributi (tipo, larghezza delle colonne, se indicizzabili) non verranno riflesse nel database dopo che uno schema è stato registrato. L'unico modo per riconoscere queste modifiche dopo che lo schema è stato registrato una volta in un sistema sarebbe ricompilare l'indice e quindi registrare il nuovo schema oppure per registrare lo schema e quindi creare una nuova proprietà per ogni versione successiva; ad esempio `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` e così via. Non è consigliabile creare nuove proprietà in questo modo, perché più colonne estranee potrebbero avere conseguenze sulle prestazioni del sistema.

## <a name="windows-property-system-documentation"></a>Documentazione del sistema di proprietà di Windows

Il resto della documentazione include le sezioni seguenti:

-   [Guida per gli sviluppatori del sistema di proprietà di Windows](property-system-developer-s-guide.md)

    Viene descritto in dettaglio come implementare gli scenari di sviluppo principali utilizzando il sistema di proprietà di Windows.

-   [Riferimento al sistema di proprietà](property-system-reference.md)

    Documenta le [proprietà di Windows](props.md), lo [schema della descrizione della proprietà](property-description-schema.md), le [interfacce](interfaces.md), le [funzioni](functions.md), le [strutture](structures.md)e le [costanti, le enumerazioni e i flag](constants--enumerations--and-flags.md) del sistema di proprietà di Windows.

-   [Esempi di codice del sistema di proprietà](property-system-code-samples.md)

    Vengono descritti esempi che illustrano come utilizzare il sistema di proprietà di Windows.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sul riutilizzo del In-Memory archivio delle proprietà, vedere [inizializzazione di gestori di proprietà](building-property-handlers-property-handlers.md) e [**PSCreateMemoryPropertyStore**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore).
-   Per una specifica del formato di file binario dell'archivio delle proprietà Microsoft, vedere [ \[ MS \_ PROPSTORE \] ](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   La relazione tra ricerca e indicizzazione di Windows e come estendere l'indice viene illustrata negli argomenti seguenti in Windows Search:
    -   [Sviluppo di gestori di filtri per la ricerca di Windows](../search/-search-ifilter-conceptual.md)
    -   [Sviluppo di gestori di protocollo per Windows Search](../search/-search-3x-wds-phaddins.md)
    -   [Sviluppo di gestori di proprietà per Windows Search](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Per il download di Windows 7 o Windows Vista SDK aggiornato, vedere la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per gli sviluppatori del sistema di proprietà di Windows](property-system-developer-s-guide.md)
</dt> <dt>

[Riferimento al sistema di proprietà](property-system-reference.md)
</dt> <dt>

[Esempi di codice del sistema di proprietà](property-system-code-samples.md)
</dt> </dl>

 

 
