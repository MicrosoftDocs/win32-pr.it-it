---
title: Messaggio WM_UNICHAR (winuser. h)
description: Il messaggio di WM \_ UNICHAR può essere usato da un'applicazione per inserire l'input in altre finestre.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Input della tastiera e del mouse WM_UNICHAR messaggio
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301676"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="814da-104">\_Messaggio UNICHAR WM</span><span class="sxs-lookup"><span data-stu-id="814da-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="814da-105">Il messaggio di **WM \_ UNICHAR** può essere usato da un'applicazione per inserire l'input in altre finestre.</span><span class="sxs-lookup"><span data-stu-id="814da-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="814da-106">Questo messaggio contiene il codice carattere della chiave che è stata premuta.</span><span class="sxs-lookup"><span data-stu-id="814da-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="814da-107">(Verificare se un'app di destinazione può elaborare messaggi **WM \_ UNICHAR** inviando il messaggio con *wParam* impostato su **Unicode \_ nochar**).</span><span class="sxs-lookup"><span data-stu-id="814da-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="814da-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="814da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814da-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="814da-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="814da-110">Codice carattere della chiave.</span><span class="sxs-lookup"><span data-stu-id="814da-110">The character code of the key.</span></span>

<span data-ttu-id="814da-111">Se *wParam* è **Unicode \_ nochar** e l'applicazione elabora il messaggio, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="814da-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="814da-112">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituirà **false** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="814da-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="814da-113">Se *wParam* non è **Unicode \_ nochar**, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="814da-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="814da-114">Il  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Unicode Invia un messaggio [**WM \_ char**](wm-char.md) con gli stessi parametri e la funzione **DefWindowProc** ANSI invia uno o due messaggi **WM \_ char** con i caratteri ANSI corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="814da-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="814da-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="814da-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="814da-116">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato precedente e il flag di stato di transizione, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="814da-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="814da-117">BITS</span><span class="sxs-lookup"><span data-stu-id="814da-117">Bits</span></span>  | <span data-ttu-id="814da-118">Significato</span><span class="sxs-lookup"><span data-stu-id="814da-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814da-119">0-15</span><span class="sxs-lookup"><span data-stu-id="814da-119">0-15</span></span>  | <span data-ttu-id="814da-120">Numero di ripetizioni per il messaggio corrente.</span><span class="sxs-lookup"><span data-stu-id="814da-120">The repeat count for the current message.</span></span> <span data-ttu-id="814da-121">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in modo ripetitivo a causa dell'arresto della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="814da-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="814da-122">Se la sequenza di tasti viene mantenuta abbastanza a lungo, vengono inviati più messaggi.</span><span class="sxs-lookup"><span data-stu-id="814da-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="814da-123">Tuttavia, il numero di ripetizioni non è cumulativo.</span><span class="sxs-lookup"><span data-stu-id="814da-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="814da-124">16-23</span><span class="sxs-lookup"><span data-stu-id="814da-124">16-23</span></span> | <span data-ttu-id="814da-125">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="814da-125">The scan code.</span></span> <span data-ttu-id="814da-126">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="814da-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="814da-127">24</span><span class="sxs-lookup"><span data-stu-id="814da-127">24</span></span>    | <span data-ttu-id="814da-128">Indica se la chiave è una chiave estesa, ad esempio i tasti ALT e CTRL a destra che vengono visualizzati in una tastiera migliorata 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="814da-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="814da-129">Il valore è 1 se è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="814da-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="814da-130">25-28</span><span class="sxs-lookup"><span data-stu-id="814da-130">25-28</span></span> | <span data-ttu-id="814da-131">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="814da-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="814da-132">29</span><span class="sxs-lookup"><span data-stu-id="814da-132">29</span></span>    | <span data-ttu-id="814da-133">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="814da-133">The context code.</span></span> <span data-ttu-id="814da-134">Il valore è 1 se il tasto ALT è premuto mentre il tasto è premuto; in caso contrario, il valore è 0.</span><span class="sxs-lookup"><span data-stu-id="814da-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="814da-135">30</span><span class="sxs-lookup"><span data-stu-id="814da-135">30</span></span>    | <span data-ttu-id="814da-136">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="814da-136">The previous key state.</span></span> <span data-ttu-id="814da-137">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio oppure è 0 se la chiave è attiva.</span><span class="sxs-lookup"><span data-stu-id="814da-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="814da-138">31</span><span class="sxs-lookup"><span data-stu-id="814da-138">31</span></span>    | <span data-ttu-id="814da-139">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="814da-139">The transition state.</span></span> <span data-ttu-id="814da-140">Il valore è 1 se la chiave viene rilasciata oppure è 0 se viene premuto il tasto.</span><span class="sxs-lookup"><span data-stu-id="814da-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="814da-141">Per informazioni dettagliate, vedere [flag dei messaggi di sequenza di tasti](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="814da-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814da-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="814da-142">Return value</span></span>

<span data-ttu-id="814da-143">Un'applicazione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="814da-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="814da-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="814da-144">Remarks</span></span>

<span data-ttu-id="814da-145">Il messaggio di **WM \_ UNICHAR** è simile a [**WM \_ char**](wm-char.md), ma usa Unicode Transformation Format (UTF)-32, mentre **WM \_ char** usa la codifica UTF-16.</span><span class="sxs-lookup"><span data-stu-id="814da-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="814da-146">Questo messaggio è progettato per inviare o inviare caratteri Unicode alle finestre ANSI e può gestire i caratteri del piano supplementare Unicode.</span><span class="sxs-lookup"><span data-stu-id="814da-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="814da-147">Poiché non esiste necessariamente una corrispondenza uno-a-uno tra i tasti premuti e i messaggi di tipo carattere generati, le informazioni nella parola più significativa del parametro *lParam* non sono in genere utili per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="814da-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="814da-148">Le informazioni nella parola più ordinata si applicano solo al messaggio più recente di [**WM \_ KeyDown**](wm-keydown.md) che precede l'inserimento del messaggio **WM \_ UNICHAR** .</span><span class="sxs-lookup"><span data-stu-id="814da-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="814da-149">Per le tastiere avanzate 101 e 102-Key, le chiavi estese sono i tasti ALT e CTRL destro nella sezione principale della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e freccia nei cluster a sinistra del tastierino numerico; e la divisione (/) e immettere le chiavi nel tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="814da-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="814da-150">È possibile che alcune altre tastiere supportino il bit della chiave estesa nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="814da-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="814da-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="814da-151">Requirements</span></span>



| <span data-ttu-id="814da-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="814da-152">Requirement</span></span> | <span data-ttu-id="814da-153">Valore</span><span class="sxs-lookup"><span data-stu-id="814da-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814da-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="814da-154">Minimum supported client</span></span><br/> | <span data-ttu-id="814da-155">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="814da-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="814da-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="814da-156">Minimum supported server</span></span><br/> | <span data-ttu-id="814da-157">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="814da-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="814da-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="814da-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="814da-159"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="814da-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814da-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="814da-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="814da-161">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="814da-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="814da-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="814da-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="814da-163">**\_carattere WM**</span><span class="sxs-lookup"><span data-stu-id="814da-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="814da-164">**KeyDown di WM \_**</span><span class="sxs-lookup"><span data-stu-id="814da-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="814da-165">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="814da-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="814da-166">Input da tastiera</span><span class="sxs-lookup"><span data-stu-id="814da-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

