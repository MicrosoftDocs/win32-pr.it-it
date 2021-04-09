---
title: Struttura IPX_NETWORK (RTM. h)
description: La \_ struttura di rete IPX descrive un indirizzo di rete IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- RAS struttura IPX_NETWORK
- RAS puntatore alla struttura PIPX_NETWORK
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963730"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="6b8cc-105">\_Struttura di rete IPX</span><span class="sxs-lookup"><span data-stu-id="6b8cc-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="6b8cc-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="6b8cc-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="6b8cc-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="6b8cc-108">La struttura di **\_ rete IPX** descrive un indirizzo di rete IPX.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8cc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8cc-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="6b8cc-110">Members</span><span class="sxs-lookup"><span data-stu-id="6b8cc-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6b8cc-111">**N \_ NetNumber**</span><span class="sxs-lookup"><span data-stu-id="6b8cc-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="6b8cc-112">Contiene il numero di rete IPX nell'ordine dei byte del computer.</span><span class="sxs-lookup"><span data-stu-id="6b8cc-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b8cc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8cc-113">Requirements</span></span>



| <span data-ttu-id="6b8cc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8cc-114">Requirement</span></span> | <span data-ttu-id="6b8cc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8cc-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6b8cc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8cc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8cc-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6b8cc-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="6b8cc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8cc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8cc-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8cc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6b8cc-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="6b8cc-120">End of server support</span></span><br/>    | <span data-ttu-id="6b8cc-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6b8cc-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="6b8cc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b8cc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b8cc-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8cc-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8cc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8cc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8cc-125">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="6b8cc-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="6b8cc-126">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="6b8cc-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="6b8cc-127">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="6b8cc-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





