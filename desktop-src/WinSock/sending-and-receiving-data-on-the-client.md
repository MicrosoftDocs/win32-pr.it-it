---
description: Nel codice seguente vengono illustrate le funzioni send e ricezione utilizzate dal client dopo che è stata stabilita una connessione.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Invio e ricezione di dati sul client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315791"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Invio e ricezione di dati sul client

Nel codice seguente vengono illustrate le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) utilizzate dal client dopo che è stata stabilita una connessione.

## <a name="client"></a>Client


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



Le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono entrambi un valore integer del numero di byte inviati o ricevuti, rispettivamente, o un errore. Ogni funzione accetta anche gli stessi parametri, ovvero il socket attivo, un buffer **char** , il numero di byte da inviare o ricevere ed eventuali flag da usare.

Passaggio successivo: [disconnessione del client](disconnecting-the-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> <dt>

[Connessione a un socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



