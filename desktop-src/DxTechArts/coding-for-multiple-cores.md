---
title: Codifica per multicore in Xbox 360 e Windows
description: In questo argomento vengono fornite alcune indicazioni su come iniziare a usare la programmazione multithreading.
ms.assetid: 661f13a6-c73d-8513-2bad-0ef9d1a361a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75899dacdfba829fc1a83e9393e6aa58574c9f30
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "104399914"
---
# <a name="coding-for-multicore-on-xbox-360-and-windows"></a>Codifica per multicore in Xbox 360 e Windows

Per anni le prestazioni dei processori sono aumentate costantemente e i giochi e altri programmi hanno sfruttato i vantaggi di questa potenza crescente senza dover eseguire alcuna operazione speciale.

Le regole sono state modificate. Le prestazioni dei core del processore singolo ora aumentano molto lentamente. Tuttavia, la potenza di calcolo disponibile in un computer o in una console tipica continua ad aumentare. La differenza è che la maggior parte di questo miglioramento delle prestazioni ora deriva dalla presenza di più core del processore in un singolo computer, spesso in un singolo chip. La CPU Xbox 360 dispone di tre core del processore su un chip e circa il 70% dei processori del PC venduti in 2006 era multicore.

L'aumento della potenza di elaborazione disponibile è altrettanto drammatico quanto in passato, ma ora gli sviluppatori devono scrivere codice multithreading per poter usare questa potenza. La programmazione multithread comporta nuove problemi di progettazione e programmazione. In questo argomento vengono fornite alcune indicazioni su come iniziare a usare la programmazione multithreading.

## <a name="the-importance-of-good-design"></a>Importanza della progettazione corretta

La progettazione di un programma multithreading efficace è fondamentale, ma può essere molto difficile. Se si spostano i sistemi di gioco principali su thread diversi, probabilmente si noterà che ogni thread trascorre la maggior parte del tempo in attesa sugli altri thread. Questo tipo di progettazione comporta una maggiore complessità e un lavoro di debug significativo, senza praticamente alcun miglioramento delle prestazioni.

Ogni volta che i thread devono sincronizzare o condividere dati, è possibile che si verifichino danneggiamenti dei dati, sovraccarico della sincronizzazione, deadlock e complessità. Pertanto, la progettazione multithreading deve documentare chiaramente ogni punto di sincronizzazione e di comunicazione ed è necessario ridurre al minimo tali punti. Quando i thread devono comunicare, il lavoro di codifica aumenterà, che può ridurre la produttività se interessa un codice sorgente troppo elevato.

L'obiettivo di progettazione più semplice per il multithreading consiste nel suddividere il codice in parti indipendenti di grandi dimensioni. Se quindi si limitano queste parti alla comunicazione solo alcune volte per fotogramma, si noterà un aumento significativo del multithreading, senza eccessive complessità.

## <a name="typical-threaded-tasks"></a>Attività tipiche con thread

Alcuni tipi di attività si sono rivelati suscettibili di essere inseriti su thread separati. L'elenco seguente non è destinato a essere esaustivo, ma dovrebbe fornire alcune idee.

### <a name="rendering"></a>Rendering

Il rendering, che può includere l'esplorazione del grafico della scena o, probabilmente, solo la chiamata di funzioni D3D, spesso rappresenta il 50% o più del tempo di CPU. Pertanto, lo stato del rendering in un altro thread può avere vantaggi significativi. Il thread di aggiornamento può compilare un tipo di buffer di descrizione di rendering, che può essere elaborato dal thread di rendering.

Il thread di aggiornamento del gioco è sempre un fotogramma avanti rispetto al thread di rendering, il che significa che prima di visualizzare le azioni utente sullo schermo sono necessari due fotogrammi. Anche se questa latenza maggiore può costituire un problema, la frequenza dei fotogrammi aumentata dalla suddivisione del carico di lavoro in genere mantiene la latenza totale accettabile.

Nella maggior parte dei casi, tutto il rendering viene ancora eseguito su un singolo thread, ma è un thread diverso dall'aggiornamento del gioco.

