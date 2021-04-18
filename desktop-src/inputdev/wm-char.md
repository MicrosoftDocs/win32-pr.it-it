---
title: Messaggio WM_CHAR (winuser. h)
description: Inviato alla finestra con lo stato attivo quando un \_ messaggio di WM KeyDown viene convertito dalla funzione TranslateMessage. Il \_ messaggio WM Char contiene il codice carattere della chiave che è stata premuta.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Input della tastiera e del mouse WM_CHAR messaggio
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328281"
---
# <a name="wm_char-message"></a><span data-ttu-id="73307-105">\_Messaggio WM char</span><span class="sxs-lookup"><span data-stu-id="73307-105">WM\_CHAR message</span></span>

<span data-ttu-id="73307-106">Inviato alla finestra con lo stato attivo quando un messaggio di [**WM \_ KeyDown**](wm-keydown.md) viene convertito dalla funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="73307-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="73307-107">Il messaggio **WM \_ char** contiene il codice carattere della chiave che è stata premuta.</span><span class="sxs-lookup"><span data-stu-id="73307-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="73307-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="73307-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73307-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73307-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73307-110">Codice carattere della chiave.</span><span class="sxs-lookup"><span data-stu-id="73307-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="73307-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73307-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="73307-112">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="73307-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="73307-113">BITS</span><span class="sxs-lookup"><span data-stu-id="73307-113">Bits</span></span>  | <span data-ttu-id="73307-114">Significato</span><span class="sxs-lookup"><span data-stu-id="73307-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73307-115">0-15</span><span class="sxs-lookup"><span data-stu-id="73307-115">0-15</span></span>  | <span data-ttu-id="73307-116">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="73307-116">The repeat count for the current message.</span></span> <span data-ttu-id="73307-117">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="73307-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="73307-118">Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="73307-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="73307-119">Tuttavia, il numero di ripetizioni non è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="73307-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="73307-120">16-23</span><span class="sxs-lookup"><span data-stu-id="73307-120">16-23</span></span> | <span data-ttu-id="73307-121">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="73307-121">The scan code.</span></span> <span data-ttu-id="73307-122">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="73307-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="73307-123">24</span><span class="sxs-lookup"><span data-stu-id="73307-123">24</span></span>    | <span data-ttu-id="73307-124">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="73307-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="73307-125">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="73307-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="73307-126">25-28</span><span class="sxs-lookup"><span data-stu-id="73307-126">25-28</span></span> | <span data-ttu-id="73307-127">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="73307-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="73307-128">29</span><span class="sxs-lookup"><span data-stu-id="73307-128">29</span></span>    | <span data-ttu-id="73307-129">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="73307-129">The context code.</span></span> <span data-ttu-id="73307-130">Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.</span><span class="sxs-lookup"><span data-stu-id="73307-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="73307-131">30</span><span class="sxs-lookup"><span data-stu-id="73307-131">30</span></span>    | <span data-ttu-id="73307-132">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="73307-132">The previous key state.</span></span> <span data-ttu-id="73307-133">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.</span><span class="sxs-lookup"><span data-stu-id="73307-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="73307-134">31</span><span class="sxs-lookup"><span data-stu-id="73307-134">31</span></span>    | <span data-ttu-id="73307-135">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="73307-135">The transition state.</span></span> <span data-ttu-id="73307-136">Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.</span><span class="sxs-lookup"><span data-stu-id="73307-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="73307-137">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="73307-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73307-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73307-138">Return value</span></span>

<span data-ttu-id="73307-139">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="73307-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="73307-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="73307-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="73307-141">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="73307-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="73307-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="73307-142">Remarks</span></span>

<span data-ttu-id="73307-143">Il messaggio **WM \_ char** usa Unicode Transformation Format (UTF)-16.</span><span class="sxs-lookup"><span data-stu-id="73307-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="73307-144">Non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, quindi le informazioni nella parola più significativa del parametro *lParam* non sono in genere utili per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="73307-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="73307-145">Le informazioni nella parola più ordinata si applicano solo al messaggio più recente di [**WM \_ KeyDown**](wm-keydown.md) che precede la pubblicazione del messaggio **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="73307-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="73307-146">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL destro nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="73307-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="73307-147">È possibile che alcune altre tastiere supportino il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="73307-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="73307-148">Il messaggio di [**WM \_ UNICHAR**](wm-unichar.md) è uguale a **WM \_ char**, ad eccezione del fatto che usa UTF-32.</span><span class="sxs-lookup"><span data-stu-id="73307-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="73307-149">È progettato per inviare o inviare caratteri Unicode alle finestre ANSI e può gestire i caratteri del piano supplementare Unicode.</span><span class="sxs-lookup"><span data-stu-id="73307-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="73307-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73307-150">Requirements</span></span>



| <span data-ttu-id="73307-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="73307-151">Requirement</span></span> | <span data-ttu-id="73307-152">Valore</span><span class="sxs-lookup"><span data-stu-id="73307-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73307-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73307-153">Minimum supported client</span></span><br/> | <span data-ttu-id="73307-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="73307-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="73307-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73307-155">Minimum supported server</span></span><br/> | <span data-ttu-id="73307-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="73307-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="73307-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73307-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="73307-158"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73307-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73307-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73307-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="73307-160">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="73307-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="73307-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="73307-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="73307-162">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="73307-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="73307-163">**UNICHAR WM \_**</span><span class="sxs-lookup"><span data-stu-id="73307-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="73307-164">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="73307-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="73307-165">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="73307-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

