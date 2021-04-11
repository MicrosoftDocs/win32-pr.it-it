---
description: Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto SOCKET per l'utilizzo da parte del server.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Creazione di un socket per il server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129206"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="f0414-103">Creazione di un socket per il server</span><span class="sxs-lookup"><span data-stu-id="f0414-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="f0414-104">Dopo l'inizializzazione, è necessario creare un'istanza di un oggetto **socket** per l'utilizzo da parte del server.</span><span class="sxs-lookup"><span data-stu-id="f0414-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="f0414-105">**Per creare un socket per il server**</span><span class="sxs-lookup"><span data-stu-id="f0414-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="f0414-106">La funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) viene usata per determinare i valori nella struttura [**sockaddr**](sockaddr-2.md) :</span><span class="sxs-lookup"><span data-stu-id="f0414-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="f0414-107">**AF \_ INET** viene usato per specificare la famiglia di indirizzi IPv4.</span><span class="sxs-lookup"><span data-stu-id="f0414-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="f0414-108">**Calzino \_ Il flusso** viene usato per specificare un socket di flusso.</span><span class="sxs-lookup"><span data-stu-id="f0414-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="f0414-109">**IPPROTO \_ TCP** viene utilizzato per specificare il protocollo TCP.</span><span class="sxs-lookup"><span data-stu-id="f0414-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="f0414-110">**Intelligenza artificiale \_ Il flag PASSIvo** indica che il chiamante intende utilizzare la struttura di indirizzi socket restituita in una chiamata alla funzione di [**associazione**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="f0414-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="f0414-111">Quando il flag **ai \_ passivi** è impostato e il parametro *NodeName* per la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) è un puntatore **null** , la parte dell'indirizzo IP della struttura di indirizzi del socket è impostata su **inaddr \_ any** per gli indirizzi IPv4 o **IN6ADDR \_ Any \_ init** per gli indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="f0414-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="f0414-112">27015 è il numero di porta associato al server a cui si connetterà il client.</span><span class="sxs-lookup"><span data-stu-id="f0414-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="f0414-113">La struttura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) viene utilizzata dalla funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="f0414-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="f0414-114">Creare un oggetto **socket** denominato ListenSocket per il server per l'ascolto delle connessioni client.</span><span class="sxs-lookup"><span data-stu-id="f0414-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="f0414-115">Chiamare la funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e restituire il relativo valore alla variabile ListenSocket.</span><span class="sxs-lookup"><span data-stu-id="f0414-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="f0414-116">Per questa applicazione server, usare il primo indirizzo IP restituito dalla chiamata a [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) che corrisponde alla famiglia di indirizzi, al tipo di socket e al protocollo specificati nel parametro *hints* .</span><span class="sxs-lookup"><span data-stu-id="f0414-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="f0414-117">In questo esempio è stato richiesto un socket del flusso TCP per IPv4 con una famiglia di indirizzi IPv4, un tipo di socket del \_ flusso Sock e un protocollo di IPPROTO \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="f0414-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="f0414-118">Per ListenSocket è quindi richiesto un indirizzo IPv4.</span><span class="sxs-lookup"><span data-stu-id="f0414-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="f0414-119">Se l'applicazione server vuole restare in ascolto su IPv6, la famiglia di indirizzi deve essere impostata su AF \_ INET6 nel parametro *hints* .</span><span class="sxs-lookup"><span data-stu-id="f0414-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="f0414-120">Se un server vuole restare in ascolto su IPv6 e IPv4, è necessario creare due socket di ascolto, uno per IPv6 e uno per IPv4.</span><span class="sxs-lookup"><span data-stu-id="f0414-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="f0414-121">Questi due socket devono essere gestiti separatamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0414-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="f0414-122">Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 inserito in modalità dual stack per l'ascolto su IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="f0414-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="f0414-123">Per altre informazioni su questa funzionalità, vedere [socket a doppio stack](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="f0414-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="f0414-124">Verificare la presenza di errori per verificare che il socket sia un socket valido.</span><span class="sxs-lookup"><span data-stu-id="f0414-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="f0414-125">Passaggio successivo: [associazione di un socket](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="f0414-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0414-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0414-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0414-127">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="f0414-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="f0414-128">Inizializzazione di Winsock</span><span class="sxs-lookup"><span data-stu-id="f0414-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="f0414-129">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="f0414-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
