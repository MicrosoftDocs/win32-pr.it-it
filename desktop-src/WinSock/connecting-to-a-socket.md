---
description: Per comunicare in rete, un client deve connettersi a un server.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Connessione a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132674"
---
# <a name="connecting-to-a-socket"></a>Connessione a un socket

Per comunicare in rete, un client deve connettersi a un server.

## <a name="to-connect-to-a-socket"></a>Per connettersi a un socket

Chiamare la [**funzione connect,**](/windows/desktop/api/Winsock2/nf-winsock2-connect) passando il socket creato e la struttura [**sockaddr**](sockaddr-2.md) come parametri. Verificare la presenza di errori generali.


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



La [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) viene usata per determinare i valori nella struttura [**sockaddr.**](sockaddr-2.md) In questo esempio il primo indirizzo IP restituito dalla **funzione getaddrinfo** viene usato per specificare la struttura **sockaddr** passata alla [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Se la **chiamata connect** non riesce al primo indirizzo IP, provare la struttura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) successiva nell'elenco collegato restituito dalla **funzione getaddrinfo.**

Le informazioni specificate nella [**struttura sockaddr**](sockaddr-2.md) includono:

-   l'indirizzo IP del server a cui il client tenterà di connettersi.
-   il numero di porta nel server a cui si connetterà il client. Questa porta è stata specificata come porta 27015 quando il client ha chiamato la [**funzione getaddrinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)

Passaggio successivo: [Invio e ricezione di dati nel client](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> <dt>

[Creazione di un socket per il client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
