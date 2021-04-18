---
title: Messaggio WM_SYSKEYDOWN (winuser. h)
description: Inserito nella finestra con lo stato attivo quando l'utente preme il tasto F10 (che attiva la barra dei menu) o tiene premuto il tasto ALT, quindi preme un altro tasto.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Input della tastiera e del mouse WM_SYSKEYDOWN messaggio
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301677"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="ff1e6-104">\_Messaggio SYSKEYDOWN WM</span><span class="sxs-lookup"><span data-stu-id="ff1e6-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="ff1e6-105">Inserito nella finestra con lo stato attivo quando l'utente preme il tasto F10 (che attiva la barra dei menu) o tiene premuto il tasto ALT, quindi preme un altro tasto.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="ff1e6-106">Si verifica anche quando nessuna finestra dispone attualmente dello stato attivo della tastiera; in questo caso, il messaggio **WM \_ SYSKEYDOWN** viene inviato alla finestra attiva.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="ff1e6-107">La finestra che riceve il messaggio può distinguere tra questi due contesti controllando il codice del contesto nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ff1e6-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="ff1e6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff1e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff1e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff1e6-110">Codice della chiave virtuale del tasto premuto.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="ff1e6-111">Vedere [**codici chiave virtuale**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ff1e6-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff1e6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff1e6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff1e6-113">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="ff1e6-114">BITS</span><span class="sxs-lookup"><span data-stu-id="ff1e6-114">Bits</span></span>  | <span data-ttu-id="ff1e6-115">Significato</span><span class="sxs-lookup"><span data-stu-id="ff1e6-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1e6-116">0-15</span><span class="sxs-lookup"><span data-stu-id="ff1e6-116">0-15</span></span>  | <span data-ttu-id="ff1e6-117">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-117">The repeat count for the current message.</span></span> <span data-ttu-id="ff1e6-118">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="ff1e6-119">Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="ff1e6-120">Tuttavia, il numero di ripetizioni non è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="ff1e6-121">16-23</span><span class="sxs-lookup"><span data-stu-id="ff1e6-121">16-23</span></span> | <span data-ttu-id="ff1e6-122">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-122">The scan code.</span></span> <span data-ttu-id="ff1e6-123">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="ff1e6-124">24</span><span class="sxs-lookup"><span data-stu-id="ff1e6-124">24</span></span>    | <span data-ttu-id="ff1e6-125">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="ff1e6-126">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="ff1e6-127">25-28</span><span class="sxs-lookup"><span data-stu-id="ff1e6-127">25-28</span></span> | <span data-ttu-id="ff1e6-128">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ff1e6-129">29</span><span class="sxs-lookup"><span data-stu-id="ff1e6-129">29</span></span>    | <span data-ttu-id="ff1e6-130">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-130">The context code.</span></span> <span data-ttu-id="ff1e6-131">Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; è 0 se il messaggio **WM \_ SYSKEYDOWN** viene inserito nella finestra attiva perché nessuna finestra dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="ff1e6-132">30</span><span class="sxs-lookup"><span data-stu-id="ff1e6-132">30</span></span>    | <span data-ttu-id="ff1e6-133">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-133">The previous key state.</span></span> <span data-ttu-id="ff1e6-134">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="ff1e6-135">31</span><span class="sxs-lookup"><span data-stu-id="ff1e6-135">31</span></span>    | <span data-ttu-id="ff1e6-136">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-136">The transition state.</span></span> <span data-ttu-id="ff1e6-137">Il valore è sempre 0 per un messaggio **WM \_ SYSKEYDOWN** .</span><span class="sxs-lookup"><span data-stu-id="ff1e6-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="ff1e6-138">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="ff1e6-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1e6-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff1e6-139">Return value</span></span>

<span data-ttu-id="ff1e6-140">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1e6-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff1e6-141">Remarks</span></span>

<span data-ttu-id="ff1e6-142">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esamina la chiave specificata e genera un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) se la chiave è Tab o ENTER.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="ff1e6-143">Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un normale messaggio chiave invece di un messaggio chiave-carattere.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="ff1e6-144">In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="ff1e6-145">A causa della ripetizione automatica, possono verificarsi più di un messaggio **WM \_ SYSKEYDOWN** prima dell'invio di un messaggio [**WM \_ SYSKEYUP**](wm-syskeyup.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1e6-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="ff1e6-146">Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio **WM \_ SYSKEYDOWN** indica la prima transizione verso il basso o una transizione ripetuta verso il basso.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="ff1e6-147">Per le tastiere ottimizzate 101 e 102, le chiavi avanzate sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="ff1e6-148">Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ff1e6-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="ff1e6-149">Questo messaggio viene inviato anche ogni volta che l'utente preme il tasto F10 senza il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="ff1e6-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff1e6-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff1e6-150">Requirements</span></span>



| <span data-ttu-id="ff1e6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff1e6-151">Requirement</span></span> | <span data-ttu-id="ff1e6-152">Valore</span><span class="sxs-lookup"><span data-stu-id="ff1e6-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1e6-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff1e6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1e6-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff1e6-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff1e6-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff1e6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1e6-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff1e6-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff1e6-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff1e6-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1e6-158"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff1e6-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff1e6-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff1e6-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff1e6-160">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff1e6-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ff1e6-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="ff1e6-163">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="ff1e6-164">**\_SYSKEYUP WM**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="ff1e6-165">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="ff1e6-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff1e6-166">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="ff1e6-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

