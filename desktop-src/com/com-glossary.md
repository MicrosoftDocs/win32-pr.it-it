---
title: Glossario COM
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0c4c1aa78c81484666311dfcdd6bae8b4e6daaa45581af98f50171f48b4b58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048509"
---
# <a name="com-glossary"></a>Glossario COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**Attivazione**
</dt> <dd>

Processo di caricamento di un oggetto in memoria, che lo inserisce nello stato di esecuzione.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**stato attivo**
</dt> <dd>

Oggetto COM che si trova nello stato in esecuzione e ha un'interfaccia utente visibile.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker assoluto**
</dt> <dd>

Moniker che specifica la posizione assoluta di un oggetto . Un moniker assoluto è analogo a un percorso completo.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titolare dell'advisory**
</dt> <dd>

Oggetto COM che memorizza nella cache, gestisce e invia notifiche di modifiche ai sink consultivi delle applicazioni contenitore.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**sink di consulenza**
</dt> <dd>

Oggetto COM che può ricevere notifiche di modifiche in un oggetto incorporato o collegato perché implementa l'interfaccia [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2.**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) I contenitori che devono ricevere una notifica delle modifiche negli oggetti implementano un sink consultivo. Le notifiche hanno origine nel server, che usa un oggetto titolare di consulenza per memorizzare nella cache e gestire le notifiche ai contenitori.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**oggetto di aggregazione**
</dt> <dd>

Oggetto COM costituito da uno o più altri oggetti COM. Un oggetto nell'aggregazione è designato come oggetto di controllo, che controlla quali interfacce nell'aggregazione sono esposte e quali sono private. Questo oggetto di controllo ha un'implementazione speciale [**di IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominata **controllo IUnknown**. Tutti gli oggetti nell'aggregazione devono passare le **chiamate ai metodi IUnknown** tramite il controllo **IUnknown**.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Aggregazione**
</dt> <dd>

Tecnica di composizione per l'implementazione di oggetti COM. Consente di compilare un nuovo oggetto riutilizzando una o più implementazioni dell'interfaccia di oggetti esistenti. L'oggetto di aggregazione sceglie le interfacce da esporre ai client e le interfacce vengono esposte come se fossero implementate dall'oggetto di aggregazione. I client dell'oggetto di aggregazione comunicano solo con l'oggetto aggregato.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**proprietà di ambiente**
</dt> <dd>

Proprietà di run-time gestita ed esposta dal contenitore. In genere, una proprietà di ambiente rappresenta una caratteristica di un form, ad esempio il colore di sfondo, che deve essere comunicata a un controllo in modo che il controllo possa assumere l'aspetto dell'ambiente circostante.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**
</dt> <dd>

L'inverso di un moniker di file, elemento o puntatore. Un anti-moniker viene aggiunto alla fine di un moniker di file, elemento o puntatore per annullarlo. Gli anti-moniker vengono usati nella costruzione di moniker relativi.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**conteggio dei riferimenti artificiali**
</dt> <dd>

Tecnica usata per proteggere un oggetto prima di chiamare una funzione o un metodo che potrebbe annientarlo in modo prematuro. Un programma chiama **IUnknown::AddRef** per incrementare il conteggio dei riferimenti dell'oggetto prima di effettuare la chiamata che potrebbe liberare l'oggetto. Al termine della funzione, il programma chiama **IUnknown::Release** per decrementare il conteggio.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**associazione asincrona**
</dt> <dd>

Tipo di associazione in cui è necessario che il processo si verifichi in modo asincrono per evitare una riduzione delle prestazioni per l'utente finale. In genere, l'associazione asincrona viene usata in ambienti distribuiti, ad esempio World Wide Web. OLE supporta classi di moniker asincroni e meccanismi di callback che consentono il processo di individuazione e inizializzazione di un oggetto in un ambiente distribuito durante l'esecuzione di altre operazioni.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**chiamata asincrona**
</dt> <dd>

Chiamata a una funzione eseguita separatamente in modo che il chiamante possa continuare a elaborare le istruzioni senza attendere la restituzione della funzione.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrono**
</dt> <dd>

Moniker che supporta l'associazione asincrona. Ad esempio, le istanze della classe moniker URL fornita dal sistema sono moniker asincroni.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**Automazione**
</dt> <dd>

Un modo per modificare gli oggetti di un'applicazione dall'esterno dell'applicazione. L'automazione viene in genere usata per creare applicazioni che espongono oggetti a strumenti di programmazione e linguaggi macro, creare e modificare gli oggetti di un'applicazione da un'altra applicazione o per creare strumenti per l'accesso e la modifica di oggetti.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contesto di associazione**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IBindCtx.**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) I contesti di associazione vengono usati nelle operazioni del moniker per contenere riferimenti agli oggetti attivati quando viene associato un moniker. Il contesto di associazione contiene parametri che si applicano a tutte le operazioni durante l'associazione di un moniker composito generico e fornisce all'implementazione del moniker l'accesso alle informazioni sul relativo ambiente.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**Associazione**
</dt> <dd>

