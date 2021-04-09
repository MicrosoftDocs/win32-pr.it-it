---
description: Una volta che il server ha completato la ricezione dei dati dal client e l'invio di dati al client, il server si disconnette dal client e chiude il socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Disconnessione del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879217"
---
# <a name="disconnecting-the-server"></a>Disconnessione del server

Una volta che il server ha completato la ricezione dei dati dal client e l'invio di dati al client, il server si disconnette dal client e chiude il socket.

**Per disconnettere e arrestare un socket**

1.  Al termine dell'invio dei dati al client da parte del server, è possibile chiamare la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) specificando SD \_ Send per arrestare il lato di invio del socket. Ciò consente al client di rilasciare alcune risorse per questo socket. L'applicazione server può comunque ricevere dati sul socket.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Al termine della ricezione dei dati da parte dell'applicazione client, viene chiamata la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per chiudere il socket.

    Quando l'applicazione client viene completata utilizzando la DLL di Windows Sockets, la funzione [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene chiamata per rilasciare le risorse.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Completa codice sorgente server

-   [Completa codice server](complete-server-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Ricezione e invio di dati sul server](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Esecuzione dell'esempio di codice server e client Winsock](finished-server-and-client-code.md)
</dt> </dl>

 

 



