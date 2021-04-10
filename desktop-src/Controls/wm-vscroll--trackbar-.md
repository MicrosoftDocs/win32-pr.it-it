---
title: Codice di notifica di WM_VSCROLL (TrackBar) (winuser. h)
description: Il \_ messaggio WM VSCROLL viene inviato al proprietario di un controllo TrackBar verticale quando il dispositivo di scorrimento cambia posizione. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: E491E210-9605-4ABB-A667-471830DA7C2B
keywords:
- Codice di notifica di WM_VSCROLL (TrackBar)-controlli Windows
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
ms.openlocfilehash: d1e13b07fab3335bf99469cd43ed1caa10373a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120262"
---
# <a name="wm_vscroll-trackbar-notification-code"></a><span data-ttu-id="5ac4d-105">Codice di notifica di WM \_ VSCROLL (TrackBar)</span><span class="sxs-lookup"><span data-stu-id="5ac4d-105">WM\_VSCROLL (Trackbar) notification code</span></span>

<span data-ttu-id="5ac4d-106">Il messaggio **WM \_ VSCROLL** viene inviato al proprietario di un controllo TrackBar verticale quando il dispositivo di scorrimento cambia posizione.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-106">The **WM\_VSCROLL** message is sent to the owner of a vertical trackbar control when the slider changes position.</span></span>

<span data-ttu-id="5ac4d-107">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ac4d-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5ac4d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ac4d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac4d-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la posizione corrente del dispositivo di scorrimento se [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) è TB \_ THUMBPOSITION o TB \_ THUMBTRACK.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the slider if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is TB\_THUMBPOSITION or TB\_THUMBTRACK.</span></span> <span data-ttu-id="5ac4d-111">Per tutti gli altri codici di notifica, la parola più ordinata è zero; inviare il messaggio [**TBM \_ GETPOS**](tbm-getpos.md) per determinare la posizione del dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-111">For all other notification codes, the high-order word is zero; send the [**TBM\_GETPOS**](tbm-getpos.md) message to determine the slider position.</span></span>

<span data-ttu-id="5ac4d-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica un codice di notifica che indica l'interazione dell'utente con il TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a notification code that indicates the user's interaction with the trackbar.</span></span> <span data-ttu-id="5ac4d-113">Questa parola può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-113">This word can be one of the following values.</span></span>



