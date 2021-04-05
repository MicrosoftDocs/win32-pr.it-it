---
title: Messaggio WM_XBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- Input della tastiera e del mouse WM_XBUTTONDBLCLK messaggio
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742343"
---
# <a name="wm_xbuttondblclk-message"></a><span data-ttu-id="2cc8e-104">\_Messaggio XBUTTONDBLCLK WM</span><span class="sxs-lookup"><span data-stu-id="2cc8e-104">WM\_XBUTTONDBLCLK message</span></span>

<span data-ttu-id="2cc8e-105">Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-105">Posted when the user double-clicks the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="2cc8e-106">Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="2cc8e-107">In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="2cc8e-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2cc8e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a><span data-ttu-id="2cc8e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cc8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc8e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cc8e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc8e-111">La parola più bassa indica se le varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="2cc8e-112">Può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="2cc8e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc8e-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="2cc8e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc8e-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="2cc8e-115"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="2cc8e-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="2cc8e-116">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="2cc8e-117"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="2cc8e-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="2cc8e-118">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="2cc8e-119"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="2cc8e-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="2cc8e-120">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="2cc8e-121"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="2cc8e-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="2cc8e-122">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="2cc8e-123"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="2cc8e-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="2cc8e-124">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="2cc8e-125"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="2cc8e-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="2cc8e-126">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="2cc8e-127"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="2cc8e-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="2cc8e-128">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="2cc8e-129">La parola più ordinata indica il pulsante su cui è stato fatto doppio clic.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-129">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="2cc8e-130">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-130">It can be one of the following values.</span></span>



| <span data-ttu-id="2cc8e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc8e-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="2cc8e-132">Significato</span><span class="sxs-lookup"><span data-stu-id="2cc8e-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="2cc8e-133"><dt></dt> <dt>0x0001</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="2cc8e-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="2cc8e-134">È stato fatto doppio clic sul primo pulsante X.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-134">The first X button was double-clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="2cc8e-135"><dt></dt> <dt>0x0002</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="2cc8e-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="2cc8e-136">È stato fatto doppio clic sul secondo pulsante X.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-136">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2cc8e-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cc8e-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc8e-138">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="2cc8e-139">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="2cc8e-140">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="2cc8e-141">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc8e-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cc8e-142">Return value</span></span>

<span data-ttu-id="2cc8e-143">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="2cc8e-144">Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc8e-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cc8e-145">Remarks</span></span>

<span data-ttu-id="2cc8e-146">Usare il codice seguente per ottenere le informazioni nel parametro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="2cc8e-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="2cc8e-147">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="2cc8e-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="2cc8e-148">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="2cc8e-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="2cc8e-149">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="2cc8e-150">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="2cc8e-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2cc8e-151">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="2cc8e-152">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="2cc8e-153">Solo le finestre con lo stile **cs \_ DBLCLKS** possono ricevere messaggi **WM \_ XBUTTONDBLCLK** , generati dal sistema ogni volta che l'utente preme, rilascia e preme di nuovo un pulsante X entro il limite di tempo doppio clic del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-153">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_XBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="2cc8e-154">Facendo doppio clic su uno di questi pulsanti vengono effettivamente generati quattro messaggi: [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md), [**WM \_ XBUTTONUP**](wm-xbuttonup.md), **WM \_ XBUTTONDBLCLK** e **WM \_ XBUTTONUP** .</span><span class="sxs-lookup"><span data-stu-id="2cc8e-154">Double-clicking one of these buttons actually generates four messages: [**WM\_XBUTTONDOWN**](wm-xbuttondown.md), [**WM\_XBUTTONUP**](wm-xbuttonup.md), **WM\_XBUTTONDBLCLK**, and **WM\_XBUTTONUP** again.</span></span>

<span data-ttu-id="2cc8e-155">A differenza dei [**messaggi \_ WM LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)e [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-155">Unlike the [**WM\_LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM\_MBUTTONDBLCLK**](wm-mbuttondblclk.md), and [**WM\_RBUTTONDBLCLK**](wm-rbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="2cc8e-156">In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.</span><span class="sxs-lookup"><span data-stu-id="2cc8e-156">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc8e-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc8e-157">Requirements</span></span>



| <span data-ttu-id="2cc8e-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc8e-158">Requirement</span></span> | <span data-ttu-id="2cc8e-159">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc8e-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc8e-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc8e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc8e-161">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2cc8e-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2cc8e-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc8e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc8e-163">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2cc8e-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2cc8e-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cc8e-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc8e-165"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cc8e-165"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc8e-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cc8e-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="2cc8e-167">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2cc8e-168">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-168">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="2cc8e-169">**OTTENERE \_ lo stato di un \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-169">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="2cc8e-170">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-170">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="2cc8e-171">**OTTENERE \_ XBUTTON \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-171">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="2cc8e-172">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-172">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="2cc8e-173">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-173">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="2cc8e-174">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-174">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="2cc8e-175">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-175">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="2cc8e-176">**\_XBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-176">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

[<span data-ttu-id="2cc8e-177">**\_XBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-177">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="2cc8e-178">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-178">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2cc8e-179">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="2cc8e-179">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="2cc8e-180">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-180">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="2cc8e-181">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="2cc8e-181">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="2cc8e-182">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2cc8e-182">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

