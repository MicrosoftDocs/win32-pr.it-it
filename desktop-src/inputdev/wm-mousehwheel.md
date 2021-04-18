---
title: Messaggio WM_MOUSEHWHEEL (winuser. h)
description: Inviato alla finestra attiva quando la rotellina di scorrimento orizzontale del mouse viene inclinata o ruotata.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- Input della tastiera e del mouse WM_MOUSEHWHEEL messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301424"
---
# <a name="wm_mousehwheel-message"></a><span data-ttu-id="9ba59-104">\_Messaggio MOUSEHWHEEL WM</span><span class="sxs-lookup"><span data-stu-id="9ba59-104">WM\_MOUSEHWHEEL message</span></span>

<span data-ttu-id="9ba59-105">Inviato alla finestra attiva quando la rotellina di scorrimento orizzontale del mouse viene inclinata o ruotata.</span><span class="sxs-lookup"><span data-stu-id="9ba59-105">Sent to the active window when the mouse's horizontal scroll wheel is tilted or rotated.</span></span> <span data-ttu-id="9ba59-106">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra.</span><span class="sxs-lookup"><span data-stu-id="9ba59-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="9ba59-107">Non devono essere presenti inoltri interni del messaggio, poiché **DefWindowProc** lo propaga alla catena padre fino a quando non trova una finestra che la elabora.</span><span class="sxs-lookup"><span data-stu-id="9ba59-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="9ba59-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9ba59-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a><span data-ttu-id="9ba59-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ba59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba59-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ba59-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba59-111">La parola più significativa indica la distanza con cui la rotellina viene ruotata, espressa in multipli o fattori **di \_ Delta della rotella**, impostata su 120.</span><span class="sxs-lookup"><span data-stu-id="9ba59-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or factors of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="9ba59-112">Un valore positivo indica che la rotellina è stata ruotata a destra; un valore negativo indica che la rotellina è stata ruotata a sinistra.</span><span class="sxs-lookup"><span data-stu-id="9ba59-112">A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left.</span></span>

<span data-ttu-id="9ba59-113">La parola più bassa indica se le varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="9ba59-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="9ba59-114">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ba59-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="9ba59-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9ba59-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="9ba59-116">Significato</span><span class="sxs-lookup"><span data-stu-id="9ba59-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="9ba59-117"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="9ba59-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="9ba59-118">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="9ba59-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="9ba59-119"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="9ba59-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="9ba59-120">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="9ba59-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="9ba59-121"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="9ba59-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="9ba59-122">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="9ba59-123"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="9ba59-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="9ba59-124">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="9ba59-125"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="9ba59-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="9ba59-126">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="9ba59-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="9ba59-127"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="9ba59-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="9ba59-128">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="9ba59-129"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="9ba59-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="9ba59-130">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="9ba59-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ba59-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba59-132">La parola di ordine inferiore specifica la coordinata x del puntatore, relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="9ba59-133">La parola più significativa specifica la coordinata y del puntatore, relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9ba59-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba59-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ba59-134">Return value</span></span>

<span data-ttu-id="9ba59-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="9ba59-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba59-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ba59-136">Remarks</span></span>

<span data-ttu-id="9ba59-137">Usare il codice seguente per ottenere le informazioni nel parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="9ba59-137">Use the following code to obtain the information in the *wParam* parameter.</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="9ba59-138">Usare il codice seguente per ottenere la posizione orizzontale e verticale.</span><span class="sxs-lookup"><span data-stu-id="9ba59-138">Use the following code to obtain the horizontal and vertical position.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="9ba59-139">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="9ba59-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="9ba59-140">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9ba59-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="9ba59-141">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="9ba59-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9ba59-142">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="9ba59-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="9ba59-143">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="9ba59-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="9ba59-144">La rotazione della rotellina è un multiplo del **\_ Delta della rotellina**, che è impostato su 120.</span><span class="sxs-lookup"><span data-stu-id="9ba59-144">The wheel rotation is a multiple of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="9ba59-145">Si tratta della soglia per l'azione da intraprendere e una di queste azioni, ad esempio lo scorrimento di un incremento, deve verificarsi per ogni Delta.</span><span class="sxs-lookup"><span data-stu-id="9ba59-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="9ba59-146">Il Delta è stato impostato su 120 per consentire a Microsoft o altri fornitori di creare ruote a risoluzione più fine (ad esempio, una rotellina a rotazione libera senza tacche) per inviare più messaggi per rotazione, ma con un valore inferiore in ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="9ba59-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (for example, a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="9ba59-147">Per usare questa funzionalità, è possibile aggiungere i valori Delta in entrata fino a raggiungere il **\_ Delta della rotella** (pertanto, per una rotazione delta si ottiene la stessa risposta) o scorrere righe parziali in risposta a messaggi più frequenti.</span><span class="sxs-lookup"><span data-stu-id="9ba59-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to more frequent messages.</span></span> <span data-ttu-id="9ba59-148">È anche possibile scegliere la granularità di scorrimento e accumulare delta fino a quando non viene raggiunto.</span><span class="sxs-lookup"><span data-stu-id="9ba59-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba59-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ba59-149">Requirements</span></span>



| <span data-ttu-id="9ba59-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ba59-150">Requirement</span></span> | <span data-ttu-id="9ba59-151">Valore</span><span class="sxs-lookup"><span data-stu-id="9ba59-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba59-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ba59-152">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba59-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ba59-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9ba59-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ba59-154">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba59-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ba59-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ba59-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ba59-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba59-157"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ba59-157"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ba59-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ba59-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="9ba59-159">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9ba59-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ba59-160">**OTTENERE \_ lo stato di un \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="9ba59-160">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="9ba59-161">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="9ba59-161">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="9ba59-162">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="9ba59-162">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="9ba59-163">**OTTENERE \_ la \_ Delta del cerchio \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="9ba59-163">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="9ba59-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba59-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9ba59-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba59-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ba59-166">**\_evento mouse**</span><span class="sxs-lookup"><span data-stu-id="9ba59-166">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="9ba59-167">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="9ba59-167">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ba59-168">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="9ba59-168">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="9ba59-169">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="9ba59-169">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="9ba59-170">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="9ba59-170">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="9ba59-171">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="9ba59-171">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="9ba59-172">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ba59-172">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9ba59-173">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="9ba59-173">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

