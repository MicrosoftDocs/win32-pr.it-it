---
description: Questa sezione descrive la programmazione multicast basata sullo stato finale usando IOCTLs anziché le opzioni socket. Per una panoramica del modo in cui la programmazione multicast basata sullo stato finale è diversa dalla programmazione multicast basata sulle modifiche, vedere programmazione multicast.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programmazione multicast basata sullo stato finale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306983"
---
# <a name="final-state-based-multicast-programming"></a><span data-ttu-id="f3fd2-104">Programmazione multicast basata sullo stato finale</span><span class="sxs-lookup"><span data-stu-id="f3fd2-104">Final-State-Based Multicast Programming</span></span>

<span data-ttu-id="f3fd2-105">Questa sezione descrive la programmazione multicast basata sullo stato finale usando IOCTLs anziché le opzioni socket.</span><span class="sxs-lookup"><span data-stu-id="f3fd2-105">This section describes final-state-based multicast programming using IOCTLs instead of socket options.</span></span> <span data-ttu-id="f3fd2-106">Per una panoramica del modo in cui la programmazione multicast basata sullo stato finale è diversa dalla programmazione multicast basata sulle modifiche, vedere [programmazione multicast](multicast-programming.md).</span><span class="sxs-lookup"><span data-stu-id="f3fd2-106">For an overview of how final-state-based multicast programming differs from change-based multicast programming, see [Multicast Programming](multicast-programming.md).</span></span>

<span data-ttu-id="f3fd2-107">La tabella seguente descrive i IOCTL Windows Sockets usati per la programmazione multicast in Windows.</span><span class="sxs-lookup"><span data-stu-id="f3fd2-107">The following table describes the Windows Sockets IOCTLs used for multicast programming on Windows.</span></span> 

| <span data-ttu-id="f3fd2-108">IOCTL</span><span class="sxs-lookup"><span data-stu-id="f3fd2-108">IOCTL</span></span>                       | <span data-ttu-id="f3fd2-109">Tipo di argomento</span><span class="sxs-lookup"><span data-stu-id="f3fd2-109">Argument type</span></span>                                   |
|-----------------------------|-------------------------------------------------|
| <span data-ttu-id="f3fd2-110">SIOCSMSFILTER</span><span class="sxs-lookup"><span data-stu-id="f3fd2-110">SIOCSMSFILTER</span></span>               | <span data-ttu-id="f3fd2-111">[**Gruppo \_ di Struttura filtro**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter)</span><span class="sxs-lookup"><span data-stu-id="f3fd2-111">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="f3fd2-112">SIOCGMSFILTER</span><span class="sxs-lookup"><span data-stu-id="f3fd2-112">SIOCGMSFILTER</span></span>               | <span data-ttu-id="f3fd2-113">[**Gruppo \_ di Struttura filtro**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter)</span><span class="sxs-lookup"><span data-stu-id="f3fd2-113">[**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) structure</span></span> |
| <span data-ttu-id="f3fd2-114">\_ \_ filtro multicast sio \_ Get</span><span class="sxs-lookup"><span data-stu-id="f3fd2-114">SIO\_GET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="f3fd2-115">[**struttura \_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="f3fd2-115">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |
| <span data-ttu-id="f3fd2-116">\_ \_ filtro multicast set \_ sio</span><span class="sxs-lookup"><span data-stu-id="f3fd2-116">SIO\_SET\_MULTICAST\_FILTER</span></span> | <span data-ttu-id="f3fd2-117">[**struttura \_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)</span><span class="sxs-lookup"><span data-stu-id="f3fd2-117">[**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) structure</span></span>   |



 

<span data-ttu-id="f3fd2-118">Si noti che le IOCTL **SIOCSMSFILTER** e **SIOCGMSFILTER** sono disponibili in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f3fd2-118">Note that the **SIOCSMSFILTER** and **SIOCGMSFILTER** IOCTLS are available on Windows Vista and later.</span></span>

<span data-ttu-id="f3fd2-119">L'uso di questi IOCTL per la programmazione multicast offre vantaggi in merito alle prestazioni quando si utilizzano elenchi di origine di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="f3fd2-119">Using these IOCTLs for multicast programming has performance benefits when working with large source lists.</span></span> <span data-ttu-id="f3fd2-120">Per altre informazioni sui parametri e le impostazioni associati all'uso di SIO \_ get \_ multicast \_ Filter o SIO \_ set \_ multicast \_ Filter, vedere la pagina di riferimento del [**\_ filtro di gruppo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) .</span><span class="sxs-lookup"><span data-stu-id="f3fd2-120">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**GROUP\_FILTER**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) reference page.</span></span> <span data-ttu-id="f3fd2-121">Per altre informazioni sui parametri e le impostazioni associati all'uso di SIO \_ get \_ multicast \_ Filter o SIO \_ set \_ multicast \_ Filter, vedere la pagina di riferimento [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) .</span><span class="sxs-lookup"><span data-stu-id="f3fd2-121">For more information about the parameters and settings associated with using SIO\_GET\_MULTICAST\_FILTER or SIO\_SET\_MULTICAST\_FILTER, consult the [**ip\_msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) reference page.</span></span>

 

 