Il \_ flag MULTIthreading D3DCREATE viene talvolta usato per consentire il rendering in un thread e la creazione di risorse in altri thread. questo flag viene ignorato in Xbox 360 ed è consigliabile evitare di usarlo in Windows. In Windows, se si specifica questo flag, D3D impiega una quantità di tempo significativa per la sincronizzazione, rallentando così il thread di rendering.

### <a name="file-decompression"></a>Decompressione file

I tempi di caricamento sono sempre troppo lunghi e il flusso dei dati in memoria senza influire sulla frequenza dei fotogrammi può risultare complesso. Se tutti i dati sono compressi in modo aggressivo sul disco, la velocità di trasferimento dei dati dal disco rigido o dal disco ottico è meno probabile che sia un fattore limitante. In un processore a thread singolo, il tempo di elaborazione disponibile in genere non è sufficiente per la compressione, in modo da agevolare i tempi di caricamento. In un sistema multiprocessore, tuttavia, la decompressione dei file USA cicli CPU che altrimenti sarebbero sprecati; migliora i tempi di caricamento e il flusso; e salva spazio sul disco.

Non utilizzare la decompressione di file come sostituzione per l'elaborazione da eseguire durante la produzione. Se ad esempio si dedica un thread aggiuntivo all'analisi dei dati XML durante il caricamento del livello, non si usa il multithreading per migliorare l'esperienza del lettore.

Quando si utilizza un thread di decompressione file, è comunque necessario utilizzare l'I/O di file asincrono e le letture di grandi dimensioni per ottimizzare l'efficienza di lettura dei dati.

### <a name="graphics-fluff"></a>Fluff grafica

Sono disponibili molte sottigliezze grafiche che consentono di migliorare l'aspetto del gioco, ma non sono strettamente necessarie. Sono inclusi elementi come animazioni cloud generate in modo procedurale, simulazioni di stoffa e capelli, onde procedurali, vegetazione procedurale, più particelle o fisica non di gioco.

Poiché questi effetti non influiscono sul gameplay, non causano problemi di sincronizzazione complessi, ma possono essere sincronizzati con gli altri thread una volta per frame o meno spesso. Inoltre, nei giochi per Windows questi effetti possono aggiungere valore per i giocatori con CPU multicore, ignorando in modo invisibile i computer a core singolo, offrendo così un modo semplice per ridimensionare un'ampia gamma di funzionalità.

### <a name="physics"></a>Fisica

Spesso la fisica non può essere inserita in un thread separato per l'esecuzione in parallelo con l'aggiornamento del gioco, perché l'aggiornamento del gioco richiede in genere i risultati dei calcoli fisici immediatamente. L'alternativa per la fisica del multithreading consiste nell'eseguirla su più processori. Sebbene sia possibile eseguire questa operazione, si tratta di un'attività complessa che richiede l'accesso frequente alle strutture di dati condivise. Se il carico di lavoro fisico può essere sufficientemente basso da adattarsi al thread principale, il processo sarà più semplice.

Sono disponibili librerie che supportano l'esecuzione di fisica in più thread. Tuttavia, questo può causare un problema: quando il gioco esegue la fisica, USA molti thread, ma il resto del tempo ne usa pochi. Per eseguire la fisica su più thread, è necessario risolverlo in modo che il carico di lavoro venga distribuito uniformemente sul frame. Se si scrive un motore di fisica multithreading, è necessario prestare attenzione a tutte le strutture di dati, i punti di sincronizzazione e il bilanciamento del carico.

## <a name="example-multithreaded-designs"></a>Esempi di progettazione multithreading

I giochi per Windows devono essere eseguiti in computer con diversi numeri di core CPU. La maggior parte dei computer di gioco ha ancora un solo core, sebbene il numero di macchine virtuali a due core stia crescendo rapidamente. Un tipico gioco per Windows potrebbe suddividere il carico di lavoro in un thread per l'aggiornamento e il rendering, con thread di lavoro facoltativi per l'aggiunta di funzionalità aggiuntive. Inoltre, potrebbero essere usati alcuni thread in background per l'I/O dei file e la rete. Nella figura 1 vengono illustrati i thread, insieme ai punti di trasferimento dei dati principali.

