---
title: Messaggio WM_KEYUP (winuser. h)
description: Inviato alla finestra con lo stato attivo quando viene rilasciato un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto oppure un tasto di scelta rapida quando una finestra ha lo stato attivo della tastiera.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Input della tastiera e del mouse WM_KEYUP messaggio
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400504"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="bc0a7-105">\_Messaggio WM KEYUP</span><span class="sxs-lookup"><span data-stu-id="bc0a7-105">WM\_KEYUP message</span></span>

<span data-ttu-id="bc0a7-106">Inviato alla finestra con lo stato attivo quando viene rilasciato un tasto non di sistema.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="bc0a7-107">Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT *non* viene premuto oppure un tasto di scelta rapida quando una finestra ha lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="bc0a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc0a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc0a7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc0a7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0a7-110">Codice della chiave virtuale della chiave non di sistema.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="bc0a7-111">Vedere [codici chiave virtuale](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bc0a7-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc0a7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc0a7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc0a7-113">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="bc0a7-114">BITS</span><span class="sxs-lookup"><span data-stu-id="bc0a7-114">Bits</span></span>  | <span data-ttu-id="bc0a7-115">Significato</span><span class="sxs-lookup"><span data-stu-id="bc0a7-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0a7-116">0-15</span><span class="sxs-lookup"><span data-stu-id="bc0a7-116">0-15</span></span>  | <span data-ttu-id="bc0a7-117">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-117">The repeat count for the current message.</span></span> <span data-ttu-id="bc0a7-118">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="bc0a7-119">Il numero di ripetizioni è sempre 1 per un messaggio **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="bc0a7-120">16-23</span><span class="sxs-lookup"><span data-stu-id="bc0a7-120">16-23</span></span> | <span data-ttu-id="bc0a7-121">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-121">The scan code.</span></span> <span data-ttu-id="bc0a7-122">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="bc0a7-123">24</span><span class="sxs-lookup"><span data-stu-id="bc0a7-123">24</span></span>    | <span data-ttu-id="bc0a7-124">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="bc0a7-125">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="bc0a7-126">25-28</span><span class="sxs-lookup"><span data-stu-id="bc0a7-126">25-28</span></span> | <span data-ttu-id="bc0a7-127">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="bc0a7-128">29</span><span class="sxs-lookup"><span data-stu-id="bc0a7-128">29</span></span>    | <span data-ttu-id="bc0a7-129">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-129">The context code.</span></span> <span data-ttu-id="bc0a7-130">Il valore è sempre 0 per un messaggio **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="bc0a7-131">30</span><span class="sxs-lookup"><span data-stu-id="bc0a7-131">30</span></span>    | <span data-ttu-id="bc0a7-132">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-132">The previous key state.</span></span> <span data-ttu-id="bc0a7-133">Il valore è sempre 1 per un messaggio **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="bc0a7-134">31</span><span class="sxs-lookup"><span data-stu-id="bc0a7-134">31</span></span>    | <span data-ttu-id="bc0a7-135">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-135">The transition state.</span></span> <span data-ttu-id="bc0a7-136">Il valore è sempre 1 per un messaggio **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="bc0a7-137">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="bc0a7-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc0a7-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc0a7-138">Return value</span></span>

<span data-ttu-id="bc0a7-139">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc0a7-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc0a7-140">Remarks</span></span>

<span data-ttu-id="bc0a7-141">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello se è stato rilasciato il tasto F10 o il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="bc0a7-142">Il parametro *wParam* del messaggio viene impostato sul menu SC \_ .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="bc0a7-143">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="bc0a7-144">Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="bc0a7-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="bc0a7-145">Le applicazioni devono passare *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo.</span><span class="sxs-lookup"><span data-stu-id="bc0a7-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc0a7-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc0a7-146">Requirements</span></span>



| <span data-ttu-id="bc0a7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc0a7-147">Requirement</span></span> | <span data-ttu-id="bc0a7-148">Valore</span><span class="sxs-lookup"><span data-stu-id="bc0a7-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc0a7-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc0a7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="bc0a7-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc0a7-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bc0a7-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc0a7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="bc0a7-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc0a7-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bc0a7-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc0a7-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc0a7-154"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc0a7-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc0a7-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc0a7-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc0a7-156">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bc0a7-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bc0a7-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="bc0a7-159">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="bc0a7-160">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="bc0a7-161">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bc0a7-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc0a7-162">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="bc0a7-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

