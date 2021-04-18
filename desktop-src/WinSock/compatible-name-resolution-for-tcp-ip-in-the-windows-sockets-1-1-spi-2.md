---
description: Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi IPv4 con le reti TCP/IP. Queste sono comunemente chiamate funzioni GetXbyY e includono quanto segue.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307015"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="4268f-104">Risoluzione dei nomi compatibile per TCP/IP in Windows Sockets 1,1 SPI</span><span class="sxs-lookup"><span data-stu-id="4268f-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="4268f-105">Windows Sockets 1,1 definisce un numero di routine utilizzate per la risoluzione dei nomi IPv4 con le reti TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="4268f-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="4268f-106">Queste sono comunemente chiamate funzioni **GetXbyY** e includono quanto segue.</span><span class="sxs-lookup"><span data-stu-id="4268f-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="4268f-107">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="4268f-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="4268f-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="4268f-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="4268f-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="4268f-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="4268f-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="4268f-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="4268f-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="4268f-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="4268f-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="4268f-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="4268f-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="4268f-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="4268f-114">Sono state definite anche le versioni asincrone di queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="4268f-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="4268f-115">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="4268f-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="4268f-116">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="4268f-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="4268f-117">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="4268f-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="4268f-118">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="4268f-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="4268f-119">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="4268f-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="4268f-120">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="4268f-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="4268f-121">Queste funzioni sono specifiche delle reti TCP/IP; gli sviluppatori di applicazioni indipendenti dal protocollo sono sconsigliati di continuare a utilizzare queste funzioni specifiche del trasporto.</span><span class="sxs-lookup"><span data-stu-id="4268f-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="4268f-122">Tuttavia, per mantenere rigorosa la compatibilità con le versioni precedenti di Windows Sockets 1,1, le funzioni precedenti continuano a essere supportate purché sia presente almeno un provider dello spazio dei nomi che supporta la \_ famiglia di indirizzi AF inet.</span><span class="sxs-lookup"><span data-stu-id="4268f-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="4268f-123">Il *\_32.dllWS2* implementa queste funzioni di compatibilità in termini di nuove funzionalità di risoluzione dei nomi indipendenti dal protocollo usando una sequenza appropriata di chiamate di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)e [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .</span><span class="sxs-lookup"><span data-stu-id="4268f-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="4268f-124">Di seguito sono riportati i dettagli relativi alla modalità di mapping delle funzioni **GetXbyY** alle funzioni di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="4268f-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="4268f-125">Il \_32.dll WS2 gestisce le differenze tra le versioni asincrone e sincrone delle funzioni **GetXbyY** , in modo che venga discussa solo l'implementazione delle funzioni **GetXbyY** sincrone.</span><span class="sxs-lookup"><span data-stu-id="4268f-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
