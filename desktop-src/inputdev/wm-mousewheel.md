---
title: Messaggio WM_MOUSEWHEEL (winuser. h)
description: Inviato alla finestra con lo stato attivo quando la rotellina del mouse viene ruotata.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- Input della tastiera e del mouse WM_MOUSEWHEEL messaggio
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301423"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="e450e-104">Messaggio di WM \_ MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="e450e-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="e450e-105">Inviato alla finestra con lo stato attivo quando la rotellina del mouse viene ruotata.</span><span class="sxs-lookup"><span data-stu-id="e450e-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="e450e-106">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) propaga il messaggio all'elemento padre della finestra.</span><span class="sxs-lookup"><span data-stu-id="e450e-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="e450e-107">Non devono essere presenti inoltri interni del messaggio, poiché **DefWindowProc** lo propaga alla catena padre fino a quando non trova una finestra che la elabora.</span><span class="sxs-lookup"><span data-stu-id="e450e-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="e450e-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e450e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="e450e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e450e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e450e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e450e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e450e-111">La parola più ordinata indica la distanza con cui la rotellina viene ruotata, espressa in multipli o divisioni di **\_ Delta della rotella**, ovvero 120.</span><span class="sxs-lookup"><span data-stu-id="e450e-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="e450e-112">Un valore positivo indica che la rotellina è stata ruotata in orizzontale, lontano dall'utente; un valore negativo indica che la rotellina è stata ruotata indietro verso l'utente.</span><span class="sxs-lookup"><span data-stu-id="e450e-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="e450e-113">La parola più bassa indica se le varie chiavi virtuali sono inattive.</span><span class="sxs-lookup"><span data-stu-id="e450e-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="e450e-114">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e450e-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="e450e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e450e-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="e450e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e450e-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="e450e-117"><dt>**MK \_**</dt> <dt>0x0008</dt> di controllo</span><span class="sxs-lookup"><span data-stu-id="e450e-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="e450e-118">Il tasto CTRL è premuto.</span><span class="sxs-lookup"><span data-stu-id="e450e-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="e450e-119"><dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON</span><span class="sxs-lookup"><span data-stu-id="e450e-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="e450e-120">Il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="e450e-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="e450e-121"><dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON</span><span class="sxs-lookup"><span data-stu-id="e450e-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="e450e-122">Il pulsante centrale del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e450e-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="e450e-123"><dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON</span><span class="sxs-lookup"><span data-stu-id="e450e-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="e450e-124">Il pulsante destro del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e450e-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="e450e-125"><dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="e450e-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="e450e-126">Il tasto MAIUSC è premuto.</span><span class="sxs-lookup"><span data-stu-id="e450e-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="e450e-127"><dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1</span><span class="sxs-lookup"><span data-stu-id="e450e-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="e450e-128">Il primo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e450e-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="e450e-129"><dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2</span><span class="sxs-lookup"><span data-stu-id="e450e-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="e450e-130">Il secondo pulsante X è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e450e-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="e450e-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e450e-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e450e-132">La parola di ordine inferiore specifica la coordinata x del puntatore, relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e450e-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="e450e-133">La parola più significativa specifica la coordinata y del puntatore, relativa all'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="e450e-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e450e-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e450e-134">Return value</span></span>

<span data-ttu-id="e450e-135">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="e450e-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e450e-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="e450e-136">Remarks</span></span>