Associazione di un nome al relativo riferimento. In particolare, individuando l'oggetto denominato da un moniker, inserendolo nello stato di esecuzione, se non lo è già, e restituisce un puntatore a interfaccia. Gli oggetti possono essere associati in fase di esecuzione (detto anche associazione tardiva o associazione dinamica) o in fase di compilazione (detto anche associazione statica).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**Cache**
</dt> <dd>

Archivio locale (in genere temporaneo) di informazioni. In OLE una cache contiene informazioni che definiscono la presentazione di un oggetto collegato o incorporato all'apertura del contenitore.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inizializzazione della cache**
</dt> <dd>

Riempimento di dati di presentazione nella cache di un oggetto collegato o incorporato. [**L'interfaccia IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fornisce metodi che un contenitore può chiamare per controllare i dati memorizzati nella cache per gli oggetti collegati o incorporati.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**Classe**
</dt> <dd>

Definizione di un oggetto nel codice. In C++ la classe di un oggetto è definita come tipo di dati, ma non in altri linguaggi. Poiché OLE può essere codificato in qualsiasi linguaggio, la classe viene usata per fare riferimento alla definizione generale dell'oggetto.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e che crea una o più istanze di un oggetto identificato da un identificatore di classe (CLSID) specificato.

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**Identificatore di classe (CLSID)**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un oggetto classe OLE. Se un oggetto classe verrà usato per creare più istanze di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel Registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti. Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**oggetto classe**
</dt> <dd>

Nella programmazione orientata a oggetti, un oggetto il cui stato è condiviso da tutti gli oggetti in una classe e il cui comportamento agisce sui dati dello stato a livello di classe. In COM gli oggetti classe sono denominati class factory e in genere non hanno alcun comportamento se non creare nuove istanze della classe.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**Client**
</dt> <dd>

Oggetto COM che richiede servizi da un altro oggetto.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sito client**
</dt> <dd>

Sito di visualizzazione per un oggetto incorporato o collegato all'interno di un documento composto. Il sito client è il mezzo principale con cui un oggetto richiede servizi dal relativo contenitore.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**Clsid**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un oggetto classe OLE. Se un oggetto classe verrà usato per creare più istanze di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel Registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti. Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**Commettere**
</dt> <dd>

Per salvare in modo permanente le modifiche apportate a un oggetto di archiviazione o flusso dopo l'apertura o l'ultimo salvataggio delle modifiche.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**Componente**
</dt> <dd>

Oggetto che incapsula dati e codice e fornisce un set ben specificato di servizi disponibili pubblicamente.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**
</dt> <dd>

Modello di programmazione ole orientato a oggetti che definisce il modo in cui gli oggetti interagiscono all'interno di un singolo processo o tra processi. In COM i client hanno accesso a un oggetto tramite interfacce implementate nell'oggetto.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra dei menu composita**
</dt> <dd>

Barra dei menu condivisa composta da gruppi di menu sia da un'applicazione contenitore che da un'applicazione server attivata sul posto.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composito**
</dt> <dd>

Moniker costituito da due o più moniker trattati come unità. Un moniker composito può essere non generico, vale a dire che i moniker dei relativi componenti hanno una conoscenza speciale l'uno dell'altro o generici, vale a dire che i moniker dei componenti non sanno nulla l'uno dell'altro, ad eccezione del fatto che sono moniker

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento composto**
</dt> <dd>

Documento che include oggetti collegati o incorporati, nonché i propri dati nativi.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**file composto**
</dt> <dd>

Implementazione di un'Archiviazione strutturata fornita da OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Oggetto COM**
</dt> <dd>

Oggetto conforme all'oggetto OLE Component Object Model (COM). Un oggetto COM è un'istanza di una definizione di oggetto, che specifica i dati dell'oggetto e una o più implementazioni di interfacce sull'oggetto. I client interagiscono con un oggetto COM solo tramite le relative interfacce.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**oggetto collegabile**
</dt> <dd>

Oggetto COM che implementa almeno l'interfaccia [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) per la gestione degli oggetti punto di connessione. Gli oggetti collegabili supportano la comunicazione dal server al client. Un oggetto collegabile crea e gestisce uno o più sottooggetti del punto di connessione, che ricevono eventi dalle interfacce implementate su altri oggetti e li inviano al client.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**oggetto punto di connessione**
</dt> <dd>

Oggetto COM gestito da un oggetto collegabile che implementa [**l'interfaccia IConnectionPoint.**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) Uno o più oggetti punto di connessione possono essere creati e gestiti da un oggetto collegabile. Ogni oggetto punto di connessione gestisce gli eventi in ingresso da un'interfaccia specifica su un altro oggetto e li invia al client.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**applicazione contenitore**
</dt> <dd>

Applicazione che supporta documenti composti. L'applicazione contenitore fornisce l'archiviazione per un oggetto incorporato o collegato, un sito per la relativa visualizzazione, l'accesso al sito di visualizzazione e un sink consultivo per la ricezione di notifiche delle modifiche nell'oggetto.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**Contenimento**
</dt> <dd>

Tecnica di composizione per l'implementazione di oggetti COM. Consente a un oggetto di riutilizzare alcune o tutte le implementazioni dell'interfaccia di uno o più oggetti. L'oggetto esterno funge da client per gli altri oggetti, delegando l'implementazione quando vuole usare i servizi di uno degli oggetti contenuti.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**Contesto**
</dt> <dd>

In COM+, set di proprietà di run-time associate a uno o più oggetti COM usati per fornire servizi per tali oggetti.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**Controllo**
</dt> <dd>

Oggetto COM incorporabile e riutilizzabile che supporta almeno [**l'interfaccia IOleControl.**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) I controlli sono in genere associati all'interfaccia utente. Supportano anche la comunicazione con un contenitore e possono essere riutilizzati da più client, a seconda dei criteri di licenza.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenitore di controlli**
</dt> <dd>

Applicazione che supporta l'incorporamento di controlli implementando [**l'interfaccia IOleControlSite.**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**proprietà control**
</dt> <dd>

Proprietà di run-time esposta e gestita dal controllo stesso. Ad esempio, il tipo di carattere e le dimensioni del testo usate dal controllo sono proprietà del controllo .

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controllo dell'oggetto**
</dt> <dd>

Oggetto all'interno di un oggetto di aggregazione che controlla quali interfacce all'interno dell'oggetto di aggregazione vengono esposte e quali sono private. [**L'interfaccia IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto di controllo è denominata **controllo IUnknown**. Le chiamate **ai metodi IUnknown** di altri oggetti nell'aggregazione devono essere passate al controllo **IUnknown**.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sito di controllo**
</dt> <dd>

Struttura implementata da un contenitore di controlli per la gestione della visualizzazione e dell'archiviazione di un controllo. All'interno di un contenitore specificato, ogni controllo ha un sito di controllo corrispondente.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**oggetto di trasferimento dei dati**
</dt> <dd>

Oggetto che implementa [**l'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e contiene i dati da trasferire da un oggetto a un altro tramite gli Appunti o le operazioni di trascinamento della selezione.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**gestore di oggetti predefinito**
</dt> <dd>

DLL fornita con OLE che funge da surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.

Con il gestore di oggetti predefinito, è possibile esaminare i dati archiviati di un oggetto senza attivare effettivamente l'oggetto. Il gestore di oggetti predefinito esegue altre attività, ad esempio il rendering di un oggetto dallo stato memorizzato nella cache quando l'oggetto viene caricato in memoria.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**oggetto dipendente**
</dt> <dd>

Oggetto COM in genere inizializzato da un altro oggetto (l'oggetto host). Anche se la durata dell'oggetto dipendente può avere senso solo durante la durata dell'oggetto host, l'oggetto host non funziona come [**controllo IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) per l'oggetto dipendente. Al contrario, un oggetto è un oggetto aggregato quando la relativa durata (tramite il conteggio dei riferimenti) è completamente controllata dall'oggetto di gestione.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modalità di accesso diretto**
</dt> <dd>

Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione. In modalità diretta, viene eseguito immediatamente il commit di tutte le modifiche nell'oggetto di archiviazione radice.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**oggetto documento**
</dt> <dd>

Documento OLE in grado di visualizzare una o più visualizzazioni attivate sul posto dei dati all'interno di un frame nativo o estraneo, ad esempio un browser, mantenendo il controllo completo sull'interfaccia utente. Oltre a implementare le consuete interfacce di attivazione sul posto e del documento OLE, un oggetto documento deve implementare [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)e ognuna delle visualizzazioni (sotto forma di oggetto visualizzazione documento) deve implementare [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenitore di oggetti documento**
</dt> <dd>

Applicazione contenitore in grado di visualizzare una o più visualizzazioni di uno o più oggetti documento e di gestire tutti gli oggetti documento contenuti all'interno di un file. Ogni oggetto documento è associato a un sito di documenti e ogni sito di documenti contiene uno o più siti di visualizzazione documenti corrispondenti alle visualizzazioni supportate dall'oggetto documento. Un contenitore di oggetti documento include anche una cornice contenitore, che gestisce la negoziazione di menu e barra degli strumenti e l'enumerazione di oggetti contenuti.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**server oggetti documento**
</dt> <dd>

Applicazione server in grado di fornire oggetti documento.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sito di documenti**
</dt> <dd>

Sito client implementato da un contenitore di oggetti documento per la gestione della visualizzazione e dell'archiviazione di un oggetto documento. Ogni oggetto documento in un contenitore ha un sito documento corrispondente.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**oggetto sito del documento**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IOleDocumentSite,**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) oltre alle consuete interfacce client-sito ( ad esempio [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**visualizzazione documento**
</dt> <dd>

Presentazione specifica dei dati di un documento. Un singolo oggetto documento può avere una o più visualizzazioni, ma una singola visualizzazione documento può appartenere a un solo oggetto documento.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**oggetto visualizzazione documento**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) e corrisponde a una visualizzazione documento specifica. Un oggetto con più visualizzazioni documento aggrega un oggetto visualizzazione documento separato per ogni visualizzazione.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sito di visualizzazione dei documenti**
</dt> <dd>

Oggetto aggregato da un oggetto sito del documento per la gestione dello spazio di visualizzazione per una determinata visualizzazione di un oggetto documento. All'interno di un determinato sito di documenti, ogni visualizzazione documento ha un sito di visualizzazione documenti corrispondente.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**oggetto sito visualizzazione documento**
</dt> <dd>

Oggetto COM aggregato in un oggetto sito del documento e che implementa [**l'interfaccia IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) e, facoltativamente, [**l'interfaccia IContinueCallback.**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback)

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**trascinamento della selezione**
</dt> <dd>

Operazione in cui l'utente finale usa il mouse o un altro dispositivo di puntamento per spostare i dati in un'altra posizione nella stessa finestra o in un'altra finestra.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorpora**
</dt> <dd>

Per inserire un oggetto in un documento composto in modo da mantenere i formati di dati nativi di tale oggetto e per consentirne la modifica dall'interno del relativo contenitore usando gli strumenti esposti dal server.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**oggetto incorporato**
</dt> <dd>

Oggetto i cui dati sono archiviati in un documento composto, ma l'oggetto viene eseguito nello spazio di elaborazione del server. Il gestore di oggetti predefinito fornisce un surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**proprietà estesa**
</dt> <dd>

Proprietà di run-time, ad esempio la posizione e le dimensioni di un controllo, che un utente presupporrebbe di essere esposta dal controllo, ma viene esposta e gestita dal contenitore.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker di file**
</dt> <dd>

Moniker basato su un percorso nel file system. I moniker di file possono essere usati per identificare gli oggetti salvati nei propri file. Un moniker di file è un oggetto COM che supporta l'implementazione fornita dal sistema [**dell'interfaccia IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) per la classe del moniker di file.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**oggetto font**
</dt> <dd>

Oggetto COM che fornisce l'accesso ai Graphics Device Interface (GDI) implementando [**l'interfaccia IFont.**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificatore di formato**
</dt> <dd>

GUID che identifica un set di proprietà persistenti. Definito anche FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**Telaio**
</dt> <dd>

Parte di un'applicazione contenitore responsabile della negoziazione di menu, tasti di scelta rapida, barre degli strumenti e altri elementi dell'interfaccia utente condivisi con un oggetto COM incorporato o un oggetto documento.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**oggetto frame**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) e, facoltativamente, [**l'interfaccia IOleCommandTarget.**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget)

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composito generico**
</dt> <dd>

Raccolta sequenziata di moniker, a partire da un moniker di file per fornire il percorso a livello di documento e continuando con uno o più moniker di elemento che, nel loro complesso, identificano in modo univoco un oggetto.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**Funzione helper**
</dt> <dd>

Funzione che incapsula le chiamate ad altre funzioni e metodi di interfaccia disponibili pubblicamente in OLE SDK. Le funzioni helper sono un modo pratico per chiamare sequenze usate di frequente di chiamate di funzioni e metodi che esere attività comuni.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**oggetto host**
</dt> <dd>

Oggetto COM che forma una relazione gerarchica con uno o più oggetti COM, noti come oggetti dipendenti. In genere, l'oggetto host crea un'istanza degli oggetti dipendenti e la relativa esistenza ha senso solo all'interno della durata dell'oggetto host. Tuttavia, l'oggetto host non funge da [**controllo IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) per gli oggetti dipendenti, né delega direttamente alle implementazioni dell'interfaccia di tali oggetti.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**Hresult**
</dt> <dd>

Handle di risultato opaco definito come zero per un esito positivo restituito da una funzione e diverso da zero se vengono restituite informazioni sull'errore o sullo stato.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**oggetto collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa almeno l'interfaccia [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) e funge da collegamento a un oggetto in un'altra posizione (destinazione). Un collegamento ipertestuale è costituito da quattro parti: un moniker che identifica la posizione della destinazione. stringa per la posizione all'interno della destinazione. nome descrittivo o visualizzabile per la destinazione. e una stringa che può contenere parametri aggiuntivi.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contesto di esplorazione dei collegamenti ipertestuali**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) e gestisce lo stack di navigazione dei collegamenti ipertestuali. L'oggetto del contesto di esplorazione gestisce la finestra cornice del collegamento ipertestuale e la finestra dell'oggetto destinazione del collegamento ipertestuale.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenitore collegamento ipertestuale**
</dt> <dd>

Applicazione contenitore che supporta i collegamenti ipertestuali implementando l'interfaccia [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e, se gli oggetti del contenitore possono essere destinazioni di altri collegamenti ipertestuali, [**l'interfaccia IHlinkTarget.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85))

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**Oggetto frame collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) e controlla la navigazione di primo livello e la visualizzazione dei collegamenti ipertestuali per il contenitore del frame e il server della destinazione del collegamento ipertestuale.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**oggetto sito collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e fornisce il moniker o l'identificatore di interfaccia del contenitore collegamento ipertestuale. Un sito collegamento ipertestuale può contenere più collegamenti ipertestuali.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**oggetto destinazione collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) e fornisce il relativo moniker, nome descrittivo e altre informazioni che altri oggetti collegamento ipertestuale useranno per spostarsi su di essa.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**parametro in**
</dt> <dd>