**Figura 1. Progettazione del threading in un gioco per Windows**

![progettazione del threading in un gioco per Windows](images/coding-for-multiple-cores-1.gif)

Un tipico gioco Xbox 360 può utilizzare thread software a elevato utilizzo di CPU, quindi potrebbe suddividere il carico di lavoro in un thread di aggiornamento, un thread di rendering e tre thread di lavoro, come illustrato nella figura 2.

**Figura 2. Progettazione del threading in un gioco per Xbox 360**

![progettazione del threading in un gioco per Xbox 360](images/coding-for-multiple-cores-2.gif)

Fatta eccezione per le operazioni di I/O di file e di rete, queste attività possono avere un elevato utilizzo della CPU per trarre vantaggio dal proprio thread hardware. Queste attività hanno anche la possibilità di essere sufficientemente indipendenti da poter essere eseguite per un intero frame senza comunicazione.

Il thread di aggiornamento del gioco gestisce l'input del controller, l'intelligenza artificiale e la fisica e prepara le istruzioni per gli altri quattro thread. Queste istruzioni vengono inserite nei buffer di proprietà del thread di aggiornamento del gioco, pertanto non è necessaria alcuna sincronizzazione quando vengono generate le istruzioni.

Alla fine del frame, il thread di aggiornamento del gioco passa i buffer di istruzione ai quattro altri thread, quindi inizia a lavorare sul frame successivo, compilando un altro set di buffer di istruzioni.

Poiché i thread di aggiornamento e di rendering funzionano in contemporanea l'uno con l'altro, i buffer di comunicazione sono semplicemente a doppio buffer: in un determinato momento, il thread di aggiornamento sta riempiendo un buffer mentre il thread di rendering sta leggendo l'altro.

Gli altri thread di lavoro non sono necessariamente collegati alla frequenza dei fotogrammi. La decompressione di una porzione di dati potrebbe richiedere molto meno di un frame o potrebbe richiedere molti frame. Anche la simulazione del panno e dei capelli potrebbe non essere necessaria per essere eseguita esattamente alla frequenza dei fotogrammi perché gli aggiornamenti meno frequenti possono essere abbastanza accettabili. Pertanto, questi tre thread necessitano di strutture di dati diverse per comunicare con il thread di aggiornamento e il thread di rendering. Ognuno di essi necessita di una coda di input in grado di gestire le richieste di lavoro e il thread di rendering necessita di una coda di dati che può conservare i risultati prodotti dai thread. Alla fine di ogni frame, il thread di aggiornamento aggiungerà un blocco di richieste di lavoro alle code dei thread di lavoro. L'aggiunta all'elenco una sola volta per frame garantisce che il thread di aggiornamento riduca al minimo l'overhead di sincronizzazione. Ogni thread di lavoro estrae le assegnazioni dalla coda di lavoro nel modo più rapido possibile, usando un ciclo simile al seguente:


```C++
for(;;)
{
    while( WorkQueueNotEmpty() )
    {
        RemoveWorkItemFromWorkQueue();
        ProcessWorkItem();
        PutResultInDataQueue();
    }
    WaitForSingleObject( hWorkSemaphore ); 
}
```



Poiché i dati passano dai thread di aggiornamento ai thread di lavoro e quindi al thread di rendering, può esserci un ritardo di tre o più frame prima che alcune azioni lo rendano sullo schermo. Tuttavia, se si assegnano attività a tolleranza di latenza ai thread di lavoro, questo non dovrebbe essere un problema.

Una progettazione alternativa consiste nel fare in modo che diversi thread di lavoro vengano disegnati dalla stessa coda di lavoro. Questo darebbe un bilanciamento automatico del carico e renderà più probabile che tutti i thread di lavoro rimarranno occupati.

Il thread di aggiornamento del gioco deve prestare attenzione a non concedere troppo lavoro ai thread di lavoro. in caso contrario, è possibile che le code di lavoro crescano continuamente. Il modo in cui il thread di aggiornamento gestisce questa operazione dipende dal tipo di attività eseguite dai thread di lavoro.