<span data-ttu-id="e450e-137">Usare il codice seguente per ottenere le informazioni nel parametro *wParam* :</span><span class="sxs-lookup"><span data-stu-id="e450e-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="e450e-138">Usare il codice seguente per ottenere la posizione orizzontale e verticale:</span><span class="sxs-lookup"><span data-stu-id="e450e-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="e450e-139">Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi).</span><span class="sxs-lookup"><span data-stu-id="e450e-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="e450e-140">Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e450e-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="e450e-141">Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="e450e-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e450e-142">Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi.</span><span class="sxs-lookup"><span data-stu-id="e450e-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="e450e-143">I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.</span><span class="sxs-lookup"><span data-stu-id="e450e-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="e450e-144">La rotazione della rotellina sarà un multiplo del **\_ Delta della rotellina**, che viene impostato su 120.</span><span class="sxs-lookup"><span data-stu-id="e450e-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="e450e-145">Si tratta della soglia per l'azione da intraprendere e una di queste azioni, ad esempio lo scorrimento di un incremento, deve verificarsi per ogni Delta.</span><span class="sxs-lookup"><span data-stu-id="e450e-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="e450e-146">Il Delta è stato impostato su 120 per consentire a Microsoft o altri fornitori di creare ruote a risoluzione più fine, ovvero una rotellina a rotazione libera senza tacche, per inviare più messaggi per rotazione, ma con un valore inferiore in ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="e450e-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="e450e-147">Per usare questa funzionalità, è possibile aggiungere i valori Delta in entrata fino a raggiungere il **\_ Delta della rotella** (pertanto, per una rotazione delta si ottiene la stessa risposta) o scorrere righe parziali in risposta ai messaggi più frequenti.</span><span class="sxs-lookup"><span data-stu-id="e450e-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="e450e-148">È anche possibile scegliere la granularità di scorrimento e accumulare delta fino a quando non viene raggiunto.</span><span class="sxs-lookup"><span data-stu-id="e450e-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="e450e-149">Si noti che non esiste alcun *fwKeys* per **MSH \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="e450e-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="e450e-150">In caso contrario, i parametri sono esattamente uguali a quelli per **WM \_ MOUSEWHEEL**.</span><span class="sxs-lookup"><span data-stu-id="e450e-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="e450e-151">È possibile che l'applicazione inoltri **MSH \_ MOUSEWHEEL** a tutti gli oggetti o controlli incorporati.</span><span class="sxs-lookup"><span data-stu-id="e450e-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="e450e-152">L'applicazione è necessaria per inviare il messaggio a un'applicazione OLE incorporata attiva.</span><span class="sxs-lookup"><span data-stu-id="e450e-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="e450e-153">È facoltativo che l'applicazione lo invii a un controllo abilitato per la rotellina con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="e450e-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="e450e-154">Se l'applicazione invia il messaggio a un controllo, può controllare il valore restituito per verificare se il messaggio è stato elaborato.</span><span class="sxs-lookup"><span data-stu-id="e450e-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="e450e-155">I controlli sono necessari per restituire un valore **true** se elaborano il messaggio.</span><span class="sxs-lookup"><span data-stu-id="e450e-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e450e-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e450e-156">Requirements</span></span>



| <span data-ttu-id="e450e-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="e450e-157">Requirement</span></span> | <span data-ttu-id="e450e-158">Valore</span><span class="sxs-lookup"><span data-stu-id="e450e-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e450e-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e450e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="e450e-160">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e450e-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e450e-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e450e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="e450e-162">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e450e-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e450e-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e450e-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="e450e-164"><dt>Winuser. h (include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e450e-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e450e-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e450e-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="e450e-166">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e450e-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e450e-167">**OTTENERE \_ lo stato di un \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="e450e-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="e450e-168">**Ottieni \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="e450e-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="e450e-169">**OTTENERE \_ il \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="e450e-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="e450e-170">**OTTENERE \_ la \_ Delta del cerchio \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="e450e-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="e450e-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e450e-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e450e-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e450e-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e450e-173">**\_evento mouse**</span><span class="sxs-lookup"><span data-stu-id="e450e-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="e450e-174">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e450e-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e450e-175">Input del mouse</span><span class="sxs-lookup"><span data-stu-id="e450e-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="e450e-176">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e450e-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e450e-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="e450e-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="e450e-178">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="e450e-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="e450e-179">[**PUNTI**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e450e-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e450e-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="e450e-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