Parametro allocato, impostato e liberato dal chiamante di una funzione o di un metodo di interfaccia. Un parametro in non viene modificato dalla funzione chiamata.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parametro in/out**
</dt> <dd>

Parametro allocato inizialmente dal chiamante di una funzione o di un metodo di interfaccia e impostato, liberato e riallocato, se necessario, dal processo chiamato.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**attivazione sul posto**
</dt> <dd>

Modifica di un oggetto incorporato all'interno della finestra del contenitore, usando gli strumenti forniti dal server. Gli oggetti collegati non supportano l'attivazione sul posto. vengono sempre modificate nella finestra del server.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**server in-process**
</dt> <dd>

Un server implementato come DLL che viene eseguito nello spazio di elaborazione del client.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**Istanza**
</dt> <dd>

Oggetto per cui la memoria è allocata o persistente.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**Interfaccia**
</dt> <dd>

Gruppo di funzioni correlate semanticamente che forniscono l'accesso a un oggetto COM. Ogni interfaccia OLE definisce un contratto che consente agli oggetti di interagire in base alla Component Object Model (COM). Anche se OLE fornisce molte implementazioni di interfaccia, la maggior parte delle interfacce può essere implementata anche dagli sviluppatori che progettano applicazioni OLE.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificatore di interfaccia (IID)**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un'interfaccia. Alcune funzioni accettano gli ID come parametri per consentire al chiamante di specificare quale puntatore a interfaccia deve essere restituito.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker di elementi**
</dt> <dd>

