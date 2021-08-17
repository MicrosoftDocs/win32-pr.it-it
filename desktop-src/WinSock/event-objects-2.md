---
description: L'introduzione di operazioni di I/O sovrapposte richiede un meccanismo che consente alle applicazioni di associare in modo univoco le richieste di invio e ricezione alle indicazioni di completamento successive.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Oggetti evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132594"
---
# <a name="event-objects-windows-sockets-2"></a>Oggetti evento (Windows Sockets 2)

L'introduzione di operazioni di I/O sovrapposte richiede un meccanismo che consente alle applicazioni di associare in modo univoco le richieste di invio e ricezione alle indicazioni di completamento successive. In Windows Sockets 2 questa operazione viene eseguita con oggetti evento modellati in base Windows eventi. Windows Gli oggetti evento socket sono costrutti piuttosto semplici che possono essere creati e chiusi, impostati e cancellati e di cui è in attesa e di cui è stato eseguito il polling. L'utilità principale è la capacità di un'applicazione di bloccare e attendere che uno o più oggetti evento diventino impostati.

Le applicazioni usano [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) per ottenere un handle di oggetto evento che può quindi essere fornito come parametro obbligatorio per le versioni sovrapposte delle chiamate di invio e ricezione ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). L'oggetto evento, che viene cancellato alla prima creazione, viene impostato dai provider di trasporto quando l'operazione di I/O sovrapposta associata è stata completata (correttamente o con errori). Ogni oggetto evento creato da **WSACreateEvent** deve avere un [**oggetto WSACloseEvent corrispondente**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) per l'eliminazione.

Gli oggetti evento vengono usati anche in [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) per associare uno o più eventi di rete FD \_ XXX a un oggetto evento. Questa operazione è descritta in [Notifica asincrona tramite oggetti evento.](asynchronous-notification-using-event-objects-2.md)

Negli ambienti a 32 bit le funzioni correlate agli oggetti evento, tra cui [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents,**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) vengono mappate direttamente alle funzioni Windows native corrispondenti, usando lo stesso nome di funzione, ma senza il prefisso WSA.

 

 