## <a name="simultaneous-multithreading-and-number-of-threads"></a>Multithreading simultaneo e numero di thread

Tutti i thread non vengono creati uguali. Due thread hardware possono trovarsi su chip distinti, sullo stesso chip o anche sullo stesso core. La configurazione più importante per i programmatori di giochi da tenere in considerazione è costituita da due thread hardware su un core, ovvero la tecnologia multithreading (SMT) o la tecnologia Hyper-Threading (tecnologia HT).

I thread della tecnologia SMT o HT condividono le risorse del core CPU. Poiché condividono le unità di esecuzione, la massima velocità di esecuzione di due thread invece di uno è in genere dal 10 al 20%, invece del 100% che è possibile da due thread di hardware indipendenti.

Più significativamente, i thread della tecnologia SMT o HT condividono le cache di dati e l'istruzione L1. Se i modelli di accesso alla memoria non sono compatibili, possono superare la cache e causare molti mancati riscontri nella cache. Nel peggiore dei casi, le prestazioni totali per il nucleo CPU possono effettivamente diminuire quando viene eseguito un secondo thread. In Xbox 360 questo è un problema piuttosto semplice. La configurazione di Xbox 360 è nota: tre core CPU ognuno con due thread hardware, e gli sviluppatori assegnano i thread software a specifici thread della CPU e possono misurare per verificare se la progettazione del threading offre prestazioni aggiuntive.

In Windows, la situazione è più complessa. Il numero di thread e la relativa configurazione variano da computer a computer e la determinazione della configurazione è complessa. La funzione [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) fornisce informazioni sulla relazione tra diversi thread hardware e questa funzione è disponibile in Windows Vista, Windows 7 e Windows XP SP3. Per questo motivo, è necessario usare l'istruzione CPUID e gli algoritmi forniti da Intel e AMD per decidere il numero di thread "reali" disponibili. Per ulteriori informazioni, vedere i riferimenti.

L'esempio CoreDetection in DirectX SDK contiene codice di esempio che usa la funzione [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation) o l'istruzione CPUID per restituire la topologia core della CPU. L'istruzione CPUID viene utilizzata se **GetLogicalProcessorInformation** non è supportato nella piattaforma corrente. CoreDetection si trova nei percorsi seguenti:

<dl> <dt>

<span id="Source_"></span><span id="source_"></span><span id="SOURCE_"></span>Origine
</dt> <dd>

Radice di DirectX *SDK* \\ Esempi \\ C++ \\ \\ CoreDetection varie

</dd> <dt>

<span id="Executable_"></span><span id="executable_"></span><span id="EXECUTABLE_"></span>Eseguibile
</dt> <dd>

Radice di DirectX *SDK* \\ Esempi \\ \\ \\CoreDetection.exe bin varie \\ C++

</dd> </dl>

Il presupposto più sicuro consiste nel non avere più di un thread con utilizzo intensivo della CPU per ogni core CPU. La presenza di più thread con utilizzo intensivo della CPU rispetto ai core CPU non offre vantaggi minimi o null e comporta un sovraccarico aggiuntivo e una maggiore complessità dei thread aggiuntivi.

## <a name="creating-threads"></a>Creazione di thread

La creazione di thread è un'operazione piuttosto semplice, ma ci sono molti potenziali errori. Il codice seguente illustra il modo corretto per creare un thread, attenderne l'interruzione e quindi pulire.


```C++
const int stackSize = 65536;
HANDLE hThread = (HANDLE)_beginthreadex( 0, stackSize,
            ThreadFunction, 0, 0, 0 );
// Do work on main thread here.
// Wait for child thread to complete
WaitForSingleObject( hThread, INFINITE );
CloseHandle( hThread );

...

unsigned __stdcall ThreadFunction( void* data )
{
#if _XBOX_VER >= 200
    // On Xbox 360 you must explicitly assign
    // software threads to hardware threads.
    XSetThreadProcessor( GetCurrentThread(), 2 );
#endif
    // Do child thread work here.
    return 0;
}
```