Moniker basato su una stringa che identifica un oggetto in un contenitore. I moniker degli elementi possono identificare gli oggetti più piccoli di un file, inclusi gli oggetti incorporati in un documento composto o uno pseudo-oggetto (ad esempio un intervallo di celle in un foglio di calcolo).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**Licenze**
</dt> <dd>

Funzionalità di COM che fornisce il controllo sulla creazione di oggetti. Gli oggetti concessi in licenza possono essere creati solo dai client autorizzati a usarli. Le licenze vengono implementate in COM tramite [**l'interfaccia IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e tramite il supporto per una chiave di licenza che può essere passata in fase di esecuzione.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**oggetto collegamento**
</dt> <dd>

Oggetto COM creato quando viene creato o caricato un oggetto COM collegato. L'oggetto collegamento viene fornito da OLE e implementa [**l'interfaccia IOleLink.**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink)

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**oggetto collegato**
</dt> <dd>

Oggetto COM i cui dati di origine risiedono fisicamente nel punto in cui sono stati creati inizialmente. Solo un moniker che rappresenta i dati di origine e i dati di presentazione appropriati vengono conservati con il documento composto. Le modifiche apportate all'origine del collegamento vengono riflesse automaticamente nell'oggetto collegato.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origine del collegamento**
</dt> <dd>

