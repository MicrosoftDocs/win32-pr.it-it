---
description: Ogni processo dispone di un heap predefinito fornito dal sistema. Le applicazioni che effettuano allocazioni frequenti dall'heap possono migliorare le prestazioni usando gli heap privati.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funzioni heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e591c1e349ed6806cbebe00a178a99e63bb412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881505"
---
# <a name="heap-functions"></a>Funzioni heap

Ogni processo dispone di un heap predefinito fornito dal sistema. Le applicazioni che effettuano allocazioni frequenti dall'heap possono migliorare le prestazioni usando gli heap privati.

Un heap privato è un blocco di una o più pagine nello spazio degli indirizzi del processo chiamante. Dopo aver creato l'heap privato, il processo utilizza funzioni quali [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) e [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) per gestire la memoria nell'heap.

Le funzioni heap possono anche essere usate per gestire la memoria nell'heap predefinito del processo, usando l'handle restituito dalla funzione [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) . Per questo scopo, le nuove applicazioni devono usare le funzioni heap anziché le [funzioni globali e locali](global-and-local-functions.md) .

Non esiste alcuna differenza tra la memoria allocata da un heap privato e quella allocata usando le altre funzioni di allocazione della memoria. Per un elenco completo delle funzioni, vedere la tabella nelle [funzioni di gestione della memoria](memory-management-functions.md).

> [!Note]  
> Un thread deve chiamare le funzioni dell'heap solo per l'heap predefinito del processo e per gli heap privati che il thread crea e gestisce, usando gli handle restituiti dalla funzione [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) o [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) .

 

La funzione [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) crea un oggetto heap privato dal quale il processo chiamante può allocare blocchi di memoria tramite la funzione [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) . **HeapCreate** specifica una dimensione iniziale e una dimensione massima per l'heap. La dimensione iniziale determina il numero di pagine di cui è stato eseguito il commit, di lettura/scrittura inizialmente allocate per l'heap. La dimensione massima determina il numero totale di pagine riservate. Queste pagine creano un blocco contiguo nello spazio degli indirizzi virtuali di un processo in cui l'heap può aumentare. Le pagine aggiuntive vengono sottoposte automaticamente a commit da questo spazio riservato se le richieste da **HeapAlloc** superano le dimensioni correnti delle pagine di cui è stato eseguito il commit, supponendo che sia disponibile l'archiviazione fisica. Una volta eseguito il commit, le pagine non vengono sottoposte a commit finché il processo non viene terminato o fino a quando l'heap non viene eliminato definitivamente chiamando la funzione [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) .

La memoria di un oggetto heap privato è accessibile solo al processo che lo ha creato. Se una libreria a collegamento dinamico (DLL) crea un heap privato, lo esegue nello spazio degli indirizzi del processo che ha chiamato la DLL. È accessibile solo a tale processo.

La funzione [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) alloca un numero specificato di byte da un heap privato e restituisce un puntatore al blocco allocato. Questo puntatore può essere utilizzato nelle funzioni [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)e [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) .

La memoria allocata da [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) non è movibile. L'indirizzo restituito da **HeapAlloc** è valido finché il blocco di memoria non viene liberato o riallocato; non è necessario bloccare il blocco di memoria.

Poiché il sistema non può comprimere un heap privato, può diventare frammentato. Le applicazioni che allocano grandi quantità di memoria in diverse dimensioni di allocazione possono utilizzare l' [heap a frammentazione ridotta](low-fragmentation-heap.md) per ridurre la frammentazione dell'heap.

Un possibile utilizzo delle funzioni heap consiste nel creare un heap privato all'avvio di un processo, specificando una dimensione iniziale sufficiente per soddisfare i requisiti di memoria del processo. Se la chiamata alla funzione [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) ha esito negativo, il processo può terminare o notificare all'utente la carenza di memoria; Se ha esito positivo, tuttavia, il processo è sicuro di avere la memoria necessaria.

La memoria richiesta da [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) può essere o meno contigua. La memoria allocata in un heap da [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) è contigua. Non è consigliabile scrivere o leggere dalla memoria in un heap, ad eccezione di quanto allocato da **HeapAlloc**, né considerare alcuna relazione tra due aree di memoria allocate da **HeapAlloc**.

Non è consigliabile fare riferimento a memoria che è stata liberata da [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree). Dopo che la memoria è stata liberata, tutte le informazioni che potrebbero essere state rilasciate sono finite. Se sono necessarie informazioni, non liberare memoria contenente le informazioni. Le chiamate di funzione che restituiscono informazioni sulla memoria (ad esempio [**HEAPSIZE**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) non possono essere utilizzate con la memoria liberata, perché potrebbero restituire dati fasulli.

La funzione [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) Elimina un oggetto heap privato. Annulla il commit e rilascia tutte le pagine dell'oggetto heap e invalida l'handle per l'heap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Confronto tra i metodi di allocazione della memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



