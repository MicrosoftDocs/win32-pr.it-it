---
title: Messaggio MCM_GETTODAY (COMmctrl. h)
description: Recupera le informazioni sulla data per la data specificata come \ 0034; Today \ 0034; per un controllo di calendario mensile. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro MonthCal GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- Controlli di Windows Message MCM_GETTODAY
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964291"
---
# <a name="mcm_gettoday-message"></a><span data-ttu-id="8bce9-105">\_Messaggio MCM GETtoday</span><span class="sxs-lookup"><span data-stu-id="8bce9-105">MCM\_GETTODAY message</span></span>

<span data-ttu-id="8bce9-106">Recupera le informazioni sulla data per la data specificata come "Today" per un controllo di calendario mensile.</span><span class="sxs-lookup"><span data-stu-id="8bce9-106">Retrieves the date information for the date specified as "today" for a month calendar control.</span></span> <span data-ttu-id="8bce9-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**MonthCal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .</span><span class="sxs-lookup"><span data-stu-id="8bce9-107">You can send this message explicitly or by using the [**MonthCal\_GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8bce9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bce9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bce9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8bce9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8bce9-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8bce9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8bce9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8bce9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8bce9-112">Puntatore a una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che riceverà le informazioni sulla data.</span><span class="sxs-lookup"><span data-stu-id="8bce9-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that will receive the date information.</span></span> <span data-ttu-id="8bce9-113">Questo parametro deve essere un indirizzo valido e non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="8bce9-113">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bce9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bce9-114">Return value</span></span>

<span data-ttu-id="8bce9-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8bce9-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bce9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bce9-116">Requirements</span></span>



| <span data-ttu-id="8bce9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bce9-117">Requirement</span></span> | <span data-ttu-id="8bce9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8bce9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8bce9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bce9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8bce9-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bce9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8bce9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bce9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8bce9-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bce9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8bce9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bce9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bce9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bce9-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bce9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bce9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bce9-126">Orari del controllo calendario mensile</span><span class="sxs-lookup"><span data-stu-id="8bce9-126">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

