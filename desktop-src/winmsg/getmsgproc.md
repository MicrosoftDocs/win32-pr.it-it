---
UID: ''
title: Funzione di callback GetMsgProc
description: Il sistema chiama questa funzione quando una funzione Message riceve un messaggio da una coda di messaggi dell'applicazione.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "106303666"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="68f5d-103">GetMsgProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="68f5d-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="68f5d-104">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="68f5d-104">-description</span></span>

<span data-ttu-id="68f5d-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="68f5d-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="68f5d-106">Il sistema chiama questa funzione ogni volta che la funzione [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ha recuperato un messaggio da una coda di messaggi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68f5d-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="68f5d-107">Prima di restituire il messaggio recuperato al chiamante, il sistema passa il messaggio alla routine hook.</span><span class="sxs-lookup"><span data-stu-id="68f5d-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="68f5d-108">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="68f5d-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="68f5d-109">**GetMsgProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="68f5d-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="68f5d-110">-parametri</span><span class="sxs-lookup"><span data-stu-id="68f5d-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="68f5d-111">Codice [in]</span><span class="sxs-lookup"><span data-stu-id="68f5d-111">code [in]</span></span>

<span data-ttu-id="68f5d-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="68f5d-112">Type: **int**</span></span>

<span data-ttu-id="68f5d-113">Specifica se la routine hook deve elaborare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="68f5d-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="68f5d-114">Se il *codice* è **HC_ACTION**, la routine hook deve elaborare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="68f5d-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="68f5d-115">Se il *codice* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="68f5d-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="68f5d-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="68f5d-116">wParam [in]</span></span>

<span data-ttu-id="68f5d-117">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="68f5d-117">Type: **WPARAM**</span></span>

<span data-ttu-id="68f5d-118">Specifica se il messaggio è stato rimosso dalla coda.</span><span class="sxs-lookup"><span data-stu-id="68f5d-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="68f5d-119">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="68f5d-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="68f5d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="68f5d-120">Value</span></span> | <span data-ttu-id="68f5d-121">Significato</span><span class="sxs-lookup"><span data-stu-id="68f5d-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="68f5d-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="68f5d-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="68f5d-123">Il messaggio non è stato rimosso dalla coda.</span><span class="sxs-lookup"><span data-stu-id="68f5d-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="68f5d-124">(Applicazione chiamata funzione **PeekMessage** , che specifica il flag di **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="68f5d-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="68f5d-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="68f5d-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="68f5d-126">Il messaggio è stato rimosso dalla coda.</span><span class="sxs-lookup"><span data-stu-id="68f5d-126">The message has been removed from the queue.</span></span> <span data-ttu-id="68f5d-127">(Un'applicazione denominata **GetMessage** o chiamata funzione  **PeekMessage** , che specifica il flag di **PM_REMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="68f5d-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="68f5d-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="68f5d-128">lParam [in]</span></span>

<span data-ttu-id="68f5d-129">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="68f5d-129">Type: **LPARAM**</span></span>

<span data-ttu-id="68f5d-130">Puntatore a una struttura [msg](/windows/desktop/api/winuser/ns-winuser-msg) che contiene i dettagli sul messaggio.</span><span class="sxs-lookup"><span data-stu-id="68f5d-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="68f5d-131">-Restituisce</span><span class="sxs-lookup"><span data-stu-id="68f5d-131">-returns</span></span>

<span data-ttu-id="68f5d-132">Se il *codice* è minore di zero, la routine hook deve restituire il valore restituito da [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span><span class="sxs-lookup"><span data-stu-id="68f5d-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="68f5d-133">Se il *codice* è maggiore o uguale a zero, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_GETMESSAGE](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.</span><span class="sxs-lookup"><span data-stu-id="68f5d-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="68f5d-134">Se la routine hook non chiama **CallNextHookEx**, il valore restituito deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="68f5d-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="68f5d-135">-Note</span><span class="sxs-lookup"><span data-stu-id="68f5d-135">-remarks</span></span>

<span data-ttu-id="68f5d-136">La procedura **GetMsgProc** hook può esaminare o modificare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="68f5d-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="68f5d-137">Dopo che la routine hook restituisce il controllo al sistema, la funzione **GetMessage** o **PeekMessage** restituisce il messaggio, insieme alle eventuali modifiche, all'applicazione che l'ha originariamente chiamata.</span><span class="sxs-lookup"><span data-stu-id="68f5d-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="68f5d-138">Un'applicazione installa questa routine hook specificando il tipo di hook **WH_GETMESSAGE** e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="68f5d-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="68f5d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68f5d-139">See also</span></span>

[<span data-ttu-id="68f5d-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="68f5d-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="68f5d-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="68f5d-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="68f5d-142">MESSAGGIO</span><span class="sxs-lookup"><span data-stu-id="68f5d-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="68f5d-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="68f5d-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="68f5d-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="68f5d-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="68f5d-145">Hook</span><span class="sxs-lookup"><span data-stu-id="68f5d-145">Hooks</span></span>](hooks.md)
