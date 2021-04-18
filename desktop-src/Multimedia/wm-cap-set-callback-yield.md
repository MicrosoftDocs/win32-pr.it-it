---
title: Messaggio di WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ yield imposta una funzione di callback nell'applicazione. AVICap chiama questa procedura quando la finestra di acquisizione viene restituita durante l'acquisizione di flussi. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301010"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="71d63-106">\_ \_ \_ Messaggio prodotto di callback \_ set di estremità WM</span><span class="sxs-lookup"><span data-stu-id="71d63-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="71d63-107">Il messaggio **WM \_ Cap \_ set \_ callback \_ yield** imposta una funzione di callback nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="71d63-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="71d63-108">AVICap chiama questa procedura quando la finestra di acquisizione viene restituita durante l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="71d63-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="71d63-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="71d63-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="71d63-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="71d63-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d63-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="71d63-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="71d63-112">Puntatore alla funzione di callback Yield, di tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="71d63-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="71d63-113">Specificare **null** per questo parametro per disabilitare una funzione di callback yield precedentemente installata.</span><span class="sxs-lookup"><span data-stu-id="71d63-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d63-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71d63-114">Return Value</span></span>

<span data-ttu-id="71d63-115">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="71d63-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="71d63-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="71d63-116">Remarks</span></span>

<span data-ttu-id="71d63-117">Le applicazioni possono facoltativamente impostare una funzione di callback yield.</span><span class="sxs-lookup"><span data-stu-id="71d63-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="71d63-118">La funzione yield callback viene chiamata almeno una volta per ogni fotogramma video acquisito durante l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="71d63-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="71d63-119">Se una funzione di callback yield è installata, verrà chiamata indipendentemente dallo stato del membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="71d63-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="71d63-120">Se viene utilizzata la funzione yield callback, è necessario installarla prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione.</span><span class="sxs-lookup"><span data-stu-id="71d63-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="71d63-121">Può essere disabilitato al termine dell'acquisizione di streaming.</span><span class="sxs-lookup"><span data-stu-id="71d63-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="71d63-122">Le applicazioni in genere eseguono un tipo di elaborazione dei messaggi nella funzione di callback costituito da un ciclo [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , come nel ciclo di messaggi di una funzione [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="71d63-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="71d63-123">La funzione yield callback deve inoltre filtrare e rimuovere messaggi che possono causare problemi di rientranza.</span><span class="sxs-lookup"><span data-stu-id="71d63-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="71d63-124">Un'applicazione in genere restituisce **true** nella procedura yield per continuare l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="71d63-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="71d63-125">Se una funzione di callback Yield restituisce **false**, la finestra di acquisizione interrompe il processo di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="71d63-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="71d63-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71d63-126">Requirements</span></span>



| <span data-ttu-id="71d63-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d63-127">Requirement</span></span> | <span data-ttu-id="71d63-128">Valore</span><span class="sxs-lookup"><span data-stu-id="71d63-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="71d63-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d63-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71d63-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71d63-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="71d63-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d63-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71d63-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71d63-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71d63-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71d63-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d63-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d63-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d63-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d63-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d63-136">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="71d63-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="71d63-137">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="71d63-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

