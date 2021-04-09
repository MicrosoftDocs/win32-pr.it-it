---
description: La \_ notifica SPFILENOTIFY ENDQUEUE viene inviata alla routine di callback quando tutte le operazioni in coda sono state completate.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Messaggio SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968499"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="79d29-103">\_Messaggio SPFILENOTIFY ENDQUEUE</span><span class="sxs-lookup"><span data-stu-id="79d29-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="79d29-104">La notifica **SPFILENOTIFY \_ ENDQUEUE** viene inviata alla routine di callback quando tutte le operazioni in coda sono state completate.</span><span class="sxs-lookup"><span data-stu-id="79d29-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="79d29-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="79d29-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d29-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="79d29-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="79d29-107">**True** se la coda è stata elaborata correttamente; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="79d29-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="79d29-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="79d29-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="79d29-109">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="79d29-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d29-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79d29-110">Return value</span></span>

<span data-ttu-id="79d29-111">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="79d29-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="79d29-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79d29-112">Requirements</span></span>



| <span data-ttu-id="79d29-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="79d29-113">Requirement</span></span> | <span data-ttu-id="79d29-114">Valore</span><span class="sxs-lookup"><span data-stu-id="79d29-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79d29-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79d29-115">Minimum supported client</span></span><br/> | <span data-ttu-id="79d29-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="79d29-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="79d29-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79d29-117">Minimum supported server</span></span><br/> | <span data-ttu-id="79d29-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79d29-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79d29-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79d29-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d29-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d29-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79d29-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79d29-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d29-122">Overview</span><span class="sxs-lookup"><span data-stu-id="79d29-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="79d29-123">Notifications</span><span class="sxs-lookup"><span data-stu-id="79d29-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="79d29-124">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="79d29-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="79d29-125">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="79d29-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




