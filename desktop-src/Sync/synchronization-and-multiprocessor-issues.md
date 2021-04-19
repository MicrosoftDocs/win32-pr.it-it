---
description: È possibile che le applicazioni riscontrino problemi quando vengono eseguiti su sistemi multiprocessore, a causa dei presupposti che rendono validi solo nei sistemi a processore singolo.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problemi di sincronizzazione e multiprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320067"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="d6f18-103">Problemi di sincronizzazione e multiprocessore</span><span class="sxs-lookup"><span data-stu-id="d6f18-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="d6f18-104">È possibile che le applicazioni riscontrino problemi quando vengono eseguiti su sistemi multiprocessore, a causa dei presupposti che rendono validi solo nei sistemi a processore singolo.</span><span class="sxs-lookup"><span data-stu-id="d6f18-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="d6f18-105">Priorità dei thread</span><span class="sxs-lookup"><span data-stu-id="d6f18-105">Thread Priorities</span></span>

<span data-ttu-id="d6f18-106">Si consideri un programma con due thread, uno con una priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="d6f18-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="d6f18-107">In un sistema a processore singolo, il thread con priorità più alta non cede il controllo al thread con priorità inferiore perché l'utilità di pianificazione assegna la preferenza ai thread con priorità più alta.</span><span class="sxs-lookup"><span data-stu-id="d6f18-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="d6f18-108">In un sistema multiprocessore, entrambi i thread possono essere eseguiti contemporaneamente, ciascuno sul proprio processore.</span><span class="sxs-lookup"><span data-stu-id="d6f18-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="d6f18-109">Le applicazioni devono sincronizzare l'accesso alle strutture di dati per evitare race condition.</span><span class="sxs-lookup"><span data-stu-id="d6f18-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="d6f18-110">Il codice che presuppone che i thread con priorità più alta vengano eseguiti senza interferenze dai thread con priorità inferiore avranno esito negativo nei sistemi multiprocessore.</span><span class="sxs-lookup"><span data-stu-id="d6f18-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="d6f18-111">Ordine di memoria</span><span class="sxs-lookup"><span data-stu-id="d6f18-111">Memory Ordering</span></span>

<span data-ttu-id="d6f18-112">Quando un processore scrive in una posizione di memoria, il valore viene memorizzato nella cache per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d6f18-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="d6f18-113">Analogamente, il processore tenta di soddisfare le richieste di lettura dalla cache per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d6f18-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="d6f18-114">Inoltre, i processori iniziano a recuperare i valori dalla memoria prima che vengano richiesti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d6f18-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="d6f18-115">Questa operazione può essere eseguita come parte dell'esecuzione speculativa o a causa di problemi di riga della cache.</span><span class="sxs-lookup"><span data-stu-id="d6f18-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="d6f18-116">Le cache della CPU possono essere partizionate in banche a cui è possibile accedere in parallelo.</span><span class="sxs-lookup"><span data-stu-id="d6f18-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="d6f18-117">Ciò significa che le operazioni di memoria possono essere completate in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="d6f18-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="d6f18-118">Per assicurarsi che le operazioni di memoria vengano completate nell'ordine, la maggior parte dei processori fornisce istruzioni per la barriera di memoria.</span><span class="sxs-lookup"><span data-stu-id="d6f18-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="d6f18-119">Una *barriera di memoria completa* garantisce che le operazioni di lettura e scrittura della memoria visualizzate prima dell'istruzione della barriera di memoria vengano sottoposte a commit nella memoria prima di qualsiasi operazione di lettura e scrittura della memoria che viene visualizzata dopo l'istruzione della barriera di memoria.</span><span class="sxs-lookup"><span data-stu-id="d6f18-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="d6f18-120">Una *barriera di memoria in lettura* Ordina solo le operazioni di lettura della memoria e una *barriera di memoria di scrittura* Ordina solo le operazioni di scrittura della memoria.</span><span class="sxs-lookup"><span data-stu-id="d6f18-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="d6f18-121">Queste istruzioni assicurano inoltre che il compilatore Disabilita le ottimizzazioni che potrebbero riordinare le operazioni di memoria tra le barriere.</span><span class="sxs-lookup"><span data-stu-id="d6f18-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="d6f18-122">I processori possono supportare istruzioni per le barriere di memoria con semantica di acquisizione, rilascio e recinzione.</span><span class="sxs-lookup"><span data-stu-id="d6f18-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="d6f18-123">Questa semantica descrive l'ordine in cui i risultati di un'operazione diventano disponibili.</span><span class="sxs-lookup"><span data-stu-id="d6f18-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="d6f18-124">Con la semantica di acquisizione, i risultati dell'operazione sono disponibili prima dei risultati di qualsiasi operazione visualizzata dopo il codice.</span><span class="sxs-lookup"><span data-stu-id="d6f18-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="d6f18-125">Con la semantica di rilascio, i risultati dell'operazione sono disponibili dopo i risultati di qualsiasi operazione visualizzata prima nel codice.</span><span class="sxs-lookup"><span data-stu-id="d6f18-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="d6f18-126">Semantica di recinzione combinare la semantica di acquisizione e di rilascio.</span><span class="sxs-lookup"><span data-stu-id="d6f18-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="d6f18-127">I risultati di un'operazione con semantica di recinzione sono disponibili prima di quelli di qualsiasi operazione visualizzata dopo il codice e dopo quelli di qualsiasi operazione visualizzata prima.</span><span class="sxs-lookup"><span data-stu-id="d6f18-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="d6f18-128">Nei processori x86 e x64 che supportano SSE2, le istruzioni sono **mfence** (limite di memoria), **lfence** (limite di caricamento) e **sfence** (limite di archiviazione).</span><span class="sxs-lookup"><span data-stu-id="d6f18-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="d6f18-129">Nei processori ARM i supporti sono **DMB** e **DSB**.</span><span class="sxs-lookup"><span data-stu-id="d6f18-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="d6f18-130">Per ulteriori informazioni, vedere la documentazione relativa al processore.</span><span class="sxs-lookup"><span data-stu-id="d6f18-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="d6f18-131">Le seguenti funzioni di sincronizzazione usano le barriere appropriate per garantire l'ordine di memoria:</span><span class="sxs-lookup"><span data-stu-id="d6f18-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="d6f18-132">Funzioni che immettono o lasciano sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="d6f18-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="d6f18-133">Funzioni che acquisiscono o rilasciano blocchi SRW</span><span class="sxs-lookup"><span data-stu-id="d6f18-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="d6f18-134">Inizio e completamento inizializzazione unica</span><span class="sxs-lookup"><span data-stu-id="d6f18-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="d6f18-135">**EnterSynchronizationBarrier** (funzione)</span><span class="sxs-lookup"><span data-stu-id="d6f18-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="d6f18-136">Funzioni che segnalano oggetti di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="d6f18-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="d6f18-137">Funzioni Wait</span><span class="sxs-lookup"><span data-stu-id="d6f18-137">Wait functions</span></span>
-   <span data-ttu-id="d6f18-138">Funzioni Interlocked (eccetto funzioni con suffisso _nofence_ o funzioni intrinseche con suffisso _\_ NF_ )</span><span class="sxs-lookup"><span data-stu-id="d6f18-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="d6f18-139">Correzione di una race condition</span><span class="sxs-lookup"><span data-stu-id="d6f18-139">Fixing a Race Condition</span></span>

