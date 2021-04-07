---
title: Struttura RTM_IPX_ROUTE (RTM. h)
description: La \_ \_ struttura Route IPX RTM contiene informazioni che descrivono una route per la famiglia di protocolli IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS struttura RTM_IPX_ROUTE
- RAS puntatore alla struttura PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963995"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="fa90d-105">\_ \_ Struttura Route IPX RTM</span><span class="sxs-lookup"><span data-stu-id="fa90d-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="fa90d-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fa90d-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="fa90d-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="fa90d-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="fa90d-108">La **struttura \_ \_ Route IPX RTM** contiene informazioni che descrivono una route per la famiglia di protocolli IPX.</span><span class="sxs-lookup"><span data-stu-id="fa90d-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa90d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa90d-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="fa90d-110">Members</span><span class="sxs-lookup"><span data-stu-id="fa90d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa90d-111">**\_Timestamp RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-112">Specifica l'ora di creazione o dell'ultimo aggiornamento della voce della route.</span><span class="sxs-lookup"><span data-stu-id="fa90d-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="fa90d-113">Questo membro viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="fa90d-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="fa90d-114">Il tempo viene espresso come una struttura FILETIME.</span><span class="sxs-lookup"><span data-stu-id="fa90d-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-116">Specifica il protocollo di routing che ha aggiunto la route.</span><span class="sxs-lookup"><span data-stu-id="fa90d-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-117">**\_INTERFACEID RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-118">Specifica l'interfaccia tramite la quale è stata ottenuta la route.</span><span class="sxs-lookup"><span data-stu-id="fa90d-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-120">Specifica una struttura di [**\_ \_ dati specifica del protocollo**](protocol-specific-data.md) contenente memoria riservata ai dati specifici dei protocolli di routing.</span><span class="sxs-lookup"><span data-stu-id="fa90d-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-121">**\_Rete RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-122">Specifica una struttura di [**\_ rete IPX**](ipx-network.md) che contiene un indirizzo di rete IP.</span><span class="sxs-lookup"><span data-stu-id="fa90d-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-124">Specifica una struttura dell'indirizzo di un [**\_ \_ hop \_ successivo IPX**](ipx-next-hop-address.md) che contiene l'indirizzo del router di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="fa90d-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="fa90d-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="fa90d-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="fa90d-126">Specifica una struttura di [**\_ \_ dati specifica di IPX**](ipx-specific-data.md) che contiene dati specifici della famiglia di protocolli IPX.</span><span class="sxs-lookup"><span data-stu-id="fa90d-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa90d-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa90d-127">Remarks</span></span>

<span data-ttu-id="fa90d-128">I membri della struttura **di \_ \_ Route IPX RTM** sono tutti allineati a **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="fa90d-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa90d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa90d-129">Requirements</span></span>



| <span data-ttu-id="fa90d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa90d-130">Requirement</span></span> | <span data-ttu-id="fa90d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fa90d-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fa90d-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa90d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fa90d-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fa90d-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="fa90d-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa90d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fa90d-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa90d-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fa90d-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="fa90d-136">End of server support</span></span><br/>    | <span data-ttu-id="fa90d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fa90d-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="fa90d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa90d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa90d-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa90d-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa90d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa90d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa90d-141">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="fa90d-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="fa90d-142">Strutture di gestione tabelle di routing versione \_ 1 \_</span><span class="sxs-lookup"><span data-stu-id="fa90d-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="fa90d-143">**\_rete IPX**</span><span class="sxs-lookup"><span data-stu-id="fa90d-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="fa90d-144">**\_ \_ indirizzo hop successivo \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="fa90d-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="fa90d-145">**\_dati specifici di IPX \_**</span><span class="sxs-lookup"><span data-stu-id="fa90d-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





