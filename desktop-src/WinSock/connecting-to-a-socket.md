---
description: Per comunicare in rete, un client deve connettersi a un server.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Connessione a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307010"
---
# <a name="connecting-to-a-socket"></a>Connessione a un socket

Per comunicare in rete, un client deve connettersi a un server.

## <a name="to-connect-to-a-socket"></a>Per connettersi a un socket

Chiamare la funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , passando il socket creato e la struttura [**sockaddr**](sockaddr-2.md) come parametri. Verificare la presenza di errori generali.


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



La funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) viene usata per determinare i valori nella struttura [**sockaddr**](sockaddr-2.md) . In questo esempio, il primo indirizzo IP restituito dalla funzione **funzione getaddrinfo** viene usato per specificare la struttura **sockaddr** passata alla [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Se la chiamata di **connessione** non riesce al primo indirizzo IP, provare la struttura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) successiva nell'elenco collegato restituito dalla funzione **funzione getaddrinfo** .

Le informazioni specificate nella struttura [**sockaddr**](sockaddr-2.md) includono:

-   Indirizzo IP del server a cui il client tenterà di connettersi.
-   numero di porta nel server a cui si connetterà il client. Questa porta è stata specificata come porta 27015 quando il client ha chiamato la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

Passaggio successivo: [invio e ricezione di dati sul client](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> <dt>

[Creazione di un socket per il client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
