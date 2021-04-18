---
description: Quando il socket è in ascolto di una connessione, il programma deve gestire le richieste di connessione su tale socket.
ms.assetid: d01f3d90-4d83-442e-aada-e7b082ef7699
title: Accettazione di una connessione (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e066b53c22dd9964ad44dc8d67c15969641362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307058"
---
# <a name="accepting-a-connection-windows-sockets-2"></a><span data-ttu-id="d3e7c-103">Accettazione di una connessione (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="d3e7c-103">Accepting a Connection (Windows Sockets 2)</span></span>

<span data-ttu-id="d3e7c-104">Quando il socket è in ascolto di una connessione, il programma deve gestire le richieste di connessione su tale socket.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-104">Once the socket is listening for a connection, the program must handle connection requests on that socket.</span></span>

<span data-ttu-id="d3e7c-105">**Per accettare una connessione in un socket**</span><span class="sxs-lookup"><span data-stu-id="d3e7c-105">**To accept a connection on a socket**</span></span>

1.  <span data-ttu-id="d3e7c-106">Creare un oggetto **socket** temporaneo denominato ClientSocket per l'accettazione delle connessioni dai client.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-106">Create a temporary **SOCKET** object called ClientSocket for accepting connections from clients.</span></span>
    ```C++
    
    SOCKET ClientSocket;

    
    ```

    

2.  <span data-ttu-id="d3e7c-107">Normalmente un'applicazione server è progettata per restare in ascolto delle connessioni da più client.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-107">Normally a server application would be designed to listen for connections from multiple clients.</span></span> <span data-ttu-id="d3e7c-108">Per i server a prestazioni elevate, in genere vengono usati più thread per gestire più connessioni client.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-108">For high-performance servers, multiple threads are commonly used to handle the multiple client connections.</span></span>

    <span data-ttu-id="d3e7c-109">Sono disponibili diverse tecniche di programmazione con Winsock che possono essere usate per restare in ascolto di più connessioni client.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-109">There are several different programming techniques using Winsock that can be used to listen for multiple client connections.</span></span> <span data-ttu-id="d3e7c-110">Una tecnica di programmazione consiste nel creare un ciclo continuo che verifica la presenza di richieste di connessione tramite la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) (vedere [ascolto su un socket](listening-on-a-socket.md)).</span><span class="sxs-lookup"><span data-stu-id="d3e7c-110">One programming technique is to create a continuous loop that checks for connection requests using the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function (see [Listening on a Socket](listening-on-a-socket.md)).</span></span> <span data-ttu-id="d3e7c-111">Se si verifica una richiesta di connessione, l'applicazione chiama la funzione [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)o [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) e passa il lavoro a un altro thread per gestire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-111">If a connection request occurs, the application calls the [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), or [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function and passes the work to another thread to handle the request.</span></span> <span data-ttu-id="d3e7c-112">Sono possibili diverse altre tecniche di programmazione.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-112">Several other programming techniques are possible.</span></span>

    <span data-ttu-id="d3e7c-113">Si noti che questo esempio di base è molto semplice e non usa più thread.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-113">Note that this basic example is very simple and does not use multiple threads.</span></span> <span data-ttu-id="d3e7c-114">L'esempio è anche semplicemente in ascolto e accetta solo una singola connessione.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-114">The example also just listens for and accepts only a single connection.</span></span>

    ```C++
    
    ClientSocket = INVALID_SOCKET;

    // Accept a client socket
    ClientSocket = accept(ListenSocket, NULL, NULL);
    if (ClientSocket == INVALID_SOCKET) {
        printf("accept failed: %d\n", WSAGetLastError());
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
     
    
    ```

    

3.  <span data-ttu-id="d3e7c-115">Quando la connessione client è stata accettata, un'applicazione server passa normalmente il socket client accettato (la variabile ClientSocket nel codice di esempio precedente) a un thread di lavoro o a una porta di completamento di I/O e continua ad accettare connessioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-115">When the client connection has been accepted, a server application would normally pass the accepted client socket (the ClientSocket variable in the above sample code) to a worker thread or an I/O completion port and continue accepting additional connections.</span></span> <span data-ttu-id="d3e7c-116">In questo esempio di base, il server continua con il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-116">In this basic example, the server continues to the next step.</span></span>

    <span data-ttu-id="d3e7c-117">Sono disponibili diverse altre tecniche di programmazione che possono essere usate per ascoltare e accettare più connessioni.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-117">There are a number of other programming techniques that can be used to listen for and accept multiple connections.</span></span> <span data-ttu-id="d3e7c-118">Questi includono l'uso delle funzioni [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) o [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) .</span><span class="sxs-lookup"><span data-stu-id="d3e7c-118">These include using the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) or [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions.</span></span> <span data-ttu-id="d3e7c-119">Esempi di alcune di queste diverse tecniche di programmazione sono illustrate negli [esempi di Winsock avanzati](getting-started-with-winsock.md) inclusi in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d3e7c-119">Examples of some of these various programming techniques are illustrated in the [Advanced Winsock Samples](getting-started-with-winsock.md) included with the Microsoft Windows Software Development Kit (SDK).</span></span>

    > [!Note]  
    > <span data-ttu-id="d3e7c-120">Nei sistemi UNIX, una tecnica di programmazione comune per i server era che un'applicazione potesse restare in ascolto delle connessioni.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-120">On Unix systems, a common programming technique for servers was for an application to listen for connections.</span></span> <span data-ttu-id="d3e7c-121">Quando è stata accettata una connessione, il processo padre chiama la funzione **fork** per creare un nuovo processo figlio per gestire la connessione client, ereditando il socket dall'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-121">When a connection was accepted, the parent process would call the **fork** function to create a new child process to handle the client connection, inheriting the socket from the parent.</span></span> <span data-ttu-id="d3e7c-122">Questa tecnica di programmazione non è supportata in Windows, perché la funzione **fork** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-122">This programming technique is not supported on Windows, since the **fork** function is not supported.</span></span> <span data-ttu-id="d3e7c-123">Questa tecnica non è in genere adatta ai server ad alte prestazioni, perché le risorse necessarie per creare un nuovo processo sono molto più grandi di quelle necessarie per un thread.</span><span class="sxs-lookup"><span data-stu-id="d3e7c-123">This technique is also not usually suitable for high-performance servers, since the resources needed to create a new process are much greater than those needed for a thread.</span></span>

     

<span data-ttu-id="d3e7c-124">Passaggio successivo: [ricezione e invio di dati sul server](receiving-and-sending-data-on-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="d3e7c-124">Next Step: [Receiving and Sending Data on the Server](receiving-and-sending-data-on-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3e7c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d3e7c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3e7c-126">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="d3e7c-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="d3e7c-127">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="d3e7c-127">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="d3e7c-128">Ascolto su un socket</span><span class="sxs-lookup"><span data-stu-id="d3e7c-128">Listening on a Socket</span></span>](listening-on-a-socket.md)
</dt> </dl>

 

 
