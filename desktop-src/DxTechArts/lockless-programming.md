---
title: Considerazioni sulla programmazione senza blocchi per Xbox 360 e Microsoft Windows
description: In questo articolo viene illustrata una panoramica di alcuni dei problemi da considerare quando si tenta di utilizzare tecniche di programmazione non bloccate.
ms.assetid: 44700352-a791-7ef7-0858-146214b0e3da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23bf8d66cada8aff00735fe6d6ac2d4f1369bc32
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2020
ms.locfileid: "103963556"
---
# <a name="lockless-programming-considerations-for-xbox-360-and-microsoft-windows"></a>Considerazioni sulla programmazione senza blocchi per Xbox 360 e Microsoft Windows

La programmazione senza blocchi è un modo per condividere in modo sicuro i dati mutevoli tra più thread senza il costo di acquisizione e rilascio dei blocchi. Si tratta di una panacea, ma la programmazione senza blocchi è complessa e leggera e talvolta non offre i vantaggi che promette. La programmazione con blocco è particolarmente complessa in Xbox 360.

La programmazione senza blocchi è una tecnica valida per la programmazione multithreading, ma non deve essere usata con leggerezza. Prima di usarlo, è necessario comprendere le complessità ed è necessario misurarlo attentamente per assicurarsi che sia effettivamente in grado di fornire i vantaggi previsti. In molti casi sono disponibili soluzioni più semplici e veloci, ad esempio la condivisione di dati con una frequenza minore, che devono essere usate in alternativa.

L'uso corretto e sicuro della programmazione senza blocco richiede una conoscenza significativa dell'hardware e del compilatore. In questo articolo viene illustrata una panoramica di alcuni dei problemi da considerare quando si tenta di utilizzare tecniche di programmazione non bloccate.

## <a name="programming-with-locks"></a>Programmazione con blocchi

Quando si scrive codice multithread, spesso è necessario condividere i dati tra i thread. Se più thread leggono e scrivono simultaneamente le strutture dei dati condivise, può verificarsi un danneggiamento della memoria. Il modo più semplice per risolvere questo problema consiste nell'usare i blocchi. Se, ad esempio, ManipulateSharedData deve essere eseguito solo da un thread alla volta, \_ è possibile usare una sezione critica per garantire questo problema, come nel codice seguente:

``` syntax
// Initialize
CRITICAL_SECTION cs;
InitializeCriticalSection(&cs);

// Use
void ManipulateSharedData()
{
    EnterCriticalSection(&cs);
    // Manipulate stuff...
    LeaveCriticalSection(&cs);
}

// Destroy
DeleteCriticalSection(&cs);
```

Questo codice è piuttosto semplice e semplice ed è facile stabilire che sia corretto. Tuttavia, la programmazione con blocchi presenta diversi svantaggi potenziali. Se ad esempio due thread tentano di acquisire gli stessi due blocchi ma li acquisiscono in un ordine diverso, è possibile che venga generato un deadlock. Se un programma contiene un blocco per troppo tempo, a causa di una progettazione insufficiente o perché il thread è stato sostituito da un thread con priorità più elevata, è possibile che altri thread siano bloccati per un lungo periodo di tempo. Questo rischio è particolarmente utile in Xbox 360 perché ai thread software viene assegnato un thread hardware dallo sviluppatore e il sistema operativo non li sposta in un altro thread hardware, anche se uno è inattivo. La versione Xbox 360 non dispone inoltre di protezione contro la priorità inversione, in cui un thread con priorità alta si blocca in un ciclo mentre è in attesa che un thread con priorità bassa rilasci un blocco. Infine, se una chiamata di routine posticipata o una routine del servizio di interrupt tenta di acquisire un blocco, è possibile che venga generato un deadlock.

Nonostante questi problemi, le primitive di sincronizzazione, ad esempio le sezioni critiche, rappresentano in genere il modo migliore per coordinare più thread. Se le primitive di sincronizzazione sono troppo lente, la soluzione migliore è in genere utilizzarle con minore frequenza. Tuttavia, per coloro che possono permettersi la complessità aggiuntiva, un'altra opzione è la programmazione non bloccata.

## <a name="lockless-programming"></a>Programmazione con blocco

La programmazione senza blocco, come suggerisce il nome, è una famiglia di tecniche per la manipolazione sicura dei dati condivisi senza utilizzare i blocchi. Sono disponibili algoritmi di blocco per il passaggio di messaggi, la condivisione di elenchi e code di dati e altre attività.

Quando si esegue la programmazione senza blocchi, è necessario gestire due problemi: operazioni non atomiche e riordino.

## <a name="non-atomic-operations"></a>Operazioni non atomiche

Un'operazione atomica è un valore indivisibile, ovvero uno in cui si garantisce che gli altri thread non visualizzino mai l'operazione quando il tempo è finito. Le operazioni atomiche sono importanti per la programmazione senza blocco, perché senza di esse, altri thread potrebbero visualizzare valori parzialmente scritti o uno stato altrimenti incoerente.

In tutti i processori moderni è possibile presupporre che le letture e le scritture dei tipi nativi allineati naturalmente siano atomiche. Finché il bus di memoria è almeno uguale a quello del tipo letto o scritto, la CPU legge e scrive questi tipi in una singola transazione del bus, rendendo impossibile per gli altri thread visualizzarli in uno stato a metà completato. In x86 e x64 non è garantito che le letture e le Scritture maggiori di otto byte siano atomiche. Ciò significa che le letture e le Scritture a 16 byte dei registri di estensione di Streaming SIMD (SSE) e delle operazioni di stringa potrebbero non essere atomiche.

