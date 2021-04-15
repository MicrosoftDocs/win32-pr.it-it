---
title: Messaggio WM_MBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic con il pulsante centrale del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 97167941-93bc-4b83-adff-8ca7a3b2591e
keywords:
- Input della tastiera e del mouse WM_MBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_MBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9dd012051e9845fa2de608725f0f8b6af38334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517613"
---
# <a name="wm_mbuttondblclk-message"></a><span data-ttu-id="8af53-104">\_Messaggio MBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="8af53-104">WM\_MBUTTONDBLCLK message</span></span>

<span data-ttu-id="8af53-105">Inviato quando l'utente fa doppio clic con il pulsante centrale del mouse mentre il cursore si trova nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="8af53-105">Posted when the user double-clicks the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="8af53-106">Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="8af53-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="8af53-107">In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="8af53-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="8af53-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8af53-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONDBLCLK                0x0209
```



## <a name="parameters"></a><span data-ttu-id="8af53-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8af53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8af53-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8af53-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af53-111">Indica se varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="8af53-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="8af53-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8af53-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="8af53-113">Valore</span><span class="sxs-lookup"><span data-stu-id="8af53-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="8af53-114">Significato</span><span class="sxs-lookup"><span data-stu-id="8af53-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="8af53-115"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="8af53-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="8af53-116">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="8af53-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="8af53-117"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="8af53-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="8af53-118">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="8af53-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="8af53-119"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="8af53-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="8af53-120">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="8af53-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="8af53-121"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="8af53-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="8af53-122">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="8af53-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="8af53-123"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="8af53-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="8af53-124">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="8af53-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="8af53-125"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="8af53-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="8af53-126">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="8af53-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="8af53-127"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="8af53-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="8af53-128">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="8af53-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="8af53-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8af53-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8af53-130">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="8af53-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="8af53-131">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="8af53-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="8af53-132">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="8af53-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="8af53-133">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="8af53-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8af53-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8af53-134">Return value</span></span>

<span data-ttu-id="8af53-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="8af53-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8af53-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="8af53-136">Remarks</span></span>

<span data-ttu-id="8af53-137">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="8af53-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="8af53-138">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="8af53-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="8af53-139">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8af53-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="8af53-140">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="8af53-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8af53-141">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="8af53-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="8af53-142">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="8af53-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="8af53-143">Solo le finestre con lo stile **cs \_ DBLCLKS** possono ricevere messaggi **WM \_ MBUTTONDBLCLK** , generati dal sistema quando l'utente preme, rilascia e preme di nuovo il pulsante centrale del mouse nel limite di tempo doppio clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="8af53-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_MBUTTONDBLCLK** messages, which the system generates when the user presses, releases, and again presses the middle mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="8af53-144">Facendo doppio clic sul pulsante centrale del mouse vengono effettivamente generati quattro messaggi: [**WM \_ MBUTTONDOWN**](wm-mbuttondown.md), [**WM \_ MBUTTONUP**](wm-mbuttonup.md), **WM \_ MBUTTONDBLCLK** e **WM \_ MBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="8af53-144">Double-clicking the middle mouse button actually generates four messages: [**WM\_MBUTTONDOWN**](wm-mbuttondown.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), **WM\_MBUTTONDBLCLK**, and **WM\_MBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="8af53-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8af53-145">Requirements</span></span>



| <span data-ttu-id="8af53-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="8af53-146">Requirement</span></span> | <span data-ttu-id="8af53-147">Valore</span><span class="sxs-lookup"><span data-stu-id="8af53-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8af53-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8af53-148">Minimum supported client</span></span><br/> | <span data-ttu-id="8af53-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8af53-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8af53-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8af53-150">Minimum supported server</span></span><br/> | <span data-ttu-id="8af53-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8af53-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8af53-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8af53-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8af53-153"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8af53-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8af53-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8af53-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="8af53-155">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8af53-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8af53-156">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="8af53-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="8af53-157">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="8af53-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="8af53-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="8af53-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="8af53-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="8af53-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="8af53-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="8af53-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="8af53-161">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="8af53-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="8af53-162">**\_MBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="8af53-162">**WM\_MBUTTONDOWN**</span></span>](wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8af53-163">**\_MBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="8af53-163">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
</dt> <dt>

<span data-ttu-id="8af53-164">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8af53-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8af53-165">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="8af53-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="8af53-166">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="8af53-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8af53-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="8af53-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="8af53-168">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8af53-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