Quando si crea un thread, è possibile specificare la dimensione dello stack per il thread figlio o specificare zero, nel qual caso il thread figlio erediterà la dimensione dello stack del thread padre. In Xbox 360, in cui viene eseguito il commit completo degli stack all'avvio del thread, se si specifica zero è possibile sprecare memoria significativa, perché molti thread figlio non necessitano di un numero di stack pari a quello dell'elemento padre. In Xbox 360 è inoltre importante che le dimensioni dello stack siano un multiplo di 64-KB.

Se si usa la funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) per creare thread, il runtime di C/C++ (CRT) non viene inizializzato correttamente in Windows. È consigliabile usare invece la funzione CRT [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) .

Il valore restituito da [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx) è un handle di thread. Questo thread può essere usato per attendere che il thread figlio termini, che è molto più semplice e molto più efficiente rispetto alla rotazione in un ciclo che controlla lo stato del thread. Per attendere la terminazione del thread, è sufficiente chiamare [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) con l'handle del thread.

Le risorse per il thread non verranno liberate fino a quando il thread non viene terminato e l'handle del thread non è stato chiuso. Pertanto, è importante chiudere l'handle del thread con [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) al termine dell'operazione. Se si è in attesa dell'interruzione del thread con [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject), assicurarsi di non chiudere l'handle fino al completamento dell'attesa.

In Xbox 360, è necessario assegnare in modo esplicito i thread software a un particolare thread hardware usando **XSetThreadProcessor**. In caso contrario, tutti i thread figlio resteranno nello stesso thread hardware del padre. In Windows è possibile usare [**SetThreadAffinityMask**](/windows/win32/api/winbase/nf-winbase-setthreadaffinitymask) per suggerire fortemente al sistema operativo i thread di hardware in cui deve essere eseguito il thread. Questa tecnica dovrebbe in genere essere evitata in Windows, poiché non si conoscono gli altri processi che potrebbero essere in esecuzione nel sistema. È in genere preferibile consentire all'utilità di pianificazione di Windows di assegnare i thread ai thread hardware inattivi.

La creazione di thread è un'operazione costosa. I thread devono essere creati ed eliminati raramente. Se si desidera creare ed eliminare spesso i thread, utilizzare un pool di thread in attesa di lavoro.

## <a name="synchronizing-threads"></a>Sincronizzazione di thread

Per il corretto funzionamento di più thread, è necessario essere in grado di sincronizzare i thread, passare i messaggi e richiedere l'accesso esclusivo alle risorse. Windows e Xbox 360 sono dotati di un set completo di primitive di sincronizzazione. Per informazioni dettagliate sulle primitive di sincronizzazione, vedere la documentazione della piattaforma.

### <a name="exclusive-access"></a>Accesso esclusivo

Ottenere l'accesso esclusivo a una risorsa, una struttura dei dati o un percorso del codice è una necessità comune. Un'opzione per ottenere l'accesso esclusivo è un mutex, il cui utilizzo tipico è illustrato di seguito.


```C++
// Initialize
HANDLE mutex = CreateMutex( 0, FALSE, 0 );

// Use
void ManipulateSharedData()
{
    WaitForSingleObject( mutex, INFINITE );
    // Manipulate stuff...
    ReleaseMutex( mutex );
}

// Destroy
CloseHandle( mutex );
The kernel guarantees that, for a particular mutex, only one thread at a time can 
acquire it.
The main disadvantage to mutexes is that they are relatively expensive to acquire 
and release. A faster alternative is a critical section.
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection( &cs );

// Use
void ManipulateSharedData()
{
    EnterCriticalSection( &cs );
    // Manipulate stuff...
    LeaveCriticalSection( &cs );
}

// Destroy
DeleteCriticalSection( &cs );
```



Le sezioni critiche hanno una semantica simile a mutex, ma possono essere usate per la sincronizzazione solo all'interno di un processo, non tra i processi. Il vantaggio principale è che vengono eseguite approssimativamente venti volte più velocemente di mutex.

### <a name="events"></a>Eventi

