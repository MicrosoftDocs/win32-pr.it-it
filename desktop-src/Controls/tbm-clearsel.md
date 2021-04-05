---
title: Messaggio TBM_CLEARSEL (COMmctrl. h)
description: Cancella l'intervallo di selezione corrente in un TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Controlli di Windows Message TBM_CLEARSEL
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874666"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="3c173-104">\_Messaggio CLEARSEL TBM</span><span class="sxs-lookup"><span data-stu-id="3c173-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="3c173-105">Cancella l'intervallo di selezione corrente in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3c173-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c173-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c173-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c173-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c173-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c173-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="3c173-108">Redraw flag.</span></span> <span data-ttu-id="3c173-109">Se questo parametro è **true**, il TrackBar viene ridisegnato dopo la cancellazione della selezione.</span><span class="sxs-lookup"><span data-stu-id="3c173-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="3c173-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c173-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3c173-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3c173-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c173-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c173-112">Return value</span></span>

<span data-ttu-id="3c173-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3c173-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c173-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c173-114">Remarks</span></span>

<span data-ttu-id="3c173-115">Un TrackBar può avere un intervallo di selezione solo se è stato specificato lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) quando è stato creato.</span><span class="sxs-lookup"><span data-stu-id="3c173-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c173-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c173-116">Requirements</span></span>



| <span data-ttu-id="3c173-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c173-117">Requirement</span></span> | <span data-ttu-id="3c173-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3c173-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c173-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c173-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c173-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c173-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c173-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c173-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c173-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c173-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c173-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c173-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c173-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c173-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c173-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c173-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c173-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3c173-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c173-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="3c173-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="3c173-128">**\_SEselend TBM**</span><span class="sxs-lookup"><span data-stu-id="3c173-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="3c173-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="3c173-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





