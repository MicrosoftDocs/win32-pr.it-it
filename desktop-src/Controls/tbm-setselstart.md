---
title: Messaggio TBM_SETSELSTART (COMmctrl. h)
description: Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un TrackBar. Questo messaggio viene ignorato se il TrackBar non ha lo \_ stile ENABLESELRANGE di TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Controlli di Windows Message TBM_SETSELSTART
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047843"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="fd94b-105">\_Messaggio SETSELSTART TBM</span><span class="sxs-lookup"><span data-stu-id="fd94b-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="fd94b-106">Imposta la posizione logica iniziale dell'intervallo di selezione corrente in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="fd94b-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="fd94b-107">Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fd94b-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd94b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd94b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd94b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd94b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd94b-110">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="fd94b-110">Redraw flag.</span></span> <span data-ttu-id="fd94b-111">Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="fd94b-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="fd94b-112">Se questo parametro è **false**, il messaggio imposta l'intervallo di selezione senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="fd94b-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="fd94b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd94b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd94b-114">Posizione iniziale dell'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="fd94b-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd94b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd94b-115">Return value</span></span>

<span data-ttu-id="fd94b-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="fd94b-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd94b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd94b-117">Requirements</span></span>



| <span data-ttu-id="fd94b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd94b-118">Requirement</span></span> | <span data-ttu-id="fd94b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fd94b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd94b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd94b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd94b-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd94b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fd94b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd94b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd94b-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd94b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fd94b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd94b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd94b-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd94b-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd94b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd94b-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd94b-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fd94b-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fd94b-128">**TBM \_ GETselend**</span><span class="sxs-lookup"><span data-stu-id="fd94b-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="fd94b-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="fd94b-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="fd94b-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="fd94b-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="fd94b-131">**\_SEselend TBM**</span><span class="sxs-lookup"><span data-stu-id="fd94b-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 





