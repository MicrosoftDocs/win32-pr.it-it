---
title: Messaggio WM_SYSCHAR (winuser. h)
description: Inserito nella finestra con lo stato attivo quando un messaggio WM \_ SYSKEYDOWN viene convertito dalla funzione TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- Menu del messaggio WM_SYSCHAR e altre risorse
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519197"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="0e18d-104">\_Messaggio SYSCHAR WM</span><span class="sxs-lookup"><span data-stu-id="0e18d-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="0e18d-105">Inserito nella finestra con lo stato attivo quando un messaggio [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="0e18d-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="0e18d-106">Specifica il codice carattere di una chiave carattere di sistema, ovvero un tasto carattere premuto mentre il tasto ALT è premuto.</span><span class="sxs-lookup"><span data-stu-id="0e18d-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="0e18d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e18d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e18d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e18d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e18d-109">Codice carattere del tasto menu finestra.</span><span class="sxs-lookup"><span data-stu-id="0e18d-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="0e18d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e18d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e18d-111">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0e18d-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="0e18d-112">BITS</span><span class="sxs-lookup"><span data-stu-id="0e18d-112">Bits</span></span>                                                                             | <span data-ttu-id="0e18d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="0e18d-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e18d-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="0e18d-115">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="0e18d-115">The repeat count for the current message.</span></span> <span data-ttu-id="0e18d-116">Il valore è il numero di volte in cui la sequenza di tasti è stata ripetuta automaticamente in seguito all'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0e18d-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="0e18d-117">Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="0e18d-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="0e18d-118">Tuttavia, il numero di ripetizioni non è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="0e18d-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="0e18d-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="0e18d-120">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="0e18d-120">The scan code.</span></span> <span data-ttu-id="0e18d-121">Il valore dipende dall'OEM (Original Equipment Manufacturer).</span><span class="sxs-lookup"><span data-stu-id="0e18d-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="0e18d-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="0e18d-123">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="0e18d-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="0e18d-124">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="0e18d-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0e18d-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="0e18d-126">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="0e18d-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="0e18d-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="0e18d-128">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="0e18d-128">The context code.</span></span> <span data-ttu-id="0e18d-129">Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.</span><span class="sxs-lookup"><span data-stu-id="0e18d-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="0e18d-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="0e18d-131">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="0e18d-131">The previous key state.</span></span> <span data-ttu-id="0e18d-132">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.</span><span class="sxs-lookup"><span data-stu-id="0e18d-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="0e18d-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="0e18d-134">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="0e18d-134">The transition state.</span></span> <span data-ttu-id="0e18d-135">Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.</span><span class="sxs-lookup"><span data-stu-id="0e18d-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="0e18d-136">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="0e18d-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e18d-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e18d-137">Return value</span></span>

<span data-ttu-id="0e18d-138">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0e18d-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e18d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e18d-139">Remarks</span></span>

<span data-ttu-id="0e18d-140">Quando il codice del contesto è zero, il messaggio può essere passato alla funzione [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , che lo gestirà come se fosse un messaggio chiave standard anziché un messaggio di chiave del carattere di sistema.</span><span class="sxs-lookup"><span data-stu-id="0e18d-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="0e18d-141">In questo modo è possibile utilizzare i tasti di scelta rapida con la finestra attiva anche se la finestra attiva non dispone dello stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="0e18d-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="0e18d-142">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; chiave Stamp di stampa. tasto INTERr; chiave NUMLOCK; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="0e18d-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="0e18d-143">Altre tastiere possono supportare il bit della chiave estesa nel parametro.</span><span class="sxs-lookup"><span data-stu-id="0e18d-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e18d-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e18d-144">Requirements</span></span>



| <span data-ttu-id="0e18d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e18d-145">Requirement</span></span> | <span data-ttu-id="0e18d-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0e18d-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e18d-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e18d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0e18d-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e18d-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0e18d-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e18d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0e18d-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e18d-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e18d-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e18d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e18d-152"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e18d-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e18d-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e18d-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e18d-154">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0e18d-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e18d-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="0e18d-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="0e18d-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="0e18d-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="0e18d-157">**\_SYSKEYDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="0e18d-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="0e18d-158">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="0e18d-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0e18d-159">Tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="0e18d-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

