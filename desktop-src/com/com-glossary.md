---
title: Glossario COM
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300517"
---
# <a name="com-glossary"></a>Glossario COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**attivazione**
</dt> <dd>

Processo di caricamento di un oggetto in memoria, che lo inserisce nello stato di esecuzione.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**stato attivo**
</dt> <dd>

Oggetto COM che si trova nello stato in esecuzione e ha un'interfaccia utente visibile.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker assoluto**
</dt> <dd>

Moniker che specifica la posizione assoluta di un oggetto. Un moniker assoluto è analogo a un percorso completo.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titolare consultivo**
</dt> <dd>

Oggetto COM che memorizza nella cache, gestisce e invia notifiche delle modifiche ai sink consultivi delle applicazioni contenitore.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**sink consultivo**
</dt> <dd>

Oggetto COM che può ricevere notifiche delle modifiche in un oggetto incorporato o in un oggetto collegato perché implementa l'interfaccia [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) o [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) . I contenitori che devono ricevere notifiche delle modifiche negli oggetti implementano un sink consultivo. Le notifiche provengono dal server, che usa un oggetto titolare consultivo per memorizzare nella cache e gestire le notifiche ai contenitori.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**oggetto aggregate**
</dt> <dd>

Oggetto COM costituito da uno o più oggetti COM. Un oggetto nell'aggregato viene designato come oggetto di controllo, che controlla quali interfacce dell'aggregazione sono esposte e quali sono private. Questo oggetto di controllo ha un'implementazione speciale di [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) denominata **IUnknown** di controllo. Tutti gli oggetti nell'aggregato devono passare le chiamate ai metodi **IUnknown** tramite il controllo **IUnknown**.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**aggregazione**
</dt> <dd>

Tecnica di composizione per l'implementazione di oggetti COM. Consente di compilare un nuovo oggetto riutilizzando una o più implementazioni dell'interfaccia di oggetti esistenti. L'oggetto aggregato sceglie le interfacce da esporre ai client e le interfacce vengono esposte come se fossero implementate dall'oggetto aggregato. I client dell'oggetto aggregato comunicano solo con l'oggetto aggregato.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Proprietà di ambiente**
</dt> <dd>

Proprietà della fase di esecuzione gestita ed esposta dal contenitore. In genere, una proprietà di ambiente rappresenta una caratteristica di un form, ad esempio il colore di sfondo, che deve essere comunicata a un controllo in modo che il controllo possa assumere l'aspetto dell'ambiente circostante.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**
</dt> <dd>

Inverso del moniker di un file, di un elemento o di un puntatore. Un anti-moniker viene aggiunto alla fine di un file, di un elemento o di un moniker del puntatore per annullare l'errore. Gli anti-moniker vengono usati nella costruzione di moniker relativi.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**conteggio dei riferimenti artificiali**
</dt> <dd>

Tecnica utilizzata per proteggere un oggetto prima di chiamare una funzione o un metodo che potrebbe eliminarlo in modo anomalo. Un programma chiama **IUnknown:: AddRef** per incrementare il conteggio dei riferimenti dell'oggetto prima di effettuare la chiamata che può liberare l'oggetto. Dopo la restituzione della funzione, il programma chiama **IUnknown:: Release** per decrementare il numero.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**Binding asincrono**
</dt> <dd>

Tipo di associazione in cui è necessario che il processo venga eseguito in modo asincrono per evitare un calo delle prestazioni per l'utente finale. In genere, l'associazione asincrona viene utilizzata negli ambienti distribuiti, ad esempio il World Wide Web. OLE supporta classi moniker asincrone e meccanismi di callback che consentono di eseguire il processo di individuazione e inizializzazione di un oggetto in un ambiente distribuito mentre vengono eseguite altre operazioni.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**chiamata asincrona**
</dt> <dd>

Una chiamata a una funzione che viene eseguita separatamente, in modo che il chiamante possa continuare l'elaborazione delle istruzioni senza attendere la restituzione della funzione.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker asincrono**
</dt> <dd>

Moniker che supporta l'associazione asincrona. Ad esempio, le istanze della classe moniker dell'URL fornita dal sistema sono moniker asincroni.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**automazione**
</dt> <dd>

Un modo per modificare gli oggetti di un'applicazione dall'esterno dell'applicazione. L'automazione viene in genere usata per creare applicazioni che espongono oggetti a strumenti di programmazione e linguaggi macro, per creare e modificare oggetti di un'applicazione da un'altra applicazione o per creare strumenti per l'accesso e la modifica di oggetti.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contesto di associazione**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) . I contesti di binding vengono utilizzati nelle operazioni del moniker per mantenere i riferimenti agli oggetti attivati quando viene associato un moniker. Il contesto di associazione contiene i parametri che si applicano a tutte le operazioni durante l'associazione di un moniker composito generico e fornisce all'implementazione del moniker l'accesso alle informazioni relative all'ambiente.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**associazione**
</dt> <dd>

