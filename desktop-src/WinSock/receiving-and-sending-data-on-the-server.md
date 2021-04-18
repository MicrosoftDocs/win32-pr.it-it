---
description: Nel codice seguente vengono illustrate le funzioni ricezione e Send utilizzate dal server.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Ricezione e invio di dati sul server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310455"
---
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="a5b93-103">Ricezione e invio di dati sul server</span><span class="sxs-lookup"><span data-stu-id="a5b93-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="a5b93-104">Nel codice seguente vengono illustrate le funzioni [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) e [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) utilizzate dal server.</span><span class="sxs-lookup"><span data-stu-id="a5b93-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="a5b93-105">Per ricevere e inviare dati in un socket</span><span class="sxs-lookup"><span data-stu-id="a5b93-105">To receive and send data on a socket</span></span>


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



<span data-ttu-id="a5b93-106">Le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono entrambi un valore integer del numero di byte inviati o ricevuti, rispettivamente, o un errore.</span><span class="sxs-lookup"><span data-stu-id="a5b93-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="a5b93-107">Ogni funzione accetta anche gli stessi parametri, ovvero il socket attivo, un buffer **char** , il numero di byte da inviare o ricevere ed eventuali flag da usare.</span><span class="sxs-lookup"><span data-stu-id="a5b93-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="a5b93-108">Passaggio successivo: [disconnessione del server](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="a5b93-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5b93-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5b93-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5b93-110">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="a5b93-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="a5b93-111">Applicazione server Winsock</span><span class="sxs-lookup"><span data-stu-id="a5b93-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="a5b93-112">Accettazione di una connessione</span><span class="sxs-lookup"><span data-stu-id="a5b93-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



