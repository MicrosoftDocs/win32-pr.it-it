---
description: Per comunicare in rete, un client deve connettersi a un server.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Connessione a un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307010"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="c14af-103">Connessione a un socket</span><span class="sxs-lookup"><span data-stu-id="c14af-103">Connecting to a Socket</span></span>

<span data-ttu-id="c14af-104">Per comunicare in rete, un client deve connettersi a un server.</span><span class="sxs-lookup"><span data-stu-id="c14af-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="c14af-105">Per connettersi a un socket</span><span class="sxs-lookup"><span data-stu-id="c14af-105">To connect to a socket</span></span>

<span data-ttu-id="c14af-106">Chiamare la funzione [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , passando il socket creato e la struttura [**sockaddr**](sockaddr-2.md) come parametri.</span><span class="sxs-lookup"><span data-stu-id="c14af-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="c14af-107">Verificare la presenza di errori generali.</span><span class="sxs-lookup"><span data-stu-id="c14af-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="c14af-108">La funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) viene usata per determinare i valori nella struttura [**sockaddr**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c14af-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="c14af-109">In questo esempio, il primo indirizzo IP restituito dalla funzione **funzione getaddrinfo** viene usato per specificare la struttura **sockaddr** passata alla [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span><span class="sxs-lookup"><span data-stu-id="c14af-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="c14af-110">Se la chiamata di **connessione** non riesce al primo indirizzo IP, provare la struttura [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) successiva nell'elenco collegato restituito dalla funzione **funzione getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="c14af-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="c14af-111">Le informazioni specificate nella struttura [**sockaddr**](sockaddr-2.md) includono:</span><span class="sxs-lookup"><span data-stu-id="c14af-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="c14af-112">Indirizzo IP del server a cui il client tenterà di connettersi.</span><span class="sxs-lookup"><span data-stu-id="c14af-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="c14af-113">numero di porta nel server a cui si connetterà il client.</span><span class="sxs-lookup"><span data-stu-id="c14af-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="c14af-114">Questa porta è stata specificata come porta 27015 quando il client ha chiamato la funzione [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="c14af-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="c14af-115">Passaggio successivo: [invio e ricezione di dati sul client](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="c14af-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c14af-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c14af-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c14af-117">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="c14af-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="c14af-118">Applicazione client Winsock</span><span class="sxs-lookup"><span data-stu-id="c14af-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="c14af-119">Creazione di un socket per il client</span><span class="sxs-lookup"><span data-stu-id="c14af-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
