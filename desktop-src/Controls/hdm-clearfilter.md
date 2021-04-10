---
title: Messaggio HDM_CLEARFILTER (COMmctrl. h)
description: Cancella il filtro per un controllo intestazione specificato. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro ClearFilter dell'intestazione.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- Controlli di Windows Message HDM_CLEARFILTER
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120311"
---
# <a name="hdm_clearfilter-message"></a><span data-ttu-id="dfe30-105">\_Messaggio HDM CLEARFILTER</span><span class="sxs-lookup"><span data-stu-id="dfe30-105">HDM\_CLEARFILTER message</span></span>

<span data-ttu-id="dfe30-106">Cancella il filtro per un controllo intestazione specificato.</span><span class="sxs-lookup"><span data-stu-id="dfe30-106">Clears the filter for a given header control.</span></span> <span data-ttu-id="dfe30-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ ClearFilter dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .</span><span class="sxs-lookup"><span data-stu-id="dfe30-107">You can send this message explicitly or use the [**Header\_ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dfe30-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfe30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfe30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfe30-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfe30-110">Valore di colonna che indica il filtro da cancellare.</span><span class="sxs-lookup"><span data-stu-id="dfe30-110">A column value indicating which filter to clear.</span></span>

</dd> <dt>

<span data-ttu-id="dfe30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfe30-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dfe30-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="dfe30-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfe30-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfe30-113">Return value</span></span>

<span data-ttu-id="dfe30-114">Restituisce un Integer.</span><span class="sxs-lookup"><span data-stu-id="dfe30-114">Returns an integer.</span></span> <span data-ttu-id="dfe30-115">Viene eseguito il cast di **LRESULT** a un Integer che indica **true**(1) o **false**(0).</span><span class="sxs-lookup"><span data-stu-id="dfe30-115">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfe30-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfe30-116">Remarks</span></span>

<span data-ttu-id="dfe30-117">Se il valore della colonna viene specificato come-1, tutti i filtri vengono cancellati e la notifica [HDN \_ FILTERCHANGE](hdn-filterchange.md) viene inviata una sola volta.</span><span class="sxs-lookup"><span data-stu-id="dfe30-117">If the column value is specified as -1, all the filters are cleared, and the [HDN\_FILTERCHANGE](hdn-filterchange.md) notification is sent only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe30-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfe30-118">Requirements</span></span>



| <span data-ttu-id="dfe30-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfe30-119">Requirement</span></span> | <span data-ttu-id="dfe30-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dfe30-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe30-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfe30-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe30-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfe30-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dfe30-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfe30-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe30-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dfe30-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dfe30-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfe30-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfe30-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfe30-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe30-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfe30-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe30-128">**\_ClearAllFilters intestazione**</span><span class="sxs-lookup"><span data-stu-id="dfe30-128">**Header\_ClearAllFilters**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





