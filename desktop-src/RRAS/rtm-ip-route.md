---
title: Struttura RTM_IP_ROUTE (RTM. h)
description: La \_ struttura della \_ route IP RTM contiene informazioni che descrivono una route di proprietà della famiglia di protocolli IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS struttura RTM_IP_ROUTE
- RAS puntatore alla struttura PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302704"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="a1948-105">\_Struttura della \_ route IP RTM</span><span class="sxs-lookup"><span data-stu-id="a1948-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="a1948-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a1948-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a1948-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="a1948-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a1948-108">La struttura della **\_ \_ route IP RTM** contiene informazioni che descrivono una route di proprietà della famiglia di protocolli IP.</span><span class="sxs-lookup"><span data-stu-id="a1948-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1948-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1948-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="a1948-110">Members</span><span class="sxs-lookup"><span data-stu-id="a1948-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1948-111">**\_Timestamp RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-112">Specifica l'ora di creazione o dell'ultimo aggiornamento della voce della route.</span><span class="sxs-lookup"><span data-stu-id="a1948-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="a1948-113">Questo membro viene impostato da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="a1948-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="a1948-114">Il tempo viene espresso come una struttura FILETIME.</span><span class="sxs-lookup"><span data-stu-id="a1948-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-116">Specifica il protocollo di routing che ha aggiunto la route.</span><span class="sxs-lookup"><span data-stu-id="a1948-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-117">**\_INTERFACEID RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-118">Specifica l'interfaccia tramite la quale è stata ottenuta la route.</span><span class="sxs-lookup"><span data-stu-id="a1948-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-120">Specifica una struttura di [**\_ \_ dati specifica del protocollo**](protocol-specific-data.md) che contiene memoria riservata per i dati specifici del protocollo di routing.</span><span class="sxs-lookup"><span data-stu-id="a1948-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-121">**\_Rete RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-122">Specifica una struttura di [**\_ rete IP**](ip-network.md) che contiene un indirizzo di rete IP.</span><span class="sxs-lookup"><span data-stu-id="a1948-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-124">Specifica una struttura dell' [**\_ \_ \_ indirizzo di hop successivo IP**](ip-next-hop-address.md) che contiene l'indirizzo del router di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="a1948-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="a1948-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="a1948-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="a1948-126">Specifica una struttura di [**\_ \_ dati specifica dell'IP**](ip-specific-data.md) che contiene dati specifici della famiglia di protocolli IP.</span><span class="sxs-lookup"><span data-stu-id="a1948-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1948-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1948-127">Remarks</span></span>

<span data-ttu-id="a1948-128">I membri della struttura **della \_ \_ route IP RTM** sono tutti allineati a **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="a1948-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1948-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1948-129">Requirements</span></span>



| <span data-ttu-id="a1948-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1948-130">Requirement</span></span> | <span data-ttu-id="a1948-131">Valore</span><span class="sxs-lookup"><span data-stu-id="a1948-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a1948-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1948-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a1948-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a1948-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="a1948-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1948-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a1948-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1948-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a1948-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="a1948-136">End of server support</span></span><br/>    | <span data-ttu-id="a1948-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1948-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a1948-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1948-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1948-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1948-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1948-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1948-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1948-141">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="a1948-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a1948-142">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="a1948-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="a1948-143">**\_rete IP**</span><span class="sxs-lookup"><span data-stu-id="a1948-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="a1948-144">**\_ \_ indirizzo hop successivo \_ IP**</span><span class="sxs-lookup"><span data-stu-id="a1948-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="a1948-145">**\_dati specifici \_ IP**</span><span class="sxs-lookup"><span data-stu-id="a1948-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





