---
title: Struttura IP_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ struttura dell' \_ indirizzo di hop successivo IP \_ contiene l'indirizzo del router di hop successivo per una route IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS struttura IP_NEXT_HOP_ADDRESS
- RAS struttura PIP_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302187"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="1d4cd-105">\_ \_ Struttura indirizzo hop successivo IP \_</span><span class="sxs-lookup"><span data-stu-id="1d4cd-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="1d4cd-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1d4cd-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="1d4cd-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1d4cd-108">La struttura dell' **\_ \_ \_ indirizzo di hop successivo IP** contiene l'indirizzo del router di hop successivo per una route IP.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d4cd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d4cd-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="1d4cd-110">Members</span><span class="sxs-lookup"><span data-stu-id="1d4cd-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d4cd-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="1d4cd-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="1d4cd-112">Specifica l'indirizzo di rete IP espresso come indirizzo IP nell'ordine dei byte del computer.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="1d4cd-113">**Netmask N \_**</span><span class="sxs-lookup"><span data-stu-id="1d4cd-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="1d4cd-114">Specifica il network mask.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-114">Specifies the network mask.</span></span> <span data-ttu-id="1d4cd-115">Applicare questa maschera all'indirizzo IP per estrarre l'indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="1d4cd-116">Il network mask è nell'ordine dei byte del computer.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d4cd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d4cd-117">Remarks</span></span>

<span data-ttu-id="1d4cd-118">La struttura dell' **\_ \_ \_ indirizzo di hop successivo IP** è un typedef della struttura di [**\_ rete IP**](ip-network.md) .</span><span class="sxs-lookup"><span data-stu-id="1d4cd-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="1d4cd-119">Il typedef è in RTM. h.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d4cd-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d4cd-120">Requirements</span></span>



| <span data-ttu-id="1d4cd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d4cd-121">Requirement</span></span> | <span data-ttu-id="1d4cd-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1d4cd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1d4cd-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1d4cd-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1d4cd-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="1d4cd-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d4cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1d4cd-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d4cd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1d4cd-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1d4cd-127">End of server support</span></span><br/>    | <span data-ttu-id="1d4cd-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1d4cd-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="1d4cd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1d4cd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d4cd-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d4cd-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d4cd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d4cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d4cd-132">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="1d4cd-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-133">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="1d4cd-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-134">**\_rete IP**</span><span class="sxs-lookup"><span data-stu-id="1d4cd-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-135">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="1d4cd-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





