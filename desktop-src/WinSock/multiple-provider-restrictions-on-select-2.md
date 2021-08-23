---
description: La funzione select viene usata per determinare lo stato di uno o più socket in un set. Per ogni socket, il chiamante può richiedere informazioni sullo stato di lettura, scrittura o errore. Un set di socket è indicato da una struttura SET \_ FD.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Restrizioni di più provider per la selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec5c89c6dd2db809a356f5b53212fd019e32fd9e348c298bcab7f567ee2d0fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569631"
---
# <a name="multiple-provider-restrictions-on-select"></a>Restrizioni di più provider per la selezione

La [**funzione**](/windows/desktop/api/Winsock2/nf-winsock2-select) select viene usata per determinare lo stato di uno o più socket in un set. Per ogni socket, il chiamante può richiedere informazioni sullo stato di lettura, scrittura o errore. Un set di socket è indicato da una [**struttura SET \_ FD.**](/windows/desktop/api/winsock/nf-winsock-fd_set)

Windows Socket 2 consente a un'applicazione di usare più provider di servizi, ma la funzione [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) è limitata a un set di socket associati a un singolo provider di servizi. Questo non impedisce in alcun modo a un'applicazione di avere più socket aperti tramite più provider.

Esistono due modi per determinare lo stato di un set di socket che si estende su più provider di servizi:

-   Uso delle [**funzioni WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) quando viene utilizzata la semantica di blocco.
-   Uso della [**funzione WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) quando vengono utilizzate operazioni non di blocco e l'applicazione usa già Windows message pump.

Quando un'applicazione deve usare la semantica di blocco in un set di socket che si estende su più provider, è consigliabile [**usare WSAWaitForMultipleEvents.**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) L'applicazione può anche usare la funzione [**WSAEventSelect,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) che consente agli eventi di rete FD \_ XXX (vedere [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) di associare a un oggetto evento e di essere gestiti dall'interno del paradigma dell'oggetto evento (descritto in [Overlapped I/O and Event Objects](overlapped-i-o-and-event-objects-2.md)).

La [**funzione WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) non è limitata a un singolo provider perché accetta un singolo descrittore di socket come parametro di input. Si noti tuttavia che la funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) offre prestazioni e scalabilità migliori rispetto a **WSAAsyncSelect** man mano che il sovraccarico della gestione del message pump con i messaggi di evento Winsock aumenta man mano che aumenta il numero totale di socket usati.

 

 



