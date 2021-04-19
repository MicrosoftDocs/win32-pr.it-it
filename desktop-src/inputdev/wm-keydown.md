---
title: Messaggio WM_KEYDOWN (winuser. h)
description: Inserito nella finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema. Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Input della tastiera e del mouse WM_KEYDOWN messaggio
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332667"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="69c27-105">\_Messaggio KeyDown di WM</span><span class="sxs-lookup"><span data-stu-id="69c27-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="69c27-106">Inserito nella finestra con lo stato attivo della tastiera quando viene premuto un tasto non di sistema.</span><span class="sxs-lookup"><span data-stu-id="69c27-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="69c27-107">Una chiave non di sistema è una chiave che viene premuto quando il tasto ALT non viene premuto.</span><span class="sxs-lookup"><span data-stu-id="69c27-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="69c27-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="69c27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69c27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69c27-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69c27-110">Codice della chiave virtuale della chiave non di sistema.</span><span class="sxs-lookup"><span data-stu-id="69c27-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="69c27-111">Vedere [codici chiave virtuale](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="69c27-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="69c27-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69c27-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69c27-113">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato della chiave precedente e il flag di stato di transizione, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="69c27-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="69c27-114">BITS</span><span class="sxs-lookup"><span data-stu-id="69c27-114">Bits</span></span>  | <span data-ttu-id="69c27-115">Significato</span><span class="sxs-lookup"><span data-stu-id="69c27-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c27-116">0-15</span><span class="sxs-lookup"><span data-stu-id="69c27-116">0-15</span></span>  | <span data-ttu-id="69c27-117">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="69c27-117">The repeat count for the current message.</span></span> <span data-ttu-id="69c27-118">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="69c27-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="69c27-119">Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="69c27-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="69c27-120">Tuttavia, il numero di ripetizioni non è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="69c27-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="69c27-121">16-23</span><span class="sxs-lookup"><span data-stu-id="69c27-121">16-23</span></span> | <span data-ttu-id="69c27-122">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="69c27-122">The scan code.</span></span> <span data-ttu-id="69c27-123">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="69c27-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="69c27-124">24</span><span class="sxs-lookup"><span data-stu-id="69c27-124">24</span></span>    | <span data-ttu-id="69c27-125">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="69c27-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="69c27-126">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="69c27-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="69c27-127">25-28</span><span class="sxs-lookup"><span data-stu-id="69c27-127">25-28</span></span> | <span data-ttu-id="69c27-128">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="69c27-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="69c27-129">29</span><span class="sxs-lookup"><span data-stu-id="69c27-129">29</span></span>    | <span data-ttu-id="69c27-130">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="69c27-130">The context code.</span></span> <span data-ttu-id="69c27-131">Il valore è sempre 0 per un messaggio di un **\_ KeyDown di WM** .</span><span class="sxs-lookup"><span data-stu-id="69c27-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="69c27-132">30</span><span class="sxs-lookup"><span data-stu-id="69c27-132">30</span></span>    | <span data-ttu-id="69c27-133">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="69c27-133">The previous key state.</span></span> <span data-ttu-id="69c27-134">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è zero se la chiave è attiva.</span><span class="sxs-lookup"><span data-stu-id="69c27-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="69c27-135">31</span><span class="sxs-lookup"><span data-stu-id="69c27-135">31</span></span>    | <span data-ttu-id="69c27-136">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="69c27-136">The transition state.</span></span> <span data-ttu-id="69c27-137">Il valore è sempre 0 per un messaggio di un **\_ KeyDown di WM** .</span><span class="sxs-lookup"><span data-stu-id="69c27-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="69c27-138">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="69c27-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69c27-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69c27-139">Return value</span></span>

<span data-ttu-id="69c27-140">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="69c27-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="69c27-141">Esempio</span><span class="sxs-lookup"><span data-stu-id="69c27-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="69c27-142">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="69c27-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="69c27-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="69c27-143">Remarks</span></span>

<span data-ttu-id="69c27-144">Se viene premuto il tasto F10, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta un flag interno.</span><span class="sxs-lookup"><span data-stu-id="69c27-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="69c27-145">Quando **DefWindowProc** riceve il messaggio [**WM \_ KEYUP**](wm-keyup.md) , la funzione controlla se il flag interno è impostato e, in caso affermativo, invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) alla finestra di primo livello.</span><span class="sxs-lookup"><span data-stu-id="69c27-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="69c27-146">Il parametro **WM \_ SYSCOMMAND** del messaggio viene impostato sul menu SC \_ .</span><span class="sxs-lookup"><span data-stu-id="69c27-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="69c27-147">A causa della funzionalità di ripetizione, è possibile che più di un messaggio **WM \_ KeyDown** venga pubblicato prima della pubblicazione di un messaggio [**WM \_ KEYUP**](wm-keyup.md) .</span><span class="sxs-lookup"><span data-stu-id="69c27-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="69c27-148">Lo stato precedente della chiave (bit 30) può essere usato per determinare se il messaggio del **\_ KeyDown di WM** indica la prima transizione verso il basso o una transizione ripetuta verso il basso.</span><span class="sxs-lookup"><span data-stu-id="69c27-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="69c27-149">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL corretti nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="69c27-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="69c27-150">Altre tastiere possono supportare il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="69c27-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="69c27-151">Le applicazioni devono passare *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) senza modificarlo.</span><span class="sxs-lookup"><span data-stu-id="69c27-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="69c27-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69c27-152">Requirements</span></span>



| <span data-ttu-id="69c27-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="69c27-153">Requirement</span></span> | <span data-ttu-id="69c27-154">Valore</span><span class="sxs-lookup"><span data-stu-id="69c27-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69c27-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69c27-155">Minimum supported client</span></span><br/> | <span data-ttu-id="69c27-156">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69c27-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="69c27-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69c27-157">Minimum supported server</span></span><br/> | <span data-ttu-id="69c27-158">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="69c27-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69c27-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69c27-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="69c27-160"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69c27-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69c27-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69c27-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="69c27-162">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="69c27-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69c27-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="69c27-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="69c27-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="69c27-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="69c27-165">**\_carattere WM**</span><span class="sxs-lookup"><span data-stu-id="69c27-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="69c27-166">**KEYUP di WM \_**</span><span class="sxs-lookup"><span data-stu-id="69c27-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="69c27-167">**\_SYSCOMMAND WM**</span><span class="sxs-lookup"><span data-stu-id="69c27-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="69c27-168">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="69c27-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="69c27-169">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="69c27-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

