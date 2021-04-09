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
# <a name="disconnecting-the-server"></a><span data-ttu-id="d1fa3-103">Disconnessione del server</span><span class="sxs-lookup"><span data-stu-id="d1fa3-103">Disconnecting the Server</span></span>

<span data-ttu-id="d1fa3-104">Una volta che il server ha completato la ricezione dei dati dal client e l'invio di dati al client, il server si disconnette dal client e chiude il socket.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="d1fa3-105">**Per disconnettere e arrestare un socket**</span><span class="sxs-lookup"><span data-stu-id="d1fa3-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="d1fa3-106">Al termine dell'invio dei dati al client da parte del server, è possibile chiamare la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) specificando SD \_ Send per arrestare il lato di invio del socket.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="d1fa3-107">Ciò consente al client di rilasciare alcune risorse per questo socket.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="d1fa3-108">L'applicazione server può comunque ricevere dati sul socket.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-108">The server application can still receive data on the socket.</span></span>
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

    

2.  <span data-ttu-id="d1fa3-109">Al termine della ricezione dei dati da parte dell'applicazione client, viene chiamata la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per chiudere il socket.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="d1fa3-110">Quando l'applicazione client viene completata utilizzando la DLL di Windows Sockets, la funzione [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene chiamata per rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="d1fa3-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="d1fa3-111">Completa codice sorgente server</span><span class="sxs-lookup"><span data-stu-id="d1fa3-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="d1fa3-112">Completa codice server</span><span class="sxs-lookup"><span data-stu-id="d1fa3-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="d1fa3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1fa3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1fa3-114">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="d1fa3-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="d1fa3-115">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="d1fa3-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="d1fa3-116">Ricezione e invio di dati sul server</span><span class="sxs-lookup"><span data-stu-id="d1fa3-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="d1fa3-117">Esecuzione dell'esempio di codice server e client Winsock</span><span class="sxs-lookup"><span data-stu-id="d1fa3-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



