---
description: Pagina di navigazione per le opzioni del socket Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Opzioni socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306897"
---
# <a name="socket-options"></a><span data-ttu-id="a9fc9-103">Opzioni socket</span><span class="sxs-lookup"><span data-stu-id="a9fc9-103">Socket Options</span></span>

<span data-ttu-id="a9fc9-104">In questa sezione vengono descritte le opzioni del socket Winsock per varie edizioni dei sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-104">This section describes Winsock Socket Options for various editions of Windows operating systems.</span></span> <span data-ttu-id="a9fc9-105">Per ottenere e impostare le opzioni del socket, usare le funzioni [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .</span><span class="sxs-lookup"><span data-stu-id="a9fc9-105">Use the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) functions for more getting and setting socket options.</span></span> <span data-ttu-id="a9fc9-106">Per enumerare i protocolli e individuare le proprietà supportate per ogni protocollo installato, utilizzare la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="a9fc9-106">To enumerate protocols and discover supported properties for each installed protocol, use the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

<span data-ttu-id="a9fc9-107">Alcune opzioni del socket richiedono una spiegazione più che queste tabelle possono comportare; tali opzioni contengono collegamenti ad altre pagine.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-107">Some socket options require more explanation than these tables can convey; such options contain links to additional pages.</span></span>

<dl> <dt>

<span data-ttu-id="a9fc9-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**\_IP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-108"><span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO\_IP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-109">Opzioni del socket applicabili a livello di IPv4.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-109">Socket options applicable at the IPv4 level.</span></span> <span data-ttu-id="a9fc9-110">Per altre informazioni, vedere le [**\_ Opzioni del socket IP di IPPROTO**](ipproto-ip-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-110">For more information, see the [**IPPROTO\_IP Socket Options**](ipproto-ip-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-111"><span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**IPPROTO\_IPV6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-112">Opzioni del socket applicabili a livello di IPv6.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-112">Socket options applicable at the IPv6 level.</span></span> <span data-ttu-id="a9fc9-113">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPv6 di IPPROTO**](ipproto-ipv6-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-113">For more information, see the [**IPPROTO\_IPV6 Socket Options**](ipproto-ipv6-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-114"><span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO\_RM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-115">Opzioni del socket applicabili a livello di multicast affidabile.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-115">Socket options applicable at the reliable multicast level.</span></span> <span data-ttu-id="a9fc9-116">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPPROTO RM**](ipproto-rm-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-116">For more information, see the [**IPPROTO\_RM Socket Options**](ipproto-rm-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**\_TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-117"><span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO\_TCP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-118">Opzioni socket applicabili a livello TCP.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-118">Socket options applicable at the TCP level.</span></span> <span data-ttu-id="a9fc9-119">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket TCP IPPROTO**](ipproto-tcp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-119">For more information, see the [**IPPROTO\_TCP Socket Options**](ipproto-tcp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**\_UDP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-120"><span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**IPPROTO\_UDP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-121">Opzioni del socket applicabili a livello di UDP.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-121">Socket options applicable at the UDP level.</span></span> <span data-ttu-id="a9fc9-122">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket UDP di IPPROTO**](ipproto-udp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-122">For more information, see the [**IPPROTO\_UDP Socket Options**](ipproto-udp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-123"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**NSPROTO\_IPX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-124">Opzioni del socket applicabili a livello di IPX.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-124">Socket options applicable at the IPX level.</span></span> <span data-ttu-id="a9fc9-125">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket IPX di NSPROTO**](nsproto-ipx-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-125">For more information, see the [**NSPROTO\_IPX Socket Options**](nsproto-ipx-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOLENOIDE \_ AppleTalk**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-126"><span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**SOL\_APPLETALK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-127">Opzioni del socket applicabili a livello di AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-127">Socket options applicable at the AppleTalk level.</span></span> <span data-ttu-id="a9fc9-128">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket**](sol-appletalk-socket-options.md)per la tecnologia solenoide.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-128">For more information, see the [**SOL\_APPLETALK Socket Options**](sol-appletalk-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL \_ IRLMP**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-129"><span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**SOL\_IRLMP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-130">Opzioni del socket applicabili al livello del protocollo di gestione dei collegamenti a infrarossi.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-130">Socket options applicable at the InfraRed Link Management Protocol level.</span></span> <span data-ttu-id="a9fc9-131">Per altre informazioni, vedere le [**\_ Opzioni del socket Sol IRLMP**](sol-irlmp-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-131">For more information, see the [**SOL\_IRLMP Socket Options**](sol-irlmp-socket-options.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9fc9-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_socket Sol**</span><span class="sxs-lookup"><span data-stu-id="a9fc9-132"><span id="SOL_SOCKET"></span><span id="sol_socket"></span>**SOL\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a9fc9-133">Opzioni socket applicabili a livello di socket.</span><span class="sxs-lookup"><span data-stu-id="a9fc9-133">Socket options applicable at the socket level.</span></span> <span data-ttu-id="a9fc9-134">Per ulteriori informazioni, vedere le [**\_ Opzioni del socket di socket Sol**](sol-socket-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-134">For more information, see the [**SOL\_SOCKET Socket Options**](sol-socket-socket-options.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9fc9-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9fc9-135">Remarks</span></span>

<span data-ttu-id="a9fc9-136">Tutte le \_ \* Opzioni del socket sono valide anche per IPv4 e IPv6 (ad eccezione di \_ broadcast, perché broadcast non è implementato in IPv6).</span><span class="sxs-lookup"><span data-stu-id="a9fc9-136">All SO\_\* socket options apply equally to IPv4 and IPv6 (except SO\_BROADCAST, since broadcast is not implemented in IPv6).</span></span>

 

 



