---
description: La frammentazione dell'heap è uno stato in cui la memoria disponibile viene suddivisa in blocchi piccoli e non contigui.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap con frammentazione bassa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad14a97fa6d95b663f63b21f0982332ba0de01e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311736"
---
# <a name="low-fragmentation-heap"></a>Heap con frammentazione bassa

\[Le informazioni contenute in questo argomento si applicano a Windows Server 2003 e Windows XP. A partire da Windows Vista, il sistema usa l'heap di frammentazione bassa (LFH) in base alle esigenze per soddisfare le richieste di allocazione della memoria. Per le applicazioni non è necessario abilitare il LFH per gli heap.\]

La frammentazione dell'heap è uno stato in cui la memoria disponibile viene suddivisa in blocchi piccoli e non contigui. Quando un heap è frammentato, l'allocazione di memoria può non riuscire anche quando la memoria totale disponibile nell'heap è sufficiente per soddisfare una richiesta, perché nessun singolo blocco di memoria è sufficientemente grande. L'heap con frammentazione bassa (LFH) consente di ridurre la frammentazione dell'heap.

LFH non è un heap separato. Bensì un criterio che le applicazioni possono abilitare per gli heap. Quando LFH è abilitato, il sistema alloca memoria in determinate dimensioni predeterminate. Quando un'applicazione richiede un'allocazione di memoria da un heap in cui è abilitato LFH, il sistema alloca il blocco di memoria più piccolo sufficientemente grande da contenere la dimensione richiesta. Il sistema non utilizza LFH per le allocazioni maggiori di 16 KB, indipendentemente dal fatto che il LFH sia abilitato o meno.

Un'applicazione deve abilitare il LFH solo per l'heap predefinito del processo chiamante o per gli [heap privati](heap-functions.md) creati dall'applicazione. Per abilitare LFH per un heap, usare la funzione [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) per ottenere un handle per l'heap predefinito del processo chiamante oppure usare l'handle per un heap privato creato dalla funzione [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) . Chiamare quindi la funzione [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) con l'handle.

Non è possibile abilitare LFH per gli heap creati con l' **heap \_ Nessuna \_ serializzazione** o per gli heap creati con una dimensione fissa. Non è inoltre possibile abilitare LFH se si usano gli strumenti di debug dell'heap negli [strumenti di debug per Windows](/windows-hardware/drivers/debugger/) o [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Quando LFH è stato abilitato per un heap, non può essere disabilitato.

Le applicazioni che traggono vantaggio dalla maggior parte dei LFH sono applicazioni multithread che allocano spesso memoria e utilizzano una varietà di dimensioni di allocazione inferiore a 16 KB. Tuttavia, non tutte le applicazioni traggono vantaggio dal LFH. Per valutare gli effetti dell'abilitazione di LFH nell'applicazione, usare i dati di profilatura delle prestazioni.

 

 
