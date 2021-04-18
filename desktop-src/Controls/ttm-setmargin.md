---
title: Messaggio TTM_SETMARGIN (COMmctrl. h)
description: Imposta i margini superiore, sinistro, inferiore e destro per una finestra della descrizione comando. Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- Controlli di Windows Message TTM_SETMARGIN
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed46bf40833a3046d15386782897eb6b573b29c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301650"
---
# <a name="ttm_setmargin-message"></a><span data-ttu-id="52d73-105">Messaggio TTM del \_ margine</span><span class="sxs-lookup"><span data-stu-id="52d73-105">TTM\_SETMARGIN message</span></span>

<span data-ttu-id="52d73-106">Imposta i margini superiore, sinistro, inferiore e destro per una finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="52d73-106">Sets the top, left, bottom, and right margins for a tooltip window.</span></span> <span data-ttu-id="52d73-107">Un margine è la distanza, in pixel, tra il bordo della finestra della descrizione comando e il testo contenuto nella finestra della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="52d73-107">A margin is the distance, in pixels, between the tooltip window border and the text contained within the tooltip window.</span></span>

## <a name="parameters"></a><span data-ttu-id="52d73-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="52d73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d73-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52d73-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="52d73-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="52d73-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="52d73-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52d73-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52d73-112">Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che contiene le informazioni sui margini da impostare.</span><span class="sxs-lookup"><span data-stu-id="52d73-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margin information to be set.</span></span> <span data-ttu-id="52d73-113">I membri della struttura **Rect** non definiscono un rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="52d73-113">The members of the **RECT** structure do not define a bounding rectangle.</span></span> <span data-ttu-id="52d73-114">Ai fini di questo messaggio, i membri della struttura vengono interpretati nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="52d73-114">For the purpose of this message, the structure members are interpreted as follows:</span></span>



| <span data-ttu-id="52d73-115">Valore</span><span class="sxs-lookup"><span data-stu-id="52d73-115">Value</span></span>                                                                                                                                   | <span data-ttu-id="52d73-116">Significato</span><span class="sxs-lookup"><span data-stu-id="52d73-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <span data-ttu-id="52d73-117"><dt>**In alto**</dt></span><span class="sxs-lookup"><span data-stu-id="52d73-117"><dt>**top**</dt></span></span> </dl>          | <span data-ttu-id="52d73-118">Distanza tra il bordo superiore e il testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="52d73-118">Distance between top border and top of tooltip text, in pixels.</span></span><br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <span data-ttu-id="52d73-119"><dt>**sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="52d73-119"><dt>**left**</dt></span></span> </dl>       | <span data-ttu-id="52d73-120">Distanza tra il bordo sinistro e il lato sinistro del testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="52d73-120">Distance between left border and left end of tooltip text, in pixels.</span></span><br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <span data-ttu-id="52d73-121"><dt>**parte inferiore**</dt></span><span class="sxs-lookup"><span data-stu-id="52d73-121"><dt>**bottom**</dt></span></span> </dl> | <span data-ttu-id="52d73-122">Distanza tra il bordo inferiore e il testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="52d73-122">Distance between bottom border and bottom of tooltip text, in pixels.</span></span><br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <span data-ttu-id="52d73-123"><dt>**Ok**</dt></span><span class="sxs-lookup"><span data-stu-id="52d73-123"><dt>**right**</dt></span></span> </dl>    | <span data-ttu-id="52d73-124">Distanza tra il bordo destro e l'estremità destra del testo della descrizione comando, in pixel.</span><span class="sxs-lookup"><span data-stu-id="52d73-124">Distance between right border and right end of tooltip text, in pixels.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d73-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52d73-125">Return value</span></span>

<span data-ttu-id="52d73-126">Il valore restituito per questo messaggio non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="52d73-126">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d73-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="52d73-127">Remarks</span></span>

<span data-ttu-id="52d73-128">Questo messaggio non ha alcun effetto quando l'applicazione viene eseguita in Windows Vista e gli stili di visualizzazione sono abilitati per la descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="52d73-128">This message has no effect when the application runs on Windows Vista and visual styles are enabled for the tooltip.</span></span> <span data-ttu-id="52d73-129">È possibile disabilitare gli stili di visualizzazione per la descrizione comando usando [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span><span class="sxs-lookup"><span data-stu-id="52d73-129">You can disable visual styles for the tooltip by using [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).</span></span>

## <a name="requirements"></a><span data-ttu-id="52d73-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52d73-130">Requirements</span></span>



| <span data-ttu-id="52d73-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="52d73-131">Requirement</span></span> | <span data-ttu-id="52d73-132">Valore</span><span class="sxs-lookup"><span data-stu-id="52d73-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52d73-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52d73-133">Minimum supported client</span></span><br/> | <span data-ttu-id="52d73-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52d73-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52d73-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52d73-135">Minimum supported server</span></span><br/> | <span data-ttu-id="52d73-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52d73-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52d73-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52d73-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d73-138"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d73-138"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52d73-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52d73-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d73-140">**GetMargin TTM \_**</span><span class="sxs-lookup"><span data-stu-id="52d73-140">**TTM\_GETMARGIN**</span></span>](ttm-getmargin.md)
</dt> </dl>

 

