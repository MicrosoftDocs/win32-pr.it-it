---
title: Heap
description: Un heap tiene traccia di un gruppo di allocazioni liberate come unità.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Servizi Web heap per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399967"
---
# <a name="heap"></a>Heap

Un heap tiene traccia di un gruppo di allocazioni liberate come unità.

In questo modo è possibile evitare modelli complessi di allocazione e deallocazione della memoria quando si usa WWSAPI.


È presente un heap associato a ogni messaggio. Durante l'invio di un messaggio o la ricezione di un messaggio, l'heap del messaggio viene utilizzato per tutte le allocazioni relative al messaggio specifico. Dopo l'invio o la ricezione di un messaggio, l'heap viene reimpostato, che consente di eseguire la pulizia di tutte le allocazioni correlate al messaggio specifico.

Gli heap possono essere utilizzati anche per archiviare i dati dei messaggi separatamente rispetto alla durata di un messaggio. Gran parte della specifica dell'API Consenti dell'heap da usare durante la lettura dei dati fornisce un controllo esplicito sulla durata dei dati letti.

Le allocazioni da un heap sono sicuramente allineate in almeno un limite di 8 byte.

Le allocazioni di zero byte restituiranno un puntatore non NULL.

In Windows 7, se PageHeap è abilitato, per gestire la memoria viene usato un heap restituito da HeapCreate. In questo caso, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) esegue il mapping diretto a HeapAlloc e [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) a HeapDestroy.

L'enumerazione seguente viene utilizzata con l'heap:

-   [**\_ID della \_ proprietà \_ heap WS**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

Con l'heap vengono usate le funzioni seguenti:

-   [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**WsCreateHeap**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**WsFreeHeap**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**WsGetHeapProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

Con l'heap viene utilizzato l'handle seguente:

-   [\_heap WS](ws-heap.md)

Con l'heap vengono utilizzate le strutture seguenti:

-   [**\_Proprietà heap \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_Proprietà heap \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




