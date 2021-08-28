---
title: Heap
description: Un heap tiene traccia di un gruppo di allocazioni liberate come unità.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servizi Web Heap per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005931"
---
# <a name="heap"></a>Heap

Un heap tiene traccia di un gruppo di allocazioni liberate come unità.

Ciò consente di evitare modelli complessi di allocazione e deallocazione della memoria quando si usa WWSAPI.


A ogni messaggio è associato un heap. Durante l'invio di un messaggio o durante la ricezione di un messaggio, l'heap del messaggio viene usato per tutte le allocazioni relative a tale messaggio specifico. Dopo l'invio o la ricezione di un messaggio, l'heap viene reimpostato, in modo da pulire tutte le allocazioni correlate al messaggio specifico.

Gli heap possono essere usati anche per archiviare i dati dei messaggi separatamente dalla durata di un messaggio. Molte delle API consentono di specificare l'heap da usare durante la lettura dei dati e offrono un controllo esplicito sulla durata di tutti i dati letti.

È garantito che le allocazioni da un heap siano allineate su un limite di almeno 8 byte.

Zero allocazioni di byte restituiranno un puntatore non NULL.

Nella Windows 7, se PageHeap è abilitato, viene usato un heap restituito da HeapCreate per gestire la memoria. In questo caso, [**WsAlloc esegue**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) il mapping direttamente a HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) esegue il mapping a HeapDestroy.

L'enumerazione seguente viene utilizzata con l'heap:

-   [**ID PROPRIETÀ HEAP WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Con l'heap vengono usate le funzioni seguenti:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

L'handle seguente viene usato con l'heap:

-   [WS \_ HEAP](ws-heap.md)

Con l'heap vengono usate le strutture seguenti:

-   [**PROPRIETÀ HEAP WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**PROPRIETÀ \_ HEAP WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




