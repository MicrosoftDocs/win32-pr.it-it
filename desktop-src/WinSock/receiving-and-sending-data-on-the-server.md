---
description: Il codice seguente illustra le funzioni recv e send usate dal server.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Ricezione e invio di dati nel server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f943fe9f1c4045c087b31861bc6db5f1eb394ad800ee0133e0ec8fb668fcbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857851"
---
# <a name="receiving-and-sending-data-on-the-server"></a>Ricezione e invio di dati nel server

Il codice seguente illustra [**le funzioni recv**](/windows/desktop/api/winsock/nf-winsock-recv) [**e send**](/windows/desktop/api/Winsock2/nf-winsock2-send) usate dal server.

### <a name="to-receive-and-send-data-on-a-socket"></a>Per ricevere e inviare dati su un socket


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



Le [**funzioni send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**recv recv**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono rispettivamente un valore intero del numero di byte inviati o ricevuti oppure un errore. Ogni funzione accetta anche gli stessi parametri: socket attivo, buffer **char,** numero di byte da inviare o ricevere ed eventuali flag da usare.

Passaggio successivo: [Disconnessione del server](disconnecting-the-server.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Accettazione di una connessione](accepting-a-connection.md)
</dt> </dl>

 

 



