---
description: Per accettare connessioni client, un server deve essere associato a un indirizzo di rete all'interno del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Associazione di un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9e745395209228584ea5535864cca57e30494b2e30bfff02fe2abc527ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996920"
---
# <a name="binding-a-socket"></a>Associazione di un socket

Per accettare connessioni client, un server deve essere associato a un indirizzo di rete all'interno del sistema. Il codice seguente illustra come associare un socket già creato a un indirizzo IP e a una porta. Le applicazioni client usano l'indirizzo IP e la porta per connettersi alla rete host.

## <a name="to-bind-a-socket"></a>Per associare un socket

La [**struttura sockaddr**](sockaddr-2.md) contiene informazioni relative alla famiglia di indirizzi, all'indirizzo IP e al numero di porta.

Chiamare la [**funzione bind,**](/windows/desktop/api/winsock/nf-winsock-bind) passando il **socket creato** e la [**struttura sockaddr**](sockaddr-2.md) restituita dalla [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) come parametri. Verificare la presenza di errori generali.


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



Una volta [**chiamata**](/windows/desktop/api/winsock/nf-winsock-bind) la funzione di associazione, le informazioni sull'indirizzo restituite [**dalla funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) non sono più necessarie. La [**funzione freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) viene chiamata per liberare la memoria allocata dalla **funzione getaddrinfo** per queste informazioni sull'indirizzo.


```C++
    freeaddrinfo(result);

```



Passaggio successivo: [Ascolto su un socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Creazione di un socket per il server](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



