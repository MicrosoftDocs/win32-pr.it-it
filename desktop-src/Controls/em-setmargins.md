---
title: Messaggio EM_SETMARGINS (winuser. h)
description: Imposta le larghezze dei margini sinistro e destro per un controllo di modifica. Il messaggio ridisegnato il controllo in modo da riflettere i nuovi margini. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Controlli di Windows Message EM_SETMARGINS
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964393"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="cdc3d-106">\_Messaggio SEmargini em</span><span class="sxs-lookup"><span data-stu-id="cdc3d-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="cdc3d-107">Imposta le larghezze dei margini sinistro e destro per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="cdc3d-108">Il messaggio ridisegnato il controllo in modo da riflettere i nuovi margini.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="cdc3d-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdc3d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdc3d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc3d-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdc3d-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc3d-112">Margini da impostare.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-112">The margins to set.</span></span> <span data-ttu-id="cdc3d-113">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cdc3d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="cdc3d-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="cdc3d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="cdc3d-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="cdc3d-116"><dt>**\_LeftMargin EC**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3d-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="cdc3d-117">Imposta il margine sinistro.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="cdc3d-118"><dt>**\_RightMargin EC**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3d-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="cdc3d-119">Imposta il margine destro.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="cdc3d-120"><dt>**\_USEFONTINFO EC**</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3d-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="cdc3d-121">**Controlli Rich Edit:** Imposta i margini sinistro e destro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="cdc3d-122">Se per il controllo non è stato impostato alcun tipo di carattere, i margini vengono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="cdc3d-123">Il parametro *lParam* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="cdc3d-124">**Controlli di modifica:** Impossibile utilizzare il valore **EC \_ USEFONTINFO** nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cdc3d-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="cdc3d-125">Può essere usato solo nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cdc3d-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cdc3d-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdc3d-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdc3d-127">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la nuova larghezza del margine sinistro, in pixel.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="cdc3d-128">Questo valore viene ignorato se *wParam* non include la **\_ LeftMargin EC**.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="cdc3d-129">**Modificare i controlli e rich edit 3,0 e versioni successive:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) può specificare il valore **EC \_ USEFONTINFO** per impostare il margine sinistro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="cdc3d-130">Se per il controllo non è stato impostato alcun carattere, il margine è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="cdc3d-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la nuova larghezza del margine destro, in pixel.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="cdc3d-132">Questo valore viene ignorato se *wParam* non include la **\_ RightMargin EC**.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="cdc3d-133">**Modificare i controlli e rich edit 3,0 e versioni successive:** [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) può specificare il valore **EC \_ USEFONTINFO** per impostare il margine destro su una larghezza ridotta calcolata usando le metriche di testo del tipo di carattere corrente del controllo.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="cdc3d-134">Se per il controllo non è stato impostato alcun carattere, il margine è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc3d-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdc3d-135">Return value</span></span>

<span data-ttu-id="cdc3d-136">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc3d-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdc3d-137">Remarks</span></span>

<span data-ttu-id="cdc3d-138">**Controlli di modifica:** Non è possibile usare **EC \_ USEFONTINFO** nel parametro *wParam* , ma è possibile usarlo nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cdc3d-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="cdc3d-139">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cdc3d-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="cdc3d-140">Tutte le versioni Rich Edit supportano l'uso di **EC \_ USEFONTINFO** nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cdc3d-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="cdc3d-141">Tuttavia, solo Microsoft Rich Edit 3,0 e versioni successive supportano l'uso di **EC \_ USEFONTINFO** nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="cdc3d-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="cdc3d-142">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="cdc3d-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc3d-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdc3d-143">Requirements</span></span>



| <span data-ttu-id="cdc3d-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdc3d-144">Requirement</span></span> | <span data-ttu-id="cdc3d-145">Valore</span><span class="sxs-lookup"><span data-stu-id="cdc3d-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc3d-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc3d-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc3d-147">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdc3d-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cdc3d-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdc3d-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc3d-149">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cdc3d-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cdc3d-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdc3d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc3d-151"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc3d-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdc3d-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdc3d-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc3d-153">**\_GETmargini em**</span><span class="sxs-lookup"><span data-stu-id="cdc3d-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

