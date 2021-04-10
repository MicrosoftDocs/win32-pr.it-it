---
title: Riferimento all'API di supporto per il routing della connessione su richiesta
description: Negli argomenti seguenti vengono fornite informazioni dettagliate sull'helper di routing della connessione su richiesta.
ms.assetid: 39AFFD16-488E-4CA3-9161-9424F0D15948
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3049c62d7784af6430e8b93240ec79464b098043
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116921"
---
# <a name="on-demand-connection-routing-helper-api-reference"></a><span data-ttu-id="1668c-103">Riferimento all'API di supporto per il routing della connessione su richiesta</span><span class="sxs-lookup"><span data-stu-id="1668c-103">On Demand Connection Routing Helper API reference</span></span>

<span data-ttu-id="1668c-104">Negli argomenti seguenti vengono fornite informazioni dettagliate sull'helper di routing della connessione su richiesta.</span><span class="sxs-lookup"><span data-stu-id="1668c-104">The following topics provide details for the On Demand Connection Routing Helper.</span></span>



| <span data-ttu-id="1668c-105">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1668c-105">Reference</span></span>                                                                          | <span data-ttu-id="1668c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1668c-106">Description</span></span>                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1668c-107">**OnDemandGetRoutingHint**</span><span class="sxs-lookup"><span data-stu-id="1668c-107">**OnDemandGetRoutingHint**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandgetroutinghint)                           | <span data-ttu-id="1668c-108">Cercare una destinazione nella cache delle richieste di route e, se viene trovata una corrispondenza, restituisce l'ID di interfaccia corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1668c-108">Look up a destination in the Route Request cache and, if a match is found, returns the corresponding Interface ID.</span></span><br/>                                               |
| [<span data-ttu-id="1668c-109">**OnDemandRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="1668c-109">**OnDemandRegisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandregisternotification)               | <span data-ttu-id="1668c-110">Registrarsi per ricevere una notifica quando viene modificata la cache delle richieste di route.</span><span class="sxs-lookup"><span data-stu-id="1668c-110">Register to be notified when the Route Requests cache is modified.</span></span><br/>                                                                                               |
| [<span data-ttu-id="1668c-111">**OnDemandUnregisterNotification**</span><span class="sxs-lookup"><span data-stu-id="1668c-111">**OnDemandUnregisterNotification**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-ondemandunregisternotification)           | <span data-ttu-id="1668c-112">Annulla la registrazione per le notifiche e pulisci le risorse.</span><span class="sxs-lookup"><span data-stu-id="1668c-112">Unregister for notifications and clean up resources.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="1668c-113">**\_contesto dell'interfaccia net \_**</span><span class="sxs-lookup"><span data-stu-id="1668c-113">**NET\_INTERFACE\_CONTEXT**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context)                           | <span data-ttu-id="1668c-114">Contesto dell'interfaccia che fa parte della struttura [**della \_ \_ \_ tabella del contesto NET Interface**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) .</span><span class="sxs-lookup"><span data-stu-id="1668c-114">The interface context that is part of the [**NET\_INTERFACE\_CONTEXT\_TABLE**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table) structure.</span></span><br/>                                       |
| [<span data-ttu-id="1668c-115">**\_tabella del \_ contesto NET Interface \_**</span><span class="sxs-lookup"><span data-stu-id="1668c-115">**NET\_INTERFACE\_CONTEXT\_TABLE**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context_table)              | <span data-ttu-id="1668c-116">Tabella delle strutture [**di \_ \_ contesto dell'interfaccia .NET**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) .</span><span class="sxs-lookup"><span data-stu-id="1668c-116">The table of [**NET\_INTERFACE\_CONTEXT**](/windows/desktop/api/OnDemandConnRouteHelper/ns-ondemandconnroutehelper-net_interface_context) structures.</span></span><br/>                                                                                |
| [<span data-ttu-id="1668c-117">**GetInterfaceContextTableForHostName**</span><span class="sxs-lookup"><span data-stu-id="1668c-117">**GetInterfaceContextTableForHostName**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) | <span data-ttu-id="1668c-118">Questa funzione recupera una tabella del contesto dell'interfaccia per il nome host e il filtro del profilo di connessione specificati.</span><span class="sxs-lookup"><span data-stu-id="1668c-118">This function retrieves an interface context table for the given hostname and connection profile filter.</span></span><br/>                                                         |
| [<span data-ttu-id="1668c-119">**FreeInterfaceContextTable**</span><span class="sxs-lookup"><span data-stu-id="1668c-119">**FreeInterfaceContextTable**</span></span>](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-freeinterfacecontexttable)                     | <span data-ttu-id="1668c-120">Questa funzione libera la tabella del contesto dell'interfaccia recuperata tramite la funzione [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) .</span><span class="sxs-lookup"><span data-stu-id="1668c-120">This function frees the interface context table retrieved using the [**GetInterfaceContextTableForHostName**](/windows/desktop/api/OnDemandConnRouteHelper/nf-ondemandconnroutehelper-getinterfacecontexttableforhostname) function.</span></span><br/> |



 

 

 





