---
UID: ''
title: Funzione di callback LowLevelMouseProc
description: Il sistema chiama questa funzione ogni volta che un nuovo evento di input del mouse sta per essere inserito in una coda di input del thread.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/26/2020
ms.locfileid: "104047547"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="b7d36-103">LowLevelMouseProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7d36-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="b7d36-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7d36-104">Description</span></span>

<span data-ttu-id="b7d36-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="b7d36-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="b7d36-106">Il sistema chiama questa funzione ogni volta che un nuovo evento di input del mouse sta per essere inserito in una coda di input del thread.</span><span class="sxs-lookup"><span data-stu-id="b7d36-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="b7d36-107">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="b7d36-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="b7d36-108">**LowLevelMouseProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="b7d36-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="b7d36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7d36-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="b7d36-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="b7d36-110">nCode [in]</span></span>

<span data-ttu-id="b7d36-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="b7d36-111">Type: **int**</span></span>

<span data-ttu-id="b7d36-112">Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b7d36-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="b7d36-113">Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="b7d36-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="b7d36-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b7d36-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="b7d36-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b7d36-115">Value</span></span> | <span data-ttu-id="b7d36-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b7d36-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="b7d36-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="b7d36-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="b7d36-118">I parametri *wParam* e *lParam* contengono informazioni su un messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="b7d36-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="b7d36-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="b7d36-119">wParam [in]</span></span>

<span data-ttu-id="b7d36-120">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="b7d36-120">Type: **WPARAM**</span></span>

<span data-ttu-id="b7d36-121">Identificatore del messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="b7d36-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="b7d36-122">Questo parametro può essere uno dei messaggi seguenti: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) o [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="b7d36-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="b7d36-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="b7d36-123">lParam [in]</span></span>

<span data-ttu-id="b7d36-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="b7d36-124">Type: **LPARAM**</span></span>

<span data-ttu-id="b7d36-125">Puntatore a una struttura [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="b7d36-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="b7d36-126">Restituisce</span><span class="sxs-lookup"><span data-stu-id="b7d36-126">Returns</span></span>

<span data-ttu-id="b7d36-127">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b7d36-127">Type: **LRESULT**</span></span>

<span data-ttu-id="b7d36-128">Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="b7d36-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="b7d36-129">Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_MOUSE_LL](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.</span><span class="sxs-lookup"><span data-stu-id="b7d36-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="b7d36-130">Se la routine hook ha elaborato il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio al resto della catena di hook o alla routine della finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b7d36-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d36-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7d36-131">Remarks</span></span>

<span data-ttu-id="b7d36-132">Un'applicazione installa la routine hook specificando il tipo di hook **WH_MOUSE_LL** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="b7d36-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="b7d36-133">Questo hook viene chiamato nel contesto del thread che lo ha installato.</span><span class="sxs-lookup"><span data-stu-id="b7d36-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="b7d36-134">La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.</span><span class="sxs-lookup"><span data-stu-id="b7d36-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="b7d36-135">Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="b7d36-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="b7d36-136">L'input del mouse può provenire dal driver del mouse locale o dalle chiamate alla funzione [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .</span><span class="sxs-lookup"><span data-stu-id="b7d36-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="b7d36-137">Se l'input deriva da una chiamata a **mouse_event**, l'input è stato "inserito".</span><span class="sxs-lookup"><span data-stu-id="b7d36-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="b7d36-138">Tuttavia, l'hook **WH_MOUSE_LL** non viene inserito in un altro processo.</span><span class="sxs-lookup"><span data-stu-id="b7d36-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="b7d36-139">Al contrario, il contesto ritorna al processo che ha installato l'hook e viene chiamato nel contesto originale.</span><span class="sxs-lookup"><span data-stu-id="b7d36-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="b7d36-140">Il contesto ritorna quindi all'applicazione che ha generato l'evento.</span><span class="sxs-lookup"><span data-stu-id="b7d36-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="b7d36-141">La routine hook deve elaborare un messaggio in meno tempo rispetto all'immissione dati specificata nel valore **LowLevelHooksTimeout** nella seguente chiave del registro di sistema: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="b7d36-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="b7d36-142">Il valore è espresso in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="b7d36-142">The value is in milliseconds.</span></span>
<span data-ttu-id="b7d36-143">Se la procedura di hook scade, il sistema passa il messaggio al gancio successivo.</span><span class="sxs-lookup"><span data-stu-id="b7d36-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="b7d36-144">Tuttavia, in Windows 7 e versioni successive, l'hook viene rimosso automaticamente senza essere chiamato.</span><span class="sxs-lookup"><span data-stu-id="b7d36-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="b7d36-145">L'applicazione non è in grado di sapere se l'hook è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="b7d36-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="b7d36-146">**Nota:**  Gli hook di debug non possono tenere traccia di questo tipo di hook del mouse di basso livello.</span><span class="sxs-lookup"><span data-stu-id="b7d36-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="b7d36-147">Se l'applicazione deve usare hook di basso livello, deve eseguire gli hook in un thread dedicato che passa il lavoro a un thread di lavoro e quindi restituisce immediatamente il risultato.</span><span class="sxs-lookup"><span data-stu-id="b7d36-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="b7d36-148">Nella maggior parte dei casi in cui l'applicazione deve usare hook di basso livello, deve invece monitorare l'input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="b7d36-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="b7d36-149">Questo perché l'input non elaborato può monitorare in modo asincrono i messaggi del mouse e della tastiera destinati ad altri thread in modo più efficace rispetto agli hook di basso livello.</span><span class="sxs-lookup"><span data-stu-id="b7d36-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="b7d36-150">Per ulteriori informazioni sull'input non elaborato, vedere [input non elaborato](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="b7d36-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="b7d36-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7d36-151">See also</span></span>

[<span data-ttu-id="b7d36-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="b7d36-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="b7d36-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="b7d36-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="b7d36-154">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="b7d36-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="b7d36-155">MSLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="b7d36-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="b7d36-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="b7d36-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="b7d36-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="b7d36-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="b7d36-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="b7d36-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="b7d36-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="b7d36-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="b7d36-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="b7d36-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="b7d36-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="b7d36-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="b7d36-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="b7d36-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="b7d36-163">Hook</span><span class="sxs-lookup"><span data-stu-id="b7d36-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="b7d36-164">Informazioni sugli hook</span><span class="sxs-lookup"><span data-stu-id="b7d36-164">About Hooks</span></span>](about-hooks.md)
