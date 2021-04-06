---
title: Struttura IP_NETWORK (RTM. h)
description: La \_ struttura di rete IP descrive un indirizzo di rete IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- RAS struttura IP_NETWORK
- RAS puntatore alla struttura PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742479"
---
# <a name="ip_network-structure"></a><span data-ttu-id="b56ed-105">\_Struttura di rete IP</span><span class="sxs-lookup"><span data-stu-id="b56ed-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="b56ed-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b56ed-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b56ed-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="b56ed-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b56ed-108">La struttura di **\_ rete IP** descrive un indirizzo di rete IP.</span><span class="sxs-lookup"><span data-stu-id="b56ed-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="b56ed-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b56ed-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="b56ed-110">Members</span><span class="sxs-lookup"><span data-stu-id="b56ed-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="b56ed-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="b56ed-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="b56ed-112">Specifica il numero di rete IP espresso come indirizzo IP nell'ordine dei byte del computer.</span><span class="sxs-lookup"><span data-stu-id="b56ed-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="b56ed-113">**Netmask N \_**</span><span class="sxs-lookup"><span data-stu-id="b56ed-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="b56ed-114">Specifica il network mask.</span><span class="sxs-lookup"><span data-stu-id="b56ed-114">Specifies the network mask.</span></span> <span data-ttu-id="b56ed-115">Applicare questa maschera all'indirizzo IP per estrarre l'indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="b56ed-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="b56ed-116">Il network mask è nell'ordine dei byte del computer.</span><span class="sxs-lookup"><span data-stu-id="b56ed-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b56ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b56ed-117">Requirements</span></span>



| <span data-ttu-id="b56ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b56ed-118">Requirement</span></span> | <span data-ttu-id="b56ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b56ed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b56ed-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b56ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b56ed-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b56ed-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="b56ed-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b56ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b56ed-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b56ed-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b56ed-124">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="b56ed-124">End of server support</span></span><br/>    | <span data-ttu-id="b56ed-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b56ed-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="b56ed-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b56ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b56ed-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b56ed-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b56ed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b56ed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b56ed-129">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="b56ed-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b56ed-130">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="b56ed-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="b56ed-131">**\_route IP \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="b56ed-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





