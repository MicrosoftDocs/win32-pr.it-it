---
title: Struttura IPX_NEXT_HOP_ADDRESS (RTM. h)
description: La \_ struttura dell' \_ indirizzo hop successivo IPX \_ contiene l'indirizzo del router di hop successivo per una route IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- RAS struttura IPX_NEXT_HOP_ADDRESS
- RAS puntatore alla struttura PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475058"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="04655-105">\_Struttura dell' \_ indirizzo hop successivo \_ IPX</span><span class="sxs-lookup"><span data-stu-id="04655-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="04655-106">\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="04655-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="04655-107">Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]</span><span class="sxs-lookup"><span data-stu-id="04655-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="04655-108">La struttura dell' **\_ \_ \_ indirizzo hop successivo IPX** contiene l'indirizzo del router di hop successivo per una route IPX.</span><span class="sxs-lookup"><span data-stu-id="04655-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="04655-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04655-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="04655-110">Members</span><span class="sxs-lookup"><span data-stu-id="04655-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="04655-111">**\_Mac Nha**</span><span class="sxs-lookup"><span data-stu-id="04655-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="04655-112">Specifica l'indirizzo MAC del router di hop successivo.</span><span class="sxs-lookup"><span data-stu-id="04655-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04655-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04655-113">Requirements</span></span>



| <span data-ttu-id="04655-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="04655-114">Requirement</span></span> | <span data-ttu-id="04655-115">Valore</span><span class="sxs-lookup"><span data-stu-id="04655-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="04655-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04655-116">Minimum supported client</span></span><br/> | <span data-ttu-id="04655-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="04655-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="04655-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04655-118">Minimum supported server</span></span><br/> | <span data-ttu-id="04655-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="04655-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="04655-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="04655-120">End of server support</span></span><br/>    | <span data-ttu-id="04655-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04655-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="04655-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04655-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="04655-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="04655-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04655-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04655-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04655-125">Riferimento di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="04655-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="04655-126">Strutture di gestione tabelle di routing versione 1</span><span class="sxs-lookup"><span data-stu-id="04655-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="04655-127">**\_Route IPX \_ RTM**</span><span class="sxs-lookup"><span data-stu-id="04655-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





