---
UID: ''
title: Funzione di callback MouseProc
description: Il sistema chiama questa funzione quando un'applicazione chiama una funzione di messaggio ed è presente un messaggio del mouse da elaborare.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/11/2020
ms.locfileid: "106299552"
---
# <a name="mouseproc-function"></a><span data-ttu-id="3e368-103">MouseProc (funzione)</span><span class="sxs-lookup"><span data-stu-id="3e368-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="3e368-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e368-104">Description</span></span>

<span data-ttu-id="3e368-105">Funzione di callback definita dall'applicazione o definita dalla libreria utilizzata con la funzione [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="3e368-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="3e368-106">Il sistema chiama questa funzione ogni volta che un'applicazione chiama la funzione [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) ed è presente un messaggio del mouse da elaborare.</span><span class="sxs-lookup"><span data-stu-id="3e368-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="3e368-107">Il tipo **HookProc** definisce un puntatore a questa funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="3e368-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="3e368-108">**MouseProc** è un segnaposto per il nome di funzione definito dall'applicazione o dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="3e368-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="3e368-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e368-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="3e368-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="3e368-110">nCode [in]</span></span>

<span data-ttu-id="3e368-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="3e368-111">Type: **int**</span></span>

<span data-ttu-id="3e368-112">Codice utilizzato dalla routine hook per determinare la modalità di elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="3e368-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="3e368-113">Se *nCode* è minore di zero, la routine hook deve passare il messaggio alla funzione [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) senza ulteriore elaborazione e deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="3e368-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="3e368-114">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e368-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="3e368-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3e368-115">Value</span></span> | <span data-ttu-id="3e368-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3e368-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="3e368-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="3e368-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="3e368-118">I parametri *wParam* e *lParam* contengono informazioni su un messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="3e368-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="3e368-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="3e368-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="3e368-120">I parametri *wParam* e *lParam* contengono informazioni su un messaggio del mouse e il messaggio del mouse non è stato rimosso dalla coda di messaggi.</span><span class="sxs-lookup"><span data-stu-id="3e368-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="3e368-121">(Applicazione chiamata funzione **PeekMessage** , che specifica il flag di **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="3e368-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="3e368-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="3e368-122">wParam [in]</span></span>

<span data-ttu-id="3e368-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="3e368-123">Type: **WPARAM**</span></span>

<span data-ttu-id="3e368-124">Identificatore del messaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="3e368-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="3e368-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="3e368-125">lParam [in]</span></span>

<span data-ttu-id="3e368-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="3e368-126">Type: **LPARAM**</span></span>

<span data-ttu-id="3e368-127">Puntatore a una struttura [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .</span><span class="sxs-lookup"><span data-stu-id="3e368-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="3e368-128">Restituisce</span><span class="sxs-lookup"><span data-stu-id="3e368-128">Returns</span></span>

<span data-ttu-id="3e368-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="3e368-129">Type: **LRESULT**</span></span>

<span data-ttu-id="3e368-130">Se *nCode* è minore di zero, la routine hook deve restituire il valore restituito da **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="3e368-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="3e368-131">Se *nCode* è maggiore o uguale a zero e la routine hook non ha elaborato il messaggio, è consigliabile chiamare **CallNextHookEx** e restituire il valore restituito; in caso contrario, altre applicazioni che hanno installato [WH_MOUSE](about-hooks.md) hook non riceveranno le notifiche Hook e potrebbero comportarsi in modo errato.</span><span class="sxs-lookup"><span data-stu-id="3e368-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="3e368-132">Se la routine hook elabora il messaggio, può restituire un valore diverso da zero per impedire al sistema di passare il messaggio alla routine della finestra di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3e368-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e368-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e368-133">Remarks</span></span>

<span data-ttu-id="3e368-134">Un'applicazione installa la routine hook specificando il tipo di hook WH_MOUSE e un puntatore alla routine hook in una chiamata alla funzione **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="3e368-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="3e368-135">La routine hook non deve installare una funzione di callback [WH_JOURNALPLAYBACK](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="3e368-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="3e368-136">Questo hook può essere chiamato nel contesto del thread che lo ha installato.</span><span class="sxs-lookup"><span data-stu-id="3e368-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="3e368-137">La chiamata viene effettuata inviando un messaggio al thread che ha installato l'hook.</span><span class="sxs-lookup"><span data-stu-id="3e368-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="3e368-138">Pertanto, il thread che ha installato l'hook deve disporre di un ciclo di messaggi.</span><span class="sxs-lookup"><span data-stu-id="3e368-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e368-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e368-139">See also</span></span>

[<span data-ttu-id="3e368-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="3e368-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="3e368-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="3e368-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="3e368-142">MOUSEHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="3e368-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="3e368-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="3e368-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="3e368-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="3e368-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="3e368-145">Hook</span><span class="sxs-lookup"><span data-stu-id="3e368-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="3e368-146">Informazioni sugli hook</span><span class="sxs-lookup"><span data-stu-id="3e368-146">About Hooks</span></span>](about-hooks.md)