Se due thread, ad esempio un thread di aggiornamento e un thread di rendering, stanno utilizzando una coppia di buffer di descrizione di rendering, è necessario un modo per indicare quando vengono eseguiti con il buffer specifico. Questa operazione può essere eseguita associando un evento (allocato con [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)) a ogni buffer. Quando un thread viene eseguito con un buffer, può usare [**Seevent**](/windows/win32/api/synchapi/nf-synchapi-setevent) per segnalare questo e può quindi chiamare [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) sull'evento dell'altro buffer. Questa tecnica consente di estrapolare facilmente il buffering delle risorse.

### <a name="semaphores"></a>Semafori

Un semaforo viene usato per controllare il numero di thread che possono essere in esecuzione e viene comunemente usato per implementare le code di lavoro. Un thread aggiunge il lavoro a una coda e USA [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) ogni volta che aggiunge un nuovo elemento alla coda. Questo consente di rilasciare un thread di lavoro dal pool di thread in attesa. I thread di lavoro chiamano semplicemente [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)e, quando viene restituito, è presente un elemento di lavoro nella coda. Inoltre, è necessario utilizzare una sezione critica o un'altra tecnica di sincronizzazione per garantire un accesso sicuro alla coda di lavoro condivisa.

### <a name="avoid-suspendthread"></a>Evitare SuspendThread

In alcuni casi, quando si vuole che un thread interrompa il comportamento, si tenta di usare [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) anziché le primitive di sincronizzazione corrette. Si tratta sempre di una pessima idea e può causare facilmente deadlock e altri problemi. **SuspendThread** interagisce anche male con il debugger di Visual Studio. Evitare **SuspendThread**. In alternativa, usare [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) .

### <a name="waitforsingleobject-and-waitformultipleobjects"></a>WaitForSingleObject e WaitForMultipleObjects

La funzione [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) è la funzione di sincronizzazione utilizzata più di frequente. Tuttavia, a volte si vuole che un thread attenda che vengano soddisfatte contemporaneamente diverse condizioni o fino a quando non viene soddisfatta una delle condizioni. In questo caso, è consigliabile usare [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects).

### <a name="interlocked-functions-and-lockless-programming"></a>Funzioni Interlocked e programmazione con blocco

Per eseguire semplici operazioni thread-safe senza utilizzare blocchi è disponibile una famiglia di funzioni. Si tratta della famiglia di funzioni Interlocked, ad esempio [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement). Queste funzioni, oltre ad altre tecniche che usano un'attenta impostazione dei flag, sono note come programmazione non bloccata. La programmazione senza blocchi può essere estremamente difficile da eseguire correttamente ed è sostanzialmente più difficile in Xbox 360 che in Windows.

Per ulteriori informazioni sulla programmazione senza blocchi, vedere [considerazioni sulla programmazione senza blocco per Xbox 360 e Microsoft Windows](./lockless-programming.md).

### <a name="minimizing-synchronization"></a>Riduzione della sincronizzazione

Alcuni metodi di sincronizzazione sono più veloci di altri. Tuttavia, anziché ottimizzare il codice scegliendo le tecniche di sincronizzazione più veloci possibili, in genere è preferibile eseguire una sincronizzazione meno frequente. Questa operazione è più rapida della sincronizzazione troppo frequente e rende più semplice il debug del codice.

