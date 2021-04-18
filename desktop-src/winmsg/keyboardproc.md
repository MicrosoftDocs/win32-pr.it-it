---
UID: ''
title: Funzione di callback KeyboardProc
description: Il sistema chiama questa funzione per ottenere una funzione di messaggio ed è presente un messaggio da tastiera da elaborare.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299551"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="4af8a-103">KeyboardProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="4af8a-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="4af8a-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4af8a-104">Description</span></span>

<span data-ttu-id="4af8a-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="4af8a-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="4af8a-106">Il sistema chiama questa funzione ogni volta che un'applicazione chiama la funzione [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ed è presente un messaggio della tastiera ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) o [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) da elaborare.</span><span class="sxs-lookup"><span data-stu-id="4af8a-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="4af8a-107">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="4af8a-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="4af8a-108">**KeyboardProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="4af8a-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="4af8a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4af8a-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="4af8a-110">Codice [in]</span><span class="sxs-lookup"><span data-stu-id="4af8a-110">code [in]</span></span>

<span data-ttu-id="4af8a-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4af8a-111">Type: **int**</span></span>

<span data-ttu-id="4af8a-112">Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="4af8a-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="4af8a-113">Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4af8a-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="4af8a-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4af8a-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="4af8a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4af8a-115">Value</span></span> | <span data-ttu-id="4af8a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4af8a-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="4af8a-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="4af8a-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="4af8a-118">I parametri *wParam* e *lParam* contengono informazioni su un messaggio di sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="4af8a-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="4af8a-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="4af8a-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="4af8a-120">I parametri *wParam* e *lParam* contengono informazioni su un messaggio di sequenza di tasti e il messaggio di sequenza di tasti non è stato rimosso dalla coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="4af8a-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="4af8a-121">(Applicazione chiamata funzione **PeekMessage** , che specifica il flag di **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="4af8a-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="4af8a-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="4af8a-122">wParam [in]</span></span>

<span data-ttu-id="4af8a-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="4af8a-123">Type: **WPARAM**</span></span>

<span data-ttu-id="4af8a-124">[Codice della chiave virtuale](/windows/desktop/inputdev/virtual-key-codes) della chiave che ha generato il messaggio di sequenza di tasti.</span><span class="sxs-lookup"><span data-stu-id="4af8a-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="4af8a-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="4af8a-125">lParam [in]</span></span>

<span data-ttu-id="4af8a-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="4af8a-126">Type: **LPARAM**</span></span>

<span data-ttu-id="4af8a-127">Il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato di chiave precedente e il flag di stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="4af8a-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="4af8a-128">Per ulteriori informazioni sul parametro *lParam* , vedere [flag dei messaggi di sequenza di tasti](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="4af8a-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="4af8a-129">Nella tabella seguente vengono descritti i bit di questo valore.</span><span class="sxs-lookup"><span data-stu-id="4af8a-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="4af8a-130">BITS</span><span class="sxs-lookup"><span data-stu-id="4af8a-130">Bits</span></span> | <span data-ttu-id="4af8a-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4af8a-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="4af8a-132">0-15</span><span class="sxs-lookup"><span data-stu-id="4af8a-132">0-15</span></span> | <span data-ttu-id="4af8a-133">Conteggio delle ripetizioni.</span><span class="sxs-lookup"><span data-stu-id="4af8a-133">The repeat count.</span></span> <span data-ttu-id="4af8a-134">Il valore è il numero di volte in cui la sequenza di tasti viene ripetuta in seguito alla chiusura della chiave da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4af8a-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="4af8a-135">16-23</span><span class="sxs-lookup"><span data-stu-id="4af8a-135">16-23</span></span> | <span data-ttu-id="4af8a-136">Codice di analisi.</span><span class="sxs-lookup"><span data-stu-id="4af8a-136">The scan code.</span></span> <span data-ttu-id="4af8a-137">Il valore dipende dall'OEM.</span><span class="sxs-lookup"><span data-stu-id="4af8a-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="4af8a-138">24</span><span class="sxs-lookup"><span data-stu-id="4af8a-138">24</span></span> | <span data-ttu-id="4af8a-139">Indica se la chiave è una chiave estesa, ad esempio un tasto funzione o una chiave sul tastierino numerico.</span><span class="sxs-lookup"><span data-stu-id="4af8a-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="4af8a-140">Il valore è 1 se la chiave è una chiave estesa; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="4af8a-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="4af8a-141">25-28</span><span class="sxs-lookup"><span data-stu-id="4af8a-141">25-28</span></span> | <span data-ttu-id="4af8a-142">Riservato.</span><span class="sxs-lookup"><span data-stu-id="4af8a-142">Reserved.</span></span> |
| <span data-ttu-id="4af8a-143">29</span><span class="sxs-lookup"><span data-stu-id="4af8a-143">29</span></span> | <span data-ttu-id="4af8a-144">Codice del contesto.</span><span class="sxs-lookup"><span data-stu-id="4af8a-144">The context code.</span></span> <span data-ttu-id="4af8a-145">Il valore è 1 se il tasto ALT è premuto; in caso contrario, è 0.</span><span class="sxs-lookup"><span data-stu-id="4af8a-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="4af8a-146">30</span><span class="sxs-lookup"><span data-stu-id="4af8a-146">30</span></span> | <span data-ttu-id="4af8a-147">Stato precedente della chiave.</span><span class="sxs-lookup"><span data-stu-id="4af8a-147">The previous key state.</span></span> <span data-ttu-id="4af8a-148">Il valore è 1 se la chiave è inattiva prima dell'invio del messaggio; è 0 se il tasto è attivo.</span><span class="sxs-lookup"><span data-stu-id="4af8a-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="4af8a-149">31</span><span class="sxs-lookup"><span data-stu-id="4af8a-149">31</span></span> | <span data-ttu-id="4af8a-150">Stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="4af8a-150">The transition state.</span></span> <span data-ttu-id="4af8a-151">Il valore è 0 se viene premuto il tasto e 1 se è in fase di rilascio.</span><span class="sxs-lookup"><span data-stu-id="4af8a-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="4af8a-152">Restituisce</span><span class="sxs-lookup"><span data-stu-id="4af8a-152">Returns</span></span>

<span data-ttu-id="4af8a-153">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="4af8a-153">Type: **LRESULT**</span></span>

<span data-ttu-id="4af8a-154">Se il *codice* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="4af8a-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="4af8a-155">Se il *codice* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_KEYBOARD](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.</span><span class="sxs-lookup"><span data-stu-id="4af8a-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="4af8a-156">Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4af8a-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af8a-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="4af8a-157">Remarks</span></span>

<span data-ttu-id="4af8a-158">Un'applicazione installa la routine hook specificando il tipo di hook **WH_KEYBOARD** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="4af8a-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="4af8a-159">Questo hook può essere chiamato nel contesto del thread che lo ha installato.</span><span class="sxs-lookup"><span data-stu-id="4af8a-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="4af8a-160">La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.</span><span class="sxs-lookup"><span data-stu-id="4af8a-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="4af8a-161">Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="4af8a-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="4af8a-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4af8a-162">See also</span></span>

[<span data-ttu-id="4af8a-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="4af8a-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="4af8a-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="4af8a-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="4af8a-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="4af8a-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="4af8a-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="4af8a-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="4af8a-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="4af8a-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="4af8a-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="4af8a-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="4af8a-169">Hook</span><span class="sxs-lookup"><span data-stu-id="4af8a-169">Hooks</span></span>](hooks.md)
