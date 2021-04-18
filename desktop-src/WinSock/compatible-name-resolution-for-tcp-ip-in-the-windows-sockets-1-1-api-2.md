---
description: Si noti che tutte le funzioni di Windows Sockets 1,1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307017"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="fa179-103">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="fa179-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="fa179-104">Tutte le funzioni di Windows Sockets 1,1 per la risoluzione dei nomi sono specifiche delle reti TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="fa179-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="fa179-105">Gli sviluppatori di applicazioni sono fortemente sconsigliati di continuare a utilizzare queste funzioni specifiche del trasporto che supportano solo IPv4.</span><span class="sxs-lookup"><span data-stu-id="fa179-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="fa179-106">Gli sviluppatori di applicazioni devono usare le funzioni seguenti che sono indipendenti dal protocollo e supportano sia la risoluzione dei nomi IPv6 che quella IPv4.</span><span class="sxs-lookup"><span data-stu-id="fa179-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="fa179-107">**funzione getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="fa179-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="fa179-108">**GetAddrInfoEx**</span><span class="sxs-lookup"><span data-stu-id="fa179-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="fa179-109">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="fa179-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="fa179-110">**GetNameInfo**</span><span class="sxs-lookup"><span data-stu-id="fa179-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="fa179-111">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="fa179-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="fa179-112">Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi con reti TCP/IP (IP versione 4).</span><span class="sxs-lookup"><span data-stu-id="fa179-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="fa179-113">Queste sono talvolta chiamate funzioni **getXbyY** e includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="fa179-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="fa179-114">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="fa179-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="fa179-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="fa179-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="fa179-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="fa179-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="fa179-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="fa179-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="fa179-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="fa179-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="fa179-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="fa179-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="fa179-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="fa179-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="fa179-121">Sono state definite anche le versioni asincrone di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="fa179-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="fa179-122">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="fa179-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="fa179-123">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="fa179-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="fa179-124">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="fa179-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="fa179-125">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="fa179-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="fa179-126">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="fa179-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="fa179-127">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="fa179-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="fa179-128">Sono inoltre disponibili due funzioni, ora implementate nella Winsock2.dll, utilizzate per convertire rispettivamente la notazione degli indirizzi IPv4 punteggiata da e verso le rappresentazioni binarie e di stringa.</span><span class="sxs-lookup"><span data-stu-id="fa179-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="fa179-129">**\_indirizzo inet**</span><span class="sxs-lookup"><span data-stu-id="fa179-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="fa179-130">**\_NTOA inet**</span><span class="sxs-lookup"><span data-stu-id="fa179-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="fa179-131">Per mantenere rigorosa la compatibilità con le versioni precedenti di Windows Sockets 1,1, tutte le funzioni solo IPv4 precedenti continuano a essere supportate purché sia presente almeno un provider dello spazio dei nomi che supporta la \_ famiglia di indirizzi AF inet (queste funzioni non sono rilevanti per IP versione 6, indicata da AF \_ INET6).</span><span class="sxs-lookup"><span data-stu-id="fa179-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="fa179-132">Il \_32.dll WS2 implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **end** .</span><span class="sxs-lookup"><span data-stu-id="fa179-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="fa179-133">Di seguito sono riportati i dettagli relativi alla modalità di mapping delle funzioni **getXbyY** alle funzioni di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="fa179-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="fa179-134">WSs2 \_32.dll gestisce le differenze tra le versioni asincrone e sincrone delle funzioni **getXbyY** , in modo che venga discussa solo l'implementazione delle funzioni **getXbyY** sincrone.</span><span class="sxs-lookup"><span data-stu-id="fa179-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="fa179-135">In questa sezione viene descritta la risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="fa179-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="fa179-136">Nell'elenco seguente vengono descritti gli argomenti di questa sezione:</span><span class="sxs-lookup"><span data-stu-id="fa179-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="fa179-137">Approccio di base per GetXbyY nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="fa179-138">Funzioni getprotobyname e getprotobynumber nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="fa179-139">Funzioni getservbyname e getservbyport nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="fa179-140">Funzione gethostbyname nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="fa179-141">Funzione gethostbyaddr nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="fa179-142">Funzione GetHostName nell'API</span><span class="sxs-lookup"><span data-stu-id="fa179-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="fa179-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa179-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa179-144">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="fa179-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="fa179-145">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa179-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
