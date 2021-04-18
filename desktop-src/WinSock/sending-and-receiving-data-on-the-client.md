---
description: Nel codice seguente vengono illustrate le funzioni send e ricezione utilizzate dal client dopo che è stata stabilita una connessione.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Invio e ricezione di dati sul client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315791"
---
# <a name="sending-and-receiving-data-on-the-client"></a><span data-ttu-id="0c31d-103">Invio e ricezione di dati sul client</span><span class="sxs-lookup"><span data-stu-id="0c31d-103">Sending and Receiving Data on the Client</span></span>

<span data-ttu-id="0c31d-104">Nel codice seguente vengono illustrate le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) utilizzate dal client dopo che è stata stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="0c31d-104">The following code demonstrates the [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions used by the client once a connection is established.</span></span>

## <a name="client"></a><span data-ttu-id="0c31d-105">Client</span><span class="sxs-lookup"><span data-stu-id="0c31d-105">Client</span></span>


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



<span data-ttu-id="0c31d-106">Le funzioni [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono entrambi un valore integer del numero di byte inviati o ricevuti, rispettivamente, o un errore.</span><span class="sxs-lookup"><span data-stu-id="0c31d-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="0c31d-107">Ogni funzione accetta anche gli stessi parametri, ovvero il socket attivo, un buffer **char** , il numero di byte da inviare o ricevere ed eventuali flag da usare.</span><span class="sxs-lookup"><span data-stu-id="0c31d-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="0c31d-108">Passaggio successivo: [disconnessione del client](disconnecting-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="0c31d-108">Next Step: [Disconnecting the Client](disconnecting-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c31d-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c31d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c31d-110">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="0c31d-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="0c31d-111">Applicazione client Winsock</span><span class="sxs-lookup"><span data-stu-id="0c31d-111">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="0c31d-112">Connessione a un socket</span><span class="sxs-lookup"><span data-stu-id="0c31d-112">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
</dt> </dl>

 

 