Dati che sono l'origine di un oggetto collegato. Un'origine collegamento può essere un file o una parte di un file, ad esempio un intervallo selezionato di celle all'interno di un file (detto anche pseudo oggetto).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**stato caricato**
</dt> <dd>

Stato di un oggetto dopo che le strutture dei dati sono state caricate in memoria e sono accessibili al processo client.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**server locale**
</dt> <dd>

Un server out-of-process implementato come applicazione .EXE in esecuzione nello stesso computer dell'applicazione client.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**Blocco**
</dt> <dd>

Puntatore mantenuto a e possibilmente, un conteggio dei riferimenti incrementato in un oggetto in esecuzione. OLE definisce due tipi di blocchi che possono essere mantenuti su un oggetto: strong e weak. Per implementare un blocco sicuro, un server deve mantenere sia un puntatore che un conteggio dei riferimenti, in modo che l'oggetto rimanga "bloccato" in memoria almeno fino a quando il server non chiama [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Per implementare un blocco debole, il server mantiene solo un puntatore all'oggetto, in modo che l'oggetto possa essere eliminato da un altro processo.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**Marshalling**
</dt> <dd>

Creazione di pacchetti e invio di chiamate al metodo di interfaccia attraverso i limiti del thread o del processo.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo di supporto**
</dt> <dd>

Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto .

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo di contenuto MIME**
</dt> <dd>

Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto .

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**
</dt> <dd>

