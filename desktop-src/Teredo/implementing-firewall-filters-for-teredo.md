---
title: Implementazione di filtri firewall per Teredo
description: Windows consente alle applicazioni di impostare un'opzione socket che consente alle applicazioni di indicare un'intenzione esplicita di ricevere il traffico Teredo inviato al firewall host tramite la piattaforma filtro Windows.
ms.assetid: 9e53e28c-e0e5-438d-b624-27d7bd65e4a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f24d4351f10a3b37f2bf63c952e81883d97b781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729055"
---
# <a name="implementing-firewall-filters-for-teredo"></a><span data-ttu-id="dcc99-103">Implementazione di filtri firewall per Teredo</span><span class="sxs-lookup"><span data-stu-id="dcc99-103">Implementing Firewall Filters for Teredo</span></span>

<span data-ttu-id="dcc99-104">Windows consente alle applicazioni di impostare un'opzione socket che consente alle applicazioni di indicare un'intenzione esplicita di ricevere il traffico Teredo inviato al firewall host tramite la piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="dcc99-104">Windows allows applications to set a socket option that allows applications to indicate an explicit intent to receive Teredo traffic sent to the host firewall via the Windows Filtering Platform.</span></span> <span data-ttu-id="dcc99-105">In Windows, un'opzione socket per l'impostazione di un livello di protezione viene usata per consentire a un'applicazione di definire il tipo di traffico che è disposto a ricevere.</span><span class="sxs-lookup"><span data-stu-id="dcc99-105">In Windows, a socket option for setting a protection level is used to allow an application to define what type of traffic it is willing to receive.</span></span> <span data-ttu-id="dcc99-106">In particolare, in scenari che coinvolgono il traffico Teredo, viene specificata l'opzione socket del [ \_ \_ livello di protezione IPv6](/windows/desktop/WinSock/ipv6-protection-level) .</span><span class="sxs-lookup"><span data-stu-id="dcc99-106">More specifically, in scenarios involving Teredo traffic, the [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option is specified.</span></span> <span data-ttu-id="dcc99-107">È consigliabile che le implementazioni del firewall dell'host mantengano i filtri seguenti per consentire selettivamente il traffico Teredo per un'applicazione, bloccando il traffico per impostazione predefinita per qualsiasi applicazione senza esenzione.</span><span class="sxs-lookup"><span data-stu-id="dcc99-107">It is recommended that host firewall implementations maintain the following filters to selectively allow Teredo traffic for an application, while blocking traffic by default for any application without an exemption.</span></span>

## <a name="default-block-filter-for-edge-traversed-traffic"></a><span data-ttu-id="dcc99-108">Filtro di blocco predefinito per il traffico attraversato da Edge</span><span class="sxs-lookup"><span data-stu-id="dcc99-108">Default Block Filter for Edge Traversed Traffic</span></span>

<span data-ttu-id="dcc99-109">Un firewall host deve sempre mantenere un filtro di blocco predefinito all'interno \_ del \_ \_ \_ livello di filtraggio di ale auth ricezione Accept V6 per il traffico che corrisponde alle condizioni del **tunnel del tipo di interfaccia** specificato e del tipo di **tunnel** .</span><span class="sxs-lookup"><span data-stu-id="dcc99-109">A host firewall must always maintain a default block filter within the ALE\_AUTH\_RECV\_ACCEPT\_V6 filtering layer for traffic matching the specified **Interface Type Tunnel** and **Tunnel Type Teredo** conditions.</span></span> <span data-ttu-id="dcc99-110">Quando viene implementato, questo filtro indica la presenza di un firewall host compatibile con attraversamento del perimetro nel sistema.</span><span class="sxs-lookup"><span data-stu-id="dcc99-110">When implemented, this filter indicates the presence of an edge traversal aware host firewall in the system.</span></span> <span data-ttu-id="dcc99-111">Questo filtro viene visualizzato come un contratto API tra il firewall host e Windows.</span><span class="sxs-lookup"><span data-stu-id="dcc99-111">This filter is viewed as an API contract between the host firewall and Windows.</span></span> <span data-ttu-id="dcc99-112">Per impostazione predefinita, questo filtro blocca il traffico attraversato da Edge verso qualsiasi applicazione.</span><span class="sxs-lookup"><span data-stu-id="dcc99-112">By default, this filter will block edge traversed traffic to any application.</span></span>

``` syntax
   filter.layerKey  = FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_BLOCK;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;
   filter.weight.uint64 = 0;
   filter.flags = 0;
   filter.numFilterConditions = 2; // Or 3 depending on including the loopback condition
   filter.filterCondition = filterConditions;
   filter.displayData.name  = L"Teredo Edge Traversal Default Block";
   filter.displayData.description = L"Teredo Edge Traversal Default Block Filter.";

   // Match Interface type tunnel
   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   // Match tunnel type Teredo
   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   // Having this condition is OPTIONAL, including this will automatically exempt 
   // loopback traffic to receive Teredo.
   filterConditions[2].fieldKey = FWPM_CONDITION_FLAGS;
   filterConditions[2].matchType = FWP_MATCH_FLAGS_NONE_SET;
   filterConditions[2].conditionValue.type = FWP_UINT32;
   filterConditions[2].conditionValue.uint32 = FWP_CONDITION_FLAG_IS_LOOPBACK;
```

> [!Note]  
> <span data-ttu-id="dcc99-113">Le classi ' Delivery ',' arrival ' è next hop ' di condizioni di interfaccia vengono usate per controllare un modello di host debole e l'invio di pacchetti tra le interfacce.</span><span class="sxs-lookup"><span data-stu-id="dcc99-113">The 'Delivery', 'Arrival', and 'Next Hop' classes of interface conditions are used to control a weak-host model and packet forwarding across interfaces.</span></span> <span data-ttu-id="dcc99-114">Nell'esempio precedente viene utilizzata la classe ' Delivery '.</span><span class="sxs-lookup"><span data-stu-id="dcc99-114">The example above utilizes the 'Delivery' class.</span></span> <span data-ttu-id="dcc99-115">Esaminare le [condizioni di filtro disponibili a ogni livello di filtro](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) nella documentazione di WFP SDK, in quanto la progettazione della sicurezza deve prendere in considerazione ogni caso.</span><span class="sxs-lookup"><span data-stu-id="dcc99-115">Please review [Filtering Conditions Available at Each Filtering Layer](/windows/desktop/FWP/filtering-conditions-available-at-each-filtering-layer) in the WFP SDK documentation, as your security design must take each case into consideration.</span></span>

 

## <a name="allow-filter-for-exempt-applications"></a><span data-ttu-id="dcc99-116">Consenti filtro per applicazioni esenti</span><span class="sxs-lookup"><span data-stu-id="dcc99-116">Allow Filter for Exempt Applications</span></span>

<span data-ttu-id="dcc99-117">Se un'applicazione viene esentata dalla ricezione di traffico Teredo su un socket di ascolto, è necessario implementare un filtro di autorizzazione all'interno del \_ \_ \_ \_ livello di filtraggio RCV Accept V6 sul firewall host.</span><span class="sxs-lookup"><span data-stu-id="dcc99-117">If an application is exempt from receiving Teredo traffic on a listening socket, a permit filter must be implemented within the ALE\_AUTH\_RCV\_ACCEPT\_V6 filtering layer on the host firewall.</span></span> <span data-ttu-id="dcc99-118">È importante notare che, a seconda di come l'esenzione è configurata dall'utente o dall'applicazione, il firewall host può includere un'opzione socket.</span><span class="sxs-lookup"><span data-stu-id="dcc99-118">It is important to note that depending on how the exemption is configured by the user or application, the host firewall can include a socket option.</span></span>

``` syntax
   filter.layerKey   = FWPM_LAYER_ALE_AUTH_RCV_ACCEPT_V6;
   filter.action.type = FWP_ACTION_PERMIT;
   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64= 1; // Use a weight higher than the default block
   filter.flags = 0;
   filter.numFilterConditions = 3; // Or 4 depending on the socket option based condition
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal Allow Application A";
   filter.displayData.description = L"Teredo Edge Traversal Allow Application A Filter.";

   filterConditions[0].fieldKey = FWPM_CONDITION_INTERFACE_TYPE;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_UINT32;
   filterConditions[0].conditionValue.uint32 = IF_TYPE_TUNNEL;

   filterConditions[1].fieldKey = FWPM_CONDITION_TUNNEL_TYPE;
   filterConditions[1].matchType = FWP_MATCH_EQUAL;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = TUNNEL_TYPE_TEREDO;

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[2].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[2].matchType = FWP_MATCH_EQUAL;
   filterConditions[2].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[2].conditionValue.byteBlob = &byteBlob;
   filterConditions[2].conditionValue.byteBlob->data = (uint8 *) wszApplicationA;
   filterConditions[2].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[3].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[3].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[3].conditionValue.type = FWP_UINT32;
   filterConditions[3].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

## <a name="dormancy-callout-filter"></a><span data-ttu-id="dcc99-119">Filtro callout inattivo</span><span class="sxs-lookup"><span data-stu-id="dcc99-119">Dormancy Callout Filter</span></span>

<span data-ttu-id="dcc99-120">Il servizio Teredo in Windows implementa un modello inattivo.</span><span class="sxs-lookup"><span data-stu-id="dcc99-120">The Teredo service in Windows implements a dormancy model.</span></span> <span data-ttu-id="dcc99-121">In qualsiasi momento, se nessuna applicazione è in ascolto su un socket UDP o TCP con attraversamento perimetrale abilitato, il servizio passa a uno stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="dcc99-121">At any given time, if no applications are listening on a UDP or TCP socket with edge traversal enabled, the service moves to a dormant state.</span></span> <span data-ttu-id="dcc99-122">Per il corretto funzionamento del meccanismo di letargo, è necessario che il firewall host mantenga un filtro di callout per ogni applicazione esentata specificata all'interno del \_ \_ livello di filtro di ale auth Listen \_ V6 per TCP e il livello di filtro per l' \_ assegnazione di risorse ale \_ \_ V6 per le applicazioni basate su UDP.</span><span class="sxs-lookup"><span data-stu-id="dcc99-122">For the dormancy mechanism to work, the host firewall must maintain a callout filter for each exempt application specified within the ALE\_AUTH\_LISTEN\_V6 filtering layer for TCP, and ALE\_RESOURCE\_ASSIGNMENT\_V6 filtering layer for UDP based applications.</span></span> <span data-ttu-id="dcc99-123">Nell'esempio seguente viene illustrato un callout inattivo per un'applicazione **TCP** .</span><span class="sxs-lookup"><span data-stu-id="dcc99-123">The following sample below demonstrates a dormancy callout for a **TCP** application.</span></span>

``` syntax
   filter.layerKey = FWPM_LAYER_ALE_AUTH_LISTEN_V6;
   // Use FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.action.type = FWP_ACTION_CALLOUT_TERMINATING;
   filter.action.calloutKey = FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6;
   // Use FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 for UDP based exemption

   filter.subLayerKey = FWPM_SUBLAYER_EDGE_TRAVERSAL;
   filter.weight.type = FWP_UINT64;   
   filter.weight.uint64 = 1;
   filter.flags = 0;
   filter.numFilterConditions = 1; // 2 if including the socket option based condition 
   filter.filterCondition = filterConditions;
   filter.displayData.name = L"Teredo Edge Traversal dormancy callout for app A";
   filter.displayData.description = L"Teredo Edge Traversal dormancy callout filter for A.";

   FWP_BYTE_BLOB byteBlob = {0};
   filterConditions[0].fieldKey = FWPM_CONDITION_ALE_APP_ID;
   filterConditions[0].matchType = FWP_MATCH_EQUAL;
   filterConditions[0].conditionValue.type = FWP_BYTE_BLOB_TYPE;
   filterConditions[0].conditionValue.byteBlob = &byteBlob;
   filterConditions[0].conditionValue.byteBlob->data = (uint8 *)wszApplicationA;
   filterConditions[0].conditionValue.byteBlob->size = (wcslen(wszApplicationA) + 1)*sizeof(wchar_t);

   // This filter scopes to exemption to ONLY IF the socket option is set, in other words
   // application has explicitly opted in to receive Teredo traffic
   filterConditions[1].fieldKey = FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY;
   filterConditions[1].matchType = FWP_MATCH_FLAGS_ALL_SET;
   filterConditions[1].conditionValue.type = FWP_UINT32;
   filterConditions[1].conditionValue.uint32 = FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC;
```

 

 