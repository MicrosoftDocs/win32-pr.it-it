---
title: Messaggio WM_LBUTTONDOWN (winuser. h)
description: Inviato quando l'utente preme il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- Input della tastiera e del mouse WM_LBUTTONDOWN messaggio
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330441"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="75647-104">\_Messaggio LBUTTONDOWN WM</span><span class="sxs-lookup"><span data-stu-id="75647-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="75647-105">Inviato quando l'utente preme il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="75647-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="75647-106">Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore.</span><span class="sxs-lookup"><span data-stu-id="75647-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="75647-107">In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.</span><span class="sxs-lookup"><span data-stu-id="75647-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="75647-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="75647-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="75647-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="75647-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75647-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="75647-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75647-111">Indica se varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="75647-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="75647-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="75647-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="75647-113">Valore</span><span class="sxs-lookup"><span data-stu-id="75647-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="75647-114">Significato</span><span class="sxs-lookup"><span data-stu-id="75647-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="75647-115"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="75647-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="75647-116">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="75647-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="75647-117"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="75647-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="75647-118">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="75647-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="75647-119"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="75647-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="75647-120">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="75647-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="75647-121"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="75647-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="75647-122">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="75647-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="75647-123"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="75647-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="75647-124">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="75647-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="75647-125"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="75647-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="75647-126">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="75647-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="75647-127"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="75647-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="75647-128">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="75647-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="75647-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="75647-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="75647-130">La parola di ordine inferiore specifica la coordinata x del cursore.</span><span class="sxs-lookup"><span data-stu-id="75647-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="75647-131">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="75647-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="75647-132">La parola di ordine superiore specifica la coordinata y del cursore.</span><span class="sxs-lookup"><span data-stu-id="75647-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="75647-133">La coordinata è relativa all'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="75647-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75647-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75647-134">Return value</span></span>

<span data-ttu-id="75647-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="75647-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="75647-136">Esempio</span><span class="sxs-lookup"><span data-stu-id="75647-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="75647-137">Per altri esempi, vedere [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="75647-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="75647-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="75647-138">Remarks</span></span>

<span data-ttu-id="75647-139">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="75647-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="75647-140">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="75647-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="75647-141">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="75647-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75647-142">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="75647-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="75647-143">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="75647-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="75647-144">Per rilevare che è stato premuto il tasto ALT, controllare se [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) con il **\_ menu VK** < 0.</span><span class="sxs-lookup"><span data-stu-id="75647-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="75647-145">Si noti che questo non deve essere [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="75647-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="75647-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75647-146">Requirements</span></span>



| <span data-ttu-id="75647-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="75647-147">Requirement</span></span> | <span data-ttu-id="75647-148">Valore</span><span class="sxs-lookup"><span data-stu-id="75647-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75647-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75647-149">Minimum supported client</span></span><br/> | <span data-ttu-id="75647-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75647-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="75647-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75647-151">Minimum supported server</span></span><br/> | <span data-ttu-id="75647-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="75647-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75647-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75647-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="75647-154"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75647-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75647-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75647-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="75647-156">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="75647-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="75647-157">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="75647-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="75647-158">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="75647-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="75647-159">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="75647-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="75647-160">**GetKeyState**</span><span class="sxs-lookup"><span data-stu-id="75647-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="75647-161">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="75647-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="75647-162">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="75647-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="75647-163">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="75647-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="75647-164">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="75647-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75647-165">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="75647-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="75647-166">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="75647-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="75647-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="75647-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="75647-168">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75647-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

