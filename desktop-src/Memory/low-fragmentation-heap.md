---
description: La frammentazione dell'heap è uno stato in cui la memoria disponibile viene suddivisa in blocchi piccoli e non contigui.
ms.assetid: d10abf82-423c-4942-b05e-55de3a5c4219
title: Heap a bassa frammentazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d4cc6f7f0e2427a20532f5e32cc1460f9b6601d1e6dddf0de603757895005e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067741"
---
# <a name="low-fragmentation-heap"></a>Heap a bassa frammentazione

\[Le informazioni contenute in questo argomento si applicano Windows Server 2003 e Windows XP. A partire da Windows Vista, il sistema usa l'heap a bassa frammentazione (LFH) in base alle esigenze per il servizio delle richieste di allocazione della memoria. Non è necessario che le applicazioni abilitino l'LFH per gli heap.\]

La frammentazione dell'heap è uno stato in cui la memoria disponibile viene suddivisa in blocchi piccoli e non contigui. Quando un heap è frammentato, l'allocazione della memoria può avere esito negativo anche quando la memoria totale disponibile nell'heap è sufficiente per soddisfare una richiesta, perché nessun singolo blocco di memoria è sufficientemente grande. L'heap a frammentazione bassa (LFH) consente di ridurre la frammentazione dell'heap.

LFH non è un heap separato. Si tratta invece di un criterio che le applicazioni possono abilitare per gli heap. Quando l'LFH è abilitato, il sistema alloca memoria in determinate dimensioni predeterminate. Quando un'applicazione richiede un'allocazione di memoria da un heap con LFH abilitato, il sistema alloca il blocco di memoria più piccolo sufficientemente grande da contenere le dimensioni richieste. Il sistema non usa l'LFH per allocazioni superiori a 16 KB, indipendentemente dal fatto che l'LFH sia abilitato o meno.

Un'applicazione deve abilitare l'LFH solo per l'heap predefinito del processo chiamante o per [gli heap](heap-functions.md) privati creati dall'applicazione. Per abilitare LFH per un heap, usare la [**funzione GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) per ottenere un handle per l'heap predefinito del processo chiamante o usare l'handle per un heap privato creato dalla [**funzione HeapCreate.**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) Chiamare quindi la [**funzione HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) con l'handle.

L'LFH non può essere abilitato per gli heap creati con **HEAP \_ NO \_ SERIALIZE** o per gli heap creati con dimensioni fisse. L'LFH non può essere abilitato anche se si usano gli strumenti di debug heap [in](/windows-hardware/drivers/debugger/) Strumenti di debug per Windows o [Microsoft Application Verifier](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&displaylang=en).

Dopo che l'LFH è stato abilitato per un heap, non può essere disabilitato.

Le applicazioni che traggono maggior vantaggio dall'LFH sono applicazioni multithreading che allocano spesso memoria e usano un'ampia gamma di dimensioni di allocazione inferiore a 16 KB. Tuttavia, non tutte le applicazioni traggono vantaggio dall'LFH. Per valutare gli effetti dell'abilitazione dell'LFH nell'applicazione, usare i dati di profilatura delle prestazioni.

 

 
