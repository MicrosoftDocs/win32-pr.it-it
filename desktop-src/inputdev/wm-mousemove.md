---
title: Messaggio WM_MOUSEMOVE (winuser. h)
description: Inserito in una finestra quando il cursore viene spostato. Se il mouse non viene acquisito, il messaggio viene inserito nella finestra che contiene il cursore. In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.
ms.assetid: 9b99387e-e176-4b20-a05a-bc75928a1367
keywords:
- Input della tastiera e del mouse WM_MOUSEMOVE messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61ffd10edbd58d11c5667fbda9dc0408ea1d72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517607"
---
# <a name="wm_mousemove-message"></a><span data-ttu-id="60055-106">Messaggio di WM \_ MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="60055-106">WM\_MOUSEMOVE message</span></span>

<span data-ttu-id="60055-107">Inserito in una finestra quando il cursore viene spostato.</span><span class="sxs-lookup"><span data-stu-id="60055-107">Posted to a window when the cursor moves.</span></span> <span data-ttu-id="60055-108">Se il mouse non viene acquisito, il messaggio viene inserito nella finestra che contiene il cursore.</span><span class="sxs-lookup"><span data-stu-id="60055-108">If the mouse is not captured, the message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="60055-109">In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="60055-109">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="60055-110">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="60055-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEMOVE                    0x0200
```



## <a name="parameters"></a><span data-ttu-id="60055-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="60055-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60055-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60055-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60055-113">Indica se varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="60055-113">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="60055-114">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="60055-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="60055-115">Valore</span><span class="sxs-lookup"><span data-stu-id="60055-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="60055-116">Significato</span><span class="sxs-lookup"><span data-stu-id="60055-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="60055-117"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="60055-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="60055-118">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="60055-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="60055-119"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="60055-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="60055-120">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="60055-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="60055-121"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="60055-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="60055-122">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="60055-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="60055-123"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="60055-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="60055-124">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="60055-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="60055-125"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="60055-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="60055-126">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="60055-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="60055-127"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="60055-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="60055-128">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="60055-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="60055-129"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="60055-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="60055-130">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="60055-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="60055-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60055-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60055-132">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="60055-132">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="60055-133">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="60055-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="60055-134">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="60055-134">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="60055-135">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="60055-135">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60055-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60055-136">Return value</span></span>

<span data-ttu-id="60055-137">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="60055-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="60055-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="60055-138">Remarks</span></span>

<span data-ttu-id="60055-139">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="60055-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="60055-140">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="60055-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="60055-141">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="60055-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="60055-142">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="60055-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60055-143">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="60055-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="60055-144">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="60055-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="60055-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60055-145">Requirements</span></span>



| <span data-ttu-id="60055-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="60055-146">Requirement</span></span> | <span data-ttu-id="60055-147">Valore</span><span class="sxs-lookup"><span data-stu-id="60055-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60055-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60055-148">Minimum supported client</span></span><br/> | <span data-ttu-id="60055-149">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60055-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60055-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60055-150">Minimum supported server</span></span><br/> | <span data-ttu-id="60055-151">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60055-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60055-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60055-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="60055-153"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60055-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60055-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60055-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="60055-155">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="60055-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="60055-156">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="60055-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="60055-157">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="60055-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="60055-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="60055-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="60055-159">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="60055-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="60055-160">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="60055-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="60055-161">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="60055-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="60055-162">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="60055-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="60055-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="60055-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="60055-164">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60055-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

