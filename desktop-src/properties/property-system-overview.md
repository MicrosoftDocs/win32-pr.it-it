---
description: Il Windows Property System è un sistema di lettura/scrittura estendibile di definizioni di dati che fornisce un modo uniforme di esprimere metadati sugli elementi della shell.
ms.assetid: eb2dc2be-fc53-40aa-81f6-f353ab1d3a57
title: Panoramica del sistema di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742eebbdb05541a3cfcc1468cd0f93d255f13b67b4bfe777729d1d02d2ed70a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460031"
---
# <a name="property-system-overview"></a>Panoramica del sistema di proprietà

Il Windows Property System è un sistema di lettura/scrittura estendibile di definizioni di dati che fornisce un modo uniforme di esprimere metadati sugli elementi della shell. Il Windows property system in Windows Vista e versioni successive consente di archiviare e recuperare i metadati per gli elementi della shell. Un elemento shell è qualsiasi singolo elemento di contenuto, ad esempio un file, una cartella, un messaggio di posta elettronica o un contatto. Una proprietà è una singola parte di metadati associata a un elemento shell. I valori delle proprietà vengono espressi come [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Questo argomento è organizzato come segue:

-   [Introduzione](#introduction)
-   [Scenari di sviluppo](#development-scenarios)
-   [Proprietà e Windows ricerca](#properties-and-windows-search)
-   [Nota per gli implementatori](#note-to-implementers)
-   [Windows Documentazione del sistema di proprietà](#windows-property-system-documentation)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Le proprietà sono identificate in modo univoco dal nome canonico (ad esempio ) e dalla chiave `System.Document.LastAuthor` di proprietà (ad esempio `PKEY_Document_LastAuthor` ). Una chiave di proprietà (PKEY) è la parte del nome di una coppia nome-valore costituita da PKEY/PROPVARIANT o una stringa/PROPVARIANT, dove la stringa è il nome canonico della chiave PKEY (ad esempio `System.Document.LastAuthor` ). PKEY è una definizione che indica al sistema di proprietà tutto ciò che deve sapere sulla proprietà, mentre il valore è un'istanza effettiva della proprietà. Una chiave PKEY contiene internamente un formatID e un propID.

Una singola proprietà è costituita dai tre elementi seguenti:

-   Nome canonico, ad esempio `System.Music.Artist` .
-   Descrizione dello schema, specificata nel formato di file XML propdesc ed espressa a livello di codice [**tramite IPropertyDescription**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription).
-   Valore, ad esempio il nome di un cantore.

La descrizione dello schema è costituita da informazioni sulla proprietà, ad esempio il nome della proprietà, il tipo di dati, i vincoli, le informazioni sul modo in cui la proprietà interagisce con le viste e il sistema di ricerca e così via. Il nome e la descrizione dello schema sono definiti a livello globale e sono gli stessi per tutti gli elementi e i tipi. Un valore è specifico di un singolo elemento. Ovvero, la proprietà è sempre definita come stringa multivalore, ma può avere un valore diverso (o nessun `System.Music.Artist` valore) per ogni elemento.

Un gestore delle proprietà converte i dati archiviati in un file in uno schema strutturato riconosciuto da e accessibile da Windows Explorer, Windows Ricerca e altre applicazioni. Questi sistemi possono quindi interagire con il gestore delle proprietà per scrivere e leggere le proprietà da e verso il file. I dati tradotti vengono esposti a livello di codice e visualizzati all'utente tramite Windows Explorer in diversi contesti, tra cui visualizzazione dettagli, infotip, riquadro dei dettagli, pagine delle proprietà e così via. Ogni gestore delle proprietà è associato a un particolare tipo di file, identificato dall'estensione del nome file. Gli sviluppatori devono implementare un gestore delle proprietà che produce e utilizza il formato nativo del tipo di file, ad esempio .jpg o .png, o usare il In-Memory Archivio proprietà, che produce e usa il formato binario MS-PROPSTORE.

Il Windows Property System crea un modello di dati astratto che fornisce un livello di astrazione da singoli formati di file. Il modello di dati astratto fornito dal Windows Property System è un metodo per la lettura e la scrittura di un set estendibile di valori denominati associati a un elemento shell. L'espressione value è flessibile, supporta molti tipi di dati ed è estendibile, consentendo l'espressione di dati arbitrari (**\_ BLOB VT**) e oggetti come valore.

A causa dell'astrazione, è possibile eseguire query su attributi o metadati di qualsiasi elemento. Esempi di elementi che possono essere astratti includono Microsoft Office documenti, tag ID3 e AutoCAD e altro software proprietario di terze parti. Analogamente, se si dispone di un file jpeg, è possibile usare i codec JPEG ed EXIF per leggere i byte del file per individuare le dimensioni dell'immagine. Se invece si ha un file .png, è necessario un codec diverso e un codice diverso per eseguire questa operazione. L'Windows sistema di proprietà consente di evitare questo tipo di problema. Se si implementa un nuovo tipo di file, è possibile collegare l'astrazione uniforme offerta dal sistema di proprietà Windows e specificare come rendere utilizzabili i metadati. Per questi motivi, è sempre preferibile usare la piattaforma comune fornita dal sistema Windows proprietà.

## <a name="development-scenarios"></a>Scenari di sviluppo

Le proprietà sono espresse dai produttori e dai consumer. In questo contesto, i produttori sono gli inventori delle proprietà nel sistema di proprietà Windows e i consumer sono applicazioni (e i relativi sviluppatori) che utilizzano le informazioni sulle proprietà di questo sistema. Nella tabella seguente sono identificati gli Windows di proprietà di e .



| Uso del sistema Windows proprietà                                                                                                                                                                                            | Partecipante |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| Blocco predefinito che fornisce un registro estendibile di descrizioni delle proprietà, un'implementazione dell'archivio delle proprietà in memoria e servizi per l'associazione a gestori di proprietà, la conversione di tipi e la serializzazione degli archivi proprietà. | Consumer    |
| Applicazioni che vogliono leggere e scrivere proprietà in modo astratto.                                                                                                                                                       | Consumer    |
| Inventori di proprietà che definiscono nuove proprietà per il sistema di proprietà definendo schemi di proprietà personalizzati e sviluppando i propri gestori delle proprietà.                                                                          | Producer    |
| Proprietari di formati di file che vogliono abilitare l'accesso alle proprietà archiviate nei formati di file personalizzati.                                                                                                                           | Producer    |



 

I consumer utilizzano proprietà, schemi e gestori di proprietà esistenti. Le proprietà disponibili per l'utilizzo includono proprietà di lettura/scrittura dai gestori di proprietà per i tipi di file supportati e possono includere anche alcune proprietà personalizzate. Gli schemi disponibili includono almeno lo schema di sistema e talvolta anche altri. Un consumer può creare un'applicazione per utilizzare i metadati e creare una visualizzazione basata sull'artista, indipendentemente dalle cartelle in cui sono archiviati gli elementi. La gerarchia di cartelle file è irrilevante. Ad esempio, è possibile specificare tutti gli elementi del brano da un particolare cantautore senza preoccuparsi della posizione di tali elementi. Questo scenario complesso e end-to-end non è limitato al sistema di proprietà Windows, ma coinvolge diversi componenti, ad esempio l'indicizzazione e le cartelle di ricerca.

Gli inventori di proprietà, o sviluppatori di terze parti, sono produttori nel Windows Property System. Quando si prepara a definire una nuova proprietà, esaminare innanzitutto il set di proprietà Windows definisce. Se ne trova una che soddisfi le proprie esigenze, del tipo e della semantica che corrispondono all'uso richiesto, usare tale proprietà e non crearne una nuova. Se si definisce una nuova proprietà personalizzata, provare a ottenere un accordo con altri sviluppatori che potrebbero volerla usare e pubblicare il risultato di tale contratto in modo che possano unirsi alla community di utenti di tale proprietà.

I producer possono sfruttare Windows explorer. Ad esempio, se si scrive un nuovo formato di immagine e si implementa un gestore delle proprietà, il nuovo formato di file diventa disponibile in Windows Explorer. Gli utenti possono quindi contrassegnare le proprie fotografie e convertire la raccolta di fotografie in base a qualsiasi proprietà nel Windows proprietà. In effetti, qualsiasi operazione di Shell con le proprietà, gli sviluppatori di terze parti possono eseguire le proprie applicazioni. Ciò include il raggruppamento, l'ordinamento, l'esecuzione di query e la visualizzazione di proprietà complete. L'esperienza utente Windows Explorer può essere implementata in gran parte da terze parti con API disponibili pubblicamente. Windows Explorer può essere sostituito o esteso usando queste API.

Dal punto di vista di un'applicazione che usa il modello di dati Shell, esistono un'ampia gamma di scenari che comportano l'uso del sistema di proprietà Windows proprietà. Le applicazioni di gestione dei supporti sono un esempio importante. Gli scenari di base del sistema di proprietà includono scenari come la lettura della proprietà parola chiave di una fotografia o l'impostazione della proprietà datetaken. Esempi di scenari di integrazione end-to-end abilitati dal sistema di proprietà Windows, ma che richiedono diversi altri componenti per il funzionamento, includono la visualizzazione di tutte le immagini o la ricerca di un documento contenente una parola chiave.

## <a name="properties-and-windows-search"></a>Proprietà e Windows ricerca

Le proprietà servono sia ai produttori che ai consumer quando si interfacciano Windows ricerca e indicizzazione. Windows La ricerca include una cache di valori di proprietà usati nell'implementazione del Windows Search Service (WSS). È possibile eseguire query su questi valori di proprietà a livello di codice usando il provider OLE DB di ricerca Windows o [**tramite ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory), che rappresenta gli elementi nei risultati della ricerca e nelle visualizzazioni basate su query. Windows La ricerca raccoglie e archivia quindi le proprietà generate dai gestori di filtri o dai gestori delle proprietà quando un elemento, ad esempio un documento di Word, viene indicizzato. Questo archivio viene eliminato e ricompilato quando l'indice viene ricompilato.

> [!Note]  
> Tenere presente che quando si registra di nuovo uno schema, le modifiche apportate agli attributi delle proprietà definite in precedenza potrebbero non essere rispettate dall'indicizzatore. La soluzione consiste nel ricompilare l'indice o introdurre nuove proprietà che riflettano le modifiche anziché aggiornare quelle precedenti (scelta non consigliata). Per altre informazioni, vedere [Note per gli implementatori più](#note-to-implementers) avanti in questo argomento.

 

Ad esempio, uno sviluppatore che crea un'applicazione multimediale vuole mostrare agli utenti dell'applicazione tutta la musica disponibile di un determinato artista. L'applicazione fornisce all'utente un elenco di artisti disponibili e quindi genera un elenco di tutta la musica disponibile dell'artista selezionato dall'utente. In caso contrario, un utente finale potrebbe voler eseguire una query per ?artist:Beethoven?, ed essere esposto all'elenco completo delle proprietà disponibili nel corso della ricerca. Questo esempio prevede l'uso dello spazio dei nomi Shell, dei gestori delle proprietà e/o dell'esecuzione di query sull'indice tramite uno degli elementi seguenti:

-   Origine dati shell.
-   Provider OLE DB.
-   Un file di ricerca salvato (con estensione search-ms) usato per avviare una query passando al file di ricerca in Windows Explorer o associando a [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) a livello di codice.

> [!Note]  
> Anche se la proprietà non fa parte di questo scenario di applicazione multimediale, può essere usata per compilare una query che restituirebbe tutti i file con estensione `System.Kind` search-ms in un ambito specifico.

 

Il modo preferito per accedere alle API di ricerca e creare Windows di ricerca è tramite un'origine dati shell. [**ISearchFolderItemFactory**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) è un componente in grado di creare istanze dell'origine dati della cartella di ricerca, una sorta di origine dati "virtuale" fornita da Shell che può eseguire query su altre origini dati nello spazio dei nomi Shell ed enumerare i risultati. Può eseguire questa operazione usando l'indicizzatore o enumerando ed esaminando manualmente gli elementi negli ambiti specificati.

Gli sviluppatori di terze parti possono creare applicazioni che utilizzano i dati nell'indice tramite query a livello di codice e possono estendere i dati nell'indice per i tipi di file e di elementi personalizzati da indicizzare Windows ricerca. Se si desidera visualizzare i risultati della query in Windows Explorer, è necessario implementare un'origine dati shell prima di poter creare un gestore di protocollo per estendere l'indice. Tuttavia, se tutte le query saranno programmatiche (ad esempio tramite OLE DB) e interpretate dal codice dell'applicazione anziché dalla shell, è comunque preferibile ma non necessario uno spazio dei nomi della shell. È necessario un gestore di protocollo per Windows ottenere informazioni sul contenuto dei file, ad esempio elementi nei database o tipi di file personalizzati. Anche Windows ricerca può indicizzare il nome e le proprietà del file, Windows non dispone di informazioni sul contenuto del file. Di conseguenza, tali elementi non possono essere indicizzati o esposti in Windows Shell. Implementando un gestore di protocollo personalizzato, è possibile esporre questi elementi. Per un elenco dei gestori identificati dallo scenario di sviluppo che si sta tentando di ottenere, vedere "Panoramica dei gestori" in Windows [Search as a Development Platform](../search/-search-3x-wds-development-ovr.md).

> [!Note]  
> Un'origine dati shell è talvolta nota come estensione dello spazio dei nomi shell. Un gestore è talvolta noto come estensione della shell o gestore dell'estensione della shell.

 

## <a name="note-to-implementers"></a>Nota per gli implementatori

A causa di potenziali difficoltà che l'indicizzatore può avere quando utilizza lo schema del sistema di proprietà, è fondamentale definire gli attributi con attenzione e in modo strategico per la prima versione dello schema. Eventuali modifiche agli attributi (tipo, larghezza della colonna, se indicizzabili) non verranno riflesse nel database dopo la registrazione di uno schema. L'unico modo per fare in modo che queste modifiche riconosivino dopo che lo schema è stato registrato una volta in un sistema è ricompilare l'indice e quindi registrare il nuovo schema oppure registrare lo schema e quindi creare una nuova proprietà per ogni versione successiva. ad esempio `PKEY_GroupName_PropertyNameV2` `PKEY_GroupName_PropertyNameV3` , e così via. Non è consigliabile creare nuove proprietà in questo modo, perché più colonne estranee possono influire sulle prestazioni del sistema.

## <a name="windows-property-system-documentation"></a>Windows Documentazione del sistema di proprietà

La parte restante di questa documentazione contiene le sezioni seguenti:

-   [Windows Guida per gli sviluppatori del sistema di proprietà](property-system-developer-s-guide.md)

    Descrive in dettaglio come implementare i principali scenari di sviluppo usando il Windows proprietà.

-   [Riferimento al sistema di proprietà](property-system-reference.md)

    Documenta [le Windows,](props.md)lo [schema](property-description-schema.md) [](interfaces.md)di descrizione delle proprietà, le [interfacce,](functions.md)le [funzioni,](structures.md)le strutture e le [costanti,](constants--enumerations--and-flags.md) le enumerazioni e i flag del Windows proprietà.

-   [Esempi di codice del sistema di proprietà](property-system-code-samples.md)

    Vengono descritti esempi che illustrano come usare il Windows proprietà.

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per informazioni sul riutilizzo del In-Memory Archivio proprietà, vedere [Inizializzazione](building-property-handlers-property-handlers.md) dei gestori di proprietà e [**PSCreateMemoryPropertyStore.**](/windows/desktop/api/Propsys/nf-propsys-pscreatememorypropertystore)
-   Per una specifica del formato di file binario di Microsoft Archivio proprietà, vedere [ \[ MS \_ \] PROPSTORE](/openspecs/windows_protocols/ms-propstore/39ea873f-7af5-44dd-92f9-bc1f293852cc).
-   La relazione tra Windows ricerca e indicizzazione e come estendere l'indice è illustrata negli argomenti seguenti in Windows Ricerca:
    -   [Sviluppo di gestori di filtri per Windows ricerca](../search/-search-ifilter-conceptual.md)
    -   [Sviluppo di gestori di protocollo per Windows ricerca](../search/-search-3x-wds-phaddins.md)
    -   [Sviluppo di gestori di proprietà per Windows ricerca](../search/-search-3x-wds-extidx-propertyhandlers.md)
    -   Per il download Windows 7 o Windows Vista SDK, vedere [l'SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Guida per gli sviluppatori del sistema di proprietà](property-system-developer-s-guide.md)
</dt> <dt>

[Riferimento al sistema di proprietà](property-system-reference.md)
</dt> <dt>

[Esempi di codice del sistema di proprietà](property-system-code-samples.md)
</dt> </dl>

 

 