Per il corretto funzionamento di alcune operazioni, ad esempio l'allocazione della memoria, potrebbe essere necessario utilizzare primitive di sincronizzazione. Pertanto, l'esecuzione di allocazioni frequenti dall'heap condiviso predefinito comporterà una sincronizzazione frequente, che può comportare un certo dispendio di prestazioni. Evitare le allocazioni frequenti o l'utilizzo di heap per thread ( \_ \_ se si usa l'heap no Serialize se si usa HeapCreate) può evitare questa sincronizzazione nascosta.

Un'altra causa della sincronizzazione nascosta è D3DCREATE \_ MULTIthreading, in modo che D3D in Windows usi la sincronizzazione in molte operazioni. (Il flag viene ignorato in Xbox 360).

I dati per thread, noti anche come archiviazione locale di thread, possono essere un modo importante per evitare la sincronizzazione. Visual C++ consente di dichiarare le variabili globali come per thread con la sintassi **\_ \_ declspec (thread)** .


```C++
__declspec( thread ) int tls_i = 1;
```



In questo modo ogni thread del processo elabora una propria copia di TLS \_ i, a cui è possibile fare riferimento in modo sicuro ed efficiente senza richiedere la sincronizzazione.

La tecnica **\_ \_ declspec (thread)** non funziona con le DLL caricate dinamicamente. Se si usano le DLL caricate in modo dinamico, sarà necessario usare la famiglia di funzioni TLSAlloc per implementare l'archiviazione thread-local.

## <a name="destroying-threads"></a>Distruzione di thread

L'unico modo sicuro per eliminare un thread consiste nel far uscire il thread, restituendo dalla funzione thread principale o facendo in modo che il thread chiami [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) o [**\_ endthreadex**](https://msdn.microsoft.com/library/hw264s73(v=VS.71).aspx). Se viene creato un thread con [**\_ beginthreadex**](https://msdn.microsoft.com/library/ms397047(v=VS.70).aspx), è necessario usare **\_ endthreadex** o restituire dalla funzione thread principale, poiché l'uso di **ExitThread** non consentirà di liberare correttamente le risorse CRT. Non chiamare mai la funzione [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) , perché il thread non verrà pulito correttamente. I thread devono sempre eseguire il commit del suicido, non dovrebbero mai essere uccisi.

## <a name="openmp"></a>OpenMP

OpenMP è un'estensione del linguaggio per l'aggiunta del multithreading al programma usando i pragma per guidare il compilatore nei cicli parallelizzazione. OpenMP è supportato da Visual C++ 2005 in Windows e Xbox 360 e può essere usato insieme alla gestione manuale dei thread. OpenMP può essere un modo pratico per multithread le parti del codice, ma è improbabile che sia la soluzione ideale, soprattutto per i giochi. OpenMP può essere più applicabile a attività di produzione a esecuzione prolungata, ad esempio l'elaborazione dell'arte e altre risorse. Per ulteriori informazioni, vedere la documentazione di Visual C++ o accedere al [sito Web](https://www.openmp.org/)OpenMP.

## <a name="profiling"></a>Profilatura

La profilatura multithreading è importante. È facile finire con blocchi lunghi in cui i thread sono in attesa l'uno sull'altro. Questi stalli possono essere difficili da trovare e diagnosticare. Per facilitarne l'identificazione, è consigliabile aggiungere strumentazione alle chiamate di sincronizzazione. Un profiler di campionamento consente inoltre di identificare questi problemi perché può registrare le informazioni di temporizzazione senza modificarle sostanzialmente.

## <a name="timing"></a>Intervallo

L'istruzione RDTSC è un modo per ottenere informazioni accurate sull'intervallo in Windows. Sfortunatamente, RDTSC presenta diversi problemi che lo rendono una scelta scadente per il titolo di spedizione. I contatori RDTSC non sono necessariamente sincronizzati tra le CPU, pertanto quando il thread si sposta tra i thread hardware è possibile che si verifichino differenze positive o negative di grandi dimensioni. A seconda delle impostazioni di risparmio energia, la frequenza con cui incrementa il contatore RDTSC può cambiare anche durante l'esecuzione del gioco. Per evitare queste difficoltà, è preferibile preferire [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) e [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency) per la tempistica a precisione elevata nel gioco di spedizione. Per ulteriori informazioni sulla temporizzazione, vedere la pagina relativa alla [temporizzazione dei giochi e ai processori multicore](./game-timing-and-multicore-processors.md).

## <a name="debugging"></a>Debug

Visual Studio supporta completamente il debug multithread per Windows e Xbox 360. La finestra thread di Visual Studio consente di passare da un thread all'altro per visualizzare gli stack di chiamate e le variabili locali. La finestra thread consente inoltre di bloccare e sbloccare thread specifici.

In Xbox 360 è possibile usare la meta-variabile **\@ hwthread** nella finestra espressioni di controllo per visualizzare il thread hardware in cui è in esecuzione il thread software attualmente selezionato.

La finestra thread è più semplice da usare se i thread vengono denominati in modo significativo. Visual Studio e altri debugger Microsoft consentono di assegnare un nome ai thread. Implementare la funzione **Getthreadname** seguente e chiamarla da ogni thread mentre viene avviata.


```C++
typedef struct tagTHREADNAME_INFO
{
    DWORD dwType;     // must be 0x1000
    LPCSTR szName;    // pointer to name (in user address space)
    DWORD dwThreadID; // thread ID (-1 = caller thread)
    DWORD dwFlags;    // reserved for future use, must be zero
} THREADNAME_INFO;

void SetThreadName( DWORD dwThreadID, LPCSTR szThreadName )
{
    THREADNAME_INFO info;
    info.dwType = 0x1000;
    info.szName = szThreadName;
    info.dwThreadID = dwThreadID;
    info.dwFlags = 0;

    __try
    {
        RaiseException( 0x406D1388, 0,
                    sizeof(info) / sizeof(DWORD),
            (DWORD*)&info );
    }
    __except( EXCEPTION_CONTINUE_EXECUTION ) {
    }
}

// Example usage:
SetThreadName(-1, "Main thread");
```



Il debugger del kernel (KD) e WinDBG supportano anche il debug multithread.

## <a name="testing"></a>Test

La programmazione multithreading può risultare complessa e alcuni bug multithread vengono visualizzati solo raramente, rendendoli difficili da trovare e correggere. Uno dei modi migliori per scaricarli è eseguire test su un'ampia gamma di computer, in particolare su quelli con quattro o più processori. Il codice multithreading che funziona perfettamente in un computer a thread singolo potrebbe non riuscire immediatamente in un computer a quattro processori. Le caratteristiche di prestazioni e tempistiche delle CPU AMD e Intel possono variare in modo sostanziale, quindi assicurarsi di eseguire test sui computer multiprocessore basati sulle CPU di entrambi i fornitori.

## <a name="windows-vista-and-windows-7-improvements"></a>Miglioramenti di Windows Vista e Windows 7

Per i giochi destinati alle versioni più recenti di Windows, sono disponibili numerose API che consentono di semplificare la creazione di applicazioni multithreading scalabili. Questa situazione è particolarmente valida con la nuova API ThreadPool e con alcune primitive syncrhonziation aggiuntive (variabili di condizione, blocco Read/Writer Slim e inizializzazione unica). Per una panoramica di queste tecnologie, vedere gli articoli di MSDN Magazine seguenti:

-   [Migliorare la scalabilità con le nuove API del pool di thread](/archive/msdn-magazine/2007/october/pooled-threads-improve-scalability-with-new-thread-pool-apis)
-   [Primitive di sincronizzazione nuove in Windows Vista](/archive/msdn-magazine/2007/june/concurrency-synchronization-primitives-new-to-windows-vista)

Le applicazioni che usano le [funzionalità di Direct3D 11](../direct3d11/direct3d-11-features.md) in questi sistemi operativi possono anche sfruttare la nuova progettazione per la creazione di oggetti simultanei e gli elenchi di comandi di contesto posticipati per una migliore scalabilità per il rendering multithreading.

## <a name="summary"></a>Riepilogo

Con un'attenta progettazione che riduce al minimo le interazioni tra i thread, è possibile ottenere miglioramenti sostanziali in termini di prestazioni dalla programmazione multithreading senza aggiungere eccessiva complessità al codice. Questo conferirà al codice del gioco la prossima ondata di miglioramenti del processore e offrirà esperienze di gioco sempre più accattivanti.

## <a name="references"></a>Riferimenti

-   Jim Beveridge & Robert Weiner, *applicazioni multithread in Win32*, Addison-Wesley, 1997
-   Chuck Walbourn, [Time Game e processori multicore](./game-timing-and-multicore-processors.md), Microsoft Corporation, 2005
-   MSDN Library: [ **GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)
-   [OpenMP](https://www.openmp.org/)

 

 