Protocollo Internet originariamente sviluppato per consentire lo scambio di messaggi di posta elettronica con contenuti complessi in ambienti eterogenei di rete, computer e posta elettronica. In pratica, MIME è stato adottato ed esteso anche dalle applicazioni non di posta elettronica.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**Moniker**
</dt> <dd>

Oggetto che implementa [**l'interfaccia IMoniker.**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) Un moniker funge da nome che identifica in modo univoco un oggetto COM. Allo stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**Classe moniker**
</dt> <dd>

Implementazione [**dell'interfaccia IMoniker.**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) Le classi moniker fornite dal sistema includono moniker di file, moniker di elementi, moniker compositi generici, anti-moniker, moniker puntatore e moniker URL.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**client moniker**
</dt> <dd>

Applicazione che usa moniker per acquisire puntatori a interfaccia a oggetti gestiti da un'altra applicazione.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**provider di moniker**
</dt> <dd>

Applicazione che rende disponibili moniker che identificano gli oggetti gestiti, in modo che gli oggetti siano accessibili ad altre applicazioni.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**estensione dello spazio dei nomi**
</dt> <dd>

Oggetto COM in-process che implementa [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview)a volte definite interfacce di estensione dello spazio dei nomi. Un'estensione dello spazio dei nomi viene usata per estendere lo spazio dei nomi della shell o per creare uno spazio dei nomi separato. Gli utenti primari sono le finestre Windows explorer e i file comuni.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**dati nativi**
</dt> <dd>

Dati utilizzati da un'applicazione server OLE durante la modifica di un oggetto incorporato.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**Oggetto**
</dt> <dd>

In OLE una struttura di programmazione che incapsula sia i dati che le funzionalità definiti e allocati come una singola unità e per i quali l'unico accesso pubblico è tramite le interfacce della struttura di programmazione. Un oggetto COM deve supportare almeno [**l'interfaccia IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) che mantiene l'esistenza dell'oggetto durante l'uso e fornisce l'accesso alle altre interfacce dell'oggetto.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**stato dell'oggetto** 
</dt> <dd>

Relazione tra un oggetto documento composto nel contenitore e l'applicazione responsabile della creazione dell'oggetto: attivo, passivo, caricato o in esecuzione. Gli oggetti passivi vengono archiviati su disco o in un database e l'oggetto non è selezionato o attivo. Nello stato caricato le strutture dei dati dell'oggetto sono state caricate in memoria, ma non sono disponibili per operazioni quali la modifica. Gli oggetti in esecuzione vengono caricati e disponibili per tutte le operazioni. Gli oggetti attivi sono oggetti in esecuzione con un'interfaccia utente visibile.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nome del tipo di oggetto**
</dt> <dd>

Stringa di identificazione univoca archiviata come parte delle informazioni disponibili per un oggetto nel database di registrazione.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**Ole**
</dt> <dd>

Tecnologia Microsoft basata su oggetti per la condivisione di informazioni e servizi tra i limiti di processi e computer.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**server out-of-process**
</dt> <dd>

Un server, implementato come applicazione .EXE, che viene eseguito all'esterno del processo del client, nello stesso computer o in un computer remoto.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**parametro out**
</dt> <dd>

Un parametro out viene allocato dalla funzione chiamata e liberato dal chiamante.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**stato passivo**
</dt> <dd>

Stato di un oggetto COM quando viene archiviato (su disco o in un database). L'oggetto non è selezionato o attivo.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**proprietà persistente**
</dt> <dd>

Informazioni che possono essere archiviate in modo permanente come parte di un oggetto di archiviazione, ad esempio un file o una directory. Le proprietà persistenti sono raggruppate in set di proprietà, che possono essere visualizzati e modificati.

Una proprietà persistente è diversa dalle proprietà di run-time degli oggetti creati con i controlli OLE e le tecnologie di automazione, che possono essere usate per influire sul comportamento del sistema. La [**struttura PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) definisce tutti i tipi validi di proprietà persistenti, mentre la struttura **VARIANT** definisce tutti i tipi validi di proprietà di run-time.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**archiviazione permanente**
</dt> <dd>

Archiviazione di un file o di un oggetto in un supporto, ad esempio un file system o un database, in modo che l'oggetto e i relativi dati permangono quando il file viene chiuso e quindi riaperto in un secondo momento.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**oggetto immagine**
</dt> <dd>

Oggetto COM che fornisce l'accesso alle immagini GDI implementando [**l'interfaccia IPicture.**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker puntatore**
</dt> <dd>

Moniker che esegue il mapping di un puntatore di interfaccia a un oggetto in memoria. Mentre la maggior parte dei moniker identifica gli oggetti che possono essere archiviati in modo permanente, i moniker puntatore identificano gli oggetti che non possono essere archiviati. Consentono a tali oggetti di partecipare a un'operazione di associazione del moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**dati di presentazione**
</dt> <dd>

Dati utilizzati da un contenitore per visualizzare oggetti incorporati o collegati.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo primario**
</dt> <dd>

Azione associata all'operazione più comune o preferita eseguita dagli utenti su un oggetto. Il verbo primario è sempre definito come verbo zero nel database di registrazione del sistema. Il verbo principale di un oggetto viene eseguito facendo doppio clic sull'oggetto.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Proprietà**
</dt> <dd>

Informazioni associate a un oggetto . In OLE le proprietà rientrano in due categorie: proprietà di run-time e proprietà persistenti. Le proprietà di run-time sono in genere associate agli oggetti controllo o ai relativi contenitori. Ad esempio, il colore di sfondo è una proprietà di run-time impostata dal contenitore di un controllo. Le proprietà persistenti sono associate a oggetti archiviati.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**frame di proprietà**
</dt> <dd>

Meccanismo dell'interfaccia utente che visualizza una o più pagine delle proprietà per un controllo . Il sistema di run-time dei controlli OLE fornisce un'implementazione standard di un frame di proprietà accessibile tramite la funzione helper [**OleCreatePropertyFrame.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe)

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificatore di proprietà**
</dt> <dd>

Intero con segno a quattro byte che identifica una proprietà persistente all'interno di un set di proprietà.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**pagina delle proprietà**
</dt> <dd>

Oggetto COM con il proprio CLSID che fa parte di un'interfaccia utente, implementato da un controllo e consente di visualizzare e impostare le proprietà del controllo. Gli oggetti della pagina delle proprietà implementano [**l'interfaccia IPropertyPage.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sito della pagina delle proprietà**
</dt> <dd>

Posizione all'interno di un frame di proprietà in cui viene visualizzata una pagina delle proprietà. Il frame di proprietà implementa [**l'interfaccia IPropertyPageSite,**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) che contiene i metodi per gestire i siti di ognuna delle pagine delle proprietà fornite da un controllo .

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**set di proprietà**
</dt> <dd>

