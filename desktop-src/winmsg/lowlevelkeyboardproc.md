---
UID: ''
title: Funzione di callback LowLevelKeyboardProc
description: Il sistema chiama questa funzione ogni volta che un nuovo evento di input da tastiera sta per essere inserito in una coda di input del thread.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "104046466"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="78617-103">LowLevelKeyboardProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="78617-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="78617-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78617-104">Description</span></span>

<span data-ttu-id="78617-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="78617-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="78617-106">Il sistema chiama questa funzione ogni volta che un nuovo evento di input da tastiera sta per essere inserito in una coda di input del thread.</span><span class="sxs-lookup"><span data-stu-id="78617-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="78617-107">**Nota:**  Quando questa funzione di callback viene chiamata in risposta a una modifica nello stato di una chiave, la funzione di callback viene chiamata prima che lo stato asincrono della chiave venga aggiornato.</span><span class="sxs-lookup"><span data-stu-id="78617-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="78617-108">Di conseguenza, non è possibile determinare lo stato asincrono della chiave chiamando [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) dall'interno della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="78617-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="78617-109">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="78617-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="78617-110">**LowLevelKeyboardProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="78617-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="78617-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="78617-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="78617-112">Codice [in]</span><span class="sxs-lookup"><span data-stu-id="78617-112">code [in]</span></span>

<span data-ttu-id="78617-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="78617-113">Type: **int**</span></span>

<span data-ttu-id="78617-114">Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="78617-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="78617-115">Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="78617-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="78617-116">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="78617-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="78617-117">Valore</span><span class="sxs-lookup"><span data-stu-id="78617-117">Value</span></span> | <span data-ttu-id="78617-118">Significato</span><span class="sxs-lookup"><span data-stu-id="78617-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="78617-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="78617-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="78617-120">I parametri *wParam* e *lParam* contengono informazioni su un messaggio della tastiera.</span><span class="sxs-lookup"><span data-stu-id="78617-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="78617-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="78617-121">wParam [in]</span></span>

<span data-ttu-id="78617-122">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="78617-122">Type: **WPARAM**</span></span>

<span data-ttu-id="78617-123">Identificatore del messaggio della tastiera.</span><span class="sxs-lookup"><span data-stu-id="78617-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="78617-124">Questo parametro può essere uno dei messaggi seguenti: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)o [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="78617-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="78617-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="78617-125">lParam [in]</span></span>

<span data-ttu-id="78617-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="78617-126">Type: **LPARAM**</span></span>

<span data-ttu-id="78617-127">Puntatore a una struttura [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="78617-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="78617-128">Restituisce</span><span class="sxs-lookup"><span data-stu-id="78617-128">Returns</span></span>

<span data-ttu-id="78617-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="78617-129">Type: **LRESULT**</span></span>

<span data-ttu-id="78617-130">Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="78617-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="78617-131">Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_KEYBOARD_LL](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.</span><span class="sxs-lookup"><span data-stu-id="78617-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="78617-132">Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="78617-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="78617-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="78617-133">Remarks</span></span>

<span data-ttu-id="78617-134">Un'applicazione installa la routine hook specificando il tipo di hook **WH_KEYBOARD_LL** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="78617-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="78617-135">Questo hook viene chiamato nel contesto del thread che lo ha installato.</span><span class="sxs-lookup"><span data-stu-id="78617-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="78617-136">La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.</span><span class="sxs-lookup"><span data-stu-id="78617-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="78617-137">Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="78617-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="78617-138">L'input da tastiera può provenire dal driver della tastiera locale o dalle chiamate alla funzione [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .</span><span class="sxs-lookup"><span data-stu-id="78617-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="78617-139">Se l'input deriva da una chiamata a **keybd_event**, l'input è stato "inserito".</span><span class="sxs-lookup"><span data-stu-id="78617-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="78617-140">Tuttavia, l'hook WH_KEYBOARD_LL non viene inserito in un altro processo.</span><span class="sxs-lookup"><span data-stu-id="78617-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="78617-141">Al contrario, il contesto ritorna al processo che ha installato l'hook e viene chiamato nel contesto originale.</span><span class="sxs-lookup"><span data-stu-id="78617-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="78617-142">Il contesto ritorna quindi all'applicazione che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="78617-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="78617-143">La routine hook deve elaborare un messaggio in meno tempo rispetto all'immissione dati specificata nel valore **LowLevelHooksTimeout** nella seguente chiave del registro di sistema: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="78617-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="78617-144">Il valore è espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="78617-144">The value is in milliseconds.</span></span>
<span data-ttu-id="78617-145">Se la procedura di hook scade, il sistema passa il messaggio al gancio successivo.</span><span class="sxs-lookup"><span data-stu-id="78617-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="78617-146">Tuttavia, in Windows 7 e versioni successive, l'hook viene rimosso automaticamente senza essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="78617-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="78617-147">L'applicazione non è in grado di sapere se l'hook è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="78617-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="78617-148">Nota: gli hook di debug non possono tenere traccia di questo tipo di hook di tastiera di basso livello.</span><span class="sxs-lookup"><span data-stu-id="78617-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="78617-149">Se l'applicazione deve usare hook di basso livello, deve eseguire gli hook in un thread dedicato che passa il lavoro a un thread di lavoro e quindi restituisce immediatamente il risultato.</span><span class="sxs-lookup"><span data-stu-id="78617-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="78617-150">Nella maggior parte dei casi in cui l'applicazione deve usare hook di basso livello, deve invece monitorare l'input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="78617-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="78617-151">Questo perché l'input non elaborato può monitorare in modo asincrono i messaggi del mouse e della tastiera destinati ad altri thread in modo più efficace rispetto agli hook di basso livello.</span><span class="sxs-lookup"><span data-stu-id="78617-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="78617-152">Per ulteriori informazioni sull'input non elaborato, vedere [input non elaborato](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="78617-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="78617-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78617-153">See also</span></span>

[<span data-ttu-id="78617-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="78617-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="78617-155">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="78617-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="78617-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="78617-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="78617-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="78617-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="78617-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="78617-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="78617-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="78617-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="78617-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="78617-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="78617-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="78617-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="78617-162">Hook</span><span class="sxs-lookup"><span data-stu-id="78617-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="78617-163">Informazioni sugli hook</span><span class="sxs-lookup"><span data-stu-id="78617-163">About Hooks</span></span>](about-hooks.md)
