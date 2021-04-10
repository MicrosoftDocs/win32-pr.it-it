---
description: Una volta che il client ha completato l'invio e la ricezione dei dati, il client si disconnette dal server e arresta il socket.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Disconnessione del client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343531"
---
# <a name="disconnecting-the-client"></a>Disconnessione del client

Una volta che il client ha completato l'invio e la ricezione dei dati, il client si disconnette dal server e arresta il socket.

**Per disconnettere e arrestare un socket**

1.  Quando il client invia dati al server, la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) può essere chiamata specificando SD \_ Send per arrestare il lato di invio del socket. Ciò consente al server di rilasciare alcune risorse per questo socket. L'applicazione client può comunque ricevere dati sul socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Al termine della ricezione dei dati da parte dell'applicazione client, viene chiamata la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per chiudere il socket.

    Quando l'applicazione client viene completata utilizzando la DLL di Windows Sockets, la funzione [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene chiamata per rilasciare le risorse.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Completa codice sorgente client

-   [Completa codice client](complete-client-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione client Winsock](winsock-client-application.md)
</dt> <dt>

[Invio e ricezione di dati sul client](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



