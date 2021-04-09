---
description: La funzione Select viene utilizzata per determinare lo stato di uno o più socket in un set. Per ogni socket, il chiamante può richiedere informazioni sullo stato di lettura, scrittura o errore. Un set di socket è indicato da una \_ struttura di set FD.
ms.assetid: 40354d8f-1e8b-48aa-888a-81a421568f23
title: Limitazioni di più provider per Select
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2556d98aea60e6fa822f9e3df57cc142c33491d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129155"
---
# <a name="multiple-provider-restrictions-on-select"></a>Limitazioni di più provider per Select

La funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) viene utilizzata per determinare lo stato di uno o più socket in un set. Per ogni socket, il chiamante può richiedere informazioni sullo stato di lettura, scrittura o errore. Un set di socket è indicato da una struttura di [**\_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .

Windows Sockets 2 consente a un'applicazione di usare più di un provider di servizi, ma la funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) è limitata a un set di socket associato a un singolo provider di servizi. Questa operazione non consente di limitare l'apertura di più socket da parte di un'applicazione tramite più provider.

Esistono due modi per determinare lo stato di un set di socket che si estende su più provider di servizi:

-   Uso delle funzioni [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) o [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) quando viene utilizzata la semantica di blocco.
-   Utilizzo della funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) quando vengono utilizzate operazioni di non blocco e l'applicazione utilizza già un message pump di Windows.

Quando un'applicazione deve usare la semantica di blocco su un set di socket che si estende su più provider, è consigliabile [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) . L'applicazione può anche usare la funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) , che consente agli \_ eventi di rete FD xxx (vedere [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)) di essere associati a un oggetto evento ed essere gestiti dall'interno del paradigma dell'oggetto evento (descritto in [oggetti di I/O sovrapposti e oggetti evento](overlapped-i-o-and-event-objects-2.md)).

La funzione [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) non è limitata a un singolo provider perché accetta un singolo descrittore di socket come parametro di input. Si noti tuttavia che la funzione [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) offre prestazioni e scalabilità migliori rispetto a **WSAAsyncSelect** , poiché il sovraccarico della gestione dei messaggi con i messaggi degli eventi Winsock aumenta con l'aumentare del numero totale di socket in uso.

 

 



