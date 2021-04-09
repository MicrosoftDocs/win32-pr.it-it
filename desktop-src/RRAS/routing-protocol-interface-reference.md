---
title: Guida di riferimento all'interfaccia del protocollo di routing
description: In questa documentazione vengono descritte le funzioni e le strutture utilizzate per implementare un protocollo di routing come DLL in modalità utente.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Servizio Routing e accesso remoto RRAS, interfaccia protocollo di routing, riferimento
- Interfaccia del protocollo di routing RRAS, riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856097"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="a6d9d-105">Guida di riferimento all'interfaccia del protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="a6d9d-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="a6d9d-106">In questa documentazione vengono descritte le funzioni e le strutture utilizzate per implementare un protocollo di routing come DLL in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="a6d9d-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="a6d9d-107">MPR50 deve essere definito nel file make per il protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="a6d9d-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="a6d9d-108">La macro di **\_ binding IP sizeof \_ (x)** calcola la dimensione, in byte, di una struttura di [**\_ informazioni di \_ binding \_ della scheda IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) che contiene il numero di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="a6d9d-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="a6d9d-109">Questi elementi di riferimento sono descritti negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6d9d-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="a6d9d-110">Funzioni di interfaccia del protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="a6d9d-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="a6d9d-111">Strutture di interfaccia del protocollo di routing</span><span class="sxs-lookup"><span data-stu-id="a6d9d-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="a6d9d-112">Gestione tabella dei servizi IPX</span><span class="sxs-lookup"><span data-stu-id="a6d9d-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




