---
title: Messaggio WM_HSCROLL (winuser. h)
description: Il \_ messaggio WM HSCROLL viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento orizzontale standard della finestra.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Controlli di Windows Message WM_HSCROLL
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120266"
---
# <a name="wm_hscroll-message"></a><span data-ttu-id="9c57f-104">\_Messaggio HSCROLL WM</span><span class="sxs-lookup"><span data-stu-id="9c57f-104">WM\_HSCROLL message</span></span>

<span data-ttu-id="9c57f-105">Il messaggio **WM \_ HSCROLL** viene inviato a una finestra quando si verifica un evento Scroll nella barra di scorrimento orizzontale standard della finestra.</span><span class="sxs-lookup"><span data-stu-id="9c57f-105">The **WM\_HSCROLL** message is sent to a window when a scroll event occurs in the window's standard horizontal scroll bar.</span></span> <span data-ttu-id="9c57f-106">Questo messaggio viene inoltre inviato al proprietario di un controllo barra di scorrimento orizzontale quando si verifica un evento di scorrimento nel controllo.</span><span class="sxs-lookup"><span data-stu-id="9c57f-106">This message is also sent to the owner of a horizontal scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="9c57f-107">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9c57f-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9c57f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c57f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c57f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c57f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c57f-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente della casella di scorrimento se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è SB \_ THUMBPOSITION o SB THUMBTRACK. \_ in caso contrario, la parola non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="9c57f-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="9c57f-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un valore della barra di scorrimento che indica la richiesta di scorrimento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9c57f-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="9c57f-112">Questa parola può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9c57f-112">This word can be one of the following values.</span></span>



| <span data-ttu-id="9c57f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9c57f-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="9c57f-114">Significato</span><span class="sxs-lookup"><span data-stu-id="9c57f-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="9c57f-115"><dt>**\_ENDSCROLL SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-115"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="9c57f-116">Termina lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-116">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="9c57f-117"><dt>**SB a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-117"><dt>**SB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="9c57f-118">Scorre l'angolo in alto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="9c57f-118">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="9c57f-119"><dt>**SB a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-119"><dt>**SB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="9c57f-120">Scorre verso destra in basso.</span><span class="sxs-lookup"><span data-stu-id="9c57f-120">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="9c57f-121"><dt>**\_LINELEFT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-121"><dt>**SB\_LINELEFT**</dt></span></span> </dl>                | <span data-ttu-id="9c57f-122">Scorre verso sinistra di un'unità.</span><span class="sxs-lookup"><span data-stu-id="9c57f-122">Scrolls left by one unit.</span></span><br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="9c57f-123"><dt>**\_LINERIGHT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-123"><dt>**SB\_LINERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="9c57f-124">Scorre verso destra di un'unità.</span><span class="sxs-lookup"><span data-stu-id="9c57f-124">Scrolls right by one unit.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="9c57f-125"><dt>**\_PAGELEFT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-125"><dt>**SB\_PAGELEFT**</dt></span></span> </dl>                | <span data-ttu-id="9c57f-126">Scorre verso sinistra in base alla larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="9c57f-126">Scrolls left by the width of the window.</span></span><br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="9c57f-127"><dt>**\_PAGERIGHT SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-127"><dt>**SB\_PAGERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="9c57f-128">Scorre verso destra in base alla larghezza della finestra.</span><span class="sxs-lookup"><span data-stu-id="9c57f-128">Scrolls right by the width of the window.</span></span><br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="9c57f-129"><dt>**\_THUMBPOSITION SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-129"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="9c57f-130">L'utente ha trascinato la casella di scorrimento (Thumb) e ha rilasciato il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="9c57f-130">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="9c57f-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione della casella di scorrimento alla fine dell'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="9c57f-132"><dt>**\_THUMBTRACK SB**</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-132"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="9c57f-133">L'utente sta trascinando la casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-133">The user is dragging the scroll box.</span></span> <span data-ttu-id="9c57f-134">Questo messaggio viene inviato ripetutamente fino a quando l'utente rilascia il pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="9c57f-134">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="9c57f-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indica la posizione in cui è stata trascinata la casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-135">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9c57f-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c57f-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c57f-137">Se il messaggio viene inviato da un controllo barra di scorrimento, questo parametro è l'handle per il controllo barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="9c57f-138">Se il messaggio viene inviato da una barra di scorrimento standard, questo parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="9c57f-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c57f-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c57f-139">Return value</span></span>

<span data-ttu-id="9c57f-140">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="9c57f-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c57f-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c57f-141">Remarks</span></span>

<span data-ttu-id="9c57f-142">Il \_ codice di richiesta SB THUMBTRACK viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente trascina la casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="9c57f-143">Se un'applicazione scorre il contenuto della finestra, è necessario reimpostare anche la posizione della casella di scorrimento usando la funzione [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="9c57f-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="9c57f-144">Si noti che il messaggio **WM \_ HSCROLL** contiene solo 16 bit di dati di posizione della casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="9c57f-144">Note that the **WM\_HSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="9c57f-145">Di conseguenza, le applicazioni che si basano esclusivamente su **WM \_ HSCROLL** (e [**WM \_ VSCROLL**](wm-vscroll.md)) per i dati della posizione di scorrimento hanno un valore di posizione massimo pratica pari a 65.535.</span><span class="sxs-lookup"><span data-stu-id="9c57f-145">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="9c57f-146">Tuttavia, poiché le funzioni [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)e [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) supportano i dati di posizione della barra di scorrimento a 32 bit, è possibile aggirare la barriera a 16 bit dei messaggi **WM \_ HSCROLL** e [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="9c57f-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the **WM\_HSCROLL** and [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span> <span data-ttu-id="9c57f-147">Per una descrizione della tecnica, vedere **GetScrollInfo** .</span><span class="sxs-lookup"><span data-stu-id="9c57f-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c57f-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c57f-148">Requirements</span></span>



| <span data-ttu-id="9c57f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c57f-149">Requirement</span></span> | <span data-ttu-id="9c57f-150">Valore</span><span class="sxs-lookup"><span data-stu-id="9c57f-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c57f-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c57f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9c57f-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c57f-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9c57f-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c57f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9c57f-154">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c57f-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c57f-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c57f-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c57f-156"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c57f-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c57f-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c57f-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c57f-158">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9c57f-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c57f-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9c57f-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="9c57f-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="9c57f-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="9c57f-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="9c57f-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="9c57f-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="9c57f-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="9c57f-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="9c57f-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="9c57f-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="9c57f-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="9c57f-165">**\_HSCROLL WM (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="9c57f-165">**WM\_HSCROLL (trackbar)**</span></span>](wm-hscroll--trackbar-.md)
</dt> <dt>

[<span data-ttu-id="9c57f-166">**\_VSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="9c57f-166">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

