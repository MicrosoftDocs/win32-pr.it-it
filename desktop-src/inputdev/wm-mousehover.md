---
title: Messaggio WM_MOUSEHOVER (winuser. h)
description: Inserito in una finestra quando il cursore passa sull'area client della finestra per il periodo di tempo specificato in una chiamata precedente a TrackMouseEvent.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- Input della tastiera e del mouse WM_MOUSEHOVER messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476145"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="568f5-104">\_Messaggio MOUSEHOVER WM</span><span class="sxs-lookup"><span data-stu-id="568f5-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="568f5-105">Inserito in una finestra quando il cursore passa sull'area client della finestra per il periodo di tempo specificato in una chiamata precedente a [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="568f5-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="568f5-106">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="568f5-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="568f5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="568f5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="568f5-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="568f5-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="568f5-109">Indica se varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="568f5-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="568f5-110">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="568f5-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="568f5-111">Valore</span><span class="sxs-lookup"><span data-stu-id="568f5-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="568f5-112">Significato</span><span class="sxs-lookup"><span data-stu-id="568f5-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="568f5-113"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="568f5-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="568f5-114">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="568f5-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="568f5-115"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="568f5-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="568f5-116">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="568f5-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="568f5-117"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="568f5-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="568f5-118">Il pulsante centrale del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="568f5-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="568f5-119"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="568f5-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="568f5-120">Il pulsante destro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="568f5-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="568f5-121"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="568f5-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="568f5-122">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="568f5-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="568f5-123"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="568f5-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="568f5-124">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="568f5-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="568f5-125"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="568f5-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="568f5-126">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="568f5-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="568f5-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="568f5-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="568f5-128">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="568f5-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="568f5-129">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="568f5-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="568f5-130">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="568f5-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="568f5-131">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="568f5-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="568f5-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="568f5-132">Return value</span></span>

<span data-ttu-id="568f5-133">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="568f5-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="568f5-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="568f5-134">Remarks</span></span>

<span data-ttu-id="568f5-135">Il rilevamento del passaggio del mouse si interrompe quando viene generato **WM \_ MOUSEHOVER** .</span><span class="sxs-lookup"><span data-stu-id="568f5-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="568f5-136">Se è necessario tenere traccia del comportamento del passaggio del mouse, l'applicazione deve chiamare nuovamente [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) .</span><span class="sxs-lookup"><span data-stu-id="568f5-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="568f5-137">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="568f5-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="568f5-138">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="568f5-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="568f5-139">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="568f5-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="568f5-140">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="568f5-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="568f5-141">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="568f5-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="568f5-142">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="568f5-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="568f5-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="568f5-143">Requirements</span></span>



| <span data-ttu-id="568f5-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="568f5-144">Requirement</span></span> | <span data-ttu-id="568f5-145">Valore</span><span class="sxs-lookup"><span data-stu-id="568f5-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="568f5-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="568f5-146">Minimum supported client</span></span><br/> | <span data-ttu-id="568f5-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="568f5-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="568f5-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="568f5-148">Minimum supported server</span></span><br/> | <span data-ttu-id="568f5-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="568f5-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="568f5-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="568f5-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="568f5-151"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="568f5-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="568f5-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="568f5-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="568f5-153">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="568f5-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="568f5-154">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="568f5-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="568f5-155">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="568f5-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="568f5-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="568f5-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="568f5-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="568f5-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="568f5-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="568f5-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="568f5-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="568f5-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="568f5-160">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="568f5-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="568f5-161">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="568f5-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="568f5-162">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="568f5-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="568f5-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="568f5-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="568f5-164">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="568f5-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