Le letture e le scritture di tipi non allineati naturalmente, ad esempio la scrittura di DWORD che superano i limiti di quattro byte, non sono necessariamente atomiche. La CPU potrebbe dover eseguire queste operazioni di lettura e scrittura come più transazioni del bus, che potrebbero consentire a un altro thread di modificare o visualizzare i dati al centro della lettura o della scrittura.

Le operazioni composite, ad esempio la sequenza di lettura-modifica-scrittura che si verifica quando si incrementa una variabile condivisa, non sono atomiche. In Xbox 360 queste operazioni vengono implementate come più istruzioni (LWZ, addi e CAL) e il thread può essere sostituito legato tramite la sequenza. In x86 e x64 è presente una singola istruzione (Inc) che può essere usata per incrementare una variabile in memoria. Se si usa questa istruzione, l'incremento di una variabile è atomico nei sistemi a processore singolo, ma non è ancora atomico nei sistemi a più processori. Per la creazione di un sistema a più processori basato su x86 e x64 è necessario usare il prefisso di blocco, che impedisce a un altro processore di eseguire una propria sequenza di lettura-modifica-scrittura tra la lettura e la scrittura dell'istruzione Inc.

Il codice seguente illustra alcuni esempi:

``` syntax
// This write is not atomic because it is not natively aligned.
DWORD* pData = (DWORD*)(pChar + 1);
*pData = 0;

// This is not atomic because it is three separate operations.
++g_globalCounter;

// This write is atomic.
g_alignedGlobal = 0;

// This read is atomic.
DWORD local = g_alignedGlobal;
```

## <a name="guaranteeing-atomicity"></a>Garanzia dell'atomicità

È possibile assicurarsi di usare le operazioni atomiche con una combinazione dei seguenti elementi:

-   Operazioni atomiche naturalmente
-   Blocchi per eseguire il wrapping di operazioni composite
-   Funzioni del sistema operativo che implementano versioni atomiche delle operazioni composite più diffuse

L'incremento di una variabile non è un'operazione atomica e l'incremento può causare il danneggiamento dei dati se eseguiti su più thread.

``` syntax
// This will be atomic.
g_globalCounter = 0;

// This is not atomic and gives undefined behavior
// if executed on multiple threads
++g_globalCounter;
```

Win32 viene fornita con una famiglia di funzioni che offrono versioni atomiche di lettura-modifica-scrittura di diverse operazioni comuni. Si tratta della famiglia di funzioni InterlockedXxx. Se tutte le modifiche della variabile condivisa utilizzano queste funzioni, le modifiche saranno thread-safe.

``` syntax
// Incrementing our variable in a safe lockless way.
InterlockedIncrement(&g_globalCounter);
```

## <a name="reordering"></a>Riordinamento

Un problema più delicato è riordinare. Le letture e le Scritture non sempre si verificano nell'ordine in cui sono state scritte nel codice e ciò può causare problemi molto confusi. In molti algoritmi multithread, un thread scrive alcuni dati e quindi scrive in un flag che indica ad altri thread che i dati sono pronti. Questa operazione è nota come versione di scrittura. Se le scritture vengono riordinate, è possibile che altri thread rivedano che il flag è impostato prima di poter visualizzare i dati scritti.

Analogamente, in molti casi, un thread legge da un flag e quindi legge alcuni dati condivisi se il flag indica che il thread ha acquisito l'accesso ai dati condivisi. Questa operazione è nota come acquisizione di lettura. Se le letture vengono riordinate, i dati possono essere letti dallo spazio di archiviazione condiviso prima del flag e i valori visualizzati potrebbero non essere aggiornati.

Il riordino di letture e scritture può essere eseguito sia dal compilatore che dal processore. I compilatori e i processori hanno eseguito questo riordino per anni, ma sui computer a processore singolo era meno problematico. Questo è dovuto al fatto che la ridisposizione della CPU di letture e scritture è invisibile nei computer a processore singolo (per il codice di driver non di dispositivo che non fa parte di un driver di dispositivo) e la riorganizzazione del compilatore di letture e scritture è meno probabile che causi problemi sui computer a processore singolo.

Se il compilatore o la CPU riorganizza le Scritture illustrate nel codice seguente, un altro thread potrebbe vedere che il flag Alive è impostato, visualizzando comunque i valori precedenti per x o y. Una riorganizzazione simile può verificarsi durante la lettura.

In questo codice un thread aggiunge una nuova voce alla matrice sprite:

``` syntax
// Create a new sprite by writing its position into an empty
// entry and then setting the ‘alive' flag. If ‘alive' is
// written before x or y then errors may occur.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
g_sprites[nextSprite].alive = true;
```

In questo blocco di codice successivo, un altro thread legge dalla matrice di sprite:

