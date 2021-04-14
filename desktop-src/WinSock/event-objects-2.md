---
description: L'introduzione all'I/O sovrapposto richiede un meccanismo che consente alle applicazioni di associare in modo non ambiguo le richieste di invio e ricezione con le indicazioni di completamento successive.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Oggetti evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343521"
---
# <a name="event-objects-windows-sockets-2"></a>Oggetti evento (Windows Sockets 2)

L'introduzione all'I/O sovrapposto richiede un meccanismo che consente alle applicazioni di associare in modo non ambiguo le richieste di invio e ricezione con le indicazioni di completamento successive. In Windows Sockets 2 questa operazione viene eseguita con gli oggetti evento modellati dopo gli eventi di Windows. Gli oggetti evento Windows Sockets sono costrutti piuttosto semplici che possono essere creati e chiusi, impostati e cancellati, e in attesa e in polling. L'utilità principale è la possibilità che un'applicazione si blocchi e attenda che uno o più oggetti evento vengano impostati.

Le applicazioni utilizzano [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) per ottenere un handle di oggetto evento che può quindi essere fornito come parametro obbligatorio per le versioni sovrapposte delle chiamate di trasmissione e ricezione ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). L'oggetto evento, che viene cancellato quando viene creato per la prima volta, viene impostato dai provider di trasporto quando l'operazione di I/O sovrapposta associata è stata completata (correttamente o con errori). Ogni oggetto evento creato da **WSACreateEvent** deve avere un [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) corrispondente per eliminarlo.

Gli oggetti evento vengono usati anche in [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) per associare uno o più \_ eventi di rete FD xxx a un oggetto evento. Questa operazione è descritta in [notifica asincrona mediante oggetti evento](asynchronous-notification-using-event-objects-2.md).

Negli ambienti a 32 bit, le funzioni correlate agli oggetti evento, tra cui [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**WSACloseEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**WSASetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)e [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , vengono mappate direttamente alle funzioni Windows native corrispondenti, usando lo stesso nome di funzione, ma senza il prefisso WSA.

 

 