Gruppo logicamente correlato di proprietà associato a un oggetto archiviato in modo permanente. Per creare, aprire, eliminare o enumerare uno o più set di proprietà, implementare [**l'interfaccia IPropertySetStorage.**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) Se si usano file composti, è possibile usare l'implementazione OLE di questa interfaccia anziché implementare un'interfaccia personalizzata.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**archiviazione del set di proprietà**
</dt> <dd>

Oggetto di archiviazione COM che contiene un set di proprietà. L'archiviazione di un set di proprietà è un oggetto dipendente associato e gestito da un oggetto di archiviazione.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**finestra delle proprietà**
</dt> <dd>

Set di pagine delle proprietà per uno o più oggetti .

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**Proxy**
</dt> <dd>

Oggetto specifico dell'interfaccia che crea un pacchetto di parametri per tale interfaccia in preparazione a una chiamata al metodo remoto. Un proxy viene eseguito nello spazio indirizzi del mittente e comunica con uno stub corrispondente nello spazio indirizzi del ricevitore.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**gestione proxy**
</dt> <dd>

Nel marshalling standard, proxy che gestisce tutti i proxy di interfaccia per un singolo oggetto.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo-oggetto**
</dt> <dd>

Parte di un documento o di un oggetto incorporato, ad esempio un intervallo di celle in un foglio di calcolo, che può essere l'origine di un oggetto COM.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**conteggio dei riferimenti**
</dt> <dd>

Mantenere un conteggio di ogni puntatore di interfaccia mantenuto su un oggetto per assicurarsi che l'oggetto non venga eliminato prima del rilascio di tutti i riferimenti a esso.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**
</dt> <dd>

Moniker che specifica la posizione di un oggetto rispetto alla posizione di un altro oggetto. Un moniker relativo è analogo a un percorso relativo, ad esempio . \\ backup \\ report.old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**server remoto**
</dt> <dd>

Applicazione server, implementata come file EXE, in esecuzione in un computer diverso dall'applicazione client che lo utilizza.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**Ripristinare**
</dt> <dd>

Per annullare le modifiche apportate a un oggetto dall'ultima volta in cui è stato eseguito il commit delle modifiche o dall'apertura dell'archiviazione dell'oggetto.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione radice**
</dt> <dd>

Oggetto di archiviazione più esterno in un documento. Un oggetto di archiviazione radice può contenere altri oggetti di archiviazione e flusso annidati. Ad esempio, un documento composto viene salvato su disco come una serie di oggetti di archiviazione e di flusso all'interno di un oggetto di archiviazione radice.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**stato di esecuzione**
</dt> <dd>

Stato di un oggetto COM quando l'applicazione server è in esecuzione ed è possibile accedere alle interfacce e ricevere notifiche delle modifiche.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**tabella oggetti in esecuzione (ROT)**
</dt> <dd>

Tabella accessibile a livello globale in ogni computer che tiene traccia di tutti gli oggetti COM nello stato di esecuzione che possono essere identificati da un moniker. I provider di moniker registrano un oggetto nella tabella, che incrementa il conteggio dei riferimenti dell'oggetto. Prima che l'oggetto possa essere eliminato, il relativo moniker deve essere rilasciato dalla tabella.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**proprietà di run-time**
</dt> <dd>

Informazioni discrete sullo stato associate a un oggetto controllo o al relativo contenitore. Esistono tre tipi di proprietà di run-time: proprietà di ambiente, proprietà di controllo e proprietà estese.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**auto-registrazione**
</dt> <dd>

Processo tramite il quale un server può eseguire le proprie operazioni del Registro di sistema.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**applicazione server**
</dt> <dd>

Applicazione in grado di creare oggetti COM. Le applicazioni contenitore possono quindi incorporare o collegare questi oggetti.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**oggetto statico**
</dt> <dd>

Oggetto che contiene solo una presentazione, senza dati nativi. Un contenitore può trattare un oggetto statico come se fosse un oggetto collegato o incorporato, ad eccezione del fatto che non è possibile modificare un oggetto statico.

Un oggetto statico può risultare, ad esempio, dall'interruzione di un collegamento in un oggetto collegato, ad esempio l'applicazione server non è disponibile o l'utente non vuole più aggiornare l'oggetto collegato.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IStorage.**](/windows/desktop/api/objidl/nn-objidl-istorage) Un oggetto di archiviazione contiene oggetti di archiviazione annidati o oggetti flusso, con conseguente equivalente a una struttura di directory/file all'interno di un singolo file.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**oggetto flusso**
</dt> <dd>