``` syntax
// Draw all sprites. If the reads of x and y are moved ahead of
// the read of ‘alive' then errors may occur.
for( int i = 0; i < numSprites; ++i )
{
    if( g_sprites[nextSprite].alive )
    {
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

Per rendere il sistema sprite sicuro, è necessario impedire il riordinamento del compilatore e della CPU per le operazioni di lettura e scrittura.

### <a name="understanding-cpu-rearrangement-of-writes"></a>Informazioni sulla ridisposizione della CPU per le Scritture

Alcune CPU riordinano le Scritture in modo che siano visibili esternamente ad altri processori o dispositivi in ordine non di programma. Questa ridisposizione non è mai visibile al codice non driver a thread singolo, ma può causare problemi nel codice multithread.

### <a name="xbox-360"></a>Xbox 360

Sebbene la CPU Xbox 360 non riordini le istruzioni, vengono riorganizzate le operazioni di scrittura, che vengono completate dopo le istruzioni stesse. Questa ridisposizione delle Scritture è consentita in modo specifico dal modello di memoria PowerPC.

Le Scritture su Xbox 360 non passano direttamente alla cache L2. Al contrario, per migliorare la larghezza di banda di scrittura della cache L2, passano attraverso le code di archiviazione e quindi per archiviare i buffer. I buffer di archiviazione-raccolta consentono di scrivere blocchi di 64 byte nella cache L2 in un'unica operazione. Sono disponibili otto buffer di raccolta dei punti vendita, che consentono di scrivere in modo efficiente in diverse aree di memoria.

I buffer di archiviazione-raccolta vengono in genere scritti nella cache L2 nell'ordine FIFO (First in, First-out). Tuttavia, se la riga della cache di destinazione di una scrittura non è presente nella cache L2, tale scrittura può essere posticipata mentre la riga della cache viene recuperata dalla memoria.

Anche quando i buffer di raccolta dati vengono scritti nella cache L2 in un ordine FIFO rigoroso, questo non garantisce che le singole scritture vengano scritte nella cache L2 nell'ordine. Si supponga, ad esempio, che la CPU scriva nel percorso 0x1000, quindi nel percorso 0x2000 e quindi nel percorso 0x1004. La prima scrittura alloca un buffer di raccolta dati e lo inserisce all'inizio della coda. La seconda scrittura alloca un altro buffer di raccolta e lo inserisce successivamente nella coda. La terza scrittura aggiunge i dati al primo buffer di raccolta, che rimane nella parte anteriore della coda. Quindi, la terza scrittura finisce per passare alla cache L2 prima della seconda scrittura.

Il riordino causato dai buffer di raccolta dei dati di archiviazione è fondamentalmente imprevedibile, soprattutto perché entrambi i thread in un core condividono i buffer di archiviazione-raccolta, rendendo l'allocazione e lo svuotamento dei buffer di archiviazione-raccolta estremamente variabili.

Questo è un esempio di come è possibile riordinare le Scritture. Potrebbero essere disponibili altre possibilità.

### <a name="x86-and-x64"></a>x86 e x64

Anche se le CPU x86 e x64 riordinano le istruzioni, in genere non riordinano le operazioni di scrittura relative ad altre Scritture. Esistono alcune eccezioni per la memoria combinata in scrittura. Inoltre, le operazioni di stringa (MOVS e STOS) e le Scritture SSE a 16 byte possono essere riordinate internamente, ma in caso contrario, le Scritture non vengono riordinate l'una rispetto all'altra.

### <a name="understanding-cpu-rearrangement-of-reads"></a>Informazioni sulla ridisposizione della CPU delle letture

Alcune CPU riordinano le letture in modo che derivano effettivamente dall'archiviazione condivisa in ordine non di programma. Questa ridisposizione non è mai visibile al codice non driver a thread singolo, ma può causare problemi nel codice multithread.

### <a name="xbox-360"></a>Xbox 360

I mancati riscontri nella cache possono causare un ritardo delle letture, che causa la mancata riuscita delle letture dalla memoria condivisa e la tempistica dei mancati riscontri nella cache è fondamentalmente imprevedibile. La prelettura e la stima del ramo possono anche causare la derivazione dei dati dalla memoria condivisa non ordinata. Questi sono solo alcuni esempi di come è possibile riordinare le letture. Potrebbero essere disponibili altre possibilità. Questa ridisposizione delle letture è consentita in modo specifico dal modello di memoria PowerPC.

### <a name="x86-and-x64"></a>x86 e x64

Anche se le CPU x86 e x64 riordinano le istruzioni, in genere non riordinano le operazioni di lettura relative ad altre letture. Le operazioni di stringa (MOVS e STOS) e le letture SSE a 16 byte possono essere riordinate internamente, ma in caso contrario le letture non vengono riordinate in modo reciproco.

### <a name="other-reordering"></a>Altro riordino

Anche se le CPU x86 e x64 non riordinano le Scritture in relazione ad altre scritture o riordinano le letture rispetto ad altre letture, possono riordinare le letture rispetto alle Scritture. In particolare, se un programma scrive in una posizione seguita dalla lettura da una posizione diversa, i dati letti possono provenire dalla memoria condivisa prima che i dati scritti li rendano disponibili. Questo riordino può suddividere alcuni algoritmi, ad esempio gli algoritmi di esclusione reciproca di Dekker. Nell'algoritmo di Dekker ogni thread imposta un flag per indicare che vuole entrare nell'area critica, quindi controlla il flag dell'altro thread per verificare se l'altro thread si trova nell'area critica o se tenta di immetterlo. Il codice iniziale segue.

``` syntax
volatile bool f0 = false;
volatile bool f1 = false;

void P0Acquire()
{
    // Indicate intention to enter critical region
    f0 = true;
    // Check for other thread in or entering critical region
    while (f1)
    {
        // Handle contention.
    }
    // critical region
    ...
}