Associazione di un nome al relativo referente. In particolare, individuando l'oggetto denominato da un moniker, inserendolo nello stato di esecuzione, se non è già e restituendo un puntatore a interfaccia. Gli oggetti possono essere associati in fase di esecuzione (chiamato anche associazione tardiva o associazione dinamica) o in fase di compilazione (detto anche binding statico).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**cache**
</dt> <dd>

Archivio locale di informazioni (in genere temporaneo). In OLE, una cache contiene informazioni che definiscono la presentazione di un oggetto collegato o incorporato quando il contenitore viene aperto.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inizializzazione della cache**
</dt> <dd>

Riempimento della cache di un oggetto collegato o incorporato con i dati di presentazione. L'interfaccia [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fornisce metodi che possono essere chiamati da un contenitore per controllare i dati che vengono memorizzati nella cache per gli oggetti collegati o incorporati.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**classe**
</dt> <dd>

Definizione di un oggetto nel codice. In C++, la classe di un oggetto è definita come tipo di dati, ma ciò non accade in altri linguaggi. Poiché OLE può essere codificato in qualsiasi linguaggio, la classe viene utilizzata per fare riferimento alla definizione dell'oggetto generale.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**class factory**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e che consente di creare una o più istanze di un oggetto identificato da un identificatore di classe specificato (CLSID).

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificatore di classe (CLSID)**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un oggetto della classe OLE. Se un oggetto classe verrà utilizzato per creare più di un'istanza di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti. Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**Classe (oggetto)**
</dt> <dd>

Nella programmazione orientata a oggetti, un oggetto il cui stato è condiviso da tutti gli oggetti in una classe e il cui comportamento agisce sui dati dello stato classwide. In COM, gli oggetti classe sono denominati class factory e in genere non hanno alcun comportamento ad eccezione della creazione di nuove istanze della classe.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**client**
</dt> <dd>

Oggetto COM che richiede servizi da un altro oggetto.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**sito client**
</dt> <dd>

Il sito di visualizzazione per un oggetto incorporato o collegato in un documento composto. Il sito client è il mezzo principale mediante il quale un oggetto richiede servizi dal relativo contenitore.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un oggetto della classe OLE. Se un oggetto classe verrà utilizzato per creare più di un'istanza di un oggetto, l'applicazione server associata deve registrare il proprio CLSID nel registro di sistema in modo che i client possano individuare e caricare il codice eseguibile associato agli oggetti. Ogni server o contenitore OLE che consente il collegamento ai relativi oggetti incorporati deve registrare un CLSID per ogni definizione di oggetto supportata.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**commit**
</dt> <dd>

Per salvare in modo permanente le modifiche apportate a un oggetto di archiviazione o flusso dopo l'apertura o l'ultimo salvataggio delle modifiche.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**componente**
</dt> <dd>

Oggetto che incapsula sia i dati che il codice e fornisce un set ben definito di servizi disponibili pubblicamente.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**
</dt> <dd>

Modello di programmazione orientato a oggetti OLE che definisce la modalità di interazione degli oggetti all'interno di un singolo processo o tra processi. In COM, i client possono accedere a un oggetto tramite le interfacce implementate sull'oggetto.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra dei menu composita**
</dt> <dd>

Una barra dei menu condivisa composta da gruppi di menu sia da un'applicazione contenitore sia da un'applicazione server attivata sul posto.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composito**
</dt> <dd>

Moniker costituito da due o più moniker considerati come un'unità. Un moniker composito può essere non generico, vale a dire che i relativi moniker di componente hanno una conoscenza speciale, o generica, che i moniker dei componenti non conoscono l'uno dall'altro tranne che sono moniker

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento composto**
</dt> <dd>

Documento che include oggetti collegati o incorporati, nonché i propri dati nativi.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**file composto**
</dt> <dd>

Implementazione di archiviazione strutturata fornita da OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Oggetto COM**
</dt> <dd>

Oggetto conforme a OLE Component Object Model (COM). Un oggetto COM è un'istanza di una definizione di oggetto che specifica i dati dell'oggetto e una o più implementazioni di interfacce sull'oggetto. I client interagiscono con un oggetto COM solo tramite le relative interfacce.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**oggetto collegabile**
</dt> <dd>

Oggetto COM che implementa come minimo l'interfaccia [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) per la gestione degli oggetti del punto di connessione. Gli oggetti collegabili supportano la comunicazione dal server al client. Un oggetto collegabile crea e gestisce uno o più sottooggetti del punto di connessione che ricevono gli eventi dalle interfacce implementate su altri oggetti e li inviano al client.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**oggetto punto di connessione**
</dt> <dd>

