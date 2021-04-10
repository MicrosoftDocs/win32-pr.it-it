---
title: Panoramica tecnica di COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'Ulteriori informazioni su: Panoramica tecnica di COM'
keywords:
- COM Panoramica tecnica com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5dc95ffae5166d86cd8110cab1a6b90e6ffa5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126606"
---
# <a name="com-technical-overview"></a>Panoramica tecnica di COM

In questo argomento viene fornita una panoramica di Microsoft Component Object Model (COM):

-   [Introduzione a COM](#introduction-to-com)
-   [Oggetti e interfacce](#objects-and-interfaces)
-   [Implementazione dell'interfaccia](#interface-implementation)
-   [Interfaccia IUnknown](#the-iunknown-interface)
-   [Modello client/server](#the-clientserver-model)
-   [Gestione controllo servizi](#service-control-manager)
-   [Riusabilità](#reusability)
-   [Oggetti di archiviazione e di flusso](#storage-and-stream-objects)
-   [Trasferimento dati](#data-transfer)
-   [Comunicazione remota](#remoting)
-   [Sicurezza](#security)
-   [Argomenti correlati](#related-topics)

## <a name="introduction-to-com"></a>Introduzione a COM

Microsoft Component Object Model (COM) definisce uno standard di interoperabilità binaria per la creazione di librerie software riutilizzabili che interagiscono in fase di esecuzione. È possibile usare le librerie COM senza la necessità di compilarle nell'applicazione. COM è la base per diversi prodotti e tecnologie Microsoft, ad esempio Windows Media Player e Windows Server.

COM definisce uno standard binario applicabile a molti sistemi operativi e piattaforme hardware. Per l'elaborazione di rete, COM definisce un formato wire standard e un protocollo per l'interazione tra gli oggetti eseguiti su piattaforme hardware diverse. COM è indipendente dal linguaggio di implementazione, il che significa che è possibile creare librerie COM usando linguaggi di programmazione diversi, ad esempio C++ e quelli nella .NET Framework.

La specifica COM fornisce tutti i concetti fondamentali che consentono il riutilizzo del software multipiattaforma:

-   Standard binario per le chiamate di funzione tra i componenti.
-   Un provisioning per raggruppamenti fortemente tipizzati di funzioni nelle interfacce.
-   Interfaccia di base che fornisce polimorfismo, individuazione delle funzionalità e rilevamento della durata degli oggetti.
-   Meccanismo che identifica in modo univoco i componenti e le relative interfacce.
-   Caricatore di componenti che crea istanze del componente da una distribuzione.

COM dispone di diverse parti che interagiscono per consentire la creazione di applicazioni compilate da componenti riutilizzabili:

-   *Sistema host* che fornisce un ambiente di runtime conforme alla specifica com.
-   *Interfacce* che definiscono i contratti di funzionalità e i *componenti* che implementano le interfacce.
-   *Server* che forniscono componenti al sistema e *client* che utilizzano le funzionalità fornite dai componenti di.
-   *Registro di sistema* che tiene traccia dei componenti distribuiti in host locali e remoti.
-   *Gestore di controllo del servizio* che individua i componenti in host locali e remoti e connette i server ai client.
-   Protocollo di *archiviazione strutturato* che definisce la modalità di esplorazione del contenuto dei file nel file System dell'host.

L'abilitazione del riutilizzo del codice tra gli host e le piattaforme è fondamentale per COM. Un'implementazione di interfaccia riutilizzabile è denominata *componente*, *oggetto componente* o *oggetto com*. Un componente implementa una o più interfacce COM.

Per definire una libreria COM personalizzata, è necessario progettare le interfacce implementate dalla libreria. Gli utenti della libreria possono individuare e usare le proprie funzionalità senza alcuna conoscenza della distribuzione e dei dettagli di implementazione della libreria.

## <a name="objects-and-interfaces"></a>Oggetti e interfacce

Un oggetto COM espone le proprie funzionalità tramite un' *interfaccia*, ovvero una raccolta di funzioni membro. Un'interfaccia COM definisce il comportamento previsto e le responsabilità di un componente e specifica un contratto fortemente tipizzato che fornisce un piccolo set di operazioni correlate. Tutte le comunicazioni tra i componenti COM avvengono tramite le interfacce e tutti i servizi offerti da un componente vengono esposti tramite la relativa interfaccia. Un chiamante può accedere solo alle funzioni membro di interfaccia. Lo stato interno non è disponibile per un chiamante a meno che non sia esposto nell'interfaccia.

Le interfacce sono fortemente tipizzate. Ogni interfaccia ha un identificatore di interfaccia univoco, denominato IID, che elimina le collisioni che possono verificarsi con nomi leggibili. L'IID è un identificatore univoco globale (GUID), che corrisponde all'ID univoco universale (UUID) definito da Open Software Foundation (OSF) Distributed Computing Environment (DCE). Quando si crea una nuova interfaccia, è necessario creare un nuovo identificatore per tale interfaccia. Quando un chiamante usa un'interfaccia, deve usare l'identificatore univoco. Questa identificazione esplicita migliora l'affidabilità eliminando i conflitti di denominazione che comportano un errore in fase di esecuzione.

Quando si definisce una nuova interfaccia, è possibile creare una definizione di interfaccia usando il linguaggio di definizione dell'interfaccia (IDL). Da questa definizione di interfaccia, il compilatore Microsoft IDL genera file di intestazione per l'uso da parte delle applicazioni che usano l'interfaccia e il codice sorgente per gestire le chiamate di procedura remota. L'IDL fornito da Microsoft si basa su semplici estensioni di DCE IDL, uno standard di settore per il calcolo distribuito basato su RPC (Remote Procedure Call). IDL è uno strumento per la praticità di progettazione interfacce e non è fondamentale per l'interoperabilità COM. Con IDL non è necessario creare manualmente i file di intestazione per ogni ambiente di programmazione. Per ulteriori informazioni, vedere [definizione di interfacce com](defining-com-interfaces.md).

L'ereditarietà viene utilizzata sporadicamente nelle interfacce COM. COM supporta solo l'ereditarietà dell'interfaccia per riutilizzare un contratto associato a un'interfaccia di base. COM non supporta l'ereditarietà selettiva; di conseguenza, se un'interfaccia eredita da un'altra, include tutte le funzioni definite dall'interfaccia di base. Inoltre, le interfacce utilizzano solo ereditarietà singola, anziché ereditarietà multipla, per ottenere funzioni da un'interfaccia di base.

## <a name="interface-implementation"></a>Implementazione dell'interfaccia

Non è possibile creare un'istanza di un'interfaccia COM autonomamente. Al contrario, si crea un'istanza di una classe che implementa l'interfaccia. In C++, un'interfaccia COM viene modellata come una *classe base astratta*, il che significa che l'interfaccia è una classe C++ che contiene solo funzioni membro virtuali pure. Una libreria C++ implementa oggetti COM ereditando le firme della funzione membro da una o più interfacce, eseguendo l'override di ogni funzione membro e fornendo un'implementazione per ogni funzione.

È possibile utilizzare qualsiasi linguaggio di programmazione che supporti il concetto di puntatori a funzione per implementare un'interfaccia COM. In C, ad esempio, un'interfaccia è una struttura che contiene un puntatore a una tabella di puntatori a funzione, uno per ogni metodo nell'interfaccia.

Quando si implementa un'interfaccia, la classe deve fornire un'implementazione per ogni funzione nell'interfaccia. Se la classe non ha lavoro da eseguire in una funzione di interfaccia, l'implementazione può essere una singola istruzione return.

Una classe COM viene identificata usando un ID di classe a 128 bit univoco (CLSID) che associa una classe a una particolare distribuzione nel file system, che per Windows è un file DLL o EXE. Un CLSID è un GUID, il che significa che nessun'altra classe ha lo stesso CLSID. L'utilizzo di identificatori di classe univoci impedisce conflitti di nomi tra le classi. Ad esempio, due fornitori diversi possono scrivere una classe denominata CStack, ma entrambe le classi hanno un CLSID univoco, pertanto si evitano eventuali possibili collisioni.

È possibile ottenere un nuovo CLSID usando la funzione [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) o uno strumento di creazione com, ad esempio Visual Studio, che chiama questa funzione internamente.

## <a name="the-iunknown-interface"></a>Interfaccia IUnknown

Tutte le interfacce COM ereditano dall'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . L'interfaccia **IUnknown** contiene le operazioni com fondamentali per il polimorfismo e la gestione della durata dell'istanza. L'interfaccia **IUnknown** dispone di tre funzioni membro, denominate [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Tutti gli oggetti COM sono necessari per implementare l'interfaccia **IUnknown** .

La funzione membro [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fornisce polimorfismo per com. Chiamare **QueryInterface** per determinare in fase di esecuzione se un oggetto com supporta una particolare interfaccia. L'oggetto COM restituisce un puntatore a interfaccia nel `ppvObject` parametro se implementa l'interfaccia richiesta; in caso contrario, restituisce `NULL` . La funzione membro **QueryInterface** consente la navigazione tra tutte le interfacce supportate da un oggetto com.

La durata di un'istanza di un oggetto COM è controllata dal *conteggio dei riferimenti*. Le [](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) funzioni membro IUnknown [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) controllano il conteggio. **AddRef** incrementa il conteggio e il **rilascio** decrementa il conteggio. Quando il conteggio dei riferimenti raggiunge zero, la funzione membro di **versione** può liberare l'istanza, perché nessun chiamante lo utilizza.

## <a name="the-clientserver-model"></a>Modello client/server

Una classe COM implementa un numero di interfacce COM. L'implementazione di è costituita da file binari che vengono eseguiti quando un chiamante interagisce con un'istanza della classe COM. COM consente l'uso di una classe in diverse applicazioni, incluse le applicazioni scritte senza conoscere una classe specifica. In una piattaforma Windows le classi sono presenti in una libreria a collegamento dinamico (DLL) o in un'altra applicazione (EXE).

Nel sistema host, COM gestisce un database di registrazione di tutti i CLSID per gli oggetti COM installati nel sistema. Il database di registrazione è un mapping tra ogni CLSID e il percorso della DLL o del file EXE che ospita la classe corrispondente. COM esegue una query sul database ogni volta che un chiamante desidera creare un'istanza di una classe COM. È necessario che il chiamante conosca solo il CLSID per richiedere una nuova istanza della classe.

L'interazione tra un oggetto COM e i relativi chiamanti viene modellata come relazione client/server. Il client è il chiamante che richiede un oggetto COM dal sistema e il server è il modulo che ospita gli oggetti COM che forniscono servizi ai client.

Un client COM è qualsiasi chiamante che passa un CLSID al sistema per richiedere un'istanza di un oggetto COM. Il modo più semplice per creare un'istanza consiste nel chiamare la funzione COM, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

La funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) crea un'istanza del CLSID specificato e restituisce un puntatore a interfaccia del tipo richiesto dal client. Il client è responsabile della gestione della durata dell'istanza chiamando la relativa funzione [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando il client ha terminato di usarlo. Per creare più oggetti basati su un solo CLSID, chiamare la funzione [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Per connettersi a un oggetto già creato e in esecuzione, chiamare la funzione [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) .

Un server COM fornisce un'implementazione COM al sistema. Un server associa un CLSID a una classe COM, ospita l'implementazione della classe, implementa un class factory per la creazione di istanze della classe e fornisce per lo scaricamento del server.

> [!Note]  
> Un server COM non è uguale all'oggetto COM che fornisce al sistema.

 

Per abilitare la creazione di un oggetto COM, un server COM deve fornire un'implementazione dell'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . I client possono chiamare il metodo [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) per richiedere una nuova istanza di un oggetto com, ma in genere tali richieste sono incapsulate nella funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

È possibile distribuire un server COM come libreria condivisa caricata nel processo del client in fase di esecuzione (DLL sulle piattaforme Windows) o come modulo eseguibile (EXE su piattaforme Windows). Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di applicazioni com](registering-com-applications.md).

## <a name="service-control-manager"></a>Gestione controllo servizi

Gestione controllo servizi gestisce la richiesta client per un'istanza di un oggetto COM. Nell'elenco seguente viene illustrata la sequenza di eventi:

-   Un client richiede un puntatore a interfaccia a un oggetto COM dalla libreria COM chiamando una funzione come [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con il CLSID dell'oggetto com.
-   La libreria COM esegue una query su SCM per trovare il server corrispondente al CLSID richiesto.
-   Il gestore SCM individua il server e richiede la creazione dell'oggetto COM dalla class factory fornita dal server.
-   In caso di esito positivo, la libreria COM restituisce un puntatore a interfaccia al client.

Quando il sistema COM connette un oggetto server a un client, il client e l'oggetto comunicano direttamente. Non è previsto alcun sovraccarico aggiuntivo dalla chiamata tramite un tempo di esecuzione intermedio.

Quando si registra un server COM con il sistema host, è possibile specificare diversi modi per attivare il server. Nell'elenco seguente sono illustrati i tre modi in cui SCM può attivare un server COM:

-   In-process: SCM restituisce il percorso del file DLL che contiene l'implementazione del server oggetti. La libreria COM carica la DLL ed esegue una query per il puntatore di interfaccia class factory.
-   Locale: SCM avvia il file eseguibile locale che registra un class factory all'avvio e il puntatore di interfaccia è disponibile per il sistema e i client.
-   Remote: il gestore SCM locale acquisisce un puntatore a interfaccia class factory dal gestore SCM che è in esecuzione in un computer remoto.

Quando un client richiede un oggetto COM, la libreria COM Contatta SCM nell'host locale. SCM individua il server COM appropriato, che può essere locale o remoto, e il server restituisce un puntatore a interfaccia per il class factory del server. Quando il class factory è disponibile, la libreria COM o il client può usare il class factory per creare l'oggetto richiesto. Per ulteriori informazioni, vedere [implementazione di IClassFactory](implementing-iclassfactory.md).

## <a name="reusability"></a>Riusabilità

COM supporta la *riusabilità nera*, il che significa che i dettagli di implementazione di un componente riutilizzabile non vengono esposti ai client. Per ottenere la riusabilità nera, COM supporta due meccanismi tramite cui un oggetto può riutilizzarne un altro. Le due forme di riutilizzo sono denominate *contenimento* e *aggregazione*. Per convenzione, l'oggetto da riutilizzare viene denominato *oggetto interno* e l'oggetto che sta utilizzando l'oggetto interno è denominato *oggetto esterno*.

In contenimento, l'oggetto esterno si comporta come un client dell'oggetto interno. L'oggetto esterno è un contenitore logico per l'oggetto interno e quando l'oggetto esterno usa i servizi dell'oggetto interno, l'oggetto esterno delega l'implementazione alle interfacce dell'oggetto interno. Ciò significa che l'oggetto esterno viene implementato in termini di servizi dell'oggetto interno. L'oggetto esterno potrebbe non supportare le stesse interfacce dell'oggetto interno e l'oggetto esterno può utilizzare l'interfaccia di un oggetto interno per consentire l'implementazione di parti di un'interfaccia diversa nell'oggetto esterno.

Nell'aggregazione, l'oggetto esterno espone le interfacce dall'oggetto interno come se fossero implementate sull'oggetto esterno. Questa operazione è utile quando l'oggetto esterno delega sempre ogni chiamata su una delle relative interfacce alla stessa interfaccia dell'oggetto interno. L'aggregazione è una praticità che consente all'oggetto esterno di evitare un sovraccarico di implementazione aggiuntivo.

Per ulteriori informazioni, vedere [riutilizzo di oggetti](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>Oggetti di archiviazione e di flusso

Gli oggetti COM salvano lo stato in un file usando l' *archiviazione strutturata*, ovvero un tipo di archivio permanente che consente la navigazione del contenuto di un file usando la semantica file System. Il trattamento del contenuto di un file in questo modo Abilita funzionalità quali l'accesso incrementale, le transazioni e la condivisione tra i processi.

La specifica di archiviazione persistente COM fornisce due tipi di elementi di archiviazione: oggetti di archiviazione e oggetti flusso. Questi oggetti sono implementati dalla libreria COM e le applicazioni utente implementano raramente questi elementi di archiviazione. Gli oggetti di archiviazione implementano l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) e gli oggetti flusso implementano l'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .

Un oggetto flusso contiene dati ed è concettualmente simile a un singolo file in un file system. Ogni flusso dispone di diritti di accesso e di un singolo puntatore di ricerca. Tramite l'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) è possibile leggere, scrivere, cercare ed eseguire altre operazioni sui dati sottostanti del flusso. Un flusso viene denominato usando una stringa di testo. Può contenere qualsiasi struttura interna, perché si tratta di un flusso di byte flat. Inoltre, le funzioni nell'interfaccia **IStream** sono simili alle funzioni standard basate su handle di file, ad esempio quelle nella libreria di runtime del linguaggio C ANSI.

Un oggetto di archiviazione è concettualmente simile a una directory in una file system. Ogni archiviazione può contenere un numero qualsiasi di oggetti di archiviazione secondaria e un numero qualsiasi di flussi. Ogni risorsa di archiviazione ha i propri diritti di accesso. Tramite l'interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , è possibile eseguire operazioni quali l'enumerazione, lo scorrimento, la copia, la ridenominazione, la creazione e l'eliminazione di elementi. Un oggetto di archiviazione non archivia i dati definiti dall'applicazione, ma archivia in modo implicito i nomi degli elementi (archiviazione e flussi) che contiene.

Gli oggetti di archiviazione e di flusso sono condivisibili tra i processi quando vengono implementati in base alla specifica COM in una piattaforma host. In questo modo gli oggetti che sono in esecuzione in-process o out-of-process avranno un accesso incrementale uguale alla relativa archiviazione file. Poiché COM viene caricato separatamente in ogni processo, USA i meccanismi di memoria condivisa supportati dal sistema operativo per comunicare lo stato degli elementi aperti e le relative modalità di accesso tra i processi.

Ogni oggetto di archiviazione e di flusso in un file strutturato ha un nome per identificarlo. Il nome è una stringa che segue una determinata convenzione. Per altre informazioni, vedere [convenzioni di denominazione degli oggetti di archiviazione](/windows/desktop/Stg/storage-object-naming-conventions). Il nome viene passato alle funzioni [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) per specificare l'elemento nell'archivio su cui operare. I nomi degli oggetti di archiviazione radice sono uguali ai nomi di file nel file system sottostante e questi nomi devono rispettare le convenzioni e le restrizioni del file system. Stringhe passate alle funzioni correlate all'archiviazione i cui nomi vengono passati al file system senza l'interpretazione o le modifiche.

I nomi degli elementi contenuti negli oggetti di archiviazione vengono gestiti dall'implementazione dell'oggetto di archiviazione specifico in questione. Tutte le implementazioni di oggetti di archiviazione devono supportare nomi di elementi di lunghezza 32 caratteri e alcune implementazioni possono supportare nomi più lunghi. I nomi vengono archiviati con case mantenuti, ma vengono confrontati senza distinzione tra maiuscole e minuscole. Le applicazioni che definiscono i nomi degli elementi di archiviazione devono scegliere nomi che funzionano in entrambe le situazioni.

Per accedere a ogni elemento in un file di archiviazione strutturata è possibile usare funzioni e interfacce implementate da COM. Ciò significa che altre applicazioni possono esplorare il file passando con le funzioni di interfaccia [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) che forniscono servizi di tipo directory. Inoltre, altre applicazioni possono usare i dati del file, senza dover eseguire l'applicazione che ha scritto il file. Quando un'applicazione COM accede ai file di archiviazione strutturati di un'altra applicazione, si applicano i diritti di accesso standard di Windows e l'applicazione deve disporre di privilegi sufficienti.

Un oggetto COM può leggere e scrivere in un archivio permanente. Un client esegue una query per una delle interfacce correlate alla persistenza nell'oggetto COM, a seconda del contesto dell'operazione. Gli oggetti COM possono implementare qualsiasi combinazione delle interfacce seguenti:

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage): l'oggetto com legge e scrive lo stato persistente in un oggetto di archiviazione. Il client fornisce all'oggetto un puntatore [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) tramite questa interfaccia. Questa è l'unica interfaccia di persistenza che include la semantica per l'accesso incrementale.
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream): l'oggetto com legge e scrive lo stato persistente in un oggetto flusso. Il client fornisce all'oggetto un puntatore [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) tramite questa interfaccia.
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile): l'oggetto com legge e scrive lo stato persistente direttamente in un file nel sistema sottostante. Questa interfaccia non prevede [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) a meno che non si acceda al file sottostante tramite queste interfacce, ma l'interfaccia **IPersistFile** non ha semantica per archiviazione e flussi. Il client fornisce all'oggetto un nome file e chiama le funzioni [**Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) o [**Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) .

## <a name="data-transfer"></a>Trasferimento dati

L'archiviazione strutturata rappresenta la base per lo scambio di dati tra oggetti COM e processi, denominato *trasferimento dati uniformi*. Prima dell'implementazione di COM in OLE 2, il trasferimento dei dati in Windows è stato specificato dai *protocolli di trasferimento*, ad esempio gli appunti e i protocolli di trascinamento della selezione. Ogni protocollo di trasferimento disponeva di un proprio set di funzioni che delegavano il protocollo alla query e il codice specifico era necessario per gestire ogni protocollo e procedura di scambio differenti. Il trasferimento di dati uniformi rappresenta tutti i trasferimenti di dati tramite l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , che separa le operazioni comuni di scambio dei dati dal protocollo di trasferimento.

L'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) incapsula le operazioni get e set standard su dati, query ed enumerazioni e notifiche che rilevano quando i dati vengono modificati in un oggetto. Il trasferimento di dati uniformi consente descrizioni complete dei formati di dati, nonché l'uso di supporti di archiviazione diversi per il trasferimento dei dati.

Durante il trasferimento di dati uniformi, tutti i protocolli scambiano un puntatore a un'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Il server è l'origine dei dati e implementa un oggetto dati, che può essere utilizzato in qualsiasi protocollo di scambio di dati. Il client utilizza i dati e richiede i dati di un oggetto dati quando riceve un puntatore **IDataObject** da qualsiasi protocollo. Dopo che si è verificato lo scambio di puntatori, entrambi i lati gestiscono lo scambio di dati in modo uniforme, tramite l'interfaccia **IDataObject** .

COM definisce due strutture di dati che consentono il trasferimento di dati uniformi. La struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) rappresenta un formato degli Appunti generalizzato e la struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) rappresenta il supporto di trasferimento come un handle di memoria.

Il client crea una struttura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) per indicare il tipo di dati che richiede da un'origine dati e viene utilizzata dall'origine dati per descrivere i formati disponibili. Il client esegue una query su un'origine dati per i formati disponibili richiedendo l'interfaccia [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Per ulteriori informazioni, vedere [la struttura FORMATETC](the-formatetc-structure.md).

Il client crea una struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) e la passa al metodo [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e l'oggetto dati restituisce i dati nella struttura **STGMEDIUM** fornita.

La struttura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) consente a client e origini dati di scegliere il supporto di scambio più efficiente. Se, ad esempio, i dati da scambiare sono molto grandi, l'origine dati può indicare un supporto basato su disco come formato preferito, anziché la memoria principale. Questa flessibilità consente scambi di dati efficienti che possono essere veloci come il passaggio di un puntatore a un [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) o a un [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Per ulteriori informazioni, vedere [la struttura STGMEDIUM](the-stgmedium-structure.md).

Un client di un'origine dati può richiedere una notifica quando i dati vengono modificati. COM gestisce le notifiche di modifica dei dati tramite un oggetto *sink di notifica* , che implementa l'interfaccia [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) . L'oggetto sink Advise e l'interfaccia **IAdviseSink** vengono implementati dal client, che passa un puntatore **IAdviseSink** all'origine dati. Quando l'origine dati rileva una modifica nei dati sottostanti, viene chiamato un metodo **IAdviseSink** per notificare al client. Per ulteriori informazioni, vedere [notifica dati](data-notification.md).

## <a name="remoting"></a>Comunicazione remota

COM consente il calcolo remoto e distribuito. La *comunicazione remota dell'interfaccia* consente a una funzione membro di restituire un puntatore di interfaccia a un oggetto com che si trova in un processo diverso o in un computer host diverso. L'infrastruttura che esegue la comunicazione remota dell'interfaccia è trasparente sia per il client che per il server oggetti. Il client o il server non necessitano dei dettagli della distribuzione di un altro per comunicare tramite un'interfaccia remota. Un client chiama funzioni membro sulla stessa interfaccia per comunicare con un oggetto COM in-process, out-of-process nell'host locale o in un computer remoto. Le chiamate locali e remote sulla stessa interfaccia non sono distinguibili per il client.

Per comunicare con un oggetto COM, un client chiama sempre un'implementazione in-process. Se l'oggetto COM è in-process, la chiamata è diretta. Se l'oggetto COM è out-of-process o remote, COM fornisce un'implementazione del *proxy* che invia la chiamata all'oggetto tramite il protocollo RPC (Remote Procedure Call).

Un oggetto COM riceve sempre le chiamate da un client tramite un'implementazione in-process. Se il chiamante è in-process, la chiamata è diretta. Se il chiamante è out-of-process o remote, COM fornisce un'implementazione *Stub* che riceve la chiamata di procedura remota dal proxy nel processo client.

Il *marshalling* è la procedura per la creazione del pacchetto dello stack di chiamate per la trasmissione dal proxy allo stub. L'annullamento del *marshalling* è l'annullamento del packaging che si verifica all'estremità ricevente. I valori restituiti vengono sottoposti a marshalling e viene effettuato l'unmarshalling dallo stub al proxy. Questo tipo di comunicazione viene chiamato anche invio di una chiamata *sulla rete*.

Per ogni tipo di dati diverso sono presenti regole per il marshalling. I puntatori di interfaccia hanno anche un protocollo di marshalling, incapsulato nella funzione [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) . Nella maggior parte dei casi, il *marshalling dell'interfaccia standard*, fornito dal sistema, è sufficiente, ma un oggetto com può implementare facoltativamente il *marshalling dell'interfaccia personalizzato* per controllare la creazione di proxy di oggetti remoti. Per ulteriori informazioni, vedere [comunicazione tra oggetti](inter-object-communication.md).

## <a name="security"></a>Sicurezza

COM offre due forme di sicurezza dell'applicazione. Uno è la *sicurezza dell'attivazione*, che specifica come vengono creati nuovi oggetti, il modo in cui i client si connettono a oggetti nuovi ed esistenti e il modo in cui vengono protetti determinati servizi pubblici, ad esempio la tabella delle classi e la tabella degli oggetti in esecuzione. L'altro è la *sicurezza delle chiamate*, che specifica il modo in cui la sicurezza opera in una connessione stabilita tra un client e un oggetto com.

La sicurezza dell'attivazione viene applicata automaticamente da Gestione controllo servizi (SCM). Quando Gestione controllo servizi riceve una richiesta di recupero di un oggetto COM, verifica la richiesta rispetto alle informazioni di sicurezza archiviate nel registro di sistema.

Le implementazioni SCM in genere offrono la configurazione guidata dal registro di sistema per l'amministrazione delle classi distribuite e per account utente specifici nell'host. Per ulteriori informazioni, vedere [sicurezza dell'attivazione](activation-security.md).

La sicurezza delle chiamate viene applicata automaticamente o viene applicata dall'applicazione. Se l'applicazione fornisce informazioni di installazione, COM esegue i controlli necessari per proteggere l'applicazione.

Il meccanismo automatico controlla la sicurezza del processo, ma non per i singoli oggetti o metodi. Se un'applicazione richiede una sicurezza più granulare, COM fornisce funzioni che possono essere utilizzate dalle applicazioni per il controllo di sicurezza.

I meccanismi automatici e personalizzati possono essere usati insieme, quindi un'applicazione potrebbe richiedere a COM di eseguire un controllo di sicurezza automatico e quindi di eseguire le proprie operazioni.

I servizi di sicurezza delle chiamate COM sono divisi nelle categorie seguenti:

-   Funzioni generali chiamate da client e server che consentono l'inizializzazione del meccanismo di sicurezza automatico e la registrazione dei servizi di autenticazione automatica. Le API di sicurezza delle chiamate generali sono le funzioni [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .
-   Interfacce nei proxy client, che consentono al client di controllare la sicurezza sulle chiamate a singole interfacce. L'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e le funzioni [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) forniscono la sicurezza delle chiamate su un oggetto remoto.
-   Funzioni lato server e interfacce del contesto di chiamata che consentono al server di recuperare informazioni di sicurezza su una chiamata e di rappresentare il chiamante. L'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) e le funzioni [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)e [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) forniscono la sicurezza delle chiamate sul lato server.

Spesso il client esegue una query sull'oggetto COM per l'interfaccia [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) , implementata localmente dal livello di comunicazione remota. Il client usa questa interfaccia per controllare la sicurezza dei singoli proxy di interfaccia sull'oggetto COM prima di effettuare una chiamata su una delle interfacce.

Quando arriva una chiamata al server, il server può chiamare la funzione [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) per recuperare un'interfaccia [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) , che consente al server di controllare l'autenticazione del client e di rappresentare il client, se necessario. L'oggetto **IServerSecurity** è valido per la durata della chiamata.

Chiamare la funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per inizializzare il livello di sicurezza e impostare i valori specificati come valore predefinito di sicurezza. Se un processo non chiama **CoInitializeSecurity**, com lo chiama automaticamente alla prima esecuzione del marshalling o dell'annullamento del marshalling di un'interfaccia, registrando la sicurezza predefinita del sistema. La funzione **CoInitializeSecurity** consente al client di stabilire la sicurezza delle chiamate predefinita per il processo, evitando così l'uso di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) nei singoli proxy. La funzione **CoInitializeSecurity** consente a un server di registrare i servizi di autenticazione automatici per il processo. Per ulteriori informazioni, vedere [impostazione Process-Wide sicurezza con CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

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

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 
