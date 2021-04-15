---
title: Messaggio TBM_GETSELEND (COMmctrl. h)
description: Recupera la posizione finale dell'intervallo di selezione corrente in un TrackBar.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Controlli di Windows Message TBM_GETSELEND
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476804"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="b2afe-104">\_Messaggio GETselend TBM</span><span class="sxs-lookup"><span data-stu-id="b2afe-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="b2afe-105">Recupera la posizione finale dell'intervallo di selezione corrente in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b2afe-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2afe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2afe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2afe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2afe-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b2afe-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2afe-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b2afe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2afe-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b2afe-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2afe-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2afe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2afe-111">Return value</span></span>

<span data-ttu-id="b2afe-112">Restituisce un valore a 32 bit che specifica la posizione finale dell'intervallo di selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="b2afe-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2afe-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2afe-113">Remarks</span></span>

<span data-ttu-id="b2afe-114">Un TrackBar può avere un intervallo di selezione solo se è stato specificato lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) quando è stato creato.</span><span class="sxs-lookup"><span data-stu-id="b2afe-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2afe-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2afe-115">Requirements</span></span>



| <span data-ttu-id="b2afe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2afe-116">Requirement</span></span> | <span data-ttu-id="b2afe-117">Valore</span><span class="sxs-lookup"><span data-stu-id="b2afe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2afe-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2afe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2afe-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2afe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2afe-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2afe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2afe-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2afe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2afe-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2afe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2afe-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2afe-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2afe-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2afe-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2afe-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b2afe-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2afe-126">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="b2afe-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="b2afe-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="b2afe-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="b2afe-128">**\_SEselend TBM**</span><span class="sxs-lookup"><span data-stu-id="b2afe-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="b2afe-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="b2afe-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