Oggetto COM gestito da un oggetto collegabile che implementa l'interfaccia [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) . Uno o più oggetti punto di connessione possono essere creati e gestiti da un oggetto collegabile. Ogni oggetto punto di connessione gestisce gli eventi in ingresso da un'interfaccia specifica su un altro oggetto e li invia al client.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**applicazione contenitore**
</dt> <dd>

Un'applicazione che supporta documenti composti. L'applicazione contenitore fornisce spazio di archiviazione per un oggetto incorporato o collegato, un sito per la visualizzazione, l'accesso al sito di visualizzazione e un sink consultivo per la ricezione delle notifiche delle modifiche nell'oggetto.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contenimento**
</dt> <dd>

Tecnica di composizione per l'implementazione di oggetti COM. Consente a un oggetto di riutilizzare alcune o tutte le implementazioni dell'interfaccia di uno o più oggetti. L'oggetto esterno funge da client per gli altri oggetti, delegando l'implementazione quando si desidera utilizzare i servizi di uno degli oggetti contenuti.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**contesto**
</dt> <dd>

In COM+, set di proprietà di run-time associate a uno o più oggetti COM utilizzati per fornire servizi per tali oggetti.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**controllo**
</dt> <dd>

Oggetto COM riutilizzabile e incorporabile che supporta, come minimo, l'interfaccia [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) . I controlli sono in genere associati all'interfaccia utente. Supportano anche la comunicazione con un contenitore e possono essere riutilizzati da più client, a seconda dei criteri di licenza.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contenitore di controlli**
</dt> <dd>

Un'applicazione che supporta l'incorporamento dei controlli implementando l'interfaccia [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Proprietà del controllo**
</dt> <dd>

Proprietà della fase di esecuzione esposta e gestita dal controllo stesso. Ad esempio, le dimensioni del tipo di carattere e del testo utilizzate dal controllo sono proprietà del controllo.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controllo oggetto**
</dt> <dd>

Oggetto all'interno di un oggetto aggregato che controlla quali interfacce all'interno dell'oggetto di aggregazione sono esposte e quali sono private. L'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto di controllo viene chiamata **IUnknown** di controllo. Le chiamate ai metodi **IUnknown** di altri oggetti nell'aggregazione devono essere passate all' **IUnknown** di controllo.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**sito di controllo**
</dt> <dd>

Struttura implementata da un contenitore di controlli per la gestione della visualizzazione e dell'archiviazione di un controllo. All'interno di un determinato contenitore, ogni controllo dispone di un sito di controllo corrispondente.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**oggetto trasferimento dati**
</dt> <dd>

Oggetto che implementa l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e contiene i dati da trasferire da un oggetto a un altro tramite gli Appunti o le operazioni di trascinamento della selezione.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**gestore oggetti predefinito**
</dt> <dd>

DLL fornita con OLE che funge da surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.

Con il gestore di oggetti predefinito, è possibile esaminare i dati archiviati di un oggetto senza attivare effettivamente l'oggetto. Il gestore dell'oggetto predefinito esegue altre attività, ad esempio il rendering di un oggetto dallo stato memorizzato nella cache quando l'oggetto viene caricato in memoria.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**oggetto dipendente**
</dt> <dd>

