---
description: Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e la porta per le richieste di connessione in ingresso.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Ascolto su un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306935"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="02dba-103">Ascolto su un socket</span><span class="sxs-lookup"><span data-stu-id="02dba-103">Listening on a Socket</span></span>

<span data-ttu-id="02dba-104">Dopo che il socket è stato associato a un indirizzo IP e a una porta nel sistema, il server deve quindi restare in ascolto su tale indirizzo IP e la porta per le richieste di connessione in ingresso.</span><span class="sxs-lookup"><span data-stu-id="02dba-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="02dba-105">Per restare in attesa su un socket</span><span class="sxs-lookup"><span data-stu-id="02dba-105">To listen on a socket</span></span>

<span data-ttu-id="02dba-106">Chiamare la funzione [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , passando come parametri il socket creato e un valore per il *backlog*, la lunghezza massima della coda di connessioni in sospeso da accettare.</span><span class="sxs-lookup"><span data-stu-id="02dba-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="02dba-107">In questo esempio il parametro *backlog* è stato impostato su **SOMAXCONN**.</span><span class="sxs-lookup"><span data-stu-id="02dba-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="02dba-108">Questo valore è una costante speciale che indica al provider Winsock per questo socket di consentire un numero massimo ragionevole di connessioni in sospeso nella coda.</span><span class="sxs-lookup"><span data-stu-id="02dba-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="02dba-109">Controllare il valore restituito per gli errori generali.</span><span class="sxs-lookup"><span data-stu-id="02dba-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="02dba-110">Passaggio successivo: [accettazione di una connessione](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="02dba-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="02dba-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02dba-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02dba-112">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="02dba-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="02dba-113">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="02dba-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="02dba-114">Associazione di un socket</span><span class="sxs-lookup"><span data-stu-id="02dba-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