| <span data-ttu-id="5ac4d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac4d-114">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="5ac4d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5ac4d-115">Meaning</span></span>                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TB_BOTTOM"></span><span id="tb_bottom"></span><dl> <span data-ttu-id="5ac4d-116"><dt>**TB in \_ basso**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-116"><dt>**TB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="5ac4d-117">L'utente ha premuto il tasto fine ([**VK \_ end**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-117">The user pressed the END key ([**VK\_END**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                                                          |
| <span id="TB_ENDTRACK"></span><span id="tb_endtrack"></span><dl> <span data-ttu-id="5ac4d-118"><dt>**TB \_ ENDTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-118"><dt>**TB\_ENDTRACK**</dt></span></span> </dl>                | <span data-ttu-id="5ac4d-119">Il TrackBar ha ricevuto [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup), vale a dire che l'utente ha rilasciato una chiave che ha inviato un codice di chiave virtuale pertinente.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-119">The trackbar received [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup), meaning that the user released a key that sent a relevant virtual key code.</span></span> <br/>                                           |
| <span id="TB_LINEDOWN"></span><span id="tb_linedown"></span><dl> <span data-ttu-id="5ac4d-120"><dt>**TB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-120"><dt>**TB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="5ac4d-121">L'utente ha premuto il tasto freccia destra ([**VK a \_ destra**](/windows/desktop/inputdev/virtual-key-codes)) o freccia giù ([**VK in \_ basso**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-121">The user pressed the RIGHT ARROW ([**VK\_RIGHT**](/windows/desktop/inputdev/virtual-key-codes)) or DOWN ARROW ([**VK\_DOWN**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/> |
| <span id="TB_LINEUP"></span><span id="tb_lineup"></span><dl> <span data-ttu-id="5ac4d-122"><dt>**\_lineup TB**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-122"><dt>**TB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="5ac4d-123">L'utente ha premuto il tasto freccia sinistra ([**VK a \_ sinistra**](/windows/desktop/inputdev/virtual-key-codes)) o freccia su ([**VK \_ in alto**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-123">The user pressed the LEFT ARROW ([**VK\_LEFT**](/windows/desktop/inputdev/virtual-key-codes)) or UP ARROW ([**VK\_UP**](/windows/desktop/inputdev/virtual-key-codes)) key.</span></span><br/>             |
| <span id="TB_PAGEDOWN"></span><span id="tb_pagedown"></span><dl> <span data-ttu-id="5ac4d-124"><dt>**TB \_ PGGIÙ**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-124"><dt>**TB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="5ac4d-125">L'utente ha fatto clic sul canale sotto o a destra del dispositivo di scorrimento ([**VK \_ Avanti**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-125">The user clicked the channel below or to the right of the slider ([**VK\_NEXT**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                   |
| <span id="TB_PAGEUP"></span><span id="tb_pageup"></span><dl> <span data-ttu-id="5ac4d-126"><dt>**TB \_ PAGEUP**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-126"><dt>**TB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="5ac4d-127">L'utente ha fatto clic sul canale sopra o a sinistra del dispositivo di scorrimento ([**VK \_ precedente**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-127">The user clicked the channel above or to the left of the slider ([**VK\_PRIOR**](/windows/desktop/inputdev/virtual-key-codes)).</span></span><br/>                                                 |
| <span id="TB_THUMBPOSITION"></span><span id="tb_thumbposition"></span><dl> <span data-ttu-id="5ac4d-128"><dt>**TB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-128"><dt>**TB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="5ac4d-129">Il TrackBar ha ricevuto [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) dopo un \_ codice di notifica THUMBTRACK TB.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-129">The trackbar received [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) following a TB\_THUMBTRACK notification code.</span></span><br/>                                                                   |
| <span id="TB_THUMBTRACK"></span><span id="tb_thumbtrack"></span><dl> <span data-ttu-id="5ac4d-130"><dt>**TB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-130"><dt>**TB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="5ac4d-131">L'utente ha trascinato il dispositivo di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-131">The user dragged the slider.</span></span><br/>                                                                                                                                                     |
| <span id="TB_TOP"></span><span id="tb_top"></span><dl> <span data-ttu-id="5ac4d-132"><dt>**TB \_ superiore**</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-132"><dt>**TB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="5ac4d-133">L'utente ha premuto il tasto HOME ([**VK \_ Home**](/windows/desktop/inputdev/virtual-key-codes)).</span><span class="sxs-lookup"><span data-stu-id="5ac4d-133">The user pressed the HOME key ([**VK\_HOME**](/windows/desktop/inputdev/virtual-key-codes)).</span></span> <br/>                                                                                     |



 

</dd> <dt>

<span data-ttu-id="5ac4d-134">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac4d-134">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac4d-135">Handle per il controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-135">The handle to the trackbar control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac4d-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ac4d-136">Return value</span></span>

<span data-ttu-id="5ac4d-137">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac4d-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ac4d-138">Remarks</span></span>

<span data-ttu-id="5ac4d-139">Il \_ codice THUMBTRACK TB viene in genere usato dalle applicazioni che forniscono commenti e suggerimenti quando l'utente trascina la casella di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-139">The TB\_THUMBTRACK code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="5ac4d-140">Si noti che il messaggio **WM \_ VSCROLL** contiene solo 16 bit di dati sulla posizione.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-140">Note that the **WM\_VSCROLL** message carries only 16 bits of position data.</span></span> <span data-ttu-id="5ac4d-141">Pertanto, le applicazioni che si basano esclusivamente su **WM \_ VSCROLL** (e [**WM \_ HSCROLL**](wm-hscroll--trackbar-.md)) per i dati della posizione del dispositivo di scorrimento hanno un valore di posizione massimo pratica di 65.535.</span><span class="sxs-lookup"><span data-stu-id="5ac4d-141">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll--trackbar-.md)) for slider position data have a practical maximum position value of 65,535.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac4d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac4d-142">Requirements</span></span>



| <span data-ttu-id="5ac4d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac4d-143">Requirement</span></span> | <span data-ttu-id="5ac4d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac4d-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4d-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac4d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac4d-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ac4d-146">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ac4d-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac4d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac4d-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ac4d-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ac4d-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ac4d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac4d-150"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac4d-150"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac4d-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac4d-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ac4d-152">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5ac4d-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac4d-153">**\_HSCROLL WM**</span><span class="sxs-lookup"><span data-stu-id="5ac4d-153">**WM\_HSCROLL**</span></span>](wm-hscroll--trackbar-.md)
</dt> </dl>

 