void P1Acquire()
{
    // Indicate intention to enter critical region
    f1 = true;
    // Check for other thread in or entering critical region
    while (f0)
    {
        // Handle contention.
    }
    // critical region
    ...
}
```

Il problema è che la lettura di F1 in P0Acquire può leggere dallo spazio di archiviazione condiviso prima che la scrittura in F0 lo renda lo spazio di archiviazione condiviso. Nel frattempo, la lettura di F0 in P1Acquire può leggere dallo spazio di archiviazione condiviso prima che la scrittura in F1 lo renda lo spazio di archiviazione condiviso. L'effetto finale è che entrambi i thread impostano i relativi flag su TRUE ed entrambi i thread visualizzano il flag dell'altro thread come FALSE, quindi entrambi entrano nell'area critica. Pertanto, anche se i problemi di riordino nei sistemi basati su x86 e x64 sono meno comuni rispetto a Xbox 360, è possibile che si verifichino comunque. L'algoritmo di Dekker non funzionerà senza barriere di memoria hardware su nessuna di queste piattaforme.

le CPU x86 e x64 non riordinano una scrittura in anticipo rispetto a una lettura precedente. le CPU x86 e x64 riordinano le letture prima delle Scritture precedenti se hanno come destinazione posizioni diverse.

Le CPU PowerPC possono riordinare le letture prima delle Scritture e possono riordinare le Scritture prima delle letture, purché siano indirizzate a indirizzi diversi.

### <a name="reordering-summary"></a>Riepilogo di riordinamento

La CPU Xbox 360 Riordina le operazioni di memoria molto più in modo più aggressivo rispetto alle CPU x86 e x64, come illustrato nella tabella seguente. Per ulteriori informazioni, consultare la documentazione del processore.



| Riordino dell'attività           | x86 e x64 | Xbox 360 |
|-------------------------------|-------------|----------|
| Letture in avanti rispetto alle letture   | No          | Sì      |
| Scritture in avanti nelle Scritture | No          | Sì      |
| Scritture in avanti rispetto alle letture  | No          | Sì      |
| Letture in avanti nelle Scritture  | Sì         | Sì      |



 

## <a name="read-acquire-and-write-release-barriers"></a>Barriere Read-Acquire e Write-Release

I costrutti principali usati per impedire il riordino di letture e scritture sono detti barriere Read-Acquire e Write-release. Una lettura-acquisizione è una lettura di un flag o di un'altra variabile per ottenere la proprietà di una risorsa, abbinata a una barriera contro il riordinamento. Analogamente, una versione di scrittura è una scrittura di un flag o di un'altra variabile per fornire la proprietà di una risorsa, abbinata a una barriera contro il riordinamento.

Le definizioni formali, per cortesia di Herb Sutter, sono:

-   Un'acquisizione di lettura viene eseguita prima di tutte le letture e scritture da parte dello stesso thread che lo seguono nell'ordine del programma.
-   Una versione Write-Release viene eseguita dopo tutte le operazioni di lettura e scrittura dallo stesso thread che lo precede nell'ordine del programma.

Quando il codice acquisisce la proprietà di una certa memoria, acquisendo un blocco o estraendo un elemento da un elenco collegato condiviso (senza blocco), c'è sempre una lettura complessa, ovvero testando un flag o un puntatore per verificare se la proprietà della memoria è stata acquisita. Questa operazione di lettura può far parte di un'operazione **InterlockedXxx** , nel qual caso comporta sia la lettura che la scrittura, ma è la lettura che indica se la proprietà è stata acquisita. Dopo aver acquisito la proprietà della memoria, i valori vengono in genere letti o scritti in tale memoria ed è molto importante che le letture e le Scritture vengano eseguite dopo l'acquisizione della proprietà. Una barriera di lettura/acquisizione garantisce questo problema.

Quando la proprietà di una determinata memoria viene rilasciata, rilasciando un blocco o eseguendo il push di un elemento in un elenco collegato condiviso, è sempre necessario un elemento Write che notifica ad altri thread che la memoria è ora disponibile. Sebbene il codice abbia la proprietà della memoria, è probabile che sia in grado di leggere o scrivere ed è molto importante che le letture e le Scritture vengano eseguite prima di rilasciare la proprietà. Una barriera per la scrittura della versione garantisce questo problema.

È più semplice considerare le barriere Read-Acquire e Write-release come singole operazioni. In alcuni casi, tuttavia, devono essere costruiti da due parti: una lettura o una scrittura e una barriera che non consente lo spostamento di letture o Scritture. In questo caso, la posizione della barriera è fondamentale. Per una barriera di lettura/acquisizione, la lettura del flag viene innanzitutto, quindi la barriera, quindi le letture e le scritture dei dati condivisi. Per una barriera della versione Write, le letture e le scritture dei dati condivisi vengono prima di tutto, quindi la barriera, quindi la scrittura del flag.

``` syntax
// Read that acquires the data.
if( g_flag )
{
    // Guarantee that the read of the flag executes before
    // all reads and writes that follow in program order.
    BarrierOfSomeSort();

    // Now we can read and write the shared data.
    int localVariable = sharedData.y;
    sharedData.x = 0;

    // Guarantee that the write to the flag executes after all
    // reads and writes that precede it in program order.
    BarrierOfSomeSort();
    
    // Write that releases the data.
    g_flag = false;
}
```

L'unica differenza tra un'acquisizione di lettura e una versione di scrittura è la posizione della barriera di memoria. Una lettura-acquisizione presenta la barriera dopo l'operazione di blocco e una versione di scrittura ha la barriera prima di. In entrambi i casi la barriera è tra i riferimenti alla memoria bloccata e i riferimenti al blocco.

Per comprendere il motivo per cui sono necessarie le barriere durante l'acquisizione e il rilascio dei dati, è preferibile (e più accurato) considerare queste barriere come garantire la sincronizzazione con la memoria condivisa, non con altri processori. Se un processore usa una versione di scrittura per rilasciare una struttura di dati alla memoria condivisa e un altro processore usa un'acquisizione di lettura per ottenere l'accesso alla struttura dei dati dalla memoria condivisa, il codice funzionerà correttamente. Se uno dei processori non usa la barriera appropriata, la condivisione dei dati potrebbe non riuscire.

L'uso della barriera giusta per impedire il riordino del compilatore e della CPU per la piattaforma è fondamentale.

Uno dei vantaggi derivanti dall'utilizzo delle primitive di sincronizzazione fornite dal sistema operativo è che tutti includono le barriere di memoria appropriate.

## <a name="preventing-compiler-reordering"></a>Prevenzione del riordino del compilatore

Un processo del compilatore consiste nell'ottimizzare il codice in modo aggressivo per migliorare le prestazioni. Sono incluse le istruzioni per la ridisposizione laddove è utile e ovunque non cambino il comportamento. Poiché lo standard C++ non menziona mai il multithreading e perché il compilatore non sa quale codice deve essere thread-safe, il compilatore presuppone che il codice sia a thread singolo quando si definiscono le riordinazioni che può eseguire in modo sicuro. Pertanto, è necessario indicare al compilatore quando non è consentito riordinare le letture e le Scritture.

Con Visual C++ è possibile impedire il riordino del compilatore usando il [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx)intrinseco del compilatore. Quando si inserisce **\_ ReadWriteBarrier** nel codice, il compilatore non sposta le letture e le Scritture su di esso.

``` syntax
#if _MSC_VER < 1400
    // With VC++ 2003 you need to declare _ReadWriteBarrier
    extern "C" void _ReadWriteBarrier();
