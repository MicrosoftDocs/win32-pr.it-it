---
description: Dopo che il server ha completato la ricezione dei dati dal client e l'invio di dati al client, il server si disconnette dal client e arresta il socket.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Disconnessione del server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f644b8727898a9d77ab5aa5fb10b0a0ae5b58cdf88a3beb1b9642215d142b6b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898361"
---
# <a name="disconnecting-the-server"></a>Disconnessione del server

Dopo che il server ha completato la ricezione dei dati dal client e l'invio di dati al client, il server si disconnette dal client e arresta il socket.

**Per disconnettere e arrestare un socket**

1.  Al termine dell'invio dei dati al client, il server può chiamare la funzione [**di**](/windows/desktop/api/winsock/nf-winsock-shutdown) arresto specificando SD SEND per arrestare il lato di invio \_ del socket. In questo modo il client può rilasciare alcune delle risorse per questo socket. L'applicazione server può comunque ricevere dati sul socket.
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

    

2.  Al termine della ricezione dei dati da parte dell'applicazione client, viene chiamata la [**funzione closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per chiudere il socket.

    Quando l'applicazione client viene completata usando la DLL Windows Sockets, viene chiamata la [**funzione WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) per rilasciare le risorse.

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a>Completare il codice sorgente del server

-   [Completare il codice del server](complete-server-code.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Applicazione server Winsock](winsock-server-application.md)
</dt> <dt>

[Ricezione e invio di dati nel server](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[Esecuzione dell'esempio di codice client e server Winsock](finished-server-and-client-code.md)
</dt> </dl>

 

 