Oggetto COM in genere inizializzato da un altro oggetto (l'oggetto host). Sebbene la durata dell'oggetto dipendente possa essere utile solo per la durata dell'oggetto host, l'oggetto host non funziona come [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per l'oggetto dipendente. Al contrario, un oggetto è un oggetto aggregato quando la relativa durata (per mezzo del conteggio dei riferimenti) è completamente controllata dall'oggetto di gestione.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modalità di accesso diretto**
</dt> <dd>

Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione. In modalità diretta, viene immediatamente eseguito il commit di tutte le modifiche nell'oggetto di archiviazione radice.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**oggetto Document**
</dt> <dd>

Documento OLE che consente di visualizzare una o più visualizzazioni attivate sul posto dei dati all'interno di un frame nativo o esterno, ad esempio un browser, mantenendo al tempo stesso il controllo completo sulla relativa interfaccia utente. Oltre a implementare il normale documento OLE e le interfacce di attivazione sul posto, un oggetto Document deve implementare [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)e ognuna delle visualizzazioni (sotto forma di oggetto visualizzazione del documento) deve implementare [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contenitore di oggetti documento**
</dt> <dd>

Applicazione contenitore in grado di visualizzare una o più visualizzazioni di uno o più oggetti documento e di gestire tutti gli oggetti documento contenuti all'interno di un file. Ogni oggetto Document è associato a un sito del documento e ogni sito del documento contiene uno o più siti di visualizzazione del documento corrispondenti alle visualizzazioni supportate dall'oggetto Document. Un contenitore di oggetti documento include anche un frame contenitore che gestisce la negoziazione di menu e barre degli strumenti e l'enumerazione di oggetti contenuti.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**Server oggetti documento**
</dt> <dd>

Applicazione server in grado di fornire oggetti documento.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**sito del documento**
</dt> <dd>

Sito client implementato da un contenitore di oggetti documento per gestire la visualizzazione e l'archiviazione di un oggetto documento. Ogni oggetto Document in un contenitore dispone di un sito del documento corrispondente.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**oggetto del sito del documento**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , oltre alle consuete interfacce del sito client (ad esempio, [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**visualizzazione documento**
</dt> <dd>

Una presentazione particolare dei dati di un documento. Un singolo oggetto Document può avere una o più visualizzazioni, ma una sola visualizzazione documento può appartenere a un solo oggetto Document.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**oggetto visualizzazione documento**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) e corrisponde a una visualizzazione del documento particolare. Un oggetto con più visualizzazioni documento aggrega un oggetto visualizzazione documento separato per ogni visualizzazione.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**sito visualizzazione documento**
</dt> <dd>

Oggetto aggregato da un oggetto sito del documento per la gestione dello spazio di visualizzazione per una visualizzazione specifica di un oggetto documento. All'interno di un sito di documento specifico, ogni visualizzazione documento dispone di un sito di visualizzazione del documento corrispondente.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**oggetto sito visualizzazione documento**
</dt> <dd>

Oggetto COM aggregato in un oggetto sito del documento e implementa l'interfaccia [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) e, facoltativamente, l'interfaccia [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**trascinamento della selezione**
</dt> <dd>

Operazione in cui l'utente finale utilizza il mouse o un altro dispositivo di puntamento per spostare i dati in un'altra posizione nella stessa finestra o in un'altra finestra.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorpora**
</dt> <dd>

Per inserire un oggetto in un documento composto in modo da mantenere i formati di dati nativi di tale oggetto e per consentirne la modifica dall'interno del relativo contenitore utilizzando gli strumenti esposti dal server.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**oggetto incorporato**
</dt> <dd>

Oggetto i cui dati vengono archiviati in un documento composito, ma l'oggetto viene eseguito nello spazio di elaborazione del server. Il gestore dell'oggetto predefinito fornisce un surrogato nello spazio di elaborazione dell'applicazione contenitore per l'oggetto reale.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**proprietà estesa**
</dt> <dd>

Proprietà della fase di esecuzione, ad esempio la posizione e le dimensioni di un controllo, che un utente presume venga esposto dal controllo, ma viene esposto e gestito dal contenitore.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker del file**
</dt> <dd>

Moniker basato su un percorso nel file system. I moniker dei file possono essere utilizzati per identificare gli oggetti salvati nei propri file. Un moniker di file è un oggetto COM che supporta l'implementazione fornita dal sistema dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) per la classe del moniker del file.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**oggetto Font**
</dt> <dd>

Oggetto COM che fornisce l'accesso ai tipi di carattere Graphics Device Interface (GDI) implementando l'interfaccia [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificatore di formato**
</dt> <dd>

GUID che identifica un set di proprietà permanenti. Noto anche come FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**frame**
</dt> <dd>

Parte di un'applicazione contenitore responsabile della negoziazione di menu, tasti di scelta rapida, barre degli strumenti e altri elementi dell'interfaccia utente condivisi con un oggetto COM incorporato o un oggetto documento.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**oggetto frame**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) e, facoltativamente, l'interfaccia [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composito generico**
</dt> <dd>

Raccolta sequenziata di moniker, a partire da un moniker di file per fornire il percorso a livello di documento e continuare con uno o più moniker di elemento che, considerati come intero, identifica in modo univoco un oggetto.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**funzione helper**
</dt> <dd>

Funzione che incapsula le chiamate ad altre funzioni e metodi di interfaccia disponibili pubblicamente in OLE SDK. Le funzioni di supporto sono un modo pratico per chiamare sequenze di funzioni e metodi usati di frequente che eseguono attività comuni.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**oggetto host**
</dt> <dd>

Oggetto COM che costituisce una relazione gerarchica con uno o più oggetti COM, noti come oggetti dipendenti. In genere, l'oggetto host crea un'istanza degli oggetti dipendenti e la loro esistenza è utile solo nell'ambito della durata dell'oggetto host. Tuttavia, l'oggetto host non funge da [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) di controllo per gli oggetti dipendenti, né delega direttamente alle implementazioni dell'interfaccia di tali oggetti.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**HRESULT**
</dt> <dd>

Handle di risultato opaco definito come zero per un ritorno riuscito da una funzione e diverso da zero se vengono restituite informazioni sull'errore o sullo stato.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**Hyperlink (oggetto)**
</dt> <dd>

Oggetto COM che implementa come minimo l'interfaccia [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) e funge da collegamento a un oggetto in un'altra posizione, ovvero la destinazione. Un collegamento ipertestuale è costituito da quattro parti: un moniker che identifica la posizione della destinazione. stringa per la posizione all'interno della destinazione. nome descrittivo o visualizzabile per la destinazione; e una stringa che può contenere parametri aggiuntivi.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contesto di esplorazione collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) e gestisce lo stack di navigazione del collegamento ipertestuale. L'oggetto contesto browse gestisce la finestra cornice collegamento ipertestuale e la finestra dell'oggetto di destinazione del collegamento ipertestuale.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contenitore collegamento ipertestuale**
</dt> <dd>

Applicazione contenitore che supporta collegamenti ipertestuali implementando l'interfaccia [**IhlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e, se gli oggetti del contenitore possono essere destinazioni di altri collegamenti ipertestuali, l'interfaccia [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**oggetto cornice collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) e controlla l'esplorazione e la visualizzazione di primo livello dei collegamenti ipertestuali per il contenitore del frame e il server della destinazione del collegamento ipertestuale.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**oggetto collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IhlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e fornisce il moniker o l'identificatore di interfaccia del relativo contenitore Hyperlink. Un sito di collegamento ipertestuale può gestire più collegamenti ipertestuali.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**oggetto di destinazione collegamento ipertestuale**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) e fornisce il moniker, il nome descrittivo e altre informazioni che gli altri oggetti collegamento ipertestuale utilizzeranno per spostarsi su di esso.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**parametro in**
</dt> <dd>

Parametro allocato, impostato e liberato dal chiamante di una funzione o di un metodo di interfaccia. Un parametro in non viene modificato dalla funzione chiamata.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parametro in/out**
</dt> <dd>

Parametro inizialmente allocato dal chiamante di una funzione o di un metodo di interfaccia, e impostato, liberato e riallocato, se necessario, dal processo chiamato.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**attivazione sul posto**
</dt> <dd>

Modifica di un oggetto incorporato all'interno della finestra del relativo contenitore utilizzando gli strumenti forniti dal server. Gli oggetti collegati non supportano l'attivazione sul posto; vengono sempre modificati nella finestra del server.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**Server in-process**
</dt> <dd>

Server implementato come una DLL eseguita nello spazio di processo del client.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**istanza**
</dt> <dd>

Oggetto per cui viene allocata la memoria o persistente.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interfaccia**
</dt> <dd>

Gruppo di funzioni semanticamente correlate che consentono di accedere a un oggetto COM. Ogni interfaccia OLE definisce un contratto che consente agli oggetti di interagire in base al Component Object Model (COM). Sebbene OLE fornisca molte implementazioni di interfaccia, la maggior parte delle interfacce può essere implementata anche dagli sviluppatori che progettano applicazioni OLE.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificatore di interfaccia (IID)**
</dt> <dd>

Identificatore univoco globale (GUID) associato a un'interfaccia. Alcune funzioni accettano IID come parametri per consentire al chiamante di specificare quale puntatore a interfaccia deve essere restituito.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker elemento**
</dt> <dd>

Moniker basato su una stringa che identifica un oggetto in un contenitore. I moniker degli elementi possono identificare oggetti più piccoli di un file, inclusi gli oggetti incorporati in un documento composto o uno pseudo-oggetto, ad esempio un intervallo di celle in un foglio di calcolo.

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licenze**
</dt> <dd>

Funzionalità di COM che consente di controllare la creazione di oggetti. Gli oggetti con licenza possono essere creati solo dai client autorizzati a utilizzarli. Le licenze sono implementate in COM tramite l'interfaccia [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e dal supporto di un codice di licenza che può essere passato in fase di esecuzione.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**link (oggetto)**
</dt> <dd>

Oggetto COM creato quando un oggetto COM collegato viene creato o caricato. L'oggetto link viene fornito da OLE e implementa l'interfaccia [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**oggetto collegato**
</dt> <dd>

Oggetto COM i cui dati di origine si trovano fisicamente in cui è stato inizialmente creato. Con il documento composto viene mantenuto solo un moniker che rappresenta i dati di origine e i dati di presentazione appropriati. Le modifiche apportate all'origine del collegamento vengono riflesse automaticamente nell'oggetto collegato.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origine collegamento**
</dt> <dd>

Dati che rappresenta l'origine di un oggetto collegato. Un'origine di collegamento può essere un file o una parte di un file, ad esempio un intervallo selezionato di celle all'interno di un file (detto anche pseudo oggetto).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**stato caricato**
</dt> <dd>

Lo stato di un oggetto dopo la relativa struttura di dati è stato caricato in memoria e accessibile al processo client.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**server locale**
</dt> <dd>

Un server out-of-process implementato come. Applicazione EXE in esecuzione nello stesso computer dell'applicazione client.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**blocco**
</dt> <dd>

Un puntatore mantenuto e possibilmente un conteggio di riferimenti incrementato in un oggetto in esecuzione. OLE definisce due tipi di blocchi che possono essere conservati su un oggetto: forte e debole. Per implementare un blocco sicuro, è necessario che un server mantenga sia un puntatore che un conteggio dei riferimenti, in modo che l'oggetto rimanga "bloccato" nella memoria almeno finché il server non chiama [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Per implementare un blocco debole, il server gestisce solo un puntatore all'oggetto, in modo che l'oggetto possa essere eliminato da un altro processo.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshalling**
</dt> <dd>

Creazione di pacchetti e invio di chiamate al metodo di interfaccia attraverso limiti di thread o processi.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo di supporto**
</dt> <dd>

Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo di contenuto MIME**
</dt> <dd>

Estensione MIME che consente la negoziazione del formato dati tra un client e un oggetto.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**Multipurpose Internet Mail Extension (MIME)**
</dt> <dd>

Protocollo Internet sviluppato originariamente per consentire lo scambio di messaggi di posta elettronica con contenuti avanzati in ambienti di rete, computer e posta elettronica eterogenei. In pratica, MIME è stato inoltre adottato ed esteso da applicazioni non di posta elettronica.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Oggetto che implementa l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Un moniker funge da nome che identifica in modo univoco un oggetto COM. Nello stesso modo in cui un percorso identifica un file nel file system, un moniker identifica un oggetto COM nello spazio dei nomi della directory.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**Classe moniker**
</dt> <dd>

Implementazione dell'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Le classi del moniker fornite dal sistema includono moniker di file, moniker di elementi, moniker compositi generici, anti-moniker, moniker di puntatore e moniker URL.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**client moniker**
</dt> <dd>

Applicazione che usa i moniker per acquisire i puntatori di interfaccia agli oggetti gestiti da un'altra applicazione.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**provider moniker**
</dt> <dd>

Applicazione che rende disponibili moniker che identificano gli oggetti gestiti, in modo che gli oggetti siano accessibili ad altre applicazioni.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**estensione dello spazio dei nomi**
</dt> <dd>

Oggetto COM in-process che implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), che vengono talvolta definiti interfacce di estensione dello spazio dei nomi. Un'estensione dello spazio dei nomi viene utilizzata per estendere lo spazio dei nomi della shell o per creare uno spazio dei nomi separato. Gli utenti primari sono le finestre di dialogo Esplora risorse e file comuni.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**dati nativi**
</dt> <dd>

Dati utilizzati da un'applicazione server OLE durante la modifica di un oggetto incorporato.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**oggetto**
</dt> <dd>

In OLE, una struttura di programmazione che incapsula i dati e le funzionalità che vengono definiti e allocati come singola unità e per cui l'unico accesso pubblico è attraverso le interfacce della struttura di programmazione. Un oggetto COM deve supportare come minimo l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , che mantiene l'esistenza dell'oggetto mentre viene utilizzata e fornisce l'accesso alle altre interfacce dell'oggetto.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**stato dell'oggetto** 
</dt> <dd>

Relazione tra un oggetto documento composto nel relativo contenitore e l'applicazione responsabile della creazione dell'oggetto: attivo, passivo, caricato o in esecuzione. Gli oggetti passivi vengono archiviati su disco o in un database e l'oggetto non è selezionato o attivo. Nello stato Loaded, le strutture di dati dell'oggetto sono state caricate in memoria, ma non sono disponibili per operazioni come la modifica. Gli oggetti in esecuzione sono entrambi caricati e disponibili per tutte le operazioni. Gli oggetti attivi eseguono oggetti con un'interfaccia utente visibile.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nome del tipo di oggetto**
</dt> <dd>

Stringa di identificazione univoca archiviata come parte delle informazioni disponibili per un oggetto nel database di registrazione.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OLE**
</dt> <dd>

Tecnologia basata su oggetti Microsoft per la condivisione di informazioni e servizi tra i limiti del computer e del processo.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**server out-of-process**
</dt> <dd>

Un server, implementato come. Applicazione EXE, che viene eseguita all'esterno del processo del client, nello stesso computer o in un computer remoto.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**parametro out**
</dt> <dd>

Un parametro out viene allocato dalla funzione chiamata e liberata dal chiamante.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**stato passivo**
</dt> <dd>

Stato di un oggetto COM quando è archiviato (su disco o in un database). L'oggetto non è selezionato o attivo.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Proprietà persistente**
</dt> <dd>

Informazioni che possono essere archiviate in modo permanente come parte di un oggetto di archiviazione, ad esempio un file o una directory. Le proprietà permanenti vengono raggruppate in set di proprietà, che possono essere visualizzati e modificati.

Una proprietà persistente è diversa dalle proprietà di runtime di oggetti creati con controlli OLE e tecnologie di automazione, che possono essere utilizzate per influire sul comportamento del sistema. La struttura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) definisce tutti i tipi validi di proprietà permanenti, mentre la struttura **Variant** definisce tutti i tipi validi di proprietà della fase di esecuzione.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**archiviazione permanente**
</dt> <dd>

