---
title: Routing
description: Le API di routing rendono possibile la creazione di applicazioni per amministrare le funzionalità di routing del sistema operativo.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Routing RAS
- RAS di routing, pagina iniziale
- RAS RRAS
- RAS RRAS, vedere Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872897"
---
# <a name="routing"></a><span data-ttu-id="9a0f7-107">Routing</span><span class="sxs-lookup"><span data-stu-id="9a0f7-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="9a0f7-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="9a0f7-108">Purpose</span></span>

<span data-ttu-id="9a0f7-109">Le API di routing rendono possibile la creazione di applicazioni per amministrare le funzionalità di routing del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9a0f7-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="9a0f7-110">Where applicable</span></span>

<span data-ttu-id="9a0f7-111">Il routing consente a un computer di funzionare come un router di rete.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9a0f7-112">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="9a0f7-112">Developer audience</span></span>

<span data-ttu-id="9a0f7-113">Le API di routing sono progettate per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="9a0f7-114">I programmatori devono inoltre acquisire familiarità con i concetti relativi alla rete.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9a0f7-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="9a0f7-115">Run-time requirements</span></span>

<span data-ttu-id="9a0f7-116">Il routing è una tecnologia basata su server.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-116">Routing is a server-based technology.</span></span> <span data-ttu-id="9a0f7-117">Tutte le funzionalità di routing sono incorporate in Windows 2000 Server e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="9a0f7-118">Le applicazioni di routing non possono essere eseguite su workstation Windows NT 4,0 o sui sistemi operativi client, ad esempio Windows 95.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="9a0f7-119">Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9a0f7-120">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9a0f7-120">In this section</span></span>



| <span data-ttu-id="9a0f7-121">Argomento</span><span class="sxs-lookup"><span data-stu-id="9a0f7-121">Topic</span></span>                                                                                               | <span data-ttu-id="9a0f7-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a0f7-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a0f7-123">Gestione router</span><span class="sxs-lookup"><span data-stu-id="9a0f7-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="9a0f7-124">L'API di amministrazione del router consente agli sviluppatori di creare applicazioni per gestire il servizio router in un computer che esegue Windows 2000 Server e sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="9a0f7-125">Gestione router e informazioni di base sulla gestione</span><span class="sxs-lookup"><span data-stu-id="9a0f7-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="9a0f7-126">Le API MIB (Management Information Base) per la gestione dei router consentono di eseguire query e impostare i valori delle variabili MIB esportate da uno dei gestori router o da uno dei protocolli di routing del servizio.</span><span class="sxs-lookup"><span data-stu-id="9a0f7-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="9a0f7-127">Utilizzando questa API, il router supporta il Simple Network Management Protocol (SNMP).</span><span class="sxs-lookup"><span data-stu-id="9a0f7-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9a0f7-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a0f7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a0f7-129">Funzioni dell'helper IP</span><span class="sxs-lookup"><span data-stu-id="9a0f7-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="9a0f7-130">Accesso remoto</span><span class="sxs-lookup"><span data-stu-id="9a0f7-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="9a0f7-131">Protocolli di routing</span><span class="sxs-lookup"><span data-stu-id="9a0f7-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

