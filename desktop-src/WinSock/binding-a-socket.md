---
description: Affinché un server accetti le connessioni client, è necessario che sia associato a un indirizzo di rete all'interno del sistema.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Associazione di un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307046"
---
# <a name="binding-a-socket"></a><span data-ttu-id="4c4f3-103">Associazione di un socket</span><span class="sxs-lookup"><span data-stu-id="4c4f3-103">Binding a Socket</span></span>

<span data-ttu-id="4c4f3-104">Affinché un server accetti le connessioni client, è necessario che sia associato a un indirizzo di rete all'interno del sistema.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="4c4f3-105">Il codice seguente illustra come associare un socket che è già stato creato a un indirizzo IP e a una porta.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="4c4f3-106">Le applicazioni client utilizzano l'indirizzo IP e la porta per connettersi alla rete host.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="4c4f3-107">Per associare un socket</span><span class="sxs-lookup"><span data-stu-id="4c4f3-107">To bind a socket</span></span>

<span data-ttu-id="4c4f3-108">La struttura [**sockaddr**](sockaddr-2.md) include informazioni relative alla famiglia di indirizzi, all'indirizzo IP e al numero di porta.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="4c4f3-109">Chiamare la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , passando la struttura **socket** e [**sockaddr**](sockaddr-2.md) creata restituita dalla funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) come parametri.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="4c4f3-110">Verificare la presenza di errori generali.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="4c4f3-111">Una volta chiamata la funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , le informazioni sull'indirizzo restituite dalla funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="4c4f3-112">La funzione [**FreeAddrInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) viene chiamata per liberare la memoria allocata dalla funzione **funzione getaddrinfo** per le informazioni sull'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="4c4f3-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="4c4f3-113">Passaggio successivo: [ascolto su un socket](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="4c4f3-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c4f3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c4f3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c4f3-115">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="4c4f3-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="4c4f3-116">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="4c4f3-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="4c4f3-117">Creazione di un socket per il server</span><span class="sxs-lookup"><span data-stu-id="4c4f3-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