Archiviazione di un file o di un oggetto in un supporto, ad esempio un file system o un database, in modo che l'oggetto e i relativi dati vengano mantenuti quando il file viene chiuso e riaperto in un secondo momento.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**oggetto Picture**
</dt> <dd>

Oggetto COM che fornisce l'accesso alle immagini GDI implementando l'interfaccia [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker puntatore**
</dt> <dd>

Moniker che esegue il mapping di un puntatore a interfaccia a un oggetto in memoria. Mentre la maggior parte dei moniker identifica gli oggetti che possono essere archiviati in modo permanente, i moniker del puntatore identificano gli oggetti che non possono. Consentono a tali oggetti di partecipare a un'operazione di associazione del moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**dati di presentazione**
</dt> <dd>

Dati utilizzati da un contenitore per la visualizzazione di oggetti incorporati o collegati.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo primario**
</dt> <dd>

L'azione associata all'operazione più comune o preferita eseguita dagli utenti in un oggetto. Il verbo primario è sempre definito come verbo zero nel database di registrazione del sistema. Il verbo primario di un oggetto viene eseguito facendo doppio clic sull'oggetto.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Proprietà**
</dt> <dd>

Informazioni associate a un oggetto. In OLE le proprietà rientrano in due categorie: proprietà della fase di esecuzione e proprietà permanenti. Le proprietà in fase di esecuzione sono in genere associate a oggetti controllo o ai relativi contenitori. Il colore di sfondo, ad esempio, è una proprietà della fase di esecuzione impostata dal contenitore di un controllo. Le proprietà permanenti sono associate a oggetti archiviati.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**frame proprietà**
</dt> <dd>

Meccanismo dell'interfaccia utente che visualizza una o più pagine delle proprietà per un controllo. Il sistema di runtime dei controlli OLE fornisce un'implementazione standard di un frame di proprietà a cui è possibile accedere tramite la funzione di supporto [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificatore di proprietà**
</dt> <dd>

Intero con segno a quattro byte che identifica una proprietà persistente all'interno di un set di proprietà.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**pagina delle proprietà**
</dt> <dd>

Oggetto COM con il proprio CLSID che fa parte di un'interfaccia utente, implementata da un controllo e che consente di visualizzare e impostare le proprietà del controllo. Gli oggetti della pagina delle proprietà implementano l'interfaccia [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**sito della pagina delle proprietà**
</dt> <dd>

Posizione all'interno di un frame di proprietà in cui viene visualizzata una pagina delle proprietà. Il frame della proprietà implementa l'interfaccia [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , che contiene i metodi per gestire i siti di ogni pagina delle proprietà fornita da un controllo.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**set di proprietà**
</dt> <dd>

Un gruppo di proprietà correlate logicamente associato a un oggetto archiviato in modo permanente. Per creare, aprire, eliminare o enumerare uno o più set di proprietà, implementare l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) . Se si usano file composti, è possibile usare l'implementazione di OLE di questa interfaccia anziché implementarne di personalizzati.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**archiviazione set di proprietà**
</dt> <dd>

Oggetto di archiviazione COM che include un set di proprietà. Una risorsa di archiviazione del set di proprietà è un oggetto dipendente associato a e gestito da un oggetto di archiviazione.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**finestra delle proprietà**
</dt> <dd>

Set di pagine delle proprietà per uno o più oggetti.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**proxy**
</dt> <dd>

Oggetto specifico dell'interfaccia che consente di impacchettare i parametri per l'interfaccia in preparazione per una chiamata a un metodo remoto. Un proxy viene eseguito nello spazio degli indirizzi del mittente e comunica con uno stub corrispondente nello spazio degli indirizzi del destinatario.

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

Conservazione di un conteggio di ogni puntatore di interfaccia in un oggetto per garantire che l'oggetto non venga eliminato definitivamente prima del rilascio di tutti i relativi riferimenti.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**
</dt> <dd>

Moniker che specifica la posizione di un oggetto rispetto alla posizione di un altro oggetto. Un moniker relativo è analogo a un percorso relativo, ad esempio. \\ backup \\ report. old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**server remoto**
</dt> <dd>

Un'applicazione server, implementata come EXE, in esecuzione in un computer diverso dall'applicazione client che la utilizza.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**ripristinare**
</dt> <dd>

Per rimuovere le modifiche apportate a un oggetto a partire dall'ultima volta in cui è stato eseguito il commit delle modifiche o l'archiviazione dell'oggetto è stata aperta.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione radice**
</dt> <dd>

Oggetto di archiviazione più esterno in un documento. Un oggetto di archiviazione radice può contenere altri oggetti di archiviazione e di flusso annidati. Ad esempio, un documento composto viene salvato su disco come una serie di oggetti di archiviazione e di flusso all'interno di un oggetto di archiviazione radice.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**stato di esecuzione**
</dt> <dd>

Stato di un oggetto COM quando viene eseguita l'applicazione server ed è possibile accedere alle relative interfacce e ricevere una notifica delle modifiche.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**esecuzione tabella oggetti (ROT)**
</dt> <dd>

Tabella accessibile a livello globale in ogni computer che tiene traccia di tutti gli oggetti COM nello stato di esecuzione che possono essere identificati da un moniker. I provider moniker registrano un oggetto nella tabella, che incrementa il conteggio dei riferimenti dell'oggetto. Prima che l'oggetto possa essere eliminato definitivamente, il moniker deve essere rilasciato dalla tabella.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Proprietà della fase di esecuzione**
</dt> <dd>

Informazioni di stato discrete associate a un oggetto controllo o al relativo contenitore. Sono disponibili tre tipi di proprietà di runtime: proprietà di ambiente, proprietà del controllo e proprietà estese.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registrazione automatica**
</dt> <dd>

Processo mediante il quale un server può eseguire le proprie operazioni del registro di sistema.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**applicazione server**
</dt> <dd>

Un'applicazione in grado di creare oggetti COM. Le applicazioni contenitore possono quindi incorporare o collegarsi a questi oggetti.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**oggetto statico**
</dt> <dd>

Oggetto che contiene solo una presentazione, senza dati nativi. Un contenitore può considerare un oggetto statico come se fosse un oggetto collegato o incorporato, ad eccezione del fatto che non è possibile modificare un oggetto statico.

Un oggetto statico può risultare, ad esempio, dalla suddivisione di un collegamento su un oggetto collegato, ovvero l'applicazione server non è disponibile o l'utente non desidera che l'oggetto collegato venga aggiornato più.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**oggetto di archiviazione**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Un oggetto di archiviazione contiene oggetti di archiviazione annidati o oggetti flusso, ottenendo l'equivalente di una struttura di directory/file all'interno di un singolo file.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**oggetto Stream**
</dt> <dd>

Oggetto COM che implementa l'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) . Un oggetto flusso è analogo a un file in una directory/file system.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Archiviazione strutturata**
</dt> <dd>

Tecnologia OLE per l'archiviazione di file composti in file System nativi.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Stub**
</dt> <dd>

Quando viene effettuato il marshalling dei parametri di un metodo di interfaccia o di una funzione attraverso un limite del processo, lo stub è un oggetto specifico dell'interfaccia che consente di decreare il pacchetto dei parametri di marshalling e di chiamare il metodo richiesto. Lo stub viene eseguito nello spazio degli indirizzi del destinatario e comunica con un proxy corrispondente nello spazio degli indirizzi del mittente.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**gestione Stub**
</dt> <dd>

Gestisce tutti gli stub di interfaccia per un singolo oggetto.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**chiamata sincrona**
</dt> <dd>

Una chiamata di funzione che non consente l'esecuzione di istruzioni aggiuntive nel processo chiamante finché la funzione non restituisce.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**Registro di sistema**
</dt> <dd>

Un repository di informazioni a livello di sistema supportato da Windows, che contiene informazioni sul sistema e le relative applicazioni, inclusi client e server OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modalità di accesso transazionale**
</dt> <dd>

Una delle due modalità di accesso in cui è possibile aprire un oggetto di archiviazione. Quando viene aperto in modalità transazionale, le modifiche vengono archiviate nei buffer finché l'oggetto di archiviazione radice non esegue il commit delle modifiche.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informazioni sul tipo**
</dt> <dd>

Informazioni sulla classe di un oggetto fornita da una libreria dei tipi. Per fornire informazioni sul tipo, un oggetto COM implementa l'interfaccia [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**trasferimento dati uniforme**
</dt> <dd>

Modello per il trasferimento dei dati attraverso gli appunti, il trascinamento della selezione o l'automazione. Gli oggetti conformi a questo modello implementano l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Questo modello sostituisce DDE (Dynamic Data Exchange).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**unmarshaling**
</dt> <dd>

Decompressione dei parametri che sono stati inviati a un proxy tra i limiti del processo.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**URL (Universal Resource Locator)**
</dt> <dd>

Identificatore utilizzato dal World Wide Web per i nomi e le posizioni degli oggetti su Internet. OLE fornisce una classe moniker, moniker URL, la cui implementazione può essere utilizzata per associare un client a oggetti identificati da un URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker URL**
</dt> <dd>

Moniker basato su un URL (Universal Resource Locator). Un client può usare i moniker URL per eseguire l'associazione a oggetti che si trovano su Internet. La classe del moniker URL fornita dal sistema supporta l'associazione sincrona e asincrona.

</dd> </dl>

 

 