Oggetto COM che implementa [**l'interfaccia IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Un oggetto flusso è analogo a un file in una directory/file system.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Struttura Archiviazione**
</dt> <dd>

Tecnologia OLE per l'archiviazione di file compositi in file system nativi.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Stub**
</dt> <dd>

Quando viene effettuato il marshalling dei parametri di una funzione o di un metodo di interfaccia attraverso un limite di processo, lo stub è un oggetto specifico dell'interfaccia che annulla il pacchetto dei parametri di cui è stato effettuato il marshalling e chiama il metodo richiesto. Lo stub viene eseguito nello spazio indirizzi del ricevitore e comunica con un proxy corrispondente nello spazio indirizzi del mittente.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Gestione stub**
</dt> <dd>

Gestisce tutti gli stub dell'interfaccia per un singolo oggetto.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**chiamata sincrona**
</dt> <dd>

Chiamata di funzione che non consente l'esecuzione di altre istruzioni nel processo chiamante finché la funzione non viene restituita.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Registro di sistema**
</dt> <dd>

Repository a livello di sistema di informazioni supportate da Windows, che contiene informazioni sul sistema e sulle relative applicazioni, inclusi i client e i server OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modalità di accesso transazione**
</dt> <dd>

Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione. Quando vengono aperte in modalità transazione, le modifiche vengono archiviate nei buffer fino a quando l'oggetto di archiviazione radice non esegue il commit delle modifiche.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informazioni sul tipo**
</dt> <dd>

Informazioni sulla classe di un oggetto fornita da una libreria dei tipi. Per fornire informazioni sul tipo, un oggetto COM implementa [**l'interfaccia IProvideClassInfo.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo)

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**trasferimento uniforme dei dati**
</dt> <dd>

Modello per il trasferimento dei dati tramite gli Appunti, il trascinamento della selezione o l'automazione. Gli oggetti conformi a questo modello implementano [**l'interfaccia IDataObject.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Questo modello sostituisce DDE (dynamic data exchange).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**
</dt> <dd>

Decompressione dei parametri inviati a un proxy attraverso i limiti del processo.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**URL (Universal Resource Locator)**
</dt> <dd>

Identificatore usato dal World Wide Web per i nomi e i percorsi degli oggetti in Internet. OLE fornisce una classe moniker, il moniker URL, la cui implementazione può essere usata per associare un client agli oggetti identificati da un URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker URL**
</dt> <dd>

Moniker basato su un URL (Universal Resource Locator). Un client può usare moniker URL per l'associazione a oggetti che risiedono in Internet. La classe del moniker URL fornito dal sistema supporta sia l'associazione sincrona che l'associazione asincrona.

</dd> </dl>

 

 