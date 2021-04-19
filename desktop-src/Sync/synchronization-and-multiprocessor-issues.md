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
# <a name="synchronization-and-multiprocessor-issues"></a>Problemi di sincronizzazione e multiprocessore

È possibile che le applicazioni riscontrino problemi quando vengono eseguiti su sistemi multiprocessore, a causa dei presupposti che rendono validi solo nei sistemi a processore singolo.

## <a name="thread-priorities"></a>Priorità dei thread

Si consideri un programma con due thread, uno con una priorità più alta. In un sistema a processore singolo, il thread con priorità più alta non cede il controllo al thread con priorità inferiore perché l'utilità di pianificazione assegna la preferenza ai thread con priorità più alta. In un sistema multiprocessore, entrambi i thread possono essere eseguiti contemporaneamente, ciascuno sul proprio processore.

Le applicazioni devono sincronizzare l'accesso alle strutture di dati per evitare race condition. Il codice che presuppone che i thread con priorità più alta vengano eseguiti senza interferenze dai thread con priorità inferiore avranno esito negativo nei sistemi multiprocessore.

## <a name="memory-ordering"></a>Ordine di memoria

Quando un processore scrive in una posizione di memoria, il valore viene memorizzato nella cache per migliorare le prestazioni. Analogamente, il processore tenta di soddisfare le richieste di lettura dalla cache per migliorare le prestazioni. Inoltre, i processori iniziano a recuperare i valori dalla memoria prima che vengano richiesti dall'applicazione. Questa operazione può essere eseguita come parte dell'esecuzione speculativa o a causa di problemi di riga della cache.

Le cache della CPU possono essere partizionate in banche a cui è possibile accedere in parallelo. Ciò significa che le operazioni di memoria possono essere completate in modo non corretto. Per assicurarsi che le operazioni di memoria vengano completate nell'ordine, la maggior parte dei processori fornisce istruzioni per la barriera di memoria. Una *barriera di memoria completa* garantisce che le operazioni di lettura e scrittura della memoria visualizzate prima dell'istruzione della barriera di memoria vengano sottoposte a commit nella memoria prima di qualsiasi operazione di lettura e scrittura della memoria che viene visualizzata dopo l'istruzione della barriera di memoria. Una *barriera di memoria in lettura* Ordina solo le operazioni di lettura della memoria e una *barriera di memoria di scrittura* Ordina solo le operazioni di scrittura della memoria. Queste istruzioni assicurano inoltre che il compilatore Disabilita le ottimizzazioni che potrebbero riordinare le operazioni di memoria tra le barriere.

I processori possono supportare istruzioni per le barriere di memoria con semantica di acquisizione, rilascio e recinzione. Questa semantica descrive l'ordine in cui i risultati di un'operazione diventano disponibili. Con la semantica di acquisizione, i risultati dell'operazione sono disponibili prima dei risultati di qualsiasi operazione visualizzata dopo il codice. Con la semantica di rilascio, i risultati dell'operazione sono disponibili dopo i risultati di qualsiasi operazione visualizzata prima nel codice. Semantica di recinzione combinare la semantica di acquisizione e di rilascio. I risultati di un'operazione con semantica di recinzione sono disponibili prima di quelli di qualsiasi operazione visualizzata dopo il codice e dopo quelli di qualsiasi operazione visualizzata prima.

Nei processori x86 e x64 che supportano SSE2, le istruzioni sono **mfence** (limite di memoria), **lfence** (limite di caricamento) e **sfence** (limite di archiviazione). Nei processori ARM i supporti sono **DMB** e **DSB**. Per ulteriori informazioni, vedere la documentazione relativa al processore.

Le seguenti funzioni di sincronizzazione usano le barriere appropriate per garantire l'ordine di memoria:

-   Funzioni che immettono o lasciano sezioni critiche
-   Funzioni che acquisiscono o rilasciano blocchi SRW
-   Inizio e completamento inizializzazione unica
-   **EnterSynchronizationBarrier** (funzione)
-   Funzioni che segnalano oggetti di sincronizzazione
-   Funzioni Wait
-   Funzioni Interlocked (eccetto funzioni con suffisso _nofence_ o funzioni intrinseche con suffisso _\_ NF_ )

## <a name="fixing-a-race-condition"></a>Correzione di una race condition

Il codice seguente ha un race condition in un sistema multiprocessore perché il processore eseguito `CacheComputedValue` per la prima volta può scrivere `fValueHasBeenComputed` nella memoria principale prima di scrivere `iValue` nella memoria principale. Di conseguenza, un secondo processore eseguito `FetchComputedValue` allo stesso tempo legge `fValueHasBeenComputed` come **true**, ma il nuovo valore di `iValue` è ancora nella cache del primo processore e non è stato scritto in memoria.

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

Questo race condition precedente può essere corretto tramite la parola chiave **volatile** o la funzione [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) per garantire che il valore di `iValue` venga aggiornato per tutti i processori prima che il valore di `fValueHasBeenComputed` sia impostato su **true**.

A partire da Visual Studio 2005, se compilato in **/volatile: ms** Mode, il compilatore usa la semantica di acquisizione per le operazioni di lettura sulle variabili **volatili** e la semantica di rilascio per le operazioni di scrittura su variabili **volatili** (se supportate dalla CPU). È pertanto possibile correggere l'esempio nel modo seguente:

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

Con Visual Studio 2003, i riferimenti **volatili** a **volatili** sono ordinati; il compilatore non riordina l'accesso a variabili **volatili** . Tuttavia, queste operazioni potrebbero essere riordinate dal processore. È pertanto possibile correggere l'esempio nel modo seguente:

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

[Accesso a variabili Interlocked](interlocked-variable-access.md)
</dt> <dt>

[Funzioni Wait](wait-functions.md)
</dt> </dl>

 

 



