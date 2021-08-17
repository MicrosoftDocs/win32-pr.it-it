---
description: Nel codice seguente vengono illustrate le funzioni send e recv usate dal client dopo che è stata stabilita una connessione.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Invio e ricezione di dati nel client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3150c853f50e8626451cc344179645289058df928600d71bf437dc95d9738986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740562"
---
# <a name="sending-and-receiving-data-on-the-client"></a>Invio e ricezione di dati nel client

Nel codice seguente vengono illustrate [**le funzioni send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) usate dal client dopo che è stata stabilita una connessione.

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



Le [**funzioni send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv recv**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono rispettivamente un valore intero del numero di byte inviati o ricevuti oppure un errore. Ogni funzione accetta anche gli stessi parametri: il socket attivo, un buffer **char,** il numero di byte da inviare o ricevere ed eventuali flag da usare.

Passaggio successivo: [Disconnessione del client](disconnecting-the-client.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> <dt>

[Connessione a un socket](connecting-to-a-socket.md)
</dt> </dl>

 

 



