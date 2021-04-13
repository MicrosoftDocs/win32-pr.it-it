---
description: "\\_Per verificare l'esito negativo della funzione, viene fornito l'errore di socket costante manifesto. Sebbene l'utilizzo di questa costante non sia obbligatorio, è consigliabile. Nell'esempio seguente viene illustrato l'utilizzo della costante di \\_ errore socket."
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Valori restituiti sull'errore della funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226841"
---
# <a name="return-values-on-function-failure"></a><span data-ttu-id="c45f0-105">Valori restituiti sull'errore della funzione</span><span class="sxs-lookup"><span data-stu-id="c45f0-105">Return Values on Function Failure</span></span>

<span data-ttu-id="c45f0-106">Per verificare l'esito negativo della funzione, viene fornito l' **\_ errore di socket** costante manifesto.</span><span class="sxs-lookup"><span data-stu-id="c45f0-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="c45f0-107">Sebbene l'utilizzo di questa costante non sia obbligatorio, è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="c45f0-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="c45f0-108">Nell'esempio seguente viene illustrato l'utilizzo della costante **di \_ errore socket** .</span><span class="sxs-lookup"><span data-stu-id="c45f0-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="c45f0-109">Stile BSD tipico (non funziona in Windows)</span><span class="sxs-lookup"><span data-stu-id="c45f0-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="c45f0-110">Stile di Windows</span><span class="sxs-lookup"><span data-stu-id="c45f0-110">Windows Style</span></span>


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a><span data-ttu-id="c45f0-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c45f0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c45f0-112">Codici di errore-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="c45f0-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="c45f0-113">Gestione degli errori Winsock</span><span class="sxs-lookup"><span data-stu-id="c45f0-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="c45f0-114">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="c45f0-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c45f0-115">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="c45f0-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="c45f0-116">Codici di errore di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="c45f0-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