#else
    // With VC++ 2005 you can get the declaration from intrin.h
#include <intrin.h>
#endif
// Tell the compiler that this is an intrinsic, not a function.
#pragma intrinsic(_ReadWriteBarrier)

// Create a new sprite by filling in a previously empty entry.
g_sprites[nextSprite].x = x;
g_sprites[nextSprite].y = y;
// Write-release, barrier followed by write.
// Guarantee that the compiler leaves the write to the flag
// after all reads and writes that precede it in program order.
_ReadWriteBarrier();
g_sprites[nextSprite].alive = true;
```

Nel codice seguente un altro thread legge dalla matrice di sprite:

``` syntax
// Draw all sprites.
for( int i = 0; i < numSprites; ++i )
{

    // Read-acquire, read followed by barrier.
    if( g_sprites[nextSprite].alive )
    {
    
        // Guarantee that the compiler leaves the read of the flag
        // before all reads and writes that follow in program order.
        _ReadWriteBarrier();
        DrawSprite( g_sprites[nextSprite].x,
                g_sprites[nextSprite].y );
    }
}
```

È importante comprendere che [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) non inserisce istruzioni aggiuntive e non impedisce alla CPU di riorganizzare le letture e le Scritture, ma impedisce solo al compilatore di riorganizzarle. Pertanto, **\_ ReadWriteBarrier** è sufficiente quando si implementa una barriera di scrittura in x86 e x64 (poiché x86 e x64 non riordinano le Scritture e una scrittura normale è sufficiente per rilasciare un blocco), ma nella maggior parte degli altri casi è anche necessario impedire alla CPU di riordinare le letture e le Scritture.

È anche possibile usare [**\_ ReadWriteBarrier**](https://msdn.microsoft.com/library/f20w0x5e(v=VS.71).aspx) quando si scrive in una memoria non memorizzabile nella cache in scrittura per impedire il riordinamento delle Scritture. In questo caso **\_ ReadWriteBarrier** consente di migliorare le prestazioni, garantendo che le Scritture avvengano nell'ordine lineare preferito del processore.

È anche possibile usare gli intrinseci [**\_ ReadBarrier**](https://msdn.microsoft.com/library/z055s48f(v=VS.80).aspx) e [**\_ WriteBarrier**](https://msdn.microsoft.com/library/65tt87y8(v=VS.80).aspx) per un controllo più preciso del riordino del compilatore. Il compilatore non sposterà le letture in un **\_ ReadBarrier** e non sposterà le Scritture in un **\_ WriteBarrier**.

## <a name="preventing-cpu-reordering"></a>Prevenzione del riordino della CPU

Il riordino della CPU è più sottile rispetto al riordino del compilatore. Non è possibile vedere che si verifica direttamente, vengono visualizzati solo i bug inspiegabili. Per evitare il riordino della CPU di letture e scritture, è necessario usare le istruzioni per la barriera di memoria su alcuni processori. Il nome di tutte le finalità per un'istruzione della barriera di memoria, su Xbox 360 e su Windows, è [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier). Questa macro è implementata in modo appropriato per ogni piattaforma.

In Xbox 360, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) è definito come **lwsync** (Lightweight Sync), disponibile anche tramite la funzione intrinseca **\_ \_ lwsync** , definita in ppcintrinsics. h. **\_ \_ lwsync** funge anche da barriera di memoria del compilatore, impedendo la ridisposizione delle letture e scritture da parte del compilatore.

L'istruzione **lwsync** è una barriera di memoria su Xbox 360 che sincronizza un core del processore con la cache L2. Garantisce che tutte le Scritture prima di **lwsync** lo rendano nella cache L2 prima di qualsiasi scrittura successiva. Garantisce inoltre che le letture che seguono **lwsync** non ottengano dati meno recenti da L2 rispetto alle letture precedenti. Il tipo di riordino che non impedisce è quello di una lettura che precede la scrittura in un indirizzo diverso. Quindi, **lwsync** impone l'ordine di memoria che corrisponde all'ordine di memoria predefinito nei processori x86 e x64. Per ottenere l'ordinamento della memoria completa, è necessaria l'istruzione di sincronizzazione più costosa (nota anche come sincronizzazione dei pesi massimi), ma nella maggior parte dei casi questa operazione non è obbligatoria. Le opzioni di riordino della memoria in Xbox 360 sono illustrate nella tabella seguente.



| Riordino di Xbox 360           | Nessuna sincronizzazione | lwsync | sync |
|-------------------------------|---------|--------|------|
| Letture in avanti rispetto alle letture   | Sì     | No     | No   |
| Scritture in avanti nelle Scritture | Sì     | No     | No   |
| Scritture in avanti rispetto alle letture  | Sì     | No     | No   |
| Letture in avanti nelle Scritture  | Sì     | Sì    | No   |



 

PowerPC include anche le istruzioni di sincronizzazione **iSync** e **eieio** (che viene usato per controllare il riordino della memoria inibita dalla memorizzazione nella cache). Queste istruzioni di sincronizzazione non devono essere necessarie per scopi di sincronizzazione normali.

In Windows, [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) è definito in Winnt. h e fornisce un'altra istruzione della barriera di memoria a seconda che si stia compilando per x86 o x64. L'istruzione della barriera di memoria funge da barriera completa, impedendo il riordino di letture e scritture attraverso la barriera. **MemoryBarrier** in Windows offre quindi una garanzia di riordinamento più avanzata rispetto a Xbox 360.

In Xbox 360 e in molte altre CPU è possibile evitare un altro modo in cui la CPU può essere riordinata dalla CPU. Se si legge un puntatore e si utilizza tale puntatore per caricare altri dati, la CPU garantisce che le letture del puntatore non siano precedenti alla lettura del puntatore. Se il flag di blocco è un puntatore e se tutte le letture dei dati condivisi sono disattivate dal puntatore, il [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) può essere omesso, per un modesto risparmio delle prestazioni.

``` syntax
Data* localPointer = g_sharedPointer;
if( localPointer )
{
    // No import barrier is needed--all reads off of localPointer
    // are guaranteed to not be reordered past the read of
    // localPointer.
    int localVariable = localPointer->y;
    // A memory barrier is needed to stop the read of g_global
    // from being speculatively moved ahead of the read of
    // g_sharedPointer.
    int localVariable2 = g_global;
}
```

L'istruzione [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) impedisce solo il riordinamento delle letture e scritture nella memoria memorizzabile nella cache. Se si alloca memoria come pagina \_ NoCache o pagina \_ WRITECOMBINE, una tecnica comune per gli autori di driver di dispositivo e per gli sviluppatori di giochi su Xbox 360, **MemoryBarrier** non ha alcun effetto sugli accessi alla memoria. La maggior parte degli sviluppatori non necessita della sincronizzazione della memoria non memorizzabile nella cache. Questa operazione non rientra nell'ambito di questo argomento.

## <a name="interlocked-functions-and-cpu-reordering"></a>Funzioni Interlocked e riordino della CPU

In alcuni casi, la lettura o la scrittura che acquisisce o rilascia una risorsa viene eseguita utilizzando una delle funzioni **InterlockedXxx** . In Windows questo semplifica le cose; Poiché in Windows, le funzioni **InterlockedXxx** sono tutte barriere a memoria totale. Hanno una barriera di memoria della CPU sia prima che dopo di esse, il che significa che si tratta di una barriera completa di lettura/acquisizione o di scrittura.

In Xbox 360 le funzioni **InterlockedXxx** non contengono barriere di memoria CPU. Evitano il riordino del compilatore di letture e scritture ma non di riordino della CPU. Pertanto, nella maggior parte dei casi, quando si usano le funzioni **InterlockedXxx** su Xbox 360, è necessario precederle o seguirle con un **\_ \_ lwsync** per renderle una barriera di lettura/acquisizione o di scrittura. Per praticità e per semplificare la leggibilità, sono disponibili versioni di **acquisizione** e **rilascio** di molte delle funzioni di **InterlockedXxx** . Questi sono dotati di una barriera di memoria incorporata. Ad esempio, [**InterlockedIncrementAcquire**](/previous-versions/windows/desktop/legacy/ms683618(v=vs.85)) esegue un incremento Interlocked seguito da una barriera di memoria **\_ \_ lwsync** per fornire la funzionalità di lettura/acquisizione completa.

Si consiglia di usare le versioni di **acquisizione** e **rilascio** delle funzioni **InterlockedXxx** (la maggior parte delle quali sono disponibili anche in Windows, senza alcuna riduzione delle prestazioni), per rendere più ovvia la finalità e per semplificare l'ottenimento delle istruzioni della barriera di memoria nella posizione corretta. Qualsiasi uso di **InterlockedXxx** su Xbox 360 senza una barriera di memoria deve essere esaminato con molta attenzione, perché si tratta spesso di un bug.

Questo esempio illustra come un thread può passare attività o altri dati a un altro thread usando le versioni di **acquisizione** e **rilascio** delle funzioni **InterlockedXxxSList** . Le funzioni **InterlockedXxxSList** sono una famiglia di funzioni per la gestione di un elenco con collegamento singolarmente condiviso senza blocco. Si noti che le varianti di **acquisizione** e **rilascio** di queste funzioni non sono disponibili in Windows, ma le versioni normali di queste funzioni rappresentano una barriera di memoria completa per Windows.

``` syntax
// Declarations for the Task class go here.

