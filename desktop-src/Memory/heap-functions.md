---
description: Ogni processo dispone di un heap predefinito fornito dal sistema. Le applicazioni che effettuano allocazioni frequenti dall'heap possono migliorare le prestazioni usando heap privati.
ms.assetid: cfb683fa-4f46-48b5-9a28-f4625a9cb8cd
title: Funzioni heap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8171b75abf879eb50204d55541557bdbf5359bd1e8f956d147e49a9d61656d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067821"
---
# <a name="heap-functions"></a>Funzioni heap

Ogni processo dispone di un heap predefinito fornito dal sistema. Le applicazioni che effettuano allocazioni frequenti dall'heap possono migliorare le prestazioni usando heap privati.

Un heap privato è un blocco di una o più pagine nello spazio indirizzi del processo chiamante. Dopo aver creato l'heap privato, il processo usa funzioni come [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) e [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) per gestire la memoria in tale heap.

Le funzioni heap possono essere usate anche per gestire la memoria nell'heap predefinito del processo, usando l'handle restituito dalla [**funzione GetProcessHeap.**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) A questo scopo, le nuove applicazioni devono usare le funzioni heap anziché le [funzioni globali e](global-and-local-functions.md) locali.

Non esiste alcuna differenza tra la memoria allocata da un heap privato e quella allocata usando le altre funzioni di allocazione della memoria. Per un elenco completo delle funzioni, vedere la tabella in [Funzioni di gestione della memoria](memory-management-functions.md).

> [!Note]  
> Un thread deve chiamare le funzioni heap solo per gli heap predefiniti del processo e gli heap privati creati e gestiti dal thread, usando gli handle restituiti dalla [**funzione GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) o [**HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate)

 

La [**funzione HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) crea un oggetto heap privato da cui il processo chiamante può allocare blocchi di memoria usando la [**funzione HeapAlloc.**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) **HeapCreate** specifica sia una dimensione iniziale che una dimensione massima per l'heap. Le dimensioni iniziali determinano il numero di pagine di lettura/scrittura di cui è stato eseguito il commit inizialmente allocate per l'heap. Le dimensioni massime determinano il numero totale di pagine riservate. Queste pagine creano un blocco contiguo nello spazio degli indirizzi virtuali di un processo in cui l'heap può aumentare. Il commit di pagine aggiuntive viene eseguito automaticamente da questo spazio riservato se le richieste di **HeapAlloc** superano le dimensioni correnti delle pagine di cui è stato eseguito il commit, presupponendo che sia disponibile l'archiviazione fisica per tale spazio. Dopo il commit, le pagine non vengono dismesse fino a quando il processo non viene terminato o finché l'heap non viene eliminato chiamando la [**funzione HeapDestroy.**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy)

La memoria di un oggetto heap privato è accessibile solo al processo che lo ha creato. Se una libreria a collegamento dinamico (DLL) crea un heap privato, lo fa nello spazio degli indirizzi del processo che ha chiamato la DLL. È accessibile solo a tale processo.

La [**funzione HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) alloca un numero specificato di byte da un heap privato e restituisce un puntatore al blocco allocato. Questo puntatore può essere usato nelle [**funzioni HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree), [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc), [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)e [**HeapValidate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate)

La memoria [**allocata da HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) non è mobile. L'indirizzo restituito **da HeapAlloc** è valido fino a quando il blocco di memoria non viene liberato o riallocato. Non è necessario bloccare il blocco di memoria.

Poiché il sistema non è in grado di compattare un heap privato, può diventare frammentato. Le applicazioni che allocano grandi quantità di memoria in diverse dimensioni di allocazione possono usare [l'heap](low-fragmentation-heap.md) a bassa frammentazione per ridurre la frammentazione dell'heap.

Un possibile uso delle funzioni heap è la creazione di un heap privato all'avvio di un processo, specificando una dimensione iniziale sufficiente per soddisfare i requisiti di memoria del processo. Se la chiamata alla funzione [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) ha esito negativo, il processo può terminare o notificare all'utente la mancanza di memoria. se ha esito positivo, tuttavia, il processo ha la certezza di avere la memoria di cui ha bisogno.

La memoria richiesta [**da HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) può essere contigua o meno. La memoria allocata all'interno di un heap [**da HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) è contigua. Non è consigliabile scrivere o leggere dalla memoria in un heap, ad eccezione di quello allocato da **HeapAlloc**, né presupporre alcuna relazione tra due aree di memoria allocate **da HeapAlloc**.

Non è consigliabile fare riferimento in alcun modo alla memoria liberata da [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree). Dopo che la memoria è stata liberata, tutte le informazioni che potrebbero essere state contenute vengono rimosse per sempre. Se sono necessarie informazioni, non liberare memoria contenente le informazioni. Le chiamate di funzione che restituiscono informazioni sulla memoria (ad esempio [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize)) non possono essere usate con la memoria liberata, perché possono restituire dati falsi.

La [**funzione HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) elimina un oggetto heap privato. Decommita e rilascia tutte le pagine dell'oggetto heap e invalida l'handle nell'heap.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Confronto dei metodi di allocazione di memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 



