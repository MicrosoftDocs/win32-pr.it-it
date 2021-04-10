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
# <a name="disconnecting-the-client"></a><span data-ttu-id="1554d-103">Disconnessione del client</span><span class="sxs-lookup"><span data-stu-id="1554d-103">Disconnecting the Client</span></span>

<span data-ttu-id="1554d-104">Una volta che il client ha completato l'invio e la ricezione dei dati, il client si disconnette dal server e arresta il socket.</span><span class="sxs-lookup"><span data-stu-id="1554d-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="1554d-105">**Per disconnettere e arrestare un socket**</span><span class="sxs-lookup"><span data-stu-id="1554d-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="1554d-106">Quando il client invia dati al server, la funzione [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) può essere chiamata specificando SD \_ Send per arrestare il lato di invio del socket.</span><span class="sxs-lookup"><span data-stu-id="1554d-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="1554d-107">Ciò consente al server di rilasciare alcune risorse per questo socket.</span><span class="sxs-lookup"><span data-stu-id="1554d-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="1554d-108">L'applicazione client può comunque ricevere dati sul socket.</span><span class="sxs-lookup"><span data-stu-id="1554d-108">The client application can still receive data on the socket.</span></span>
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

    

2.  <span data-ttu-id="1554d-109">Al termine della ricezione dei dati da parte dell'applicazione client, viene chiamata la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) per chiudere il socket.</span><span class="sxs-lookup"><span data-stu-id="1554d-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="1554d-110">Quando l'applicazione client viene completata utilizzando la DLL di Windows Sockets, la funzione [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) viene chiamata per rilasciare le risorse.</span><span class="sxs-lookup"><span data-stu-id="1554d-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="1554d-111">Completa codice sorgente client</span><span class="sxs-lookup"><span data-stu-id="1554d-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="1554d-112">Completa codice client</span><span class="sxs-lookup"><span data-stu-id="1554d-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="1554d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1554d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1554d-114">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="1554d-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="1554d-115">Applicazione client Winsock</span><span class="sxs-lookup"><span data-stu-id="1554d-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="1554d-116">Invio e ricezione di dati sul client</span><span class="sxs-lookup"><span data-stu-id="1554d-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



