---
title: WM_LBUTTONUP messaggio (Winuser.h)
description: Pubblicato quando l'utente rilascia il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- WM_LBUTTONUP messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_LBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe921ffe68359efe15aa0782c5c8543fd0870fa
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335395"
---
# <a name="wm_lbuttonup-message"></a><span data-ttu-id="17fb9-104">Messaggio WM \_ LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="17fb9-104">WM\_LBUTTONUP message</span></span>

<span data-ttu-id="17fb9-105">Pubblicato quando l'utente rilascia il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="17fb9-105">Posted when the user releases the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="17fb9-106">Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="17fb9-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="17fb9-107">In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="17fb9-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="17fb9-108">Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17fb9-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a><span data-ttu-id="17fb9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17fb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17fb9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17fb9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17fb9-111">Indica se varie chiavi virtuali non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="17fb9-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="17fb9-112">Questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="17fb9-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="17fb9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="17fb9-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="17fb9-114">Significato</span><span class="sxs-lookup"><span data-stu-id="17fb9-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="17fb9-115"><dt>**MK \_ CONTROLLO**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="17fb9-116">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="17fb9-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="17fb9-117"><dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="17fb9-118">Il pulsante centrale del mouse è in basso.</span><span class="sxs-lookup"><span data-stu-id="17fb9-118">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="17fb9-119"><dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="17fb9-120">Il pulsante destro del mouse è verso il basso.</span><span class="sxs-lookup"><span data-stu-id="17fb9-120">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="17fb9-121"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="17fb9-122">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="17fb9-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="17fb9-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="17fb9-124">Il primo pulsante X è in basso.</span><span class="sxs-lookup"><span data-stu-id="17fb9-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="17fb9-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="17fb9-126">Il secondo pulsante X è in basso.</span><span class="sxs-lookup"><span data-stu-id="17fb9-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="17fb9-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17fb9-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17fb9-128">La parola più bassa specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="17fb9-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="17fb9-129">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="17fb9-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="17fb9-130">La parola più alta specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="17fb9-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="17fb9-131">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="17fb9-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17fb9-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17fb9-132">Return value</span></span>

<span data-ttu-id="17fb9-133">Se un'applicazione elabora questo messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="17fb9-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="17fb9-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="17fb9-134">Remarks</span></span>

<span data-ttu-id="17fb9-135">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="17fb9-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="17fb9-136">Come indicato in precedenza, la coordinata x è nell'ordine più basso **del** valore lParam. La coordinata y è nell'ordine più  breve **(entrambi** rappresentano valori con segno perché possono assumere valori negativi nei sistemi con più monitor).</span><span class="sxs-lookup"><span data-stu-id="17fb9-136">As noted above, the x-coordinate is in the low-order **short** of the lParam value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="17fb9-137">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="17fb9-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="17fb9-138">È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.</span><span class="sxs-lookup"><span data-stu-id="17fb9-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17fb9-139">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor.</span><span class="sxs-lookup"><span data-stu-id="17fb9-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="17fb9-140">I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="17fb9-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17fb9-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17fb9-141">Requirements</span></span>



| <span data-ttu-id="17fb9-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="17fb9-142">Requirement</span></span> | <span data-ttu-id="17fb9-143">Valore</span><span class="sxs-lookup"><span data-stu-id="17fb9-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17fb9-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17fb9-144">Minimum supported client</span></span><br/> | <span data-ttu-id="17fb9-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17fb9-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="17fb9-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17fb9-146">Minimum supported server</span></span><br/> | <span data-ttu-id="17fb9-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="17fb9-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="17fb9-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17fb9-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="17fb9-149"><dt>Winuser.h (includere Windowsx.h)</dt></span><span class="sxs-lookup"><span data-stu-id="17fb9-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17fb9-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17fb9-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="17fb9-151">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="17fb9-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17fb9-152">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="17fb9-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="17fb9-153">**GET \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="17fb9-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="17fb9-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="17fb9-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="17fb9-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="17fb9-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="17fb9-156">**WM \_ LBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="17fb9-156">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="17fb9-157">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="17fb9-157">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

<span data-ttu-id="17fb9-158">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="17fb9-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17fb9-159">Mouse Input</span><span class="sxs-lookup"><span data-stu-id="17fb9-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="17fb9-160">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="17fb9-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="17fb9-161">**MAKEPOINT**</span><span class="sxs-lookup"><span data-stu-id="17fb9-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="17fb9-162">[**Punti**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="17fb9-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

