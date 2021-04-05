---
title: Informazioni sull'interfaccia del protocollo di routing
description: Nella documentazione seguente viene descritta l'integrazione di protocolli di routing di terze parti nel servizio Routing e accesso remoto (RRAS).
ms.assetid: 593e3b8a-6f26-47c6-aa93-520d36db7a6f
keywords:
- Servizio Routing e accesso remoto RRAS, interfaccia protocollo di routing
- Servizio Routing e accesso remoto RRAS, interfaccia protocollo di routing, descritta
- Interfaccia routing del protocollo RRAS
- Interfaccia del protocollo di routing RRAS, descritta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc663f249ca42ebbae509c164a828d603a9b968
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711839"
---
# <a name="about-routing-protocol-interface"></a><span data-ttu-id="5a702-107">Informazioni sull'interfaccia del protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="5a702-107">About Routing Protocol Interface</span></span>

<span data-ttu-id="5a702-108">Nella documentazione seguente viene descritta l'integrazione di protocolli di routing di terze parti nel servizio Routing e accesso remoto (RRAS).</span><span class="sxs-lookup"><span data-stu-id="5a702-108">The following documentation describes the integration of third-party routing protocols into the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="5a702-109">RRAS è una funzionalità di Windows che funge da router multiprotocollo.</span><span class="sxs-lookup"><span data-stu-id="5a702-109">RRAS is a feature of Windows that acts as a multi-protocol router.</span></span> <span data-ttu-id="5a702-110">RRAS definisce l'interfaccia tra gestione router e il protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="5a702-110">RRAS defines the interface between the router manager and the routing protocol.</span></span> <span data-ttu-id="5a702-111">Il protocollo di routing viene implementato in una libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="5a702-111">The routing protocol is implemented in a dynamic link library (DLL).</span></span>

<span data-ttu-id="5a702-112">Usare questa interfaccia per implementare i protocolli di routing, ad esempio IGRP, NLSP e BGP, come dll in modalità utente che funzionano con RRAS.</span><span class="sxs-lookup"><span data-stu-id="5a702-112">Use this interface to implement routing protocols, such as IGRP, NLSP, and BGP, as user-mode DLLs that work with RRAS.</span></span>

<span data-ttu-id="5a702-113">In questa documentazione vengono descritti gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a702-113">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="5a702-114">Adapter</span><span class="sxs-lookup"><span data-stu-id="5a702-114">Adapters</span></span>](adapters.md)
-   [<span data-ttu-id="5a702-115">Interfacce</span><span class="sxs-lookup"><span data-stu-id="5a702-115">Interfaces</span></span>](interfaces.md)
-   [<span data-ttu-id="5a702-116">Route statiche e autostatiche</span><span class="sxs-lookup"><span data-stu-id="5a702-116">Static and Autostatic Routes</span></span>](static-and-autostatic-routes.md)

 

 




