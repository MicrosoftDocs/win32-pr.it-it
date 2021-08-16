---
description: Le applicazioni possono riscontrare problemi durante l'esecuzione in sistemi multiprocessore a causa di presupposti che fanno che sono validi solo nei sistemi a processore singolo.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problemi di sincronizzazione e multiprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0e86a2c69cf0a0c0e56656475f73fb489f7433a94511703b3777302702bb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886209"
---
# <a name="synchronization-and-multiprocessor-issues"></a>Problemi di sincronizzazione e multiprocessore

Le applicazioni possono riscontrare problemi durante l'esecuzione in sistemi multiprocessore a causa di presupposti che fanno che sono validi solo nei sistemi a processore singolo.

## <a name="thread-priorities"></a>Priorità dei thread

Si consideri un programma con due thread, uno con una priorità più alta rispetto all'altro. In un sistema a processore singolo, il thread con priorità più alta non rinuncia al controllo al thread con priorità inferiore perché l'utilità di pianificazione dà la preferenza ai thread con priorità più alta. In un sistema multiprocessore entrambi i thread possono essere eseguiti contemporaneamente, ognuno nel proprio processore.

Le applicazioni devono sincronizzare l'accesso alle strutture di dati per evitare race conditions. Codice che presuppone che i thread con priorità più alta eseguiti senza interferenze da thread con priorità inferiore avranno esito negativo nei sistemi multiprocessore.

## <a name="memory-ordering"></a>Ordinamento della memoria

Quando un processore scrive in una posizione di memoria, il valore viene memorizzato nella cache per migliorare le prestazioni. Analogamente, il processore tenta di soddisfare le richieste di lettura dalla cache per migliorare le prestazioni. Inoltre, i processori iniziano a recuperare i valori dalla memoria prima che siano richiesti dall'applicazione. Ciò può verificarsi come parte dell'esecuzione speculativa o a causa di problemi di riga della cache.

Le cache della CPU possono essere partizionate in banche a cui è possibile accedere in parallelo. Ciò significa che le operazioni di memoria possono essere completate in ordine. Per garantire che le operazioni di memoria siano completate nell'ordine, la maggior parte dei processori fornisce istruzioni sulla barriera di memoria. Una *barriera di memoria* completa garantisce che le operazioni di lettura e scrittura della memoria visualizzate prima dell'istruzione della barriera di memoria vengano eseguite in memoria prima di qualsiasi operazione di lettura e scrittura della memoria visualizzata dopo l'istruzione della barriera di memoria. Una *barriera di memoria di lettura* ordina solo le operazioni di lettura della memoria e una barriera di *memoria* di scrittura ordina solo le operazioni di scrittura della memoria. Queste istruzioni assicurano anche che il compilatore disabilita le ottimizzazioni che potrebbero riordinare le operazioni di memoria tra le barriere.

I processori possono supportare istruzioni per le barriere di memoria con semantica di acquisizione, rilascio e recinto. Questa semantica descrive l'ordine in cui i risultati di un'operazione diventano disponibili. Con la semantica di acquisizione, i risultati dell'operazione sono disponibili prima dei risultati di qualsiasi operazione visualizzata dopo di essa nel codice. Con la semantica di rilascio, i risultati dell'operazione sono disponibili dopo i risultati di qualsiasi operazione visualizzata prima di essa nel codice. La semantica di recinto combina la semantica di acquisizione e rilascio. I risultati di un'operazione con semantica di recinto sono disponibili prima di quelli di qualsiasi operazione visualizzata dopo di essa nel codice e dopo quelli di qualsiasi operazione visualizzata prima di essa.

Nei processori x86 e x64 che supportano SSE2, le istruzioni sono **mfence** (recinto di memoria), **lfence** (recinto del carico) e **sfence** (recinto dell'archivio). Nei processori ARM, le intrusioni sono **dmb** **e dsb**. Per altre informazioni, vedere la documentazione del processore.

Le funzioni di sincronizzazione seguenti usano le barriere appropriate per garantire l'ordinamento della memoria:

-   Funzioni che immettono o lasciano sezioni critiche
-   Funzioni che acquisiscono o rilasciano blocchi SRW
-   Inizio e completamento dell'inizializzazione una sola volta
-   **Funzione EnterSynchronizationBarrier**
-   Funzioni che segnalano gli oggetti di sincronizzazione
-   Funzioni di attesa
-   Funzioni interlock (ad eccezione delle funzioni con _suffisso NoFence_ o intrinseche con _\_ suffisso nf)_

## <a name="fixing-a-race-condition"></a>Correzione di una race condition

Il codice seguente include un race condition in un sistema multiprocessore perché il processore che viene eseguito la prima volta può scrivere nella memoria principale prima di scrivere nella `CacheComputedValue` `fValueHasBeenComputed` memoria `iValue` principale. Di conseguenza, un secondo processore in esecuzione contemporaneamente viene letto come TRUE, ma il nuovo valore di si trova ancora nella cache del primo processore e non è stato `FetchComputedValue` `fValueHasBeenComputed` scritto in  `iValue` memoria.

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

Questa race condition precedente può essere ripristinata usando la parola chiave **volatile** o la funzione [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) per assicurarsi che il valore di venga aggiornato per tutti i processori prima che il valore di sia `iValue` impostato su `fValueHasBeenComputed` **TRUE.**

A partire Visual Studio 2005, se compilato in **modalità /volatile:ms,** il compilatore usa la semantica di acquisizione per le operazioni di lettura sulle variabili **volatili** e la semantica di rilascio per le operazioni di scrittura su variabili **volatili** (se supportate dalla CPU). Pertanto, è possibile correggere l'esempio come segue:

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

Con Visual Studio 2003, **i riferimenti da volatile** a **volatile** vengono ordinati; il compilatore non riordinerà **l'accesso alle variabili volatili.** Tuttavia, queste operazioni potrebbero essere riordine dal processore. Pertanto, è possibile correggere l'esempio come segue:

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti sezione critica](critical-section-objects.md)
</dt> <dt>

[Accesso alle variabili interlock](interlocked-variable-access.md)
</dt> <dt>

[Funzioni di attesa](wait-functions.md)
</dt> </dl>

 

 



