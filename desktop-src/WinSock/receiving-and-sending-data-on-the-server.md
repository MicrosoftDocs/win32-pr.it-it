---
description: Nel codice seguente vengono illustrate le funzioni ricezione e Send utilizzate dal server.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Ricezione e invio di dati sul server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310455"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Ricezione e invio di dati sul server

Nel codice seguente vengono illustrate le funzioni [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) e [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilizzate dal server.

### <a name="to-receive-and-send-data-on-a-socket"></a>Per ricevere e inviare dati in un socket


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



Le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono entrambi un valore integer del numero di byte inviati o ricevuti, rispettivamente, o un errore. Ogni funzione accetta anche gli stessi parametri, ovvero il socket attivo, un buffer **char** , il numero di byte da inviare o ricevere ed eventuali flag da usare.

Passaggio successivo: [disconnessione del server](disconnecting-the-server.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Accettazione di una connessione](accepting-a-connection.md)
</dt> </dl>

 

 



