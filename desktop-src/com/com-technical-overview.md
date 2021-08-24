---
title: Panoramica tecnica di COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'Altre informazioni su: Panoramica tecnica di COM'
keywords:
- COM Technical Overview COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851a2147c1bbe31dd8c212f7f23089c522cf7998bc2d336e95120277fba84275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854761"
---
# <a name="com-technical-overview"></a>Panoramica tecnica di COM

Questo argomento offre una panoramica di Microsoft Component Object Model (COM):

-   [Introduzione a COM](#introduction-to-com)
-   [Oggetti e interfacce](#objects-and-interfaces)
-   [Implementazione dell'interfaccia](#interface-implementation)
-   [Interfaccia IUnknown](#the-iunknown-interface)
-   [Modello client/server](#the-clientserver-model)
-   [Gestione controllo servizi](#service-control-manager)
-   [Riutilizzabilità](#reusability)
-   [Archiviazione e oggetti Stream](#storage-and-stream-objects)
-   [Trasferimento dati](#data-transfer)
-   [Comunicazione remota](#remoting)
-   [Sicurezza](#security)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-com"></a>Introduzione a COM

Microsoft Component Object Model (COM) definisce uno standard di interoperabilità binaria per la creazione di librerie software riutilizzabili che interagiscono in fase di esecuzione. È possibile usare librerie COM senza la necessità di compilarle nell'applicazione. COM è la base per una serie di prodotti e tecnologie Microsoft, ad esempio Windows Media Player e Windows Server.

COM definisce uno standard binario che si applica a molti sistemi operativi e piattaforme hardware. Per il network computing, COM definisce un formato e un protocollo di collegamento standard per l'interazione tra oggetti eseguiti su piattaforme hardware diverse. COM è indipendente dal linguaggio di implementazione, pertanto è possibile creare librerie COM usando linguaggi di programmazione diversi, ad esempio C++ e quelli nel .NET Framework.

La specifica COM fornisce tutti i concetti fondamentali che consentono il riutilizzo del software multipiattaforma:

-   Standard binario per le chiamate di funzione tra componenti.
-   Provisioning per raggruppamenti fortemente tipizzato di funzioni in interfacce.
-   Interfaccia di base che fornisce il polimorfismo, l'individuazione delle funzionalità e il rilevamento della durata degli oggetti.
-   Meccanismo che identifica in modo univoco i componenti e le relative interfacce.
-   Caricatore di componenti che crea istanze del componente da una distribuzione.

COM include diverse parti che funzionano insieme per consentire la creazione di applicazioni compilate da componenti riutilizzabili:

-   Sistema *host che* fornisce un ambiente di run-time conforme alla specifica COM.
-   *Interfacce che* definiscono contratti di funzionalità e *componenti che* implementano le interfacce.
-   *Server* che forniscono componenti al sistema e *client* che usano le funzionalità fornite dai componenti.
-   Registro *di sistema* che tiene traccia della posizione in cui i componenti vengono distribuiti in host locali e remoti.
-   Gestione *controllo servizi che* individua i componenti in host locali e remoti e connette i server ai client.
-   Protocollo *di archiviazione* strutturata che definisce come esplorare il contenuto dei file nel file system host.

L'abilitazione del ri-uso del codice tra host e piattaforme è fondamentale per COM. Un'implementazione dell'interfaccia riutilizzabile è denominata *componente*, oggetto *componente* o *oggetto COM*. Un componente implementa una o più interfacce COM.

È possibile definire una libreria COM personalizzata progettando le interfacce implementate dalla libreria. Gli utenti della libreria possono individuare e usare le relative funzionalità senza conoscere i dettagli di distribuzione e implementazione della libreria.

## <a name="objects-and-interfaces"></a>Oggetti e interfacce

Un oggetto COM espone le funzionalità tramite *un'interfaccia*, che è una raccolta di funzioni membro. Un'interfaccia COM definisce il comportamento previsto e le responsabilità di un componente e specifica un contratto fortemente tipizzato che fornisce un piccolo set di operazioni correlate. Tutte le comunicazioni tra componenti COM si verificano tramite interfacce e tutti i servizi offerti da un componente vengono esposti tramite la relativa interfaccia. Un chiamante può accedere solo alle funzioni membro dell'interfaccia. Lo stato interno non è disponibile per un chiamante, a meno che non sia esposto nell'interfaccia .

Le interfacce sono fortemente tipizzato. Ogni interfaccia ha un proprio identificatore di interfaccia univoco, denominato IID, che elimina le collisioni che potrebbero verificarsi con nomi leggibili dall'utente. L'IID è un identificatore univoco globale (GUID), che corrisponde all'ID univoco universale (UUID) definito da Open Software Foundation (OSF) Distributed Computing Environment (DCE). Quando si crea una nuova interfaccia, è necessario creare un nuovo identificatore per tale interfaccia. Quando un chiamante usa un'interfaccia, deve usare l'identificatore univoco. Questa identificazione esplicita migliora l'affidabilità eliminando i conflitti di denominazione che causano un errore di run-time.

Quando si definisce una nuova interfaccia, è possibile creare una definizione di interfaccia usando il linguaggio IDL (Interface Definition Language). Da questa definizione di interfaccia, il compilatore IDL Microsoft genera file di intestazione per l'uso da parte delle applicazioni tramite l'interfaccia e codice sorgente per gestire le chiamate di procedura remota. Il linguaggio IDL fornito da Microsoft si basa su semplici estensioni a DCE IDL, uno standard di settore per l'elaborazione distribuita basata su RPC (Remote Procedure Call). IDL è uno strumento per la praticità della finestra di progettazione dell'interfaccia e non è fondamentale per l'interoperabilità COM. Con IDL non è necessario creare manualmente i file di intestazione per ogni ambiente di programmazione. Per altre informazioni, vedere [Definizione di interfacce COM.](defining-com-interfaces.md)

L'ereditarietà viene usata con parsimonio nelle interfacce COM. COM supporta l'ereditarietà dell'interfaccia solo per riutilizzare un contratto associato a un'interfaccia di base. COM non supporta l'ereditarietà selettiva. Pertanto, se un'interfaccia eredita da un'altra, include tutte le funzioni definite dall'interfaccia di base. Inoltre, le interfacce usano solo l'ereditarietà singola, anziché l'ereditarietà multipla, per ottenere funzioni da un'interfaccia di base.

## <a name="interface-implementation"></a>Implementazione dell'interfaccia

Non è possibile creare un'istanza di un'interfaccia COM da sola. Viene invece creata un'istanza di una classe che implementa l'interfaccia . In C++, un'interfaccia COM viene modellata come classe *di base* astratta, il che significa che l'interfaccia è una classe C++ che contiene solo funzioni membro virtuali pure. Una libreria C++ implementa gli oggetti COM ereditando le firme delle funzioni membro da una o più interfacce, eseguendo l'override di ogni funzione membro e fornendo un'implementazione per ogni funzione.

È possibile usare qualsiasi linguaggio di programmazione che supporti il concetto di puntatori a funzione per implementare un'interfaccia COM. In C, ad esempio, un'interfaccia è una struttura contenente un puntatore a una tabella di puntatori a funzione, uno per ogni metodo nell'interfaccia.

Quando si implementa un'interfaccia, la classe deve fornire un'implementazione per ogni funzione nell'interfaccia. Se la classe non ha alcuna operazione da eseguire in una funzione di interfaccia, l'implementazione può essere una singola istruzione return.

Una classe COM viene identificata usando un ID classe (CLSID) univoco a 128 bit che associa una classe a una distribuzione specifica nel file system, che per Windows è una DLL o un FILE EXE. Un CLSID è un GUID, il che significa che nessun'altra classe ha lo stesso CLSID. L'uso di identificatori di classe univoci impedisce conflitti di nomi tra le classi. Ad esempio, due fornitori diversi possono scrivere una classe denominata CStack, ma entrambe le classi hanno un CLSID univoco, quindi viene evitata qualsiasi possibilità di collisione.

È possibile ottenere un nuovo CLSID usando la funzione [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) o uno strumento di creazione COM, ad esempio Visual Studio, che chiama questa funzione internamente.

## <a name="the-iunknown-interface"></a>Interfaccia IUnknown

Tutte le interfacce COM ereditano [**dall'interfaccia IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) **L'interfaccia IUnknown** contiene le operazioni COM fondamentali per il polimorfismo e la gestione della durata dell'istanza. **L'interfaccia IUnknown** ha tre funzioni membro, denominate [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Tutti gli oggetti COM sono necessari per implementare **l'interfaccia IUnknown.**

La [**funzione membro QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fornisce il polimorfismo per COM. Chiamare **QueryInterface** per determinare in fase di esecuzione se un oggetto COM supporta una determinata interfaccia. L'oggetto COM restituisce un puntatore a interfaccia nel `ppvObject` parametro se implementa l'interfaccia richiesta, in caso contrario restituisce `NULL` . La **funzione membro QueryInterface** consente lo spostamento tra tutte le interfacce supportate da un oggetto COM.

La durata di un'istanza di oggetto COM è controllata dal relativo *conteggio dei riferimenti.* Le [**funzioni membro IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) controllano il conteggio. **AddRef** incrementa il conteggio e **Release** decrementa il conteggio. Quando il conteggio dei riferimenti raggiunge lo zero, la funzione membro **Release** può liberare l'istanza, perché nessun chiamante la usa.

## <a name="the-clientserver-model"></a>Modello client/server

Una classe COM implementa una serie di interfacce COM. L'implementazione è costituita da file binari che vengono eseguiti quando un chiamante interagisce con un'istanza della classe COM. COM consente l'uso di una classe in applicazioni diverse, incluse le applicazioni scritte senza conoscere una classe specifica. In una Windows, le classi sono presenti in una libreria collegata dinamica (DLL) o in un'altra applicazione (EXE).

Nel sistema host COM gestisce un database di registrazione di tutti i CLSID per gli oggetti COM installati nel sistema. Il database di registrazione è un mapping tra ogni CLSID e il percorso della DLL o dell'EXE che ospita la classe corrispondente. COM esegue una query su questo database ogni volta che un chiamante vuole creare un'istanza di una classe COM. Il chiamante deve conoscere solo il CLSID per richiedere una nuova istanza della classe .

L'interazione tra un oggetto COM e i relativi chiamanti viene modellata come relazione client/server. Il client è il chiamante che richiede un oggetto COM dal sistema e il server è il modulo che ospita gli oggetti COM che forniscono servizi ai client.

Un client COM è qualsiasi chiamante che passa un CLSID al sistema per richiedere un'istanza di un oggetto COM. Il modo più semplice per creare un'istanza di è chiamare la funzione COM [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

La [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) crea un'istanza del CLSID specificato e restituisce un puntatore a interfaccia del tipo richiesto dal client. Il client è responsabile della gestione della durata dell'istanza chiamando la relativa funzione [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando il client ha terminato di usarla. Per creare più oggetti basati su un singolo CLSID, chiamare la [**funzione CoGetClassObject.**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) Per connettersi a un oggetto già creato ed eseguito, chiamare la [**funzione GetActiveObject.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject)

Un server COM fornisce un'implementazione COM al sistema. Un server associa un CLSID a una classe COM, ospita l'implementazione della classe , implementa un class factory per la creazione di istanze della classe e fornisce per lo scaricamento del server.

> [!Note]  
> Un server COM non corrisponde all'oggetto COM fornito al sistema.

 

Per consentire la creazione di un oggetto COM, un server COM deve fornire un'implementazione [**dell'interfaccia IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) I client possono chiamare [**il metodo CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) per richiedere una nuova istanza di un oggetto COM, ma in genere tali richieste vengono incapsulate nella [**funzione CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

È possibile distribuire un server COM come libreria condivisa caricata nel processo del client in fase di esecuzione (DLL su piattaforme Windows) o come modulo eseguibile (EXE su piattaforme Windows). Per altre informazioni, vedere [Registrazione di applicazioni COM.](registering-com-applications.md)

## <a name="service-control-manager"></a>Gestione controllo servizi

Gestione controllo servizi gestisce la richiesta client per un'istanza di un oggetto COM. L'elenco seguente mostra la sequenza di eventi:

-   Un client richiede un puntatore a interfaccia a un oggetto COM dalla libreria COM chiamando una funzione come [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con il CLSID dell'oggetto COM.
-   La libreria COM esegue una query su SCM per trovare il server che corrisponde al CLSID richiesto.
-   Gestione controllo servizi individua il server e richiede la creazione dell'oggetto COM dal class factory fornito dal server.
-   In caso di esito positivo, la libreria COM restituisce un puntatore a interfaccia al client.

Dopo che il sistema COM ha connesso un oggetto server a un client, il client e l'oggetto comunicano direttamente. Non si verifica alcun sovraccarico aggiuntivo derivato dalla chiamata tramite un tempo di esecuzione intermedio.

Quando si registra un server COM con il sistema host, è possibile specificare modi diversi per attivare il server. L'elenco seguente illustra i tre modi in cui Gestione configurazione server può attivare un server COM:

-   In-process: Gestione controllo servizi restituisce il percorso file della DLL che contiene l'implementazione del server oggetti. La libreria COM carica la DLL ed esegue una query per il relativo puntatore class factory di interfaccia.
-   Locale: Gestione controllo servizi avvia il file eseguibile locale che registra un class factory all'avvio e il relativo puntatore di interfaccia è disponibile per il sistema e i client.
-   Remoto: gestione controllo servizi locale acquisisce un puntatore class factory di interfaccia da Gestione controllo servizi in esecuzione in un computer remoto.

Quando un client richiede un oggetto COM, la libreria COM contatta Gestione controllo servizi nell'host locale. Gestione controllo servizi individua il server COM appropriato, che può essere locale o remoto, e il server restituisce un puntatore di interfaccia al class factory del server. Quando il class factory è disponibile, la libreria COM o il client può usare il class factory per creare l'oggetto richiesto. Per altre informazioni, vedere [Implementazione di IClassFactory.](implementing-iclassfactory.md)

## <a name="reusability"></a>Riusabilità

COM supporta la *riusabilità black box,* il che significa che i dettagli di implementazione di un componente riutilizzabile non sono esposti ai client. Per ottenere la riusabilità delle black box, COM supporta due meccanismi tramite i quali un oggetto può riutilizzarne un altro. Le due forme di riutilizzo sono denominate *contenimento e* *aggregazione.* Per convenzione, l'oggetto riutilizzato è denominato oggetto interno e l'oggetto che usa l'oggetto interno è denominato oggetto *esterno.* 

Nel contenimento, l'oggetto esterno si comporta come un client dell'oggetto interno. L'oggetto esterno è un contenitore logico per l'oggetto interno e quando l'oggetto esterno usa i servizi dell'oggetto interno, l'oggetto esterno delega l'implementazione alle interfacce dell'oggetto interno. Ciò significa che l'oggetto esterno viene implementato in termini di servizi dell'oggetto interno. L'oggetto esterno potrebbe non supportare le stesse interfacce dell'oggetto interno e l'oggetto esterno può usare l'interfaccia di un oggetto interno per facilitare l'implementazione di parti di un'interfaccia diversa sull'oggetto esterno.

In aggregazione, l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate nell'oggetto esterno. Ciò è utile quando l'oggetto esterno delega sempre ogni chiamata su una delle relative interfacce alla stessa interfaccia dell'oggetto interno. L'aggregazione è una comodità che consente all'oggetto esterno di evitare un sovraccarico di implementazione aggiuntivo.

Per altre informazioni, vedere [Riutilizzo di oggetti](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>oggetti Archiviazione e Stream

Gli oggetti COM salvano lo stato in un file usando l'archiviazione strutturata *,* che è una forma di archiviazione permanente che consente la navigazione del contenuto di un file file system semantica. La gestione del contenuto di un file in questo modo consente funzionalità come l'accesso incrementale, le transazioni e la condivisione tra processi.

La specifica di archiviazione persistente COM fornisce due tipi di elementi di archiviazione: oggetti di archiviazione e oggetti flusso. Questi oggetti vengono implementati dalla libreria COM e le applicazioni utente raramente implementano questi elementi di archiviazione. Archiviazione implementano [**l'interfaccia IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) e gli oggetti flusso implementano [**l'interfaccia IStream.**](/windows/desktop/api/objidl/nn-objidl-istream)

Un oggetto flusso contiene dati ed è concettualmente simile a un singolo file in un file system. Ogni flusso ha diritti di accesso e un singolo puntatore di ricerca. Tramite [**l'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) è possibile leggere, scrivere, cercare ed eseguire altre operazioni sui dati sottostanti del flusso. Un flusso viene denominato usando una stringa di testo. Può contenere qualsiasi struttura interna, perché è un flusso flat di byte. Inoltre, le funzioni **nell'interfaccia IStream** sono simili alle funzioni standard basate su handle di file, ad esempio quelle della libreria di runtime C ANSI.

Un oggetto di archiviazione è concettualmente simile a una directory in un file system. Ogni archiviazione può contenere un numero qualsiasi di oggetti di archiviazione secondaria e qualsiasi numero di flussi. Ogni archiviazione ha i propri diritti di accesso. Tramite [**l'interfaccia IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) è possibile eseguire operazioni quali l'enumerazione, lo spostamento, la copia, la ridenominazione, la creazione e l'eliminazione di elementi. Un oggetto di archiviazione non archivia i dati definiti dall'applicazione, ma archivia in modo implicito i nomi degli elementi (archivi e flussi) in esso contenuti.

Archiviazione e gli oggetti di flusso sono gestibili tra i processi quando vengono implementati in base alla specifica COM in una piattaforma host. In questo modo gli oggetti in esecuzione in-process o out-of-process hanno lo stesso accesso incrementale all'archiviazione file. Poiché COM viene caricato separatamente in ogni processo, usa meccanismi di memoria condivisa supportati dal sistema operativo per comunicare lo stato degli elementi aperti e le relative modalità di accesso tra i processi.

Ogni oggetto di archiviazione e flusso in un file strutturato ha un nome per identificarlo. Il nome è una stringa che segue una convenzione specifica. Per altre informazioni, vedere Archiviazione [convenzioni di denominazione degli oggetti](/windows/desktop/Stg/storage-object-naming-conventions). Il nome viene passato alle [**funzioni IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) per specificare l'elemento nella memoria su cui operare. I nomi degli oggetti di archiviazione radice sono gli stessi dei nomi di file nel file system sottostante e devono seguire le convenzioni e le restrizioni del file system. Stringhe passate alle funzioni correlate all'archiviazione, i cui file dei nomi vengono passati al file system senza interpretazione o modifiche.

I nomi degli elementi contenuti negli oggetti di archiviazione vengono gestiti dall'implementazione dell'oggetto di archiviazione specifico in questione. Tutte le implementazioni di oggetti di archiviazione devono supportare nomi di elementi di lunghezza pari a 32 caratteri e alcune implementazioni possono supportare nomi più lunghi. I nomi vengono archiviati senza distinzione tra maiuscole e minuscole, ma vengono confrontati senza distinzione tra maiuscole e minuscole. Le applicazioni che definiscono i nomi degli elementi di archiviazione devono scegliere i nomi che funzionano in entrambe le situazioni.

È possibile accedere a ogni elemento in un file di archiviazione strutturata usando funzioni e interfacce implementate da COM. Ciò significa che altre applicazioni possono esplorare il file esplorando con le funzioni dell'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) che forniscono servizi simili a directory. Inoltre, altre applicazioni possono usare i dati del file, senza dover eseguire l'applicazione che ha scritto il file. Quando un'applicazione COM accede ai file di archiviazione strutturata di un'altra applicazione, vengono applicati Windows diritti di accesso standard e l'applicazione deve disporre di privilegi sufficienti.

Un oggetto COM può leggere e scrivere se stesso in un archivio permanente. Un client esegue una query per una delle interfacce correlate alla persistenza nell'oggetto COM, a seconda del contesto dell'operazione. Gli oggetti COM possono implementare qualsiasi combinazione delle interfacce seguenti:

-   [**IPersistStorage:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)l'oggetto COM legge e scrive lo stato persistente in un oggetto di archiviazione. Il client fornisce all'oggetto un puntatore [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) tramite questa interfaccia. Questa è l'unica interfaccia di persistenza che include la semantica per l'accesso incrementale.
-   [**IPersistStream:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)l'oggetto COM legge e scrive lo stato persistente in un oggetto flusso. Il client fornisce all'oggetto un [**puntatore IStream**](/windows/desktop/api/objidl/nn-objidl-istream) tramite questa interfaccia.
-   [**IPersistFile:**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)l'oggetto COM legge e scrive lo stato persistente direttamente in un file nel sistema sottostante. Questa interfaccia non coinvolge [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) a meno che non si accede al file sottostante tramite queste interfacce, ma l'interfaccia **IPersistFile** non ha alcuna semantica per le risorse di archiviazione e i flussi. Il client fornisce all'oggetto un nome file e chiama le [**funzioni Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) [**o Load.**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load)

## <a name="data-transfer"></a>Trasferimento dati

L'archiviazione strutturata costituisce la base per lo scambio di dati tra processi e oggetti COM, denominato *trasferimento uniforme dei dati.* Prima dell'implementazione di COM in OLE 2, il trasferimento dei dati in Windows è stato specificato dai protocolli di trasferimento *,* ad esempio gli Appunti e i protocolli di trascinamento della selezione. Ogni protocollo di trasferimento aveva un proprio set di funzioni che delimitava il protocollo alla query ed era necessario codice specifico per gestire ogni protocollo e procedura di scambio diversi. Il trasferimento uniforme dei dati rappresenta tutti i trasferimenti di dati tramite [**l'interfaccia IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) che separa le operazioni comuni di scambio dei dati dal protocollo di trasferimento.

[**L'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) incapsula le operazioni get e set standard su dati, query ed enumerazioni e notifiche che rilevano quando i dati cambiano in un oggetto. Il trasferimento uniforme dei dati consente descrizioni dettagliate dei formati di dati, nonché l'uso di diversi supporti di archiviazione per il trasferimento dei dati.

Durante il trasferimento uniforme dei dati, tutti i protocolli scambiano un puntatore a [**un'interfaccia IDataObject.**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) Il server è l'origine dei dati e implementa un oggetto dati, utilizzabile in qualsiasi protocollo di scambio dei dati. Il client utilizza i dati e richiede i dati da un oggetto dati quando riceve un **puntatore IDataObject** da qualsiasi protocollo. Dopo lo scambio di puntatori, entrambi i lati gestiscono lo scambio di dati in modo uniforme, tramite **l'interfaccia IDataObject.**

COM definisce due strutture di dati che consentono il trasferimento uniforme dei dati. La [**struttura FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) rappresenta un formato degli Appunti generalizzato e la [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) rappresenta il supporto di trasferimento come handle di memoria.

Il client crea una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per indicare il tipo di dati che richiede da un'origine dati e viene utilizzato dall'origine dati per descrivere i formati forniti. Il client esegue una query su un'origine dati per i formati disponibili richiedendo la relativa [**interfaccia IEnumFORMATETC.**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) Per altre informazioni, vedere [Struttura FORMATETC.](the-formatetc-structure.md)

Il client crea una [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) e la passa al metodo [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e l'oggetto dati restituisce i dati nella struttura **STGMEDIUM** fornita.

La [**struttura STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) consente ai client e alle origini dati di scegliere il supporto di scambio più efficiente. Ad esempio, se i dati da scambiare sono molto grandi, l'origine dati può indicare un supporto basato su disco come formato preferito, anziché la memoria principale. Questa flessibilità consente scambi di dati efficienti che possono essere veloci quanto il passaggio di un puntatore a [**un IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**a un IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Per altre informazioni, vedere [Struttura STGMEDIUM.](the-stgmedium-structure.md)

Un client di un'origine dati può richiedere una notifica quando i dati cambiano. COM gestisce le notifiche di modifica dei dati usando un *oggetto sink di* consulenza, che implementa [**l'interfaccia IAdviseSink.**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) L'oggetto sink advise e l'interfaccia **IAdviseSink** vengono implementati dal client, che passa un **puntatore IAdviseSink** all'origine dati. Quando l'origine dati rileva una modifica nei dati sottostanti, chiama un **metodo IAdviseSink** per notificare al client. Per altre informazioni, vedere [Notifica dei dati.](data-notification.md)

## <a name="remoting"></a>Comunicazione remota

COM consente il calcolo remoto e distribuito. *La comunicazione remota* dell'interfaccia consente a una funzione membro di restituire un puntatore a interfaccia a un oggetto COM che si trova in un processo diverso o in un computer host diverso. L'infrastruttura che esegue la comunicazione remota dell'interfaccia è trasparente sia per il client che per il server oggetti. Né il client né il server necessitano dei dettagli di distribuzione l'uno dell'altro per comunicare tramite un'interfaccia remota. Un client chiama le funzioni membro sulla stessa interfaccia per comunicare con un oggetto COM in-process, out-of-process nell'host locale o in un computer remoto. Le chiamate locali e remote sulla stessa interfaccia non sono distinguibili per il client.

Per comunicare con un oggetto COM, un client chiama sempre un'implementazione in-process. Se l'oggetto COM è in-process, la chiamata è diretta. Se l'oggetto COM è out-of-process o remoto, COM fornisce un'implementazione *proxy* che inoltra la chiamata all'oggetto tramite il protocollo RPC (Remote Procedure Call).

Un oggetto COM riceve sempre chiamate da un client tramite un'implementazione in-process. Se il chiamante è in-process, la chiamata è diretta. Se il chiamante è out-of-process o remoto, COM fornisce un'implementazione *stub* che riceve la chiamata di procedura remota dal proxy nel processo client.

*Il marshalling* è la procedura per la creazione del pacchetto dello stack di chiamate per la trasmissione da proxy a stub. *L'unmarsshaling* è il disimballaggio che si verifica all'estremità ricevente. Viene effettuato il marshalling e l'unmarssing dei valori restituiti dallo stub al proxy. Questo tipo di comunicazione è detto anche invio di una *chiamata in rete.*

Ogni tipo di dati diverso dispone di regole per il marshalling. I puntatori a interfaccia hanno anche un protocollo di marshalling, incapsulato nella [**funzione CoMarshalInterface.**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) Nella maggior parte dei casi, il marshalling dell'interfaccia *standard,* fornito dal sistema, è sufficiente, ma un oggetto COM facoltativamente può implementare il *marshalling* dell'interfaccia personalizzata per controllare la creazione di proxy di oggetti remoti verso se stesso. Per altre informazioni, vedere [Comunicazione tra oggetti.](inter-object-communication.md)

## <a name="security"></a>Sicurezza

COM offre due forme di sicurezza delle applicazioni. Uno è la sicurezza dell'attivazione, che specifica come vengono creati i nuovi oggetti, come si connettono i client a oggetti nuovi ed esistenti e come vengono protetti determinati servizi pubblici, ad esempio la tabella di classi e la tabella di oggetti in esecuzione. L'altro *è la chiamata di sicurezza*, che specifica il funzionamento della sicurezza in una connessione stabilita tra un client e un oggetto COM.

La sicurezza dell'attivazione viene applicata automaticamente da Gestione controllo servizi. Quando gestione controllo servizi riceve una richiesta di recupero di un oggetto COM, controlla la richiesta rispetto alle informazioni di sicurezza archiviate nel Registro di sistema.

Le implementazioni di Gestione controllo servizi offrono in genere una configurazione basata sul Registro di sistema per l'amministrazione di classi distribuite e per account utente specifici nell'host. Per altre informazioni, vedere [Sicurezza dell'attivazione.](activation-security.md)

La sicurezza delle chiamate viene applicata automaticamente o viene applicata dall'applicazione. Se l'applicazione fornisce informazioni di installazione, COM esegue i controlli necessari per proteggere l'applicazione.

Il meccanismo automatico controlla la sicurezza per il processo, ma non per singoli oggetti o metodi. Se un'applicazione richiede una sicurezza più granulare, COM fornisce funzioni che le applicazioni possono usare per eseguire il proprio controllo di sicurezza.

I meccanismi automatici e personalizzati possono essere usati insieme, quindi un'applicazione può chiedere a COM di eseguire il controllo di sicurezza automatico e quindi di eseguire il proprio.

I servizi di sicurezza delle chiamate COM sono suddivisi nelle categorie seguenti:

-   Funzioni generali chiamate da client e server, che consentono l'inizializzazione del meccanismo di sicurezza automatico e la registrazione dei servizi di autenticazione automatica. Le API di sicurezza delle chiamate generali sono [**le funzioni CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) [**e CoQueryAuthenticationServices.**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
-   Interfacce nei proxy client, che consentono al client di controllare la sicurezza nelle chiamate a singole interfacce. [**L'interfaccia IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e le funzioni [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) forniscono la sicurezza delle chiamate su un oggetto remoto.
-   Funzioni lato server e interfacce del contesto di chiamata, che consentono al server di recuperare informazioni di sicurezza su una chiamata e di rappresentare il chiamante. [**L'interfaccia IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) e le [**funzioni CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)e [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) forniscono la sicurezza delle chiamate lato server.

Spesso il client esegue una query sull'oggetto COM per [**l'interfaccia IClientSecurity,**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) implementata localmente dal livello di comunicazione remota. Il client utilizza questa interfaccia per controllare la sicurezza dei singoli proxy di interfaccia nell'oggetto COM prima di effettuare una chiamata a una delle interfacce.

Quando una chiamata arriva al server, il server può chiamare la funzione [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per recuperare [**un'interfaccia IServerSecurity,**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) che consente al server di controllare l'autenticazione del client e di rappresentare il client, se necessario. **L'oggetto IServerSecurity** è valido per la durata della chiamata.

Chiamare la [**funzione CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per inizializzare il livello di sicurezza e impostare i valori specificati come impostazioni predefinite per la sicurezza. Se un processo non chiama **CoInitializeSecurity**, COM la chiama automaticamente la prima volta che viene effettuato il marshalling o l'unmarsshaled di un'interfaccia, registrando la sicurezza predefinita del sistema. La **funzione CoInitializeSecurity** consente al client di stabilire la sicurezza delle chiamate predefinita per il processo, evitando così l'uso di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) nei singoli proxy. La **funzione CoInitializeSecurity** consente a un server di registrare i servizi di autenticazione automatica per il processo. Per altre informazioni, vedere [Setting Process-Wide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Definizione di interfacce COM](defining-com-interfaces.md)
</dt> <dt>

[Registrazione di applicazioni COM](registering-com-applications.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 
