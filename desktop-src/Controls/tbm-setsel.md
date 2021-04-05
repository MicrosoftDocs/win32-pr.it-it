---
title: Messaggio TBM_SETSEL (COMmctrl. h)
description: Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un TrackBar.
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- Controlli di Windows Message TBM_SETSEL
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739903"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="c91f0-104">\_Messaggio SETSEL TBM</span><span class="sxs-lookup"><span data-stu-id="c91f0-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="c91f0-105">Imposta le posizioni iniziale e finale per l'intervallo di selezione disponibile in un TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c91f0-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="c91f0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c91f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91f0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c91f0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c91f0-108">Ridisegni flag.</span><span class="sxs-lookup"><span data-stu-id="c91f0-108">Redraw flag.</span></span> <span data-ttu-id="c91f0-109">Se questo parametro è **true**, il messaggio riestrae il TrackBar dopo l'impostazione dell'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="c91f0-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="c91f0-110">Se questo parametro è **false**, il messaggio imposta l'intervallo di selezione senza ricreare il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="c91f0-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="c91f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c91f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c91f0-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la posizione logica iniziale per l'intervallo di selezione e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione logica finale.</span><span class="sxs-lookup"><span data-stu-id="c91f0-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91f0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c91f0-113">Return value</span></span>

<span data-ttu-id="c91f0-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c91f0-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c91f0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c91f0-115">Remarks</span></span>

<span data-ttu-id="c91f0-116">Questo messaggio viene ignorato se il TrackBar non ha lo stile [**\_ ENABLESELRANGE di TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c91f0-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="c91f0-117">**TBM \_ SETSEL** consente di limitare il puntatore solo a una parte dell'intervallo disponibile per l'indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="c91f0-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91f0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c91f0-118">Requirements</span></span>



| <span data-ttu-id="c91f0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91f0-119">Requirement</span></span> | <span data-ttu-id="c91f0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c91f0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c91f0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c91f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c91f0-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c91f0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c91f0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c91f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c91f0-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c91f0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c91f0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c91f0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c91f0-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c91f0-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c91f0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c91f0-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="c91f0-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c91f0-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c91f0-129">**TBM \_ GETselend**</span><span class="sxs-lookup"><span data-stu-id="c91f0-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="c91f0-130">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="c91f0-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="c91f0-131">**\_SEselend TBM**</span><span class="sxs-lookup"><span data-stu-id="c91f0-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="c91f0-132">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="c91f0-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