<span data-ttu-id="d6f18-140">Il codice seguente ha un race condition in un sistema multiprocessore perché il processore eseguito `CacheComputedValue` per la prima volta può scrivere `fValueHasBeenComputed` nella memoria principale prima di scrivere `iValue` nella memoria principale.</span><span class="sxs-lookup"><span data-stu-id="d6f18-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="d6f18-141">Di conseguenza, un secondo processore eseguito `FetchComputedValue` allo stesso tempo legge `fValueHasBeenComputed` come **true**, ma il nuovo valore di `iValue` è ancora nella cache del primo processore e non è stato scritto in memoria.</span><span class="sxs-lookup"><span data-stu-id="d6f18-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="d6f18-142">Questo race condition precedente può essere corretto tramite la parola chiave **volatile** o la funzione [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) per garantire che il valore di `iValue` venga aggiornato per tutti i processori prima che il valore di `fValueHasBeenComputed` sia impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="d6f18-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="d6f18-143">A partire da Visual Studio 2005, se compilato in **/volatile: ms** Mode, il compilatore usa la semantica di acquisizione per le operazioni di lettura sulle variabili **volatili** e la semantica di rilascio per le operazioni di scrittura su variabili **volatili** (se supportate dalla CPU).</span><span class="sxs-lookup"><span data-stu-id="d6f18-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="d6f18-144">È pertanto possibile correggere l'esempio nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d6f18-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="d6f18-145">Con Visual Studio 2003, i riferimenti **volatili** a **volatili** sono ordinati; il compilatore non riordina l'accesso a variabili **volatili** .</span><span class="sxs-lookup"><span data-stu-id="d6f18-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="d6f18-146">Tuttavia, queste operazioni potrebbero essere riordinate dal processore.</span><span class="sxs-lookup"><span data-stu-id="d6f18-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="d6f18-147">È pertanto possibile correggere l'esempio nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d6f18-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="d6f18-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6f18-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f18-149">Oggetti sezione critica</span><span class="sxs-lookup"><span data-stu-id="d6f18-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="d6f18-150">Accesso a variabili Interlocked</span><span class="sxs-lookup"><span data-stu-id="d6f18-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="d6f18-151">Funzioni Wait</span><span class="sxs-lookup"><span data-stu-id="d6f18-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