// Add a new task to the list using lockless programming.
void AddTask( DWORD ID, DWORD data )
{
    Task* newItem = new Task( ID, data );
    InterlockedPushEntrySListRelease( g_taskList, newItem );
}

// Remove a task from the list, using lockless programming.
// This will return NULL if there are no items in the list.
Task* GetTask()
{
    Task* result = (Task*)
        InterlockedPopEntrySListAcquire( g_taskList );
    return result;
}
```

## <a name="volatile-variables-and-reordering"></a>Variabili volatili e riordino

Lo standard C++ indica che le letture di variabili volatili non possono essere memorizzate nella cache, le scritture volatili non possono essere posticipate e le letture e le scritture volatili non possono essere spostate dopo l'altra. Questa operazione è sufficiente per la comunicazione con i dispositivi hardware, ovvero lo scopo della parola chiave volatile nello standard C++.

Tuttavia, le garanzie dello standard non sono sufficienti per l'uso di volatile per il multithreading. Lo standard C++ non impedisce al compilatore di riordinare le letture e le Scritture non volatili relative a letture e scritture volatili e non indica nulla sulla prevenzione del riordino della CPU.

Visual C++ 2005 va oltre il linguaggio C++ standard per definire una semantica intuitiva per il multithreading per l'accesso a variabili volatili. A partire da Visual C++ 2005, le letture dalle variabili volatili sono definite in modo da avere una semantica di lettura-acquisizione e le Scritture in variabili volatili sono definite in modo da avere una semantica di scrittura della versione. Questo significa che il compilatore non riorganizzerà le letture e le Scritture che li hanno incollato e in Windows assicurerà che la CPU non esegua questa operazione.

È importante comprendere che queste nuove garanzie si applicano solo a Visual C++ 2005 e alle versioni future di Visual C++. In genere, i compilatori di altri fornitori implementano una semantica diversa, senza le garanzie aggiuntive di Visual C++ 2005. Inoltre, su Xbox 360, il compilatore non inserisce istruzioni per impedire che la CPU riordini le letture e le Scritture.

## <a name="example-of-a-lock-free-data-pipe"></a>Esempio di una pipe di dati Lock-Free

Una pipe è un costrutto che consente a uno o più thread di scrivere dati che vengono quindi letti da altri thread. Una versione con blocco di una pipe può essere un modo elegante ed efficiente per passare il lavoro dal thread al thread. DirectX SDK fornisce **LockFreePipe**, una pipe a singolo lettore e un solo Writer, disponibile in DXUTLockFreePipe. h. Lo stesso **LockFreePipe** è disponibile in Xbox 360 SDK in AtgLockFreePipe. h.

**LockFreePipe** può essere usato quando due thread hanno una relazione producer/consumer. Il thread producer può scrivere dati sulla pipe affinché il thread consumer venga elaborato in un secondo momento, senza mai bloccarsi. Se la pipe si riempie, le Scritture hanno esito negativo e il thread producer deve riprovare più tardi, ma ciò si verifica solo se il thread Producer è in anticipo. Se la pipe viene svuotata, le letture hanno esito negativo e il thread consumer deve riprovare in un secondo momento, ma ciò si verifica solo se non sono presenti operazioni da eseguire per il thread consumer. Se i due thread sono ben bilanciati e la pipe è sufficientemente grande, la pipe consente di passare facilmente i dati insieme senza ritardi o blocchi.

## <a name="xbox-360-performance"></a>Prestazioni di Xbox 360

Le prestazioni delle istruzioni e delle funzioni di sincronizzazione in Xbox 360 variano a seconda dell'altro codice eseguito. L'acquisizione dei blocchi ridurrà molto più tempo se un altro thread attualmente possiede il blocco. Le operazioni [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e della sezione critica possono richiedere molto più tempo se altri thread scrivono nella stessa riga della cache. Anche il contenuto delle code di archiviazione può influire sulle prestazioni. Pertanto, tutti questi numeri sono solo approssimazioni, generati da test molto semplici:

-   **lwsync** è stato misurato come 33-48 cicli di esecuzione.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) è stato misurato come 225-260 cicli di esecuzione.
-   L'acquisizione o il rilascio di una sezione critica è stato misurato in modo da richiedere circa 345 cicli.
-   L'acquisizione o il rilascio di un mutex è stato misurato in modo da richiedere circa 2350 cicli.

## <a name="windows-performance"></a>Prestazioni Windows

Le prestazioni delle istruzioni e delle funzioni di sincronizzazione in Windows variano notevolmente a seconda del tipo di processore e della configurazione e dell'altro codice in esecuzione. I sistemi multicore e a più socket spesso importano più tempo per eseguire le istruzioni di sincronizzazione e l'acquisizione di blocchi è molto più lunga se un altro thread attualmente possiede il blocco.

Tuttavia, sono utili anche alcune misurazioni generate da test molto semplici:

-   [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) è stato misurato come 20-90 cicli di esecuzione.
-   [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) è stato misurato come 36-90 cicli di esecuzione.
-   L'acquisizione o il rilascio di una sezione critica è stata misurata come esecuzione di 40-100 cicli.
-   L'acquisizione o il rilascio di un mutex è stato misurato in modo da richiedere circa 750-2500 cicli.

Questi test sono stati eseguiti su Windows XP in un intervallo di processori diversi. I tempi brevi sono stati eseguiti su un computer a processore singolo e i tempi più lunghi erano in un computer a più processori.

Mentre l'acquisizione e il rilascio di blocchi è più costosa rispetto all'uso della programmazione senza blocco, è ancora meglio condividere i dati con una frequenza minore, evitando così il costo totale.

## <a name="performance-thoughts"></a>Considerazioni sulle prestazioni

L'acquisizione o il rilascio di una sezione critica è costituito da una barriera di memoria, un'operazione **InterlockedXxx** e un controllo aggiuntivo per gestire la ricorsione e per eseguire il fallback a un mutex, se necessario. È necessario prestare attenzione all'implementazione di una sezione critica, perché la rotazione in un ciclo in attesa di un blocco è disponibile, senza eseguire il fallback a un mutex, può comportare notevoli prestazioni. Per le sezioni critiche che sono molto contese ma che non vengono mantenute per un periodo di tempo elevato, è consigliabile usare [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) in modo che il sistema operativo girerà per un periodo di tempo in attesa che la sezione critica sia disponibile, anziché immediatamente rinviarla a un mutex se la sezione critica è di proprietà quando si tenta di acquisirla. Per identificare le sezioni critiche che possono trarre vantaggio da un numero di spin, è necessario misurare la lunghezza dell'attesa tipica per un blocco specifico.

Se viene usato un heap condiviso per le allocazioni di memoria, il comportamento predefinito, ogni allocazione di memoria e libero comporta l'acquisizione di un blocco. Con l'aumentare del numero di thread e del numero di allocazioni, i livelli di prestazioni sono disattivati e infine si inizia a diminuire. L'uso di heap per thread o la riduzione del numero di allocazioni può evitare questo collo di bottiglia di blocco.

Se un thread genera dati e un altro thread sta consumando dati, è possibile che i dati vengano condivisi di frequente. Questo problema può verificarsi se un thread sta caricando le risorse e un altro thread sta eseguendo il rendering della scena. Se il thread di rendering fa riferimento ai dati condivisi in ogni chiamata di progetto, il sovraccarico di blocco sarà elevato. È possibile ottenere prestazioni molto migliori se ogni thread dispone di strutture di dati private, che vengono quindi sincronizzate una volta per ogni frame o meno.

Gli algoritmi senza blocco non sono necessariamente più veloci di quelli che utilizzano blocchi. È necessario verificare se i blocchi causano effettivamente problemi prima di tentare di evitarli ed è necessario misurare per verificare se il codice non bloccato migliora effettivamente le prestazioni.

## <a name="platform-differences-summary"></a>Riepilogo delle differenze della piattaforma

-   Le funzioni **InterlockedXxx** impediscono il riordinamento della CPU in lettura/scrittura in Windows, ma non in Xbox 360.
-   La lettura e la scrittura di variabili volatili con Visual Studio C++ 2005 impedisce il riordino di lettura/scrittura della CPU in Windows, ma su Xbox 360, impedisce solo il riordino del compilatore in lettura/scrittura.
-   Le scritture vengono riordinate su Xbox 360, ma non su x86 o x64.
-   Le letture vengono riordinate su Xbox 360, ma in x86 o x64 sono riordinate solo rispetto alle Scritture e solo se le letture e le Scritture sono destinate a posizioni diverse.

## <a name="recommendations"></a>Consigli

-   Usare i blocchi quando possibile perché sono più facili da usare correttamente.
-   Evitare un blocco troppo frequente, in modo che i costi di blocco non diventino significativi.
-   Evitare di mantenere i blocchi per un tempo troppo lungo, in modo da evitare blocchi lunghi.
-   Utilizzare la programmazione senza blocco quando appropriato, ma assicurarsi che i guadagni giustifichino la complessità.
-   Utilizzare la programmazione o i blocchi di blocco in situazioni in cui non sono consentiti altri blocchi, ad esempio quando si condividono dati tra chiamate di procedure posticipate e codice normale.
-   Usare solo algoritmi di programmazione privi di blocco standard che sono stati rivelati corretti.
-   Quando si esegue la programmazione con blocco, assicurarsi di usare variabili di flag volatili e istruzioni per la barriera di memoria in base alle esigenze.
-   Quando si usa **InterlockedXxx** in Xbox 360, usare le varianti di **acquisizione** e **rilascio** .

## <a name="references"></a>Riferimenti

-   MSDN Library. "[**volatile (C++)**](https://msdn.microsoft.com/library/12a04hfd(v=VS.71).aspx)". Riferimenti al linguaggio C++.
-   Vance Morrison. "[Comprendere l'effetto delle tecniche di Low-Lock nelle app multithread](/archive/msdn-magazine/2005/october/understanding-low-lock-techniques-in-multithreaded-apps)". MSDN Magazine, ottobre 2005.
-   Lione, Michael. "[Modello di archiviazione PowerPC e programmazione Aix](https://www-128.ibm.com/developerworks/eserver/articles/powerpc.mdl)". IBM developerWorks, 16 nov 2005.
-   McKenney, Paul E. "[memoria ordinata nei microprocessori moderni, parte II](https://www.linuxjournal.com/article/8212)". Journal Linux, 2005 settembre. \[Questo articolo contiene alcuni dettagli x86.\]
-   Intel Corporation. "[Ordine di memoria architettura Intel® 64](https://www.cs.cmu.edu/~410-f10/doc/Intel_Reordering_318147.pdf)". 2007 agosto. \[Si applica a entrambi i processori IA-32 e Intel 64.\]
-   Niebler, Eric. "[Report di viaggio: riunione ad hoc sui thread in C++](https://www.artima.com/cppsource/threads_meeting.html)". Origine C++, 17 ottobre 2006.
-   Hart, Thomas E. 2006. "[Creazione rapida di sincronizzazione con blocco: implicazioni delle prestazioni del recupero di memoria](https://www.cs.toronto.edu/~tomhart/papers/hart_ipdps06.pdf)." Procedure di 2006 International Parallel and Distributed Processing Simposio (IPDPS 2006), isola di Rodi, Grecia, 2006 aprile.

 

 