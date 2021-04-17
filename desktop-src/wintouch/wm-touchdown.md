---
title: Messaggio WM_TOUCH (winuser. h)
description: Notifica alla finestra quando uno o più punti di tocco, ad esempio un dito o una penna, tocca una superficie del digitalizzatore sensibile al tocco.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- WM_TOUCH messaggio Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400763"
---
# <a name="wm_touch-message"></a><span data-ttu-id="a40de-104">\_Messaggio WM touch</span><span class="sxs-lookup"><span data-stu-id="a40de-104">WM\_TOUCH message</span></span>

<span data-ttu-id="a40de-105">Notifica alla finestra quando uno o più punti di tocco, ad esempio un dito o una penna, tocca una superficie del digitalizzatore sensibile al tocco.</span><span class="sxs-lookup"><span data-stu-id="a40de-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="a40de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a40de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a40de-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a40de-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a40de-108">La parola di ordine inferiore contiene il numero di punti di tocco associati a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a40de-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="a40de-109">La parola più ordinata è riservata per un utilizzo futuro.</span><span class="sxs-lookup"><span data-stu-id="a40de-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a40de-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a40de-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a40de-111">Contiene un handle di input tocco che può essere utilizzato in una chiamata a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) per recuperare informazioni dettagliate sui punti di tocco associati a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a40de-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="a40de-112">Questo handle è valido solo all'interno del processo corrente e non deve essere passato tra processi, ad eccezione di **lParam** in una chiamata **SendMessage** o **PostMessage** .</span><span class="sxs-lookup"><span data-stu-id="a40de-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="a40de-113">Quando l'applicazione non richiede più questo handle, l'applicazione deve chiamare **CloseTouchInputHandle** per liberare la memoria del processo associata a questo handle.</span><span class="sxs-lookup"><span data-stu-id="a40de-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="a40de-114">In caso contrario, può verificarsi una perdita di memoria dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a40de-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="a40de-115">Si noti che l'handle di input tocco in questo parametro non è più valido dopo che il messaggio è stato passato a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a40de-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="a40de-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) si chiude e invalida questo handle.</span><span class="sxs-lookup"><span data-stu-id="a40de-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="a40de-117">Si noti inoltre che l'handle di input tocco in questo parametro non è più valido dopo che il messaggio è stato inviato tramite [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una delle relative varianti.</span><span class="sxs-lookup"><span data-stu-id="a40de-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="a40de-118">Queste funzioni chiudono e invalideranno questo handle.</span><span class="sxs-lookup"><span data-stu-id="a40de-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a40de-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a40de-119">Return value</span></span>

<span data-ttu-id="a40de-120">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="a40de-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="a40de-121">Se l'applicazione non elabora il messaggio, deve chiamare [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a40de-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="a40de-122">Se non si esegue questa operazione, l'applicazione perde memoria perché l'handle di input tocco non è chiuso e la memoria del processo associata non viene liberata.</span><span class="sxs-lookup"><span data-stu-id="a40de-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="a40de-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a40de-123">Remarks</span></span>

<span data-ttu-id="a40de-124">**WM \_** I messaggi touch non rispettano le aree **HTTRANSPARENT** di Windows.</span><span class="sxs-lookup"><span data-stu-id="a40de-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="a40de-125">Se una finestra restituisce **HTTRANSPARENT** in risposta a un messaggio **WM \_ NCHITTEST** , i messaggi del mouse passano al padre e i messaggi **WM \_ touch** passano direttamente alla finestra.</span><span class="sxs-lookup"><span data-stu-id="a40de-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="a40de-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="a40de-126">Examples</span></span>

<span data-ttu-id="a40de-127">Il codice seguente è un esempio di come ottenere informazioni dettagliate sull'input di tocco associate a questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a40de-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="a40de-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a40de-128">Requirements</span></span>



| <span data-ttu-id="a40de-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a40de-129">Requirement</span></span> | <span data-ttu-id="a40de-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a40de-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a40de-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40de-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a40de-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a40de-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a40de-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a40de-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a40de-134">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a40de-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="a40de-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a40de-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a40de-136"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a40de-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a40de-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a40de-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a40de-138">Messaggi</span><span class="sxs-lookup"><span data-stu-id="a40de-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="a40de-139">Guida alla programmazione di modifiche e inerzia</span><span class="sxs-lookup"><span data-stu-id="a40de-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="a40de-140">Guida alla programmazione di input per Windows Touch</span><span class="sxs-lookup"><span data-stu-id="a40de-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

