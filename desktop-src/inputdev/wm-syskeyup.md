---
title: Messaggio WM_SYSKEYUP (winuser. h)
description: Inserito nella finestra con lo stato attivo quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Input della tastiera e del mouse WM_SYSKEYUP messaggio
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352056"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="014d7-104">\_Messaggio SYSKEYUP WM</span><span class="sxs-lookup"><span data-stu-id="014d7-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="014d7-105">Inserito nella finestra con lo stato attivo quando l'utente rilascia un tasto premuto mentre il tasto ALT è stato premuto.</span><span class="sxs-lookup"><span data-stu-id="014d7-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="014d7-106">Si verifica anche quando nessuna finestra dispone attualmente dello stato attivo della tastiera; in questo caso, il messaggio **WM \_ SYSKEYUP** viene inviato alla finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="014d7-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="014d7-107">La finestra che riceve il messaggio può distinguere tra questi due contesti controllando il codice del contesto nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="014d7-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="014d7-108">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="014d7-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="014d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="014d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="014d7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="014d7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="014d7-111">Codice della chiave virtuale della chiave da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="014d7-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="014d7-112">Vedere [**codici chiave virtuale**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="014d7-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="014d7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="014d7-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="014d7-114">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="014d7-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="014d7-115">BITS</span><span class="sxs-lookup"><span data-stu-id="014d7-115">Bits</span></span>  | <span data-ttu-id="014d7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="014d7-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="014d7-117">0-15</span><span class="sxs-lookup"><span data-stu-id="014d7-117">0-15</span></span>  | <span data-ttu-id="014d7-118">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="014d7-118">The repeat count for the current message.</span></span> <span data-ttu-id="014d7-119">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="014d7-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="014d7-120">Il numero di ripetizioni è sempre uno per un messaggio **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="014d7-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="014d7-121">16-23</span><span class="sxs-lookup"><span data-stu-id="014d7-121">16-23</span></span> | <span data-ttu-id="014d7-122">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="014d7-122">The scan code.</span></span> <span data-ttu-id="014d7-123">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="014d7-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="014d7-124">24</span><span class="sxs-lookup"><span data-stu-id="014d7-124">24</span></span>    | <span data-ttu-id="014d7-125">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="014d7-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="014d7-126">Il valore è 1 se è una chiave estesa; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="014d7-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="014d7-127">25-28</span><span class="sxs-lookup"><span data-stu-id="014d7-127">25-28</span></span> | <span data-ttu-id="014d7-128">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="014d7-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="014d7-129">29</span><span class="sxs-lookup"><span data-stu-id="014d7-129">29</span></span>    | <span data-ttu-id="014d7-130">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="014d7-130">The context code.</span></span> <span data-ttu-id="014d7-131">Il valore è 1 se il tasto ALT è premuto mentre la chiave viene rilasciata; è zero se il messaggio **WM \_ SYSKEYUP** viene inserito nella finestra attiva perché nessuna finestra dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="014d7-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="014d7-132">30</span><span class="sxs-lookup"><span data-stu-id="014d7-132">30</span></span>    | <span data-ttu-id="014d7-133">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="014d7-133">The previous key state.</span></span> <span data-ttu-id="014d7-134">Il valore è sempre 1 per un messaggio **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="014d7-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="014d7-135">31</span><span class="sxs-lookup"><span data-stu-id="014d7-135">31</span></span>    | <span data-ttu-id="014d7-136">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="014d7-136">The transition state.</span></span> <span data-ttu-id="014d7-137">Il valore è sempre 1 per un messaggio **WM \_ SYSKEYUP** .</span><span class="sxs-lookup"><span data-stu-id="014d7-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="014d7-138">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="014d7-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="014d7-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="014d7-139">Return value</span></span>

<span data-ttu-id="014d7-140">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="014d7-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="014d7-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="014d7-141">Remarks</span></span>

<span data-ttu-id="014d7-142">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="014d7-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="014d7-143">Il parametro *wParam* del messaggio viene impostato sul **\_ menu SC**.</span><span class="sxs-lookup"><span data-stu-id="014d7-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="014d7-144">Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un normale messaggio chiave invece di un messaggio chiave-carattere.</span><span class="sxs-lookup"><span data-stu-id="014d7-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="014d7-145">In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="014d7-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="014d7-146">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="014d7-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="014d7-147">Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="014d7-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="014d7-148">Per non-U. S. tastiere ottimizzate a 102 chiavi, il tasto ALT destro viene gestito come tasto CTRL + ALT.</span><span class="sxs-lookup"><span data-stu-id="014d7-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="014d7-149">Nella tabella seguente viene illustrata la sequenza di messaggi risultante quando l'utente preme e rilascia tale chiave.</span><span class="sxs-lookup"><span data-stu-id="014d7-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="014d7-150">Message</span><span class="sxs-lookup"><span data-stu-id="014d7-150">Message</span></span>                           | <span data-ttu-id="014d7-151">Codice chiave virtuale</span><span class="sxs-lookup"><span data-stu-id="014d7-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="014d7-152">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="014d7-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="014d7-153">**\_controllo VK**</span><span class="sxs-lookup"><span data-stu-id="014d7-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="014d7-154">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="014d7-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="014d7-155">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="014d7-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="014d7-156">**KEYUP di WM \_**</span><span class="sxs-lookup"><span data-stu-id="014d7-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="014d7-157">**\_controllo VK**</span><span class="sxs-lookup"><span data-stu-id="014d7-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="014d7-158">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="014d7-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="014d7-159">**\_menu VK**</span><span class="sxs-lookup"><span data-stu-id="014d7-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="014d7-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="014d7-160">Requirements</span></span>



| <span data-ttu-id="014d7-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="014d7-161">Requirement</span></span> | <span data-ttu-id="014d7-162">Valore</span><span class="sxs-lookup"><span data-stu-id="014d7-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="014d7-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="014d7-163">Minimum supported client</span></span><br/> | <span data-ttu-id="014d7-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="014d7-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="014d7-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="014d7-165">Minimum supported server</span></span><br/> | <span data-ttu-id="014d7-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="014d7-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="014d7-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="014d7-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="014d7-168"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="014d7-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="014d7-169">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="014d7-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="014d7-170">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="014d7-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="014d7-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="014d7-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="014d7-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="014d7-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="014d7-173">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="014d7-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="014d7-174">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="014d7-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="014d7-175">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="014d7-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="014d7-176">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="014d7-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

