---
title: Messaggio WM_MBUTTONDOWN (winuser. h)
description: Inviato quando l'utente preme il pulsante centrale del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 5181a425-2577-4806-8926-1075a1a756ee
keywords:
- Input della tastiera e del mouse WM_MBUTTONDOWN messaggio
topic_type:
- apiref
api_name:
- WM_MBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b0f7ce257dd50ad16eda3c13feef73890fbbfd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301426"
---
# <a name="wm_mbuttondown-message"></a><span data-ttu-id="3008e-104">\_Messaggio MBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="3008e-104">WM\_MBUTTONDOWN message</span></span>

<span data-ttu-id="3008e-105">Inviato quando l'utente preme il pulsante centrale del mouse mentre il cursore si trova nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="3008e-105">Posted when the user presses the middle mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="3008e-106">Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="3008e-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="3008e-107">In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="3008e-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="3008e-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3008e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MBUTTONDOWN                  0x0207
```



## <a name="parameters"></a><span data-ttu-id="3008e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3008e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3008e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3008e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3008e-111">Indica se varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="3008e-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="3008e-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3008e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3008e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3008e-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="3008e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="3008e-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="3008e-115"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="3008e-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="3008e-116">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="3008e-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="3008e-117"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="3008e-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="3008e-118">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="3008e-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="3008e-119"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="3008e-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="3008e-120">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="3008e-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="3008e-121"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="3008e-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="3008e-122">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="3008e-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="3008e-123"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="3008e-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="3008e-124">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="3008e-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="3008e-125"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="3008e-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="3008e-126">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="3008e-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="3008e-127"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="3008e-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="3008e-128">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="3008e-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3008e-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3008e-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3008e-130">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="3008e-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="3008e-131">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="3008e-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="3008e-132">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="3008e-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="3008e-133">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="3008e-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3008e-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3008e-134">Return value</span></span>

<span data-ttu-id="3008e-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="3008e-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3008e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="3008e-136">Remarks</span></span>

<span data-ttu-id="3008e-137">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="3008e-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="3008e-138">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="3008e-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="3008e-139">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="3008e-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="3008e-140">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="3008e-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3008e-141">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="3008e-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="3008e-142">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="3008e-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="3008e-143">Per rilevare che è stato premuto il tasto ALT, controllare se [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) con il **\_ menu VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="3008e-143">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="3008e-144">Si noti che questo non deve essere [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="3008e-144">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="3008e-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3008e-145">Requirements</span></span>



| <span data-ttu-id="3008e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="3008e-146">Requirement</span></span> | <span data-ttu-id="3008e-147">Valore</span><span class="sxs-lookup"><span data-stu-id="3008e-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3008e-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3008e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3008e-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3008e-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3008e-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3008e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3008e-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3008e-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3008e-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3008e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3008e-153"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3008e-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3008e-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3008e-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="3008e-155">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3008e-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3008e-156">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="3008e-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="3008e-157">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="3008e-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="3008e-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="3008e-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="3008e-159">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="3008e-159">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="3008e-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="3008e-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="3008e-161">**\_MBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="3008e-161">**WM\_MBUTTONDBLCLK**</span></span>](wm-mbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="3008e-162">**\_MBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="3008e-162">**WM\_MBUTTONUP**</span></span>](wm-mbuttonup.md)
</dt> <dt>

<span data-ttu-id="3008e-163">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3008e-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3008e-164">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="3008e-164">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="3008e-165">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="3008e-165">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3008e-166">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="3008e-166">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="3008e-167">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3008e-167">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

