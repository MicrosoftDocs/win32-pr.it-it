---
title: WTSLISTENERNAME (WtsApi32. h)
description: Rappresenta il nome di un listener di Servizi Desktop remoto su un server di host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400771"
---
# <a name="wtslistenername"></a><span data-ttu-id="1bb41-109">WTSLISTENERNAME</span><span class="sxs-lookup"><span data-stu-id="1bb41-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="1bb41-110">Rappresenta il nome di un listener di Servizi Desktop remoto su un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="1bb41-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="1bb41-111">**WTSLISTENERNAMEW**</span><span class="sxs-lookup"><span data-stu-id="1bb41-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-112">Nome Unicode del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="1bb41-113">**WTSLISTENERNAMEA**</span><span class="sxs-lookup"><span data-stu-id="1bb41-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-114">Puntatore al nome ANSI del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="1bb41-115">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="1bb41-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-116">Nome del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="1bb41-117">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="1bb41-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-118">Puntatore al nome del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="1bb41-119">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="1bb41-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-120">Nome del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="1bb41-121">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="1bb41-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="1bb41-122">Puntatore al nome del listener.</span><span class="sxs-lookup"><span data-stu-id="1bb41-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bb41-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bb41-123">Requirements</span></span>



| <span data-ttu-id="1bb41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bb41-124">Requirement</span></span> | <span data-ttu-id="1bb41-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1bb41-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bb41-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1bb41-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1bb41-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="1bb41-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bb41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1bb41-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1bb41-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="1bb41-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bb41-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bb41-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bb41-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 





