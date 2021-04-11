---
title: RPC e rete
description: In questa sezione viene illustrato come gestire l'inaffidabilità della rete quando si utilizza RPC e viene illustrato il modo in cui le API a livello di RPC vengono convertite in attività di rete. La sezione si riferisce solo \_ alle \_ sequenze di protocollo HTTP TCP e ncacn di ncacn IP \_ .
ms.assetid: af7c67ea-32af-40b0-b74b-0a339e5088c4
keywords:
- RPC (Remote Procedure Call), procedure consigliate, RPC e rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c0373bb81d9da0bf20eed1fb9f80863604b040
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118206"
---
# <a name="rpc-and-the-network"></a><span data-ttu-id="ef705-105">RPC e rete</span><span class="sxs-lookup"><span data-stu-id="ef705-105">RPC and the Network</span></span>

<span data-ttu-id="ef705-106">In questa sezione viene illustrato come gestire l'inaffidabilità della rete quando si utilizza RPC e viene illustrato il modo in cui le API a livello di RPC vengono convertite in attività di rete.</span><span class="sxs-lookup"><span data-stu-id="ef705-106">This section discusses how to deal with network unreliability when using RPC, and explains how RPC-level APIs translate into network activity.</span></span> <span data-ttu-id="ef705-107">La sezione si riferisce solo alle sequenze di [**protocollo \_ http**](/windows/desktop/Midl/ncacn-http) TCP e ncacn di [**ncacn \_ \_ IP**](/windows/desktop/Midl/ncacn-ip-tcp) .</span><span class="sxs-lookup"><span data-stu-id="ef705-107">The section refers only to the [**ncacn\_ip\_tcp**](/windows/desktop/Midl/ncacn-ip-tcp) and [**ncacn\_http**](/windows/desktop/Midl/ncacn-http) protocol sequences.</span></span>

<span data-ttu-id="ef705-108">Questa sezione è divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef705-108">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="ef705-109">Sviluppo rispetto alla distribuzione in rete</span><span class="sxs-lookup"><span data-stu-id="ef705-109">Development Versus Deployment in the Network</span></span>](development-versus-deployment-in-the-network.md)
-   [<span data-ttu-id="ef705-110">Prevenzione di blocchi di Client-Side</span><span class="sxs-lookup"><span data-stu-id="ef705-110">Preventing Client-Side Hangs</span></span>](preventing-client-side-hangs.md)
-   [<span data-ttu-id="ef705-111">Gestione dei set di connessioni di rete (associazioni)</span><span class="sxs-lookup"><span data-stu-id="ef705-111">Managing Network Connection Sets (Associations)</span></span>](managing-network-connection-sets-associations-.md)
-   [<span data-ttu-id="ef705-112">Pulizia della connessione inattiva</span><span class="sxs-lookup"><span data-stu-id="ef705-112">Idle Connection Cleanup</span></span>](idle-connection-cleanup.md)
-   [<span data-ttu-id="ef705-113">Gestione della perdita di connettività</span><span class="sxs-lookup"><span data-stu-id="ef705-113">Dealing with Loss of Connectivity</span></span>](dealing-with-loss-of-connectivity.md)
-   [<span data-ttu-id="ef705-114">Pulizia lato server</span><span class="sxs-lookup"><span data-stu-id="ef705-114">Server Side Cleanup</span></span>](server-side-cleanup.md)

 

 