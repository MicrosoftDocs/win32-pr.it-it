---
title: Messaggio EM_SCROLL (winuser. h)
description: Scorre il testo verticalmente in un controllo di modifica su più righe. Questo messaggio equivale all'invio \_ di un messaggio WM VSCROLL al controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Controlli di Windows Message EM_SCROLL
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121495"
---
# <a name="em_scroll-message"></a><span data-ttu-id="81f2c-106">\_Messaggio di scorrimento em</span><span class="sxs-lookup"><span data-stu-id="81f2c-106">EM\_SCROLL message</span></span>

<span data-ttu-id="81f2c-107">Scorre il testo verticalmente in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="81f2c-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="81f2c-108">Questo messaggio equivale all'invio di un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) al controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="81f2c-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="81f2c-109">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="81f2c-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="81f2c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="81f2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f2c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81f2c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f2c-112">Azione da eseguire sulla barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="81f2c-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="81f2c-113">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="81f2c-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="81f2c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="81f2c-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="81f2c-115">Significato</span><span class="sxs-lookup"><span data-stu-id="81f2c-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="81f2c-116"><dt>**\_LINEDOWN SB**</dt></span><span class="sxs-lookup"><span data-stu-id="81f2c-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="81f2c-117">Scorre verso il basso di una riga.</span><span class="sxs-lookup"><span data-stu-id="81f2c-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="81f2c-118"><dt>**\_lineup SB**</dt></span><span class="sxs-lookup"><span data-stu-id="81f2c-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="81f2c-119">Scorre verso l'alto di una riga.</span><span class="sxs-lookup"><span data-stu-id="81f2c-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="81f2c-120"><dt>**\_PGGIÙ SB**</dt></span><span class="sxs-lookup"><span data-stu-id="81f2c-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="81f2c-121">Scorre verso il basso di una pagina.</span><span class="sxs-lookup"><span data-stu-id="81f2c-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="81f2c-122"><dt>**\_PAGEUP SB**</dt></span><span class="sxs-lookup"><span data-stu-id="81f2c-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="81f2c-123">Scorre verso l'alto di una pagina.</span><span class="sxs-lookup"><span data-stu-id="81f2c-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="81f2c-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81f2c-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81f2c-125">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="81f2c-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f2c-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81f2c-126">Return value</span></span>

<span data-ttu-id="81f2c-127">Se il messaggio ha esito positivo, [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) del valore restituito è **true** e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è il numero di righe Scorrete dal comando.</span><span class="sxs-lookup"><span data-stu-id="81f2c-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="81f2c-128">Il numero restituito potrebbe non corrispondere al numero effettivo di righe a scorrimento se lo scorrimento si sposta all'inizio o alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="81f2c-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="81f2c-129">Se il parametro *wParam* specifica un valore non valido, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="81f2c-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f2c-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="81f2c-130">Remarks</span></span>

<span data-ttu-id="81f2c-131">Per scorrere fino a una riga o a una posizione specifica del carattere, usare il messaggio [**\_ LINESCROLL em**](em-linescroll.md) .</span><span class="sxs-lookup"><span data-stu-id="81f2c-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="81f2c-132">Per scorrere il punto di inserimento nella visualizzazione, usare il messaggio [**\_ SCROLLCARET em**](em-scrollcaret.md) .</span><span class="sxs-lookup"><span data-stu-id="81f2c-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="81f2c-133">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="81f2c-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="81f2c-134">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="81f2c-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81f2c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81f2c-135">Requirements</span></span>



| <span data-ttu-id="81f2c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="81f2c-136">Requirement</span></span> | <span data-ttu-id="81f2c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="81f2c-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81f2c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81f2c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="81f2c-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81f2c-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81f2c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81f2c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="81f2c-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81f2c-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81f2c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81f2c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f2c-143"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81f2c-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81f2c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81f2c-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="81f2c-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="81f2c-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81f2c-146">**\_LINESCROLL em**</span><span class="sxs-lookup"><span data-stu-id="81f2c-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="81f2c-147">**\_SCROLLCARET em**</span><span class="sxs-lookup"><span data-stu-id="81f2c-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="81f2c-148">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="81f2c-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

