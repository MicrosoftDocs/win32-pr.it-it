---
description: Affinché un server accetti le connessioni client, è necessario che sia associato a un indirizzo di rete all'interno del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Associazione di un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307046"
---
# <a name="binding-a-socket"></a>Associazione di un socket

Affinché un server accetti le connessioni client, è necessario che sia associato a un indirizzo di rete all'interno del sistema. Il codice seguente illustra come associare un socket che è già stato creato a un indirizzo IP e a una porta. Le applicazioni client utilizzano l'indirizzo IP e la porta per connettersi alla rete host.

## <a name="to-bind-a-socket"></a>Per associare un socket

La struttura [**sockaddr**](sockaddr-2.md) include informazioni relative alla famiglia di indirizzi, all'indirizzo IP e al numero di porta.

Chiamare la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , passando la struttura **socket** e [**sockaddr**](sockaddr-2.md) creata restituita dalla funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) come parametri. Verificare la presenza di errori generali.


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



Una volta chiamata la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , le informazioni sull'indirizzo restituite dalla funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) non sono più necessarie. La funzione [**FreeAddrInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) viene chiamata per liberare la memoria allocata dalla funzione **funzione getaddrinfo** per le informazioni sull'indirizzo.


```C++
    freeaddrinfo(result);

```



Passaggio successivo: [ascolto su un socket](listening-on-a-socket.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Creazione di un socket per il server](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



