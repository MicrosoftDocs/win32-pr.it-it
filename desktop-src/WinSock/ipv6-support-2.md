---
description: Supporto IPv6, allegati TCP/IP e Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Supporto IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129167"
---
# <a name="ipv6-support"></a><span data-ttu-id="41164-103">Supporto IPv6</span><span class="sxs-lookup"><span data-stu-id="41164-103">IPv6 Support</span></span>

<span data-ttu-id="41164-104">Per supportare sia IPv4 che IPv6 in Windows XP con Service Pack 1 (SP1) e in Windows Server 2003, un'applicazione deve creare due socket, un socket da usare con IPv4 e un socket per l'uso con IPv6.</span><span class="sxs-lookup"><span data-stu-id="41164-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="41164-105">Questi due socket devono essere gestiti separatamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41164-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="41164-106">Se un provider di servizi TCP/IP in Windows XP con SP1 e in Windows Server 2003 supporta l'indirizzamento IPv4 e IPv6, deve creare due socket distinti e restare in ascolto separatamente su questi socket:</span><span class="sxs-lookup"><span data-stu-id="41164-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="41164-107">Una volta per IPv4.</span><span class="sxs-lookup"><span data-stu-id="41164-107">Once for IPv4.</span></span>
-   <span data-ttu-id="41164-108">Una volta per la famiglia di indirizzi IPv6.</span><span class="sxs-lookup"><span data-stu-id="41164-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="41164-109">Windows Vista e versioni successive offrono la possibilità di creare un singolo socket IPv6 che può gestire sia il traffico IPv6 che quello IPv4.</span><span class="sxs-lookup"><span data-stu-id="41164-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="41164-110">Ad esempio, viene creato un socket di ascolto TCP per IPv6, inserito in modalità dual stack e associato alla porta 5001.</span><span class="sxs-lookup"><span data-stu-id="41164-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="41164-111">Questo socket a doppio stack può accettare connessioni da client TCP IPv6 che si connettono alla porta 5001 e dai client TCP IPv4 che si connettono alla porta 5001.</span><span class="sxs-lookup"><span data-stu-id="41164-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="41164-112">Questa funzionalità consente di semplificare notevolmente la progettazione delle applicazioni e riduce il sovraccarico delle risorse richiesto per l'invio di operazioni su due socket distinti.</span><span class="sxs-lookup"><span data-stu-id="41164-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="41164-113">Tuttavia, esistono alcune restrizioni che devono essere soddisfatte per poter utilizzare un socket a doppio stack.</span><span class="sxs-lookup"><span data-stu-id="41164-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="41164-114">Per altre informazioni, vedere [socket a doppio stack](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="41164-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="41164-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) restituisce due strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per ognuno dei tipi di socket supportati (Sock \_ Stream, Sock \_ DGRAM, Sock \_ RAW).</span><span class="sxs-lookup"><span data-stu-id="41164-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="41164-116">**IAddressFamily** deve essere impostato su AF \_ inet per l'indirizzamento IPv4 e su AF \_ INET6 per l'indirizzamento IPv6.</span><span class="sxs-lookup"><span data-stu-id="41164-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="41164-117">Gli indirizzi IPv6 sono descritti nelle seguenti strutture.</span><span class="sxs-lookup"><span data-stu-id="41164-117">The IPv6 addresses are described in the following structures.</span></span>

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

<span data-ttu-id="41164-118">Se un'applicazione usa le funzioni di Windows Sockets 1,1 e vuole usare gli indirizzi IPv6, può continuare a usare tutte le funzioni precedenti che accettano la struttura [**sockaddr**](sockaddr-2.md) come uno dei parametri ([**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto), [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)e così via).</span><span class="sxs-lookup"><span data-stu-id="41164-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="41164-119">L'unica modifica necessaria consiste nell'usare **sockaddr \_ IN6** anziché **sockaddr \_ in**.</span><span class="sxs-lookup"><span data-stu-id="41164-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="41164-120">Tuttavia, le funzioni di risoluzione dei nomi ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)e così via) e le funzioni di conversione degli indirizzi ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) non possono essere riutilizzate perché presuppongono che un indirizzo IP sia lungo 4 byte.</span><span class="sxs-lookup"><span data-stu-id="41164-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="41164-121">Un'applicazione che vuole eseguire la risoluzione dei nomi e la conversione degli indirizzi per gli indirizzi IPv6 deve usare funzioni specifiche di Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="41164-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="41164-122">Sono state introdotte molte nuove funzioni per consentire alle applicazioni Windows Sockets 2 di sfruttare i vantaggi di IPv6, incluse le funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="41164-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="41164-123">Per ulteriori informazioni su come abilitare le funzionalità IPv6 in un'applicazione, vedere la [Guida IPv6 per le applicazioni Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="41164-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
