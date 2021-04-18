---
title: Messaggio di WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ CAPCONTROL imposta una funzione di callback nell'applicazione che fornisce un controllo di registrazione preciso. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301817"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="b413b-105">\_ \_ \_ Messaggio CAPCONTROL di richiamata di WM Cap Set \_</span><span class="sxs-lookup"><span data-stu-id="b413b-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="b413b-106">Il messaggio **WM \_ Cap \_ set \_ callback \_ CAPCONTROL** imposta una funzione di callback nell'applicazione che fornisce un controllo di registrazione preciso.</span><span class="sxs-lookup"><span data-stu-id="b413b-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="b413b-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="b413b-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="b413b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b413b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b413b-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="b413b-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="b413b-110">Puntatore alla funzione di callback, di tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="b413b-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="b413b-111">Specificare **null** per questo parametro per disabilitare una funzione di callback installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b413b-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b413b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b413b-112">Return Value</span></span>

<span data-ttu-id="b413b-113">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso un'acquisizione di streaming o una sessione di acquisizione a frame singolo.</span><span class="sxs-lookup"><span data-stu-id="b413b-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="b413b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b413b-114">Remarks</span></span>

<span data-ttu-id="b413b-115">Viene usata una singola funzione di callback per concedere all'applicazione un controllo preciso sui momenti in cui l'acquisizione di flussi inizia e viene completata.</span><span class="sxs-lookup"><span data-stu-id="b413b-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="b413b-116">La finestra di acquisizione chiama innanzitutto la procedura con *nState* impostato su CONTROLCALLBACK \_ preroll dopo che tutti i buffer sono stati allocati e tutte le altre preparazioni di acquisizione sono state completate.</span><span class="sxs-lookup"><span data-stu-id="b413b-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="b413b-117">Ciò consente all'applicazione di preregistrare le origini video, restituendo la funzione di callback nel momento esatto in cui viene avviata la registrazione.</span><span class="sxs-lookup"><span data-stu-id="b413b-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="b413b-118">Un valore restituito **true** dalla funzione di callback continua l'acquisizione e il valore restituito di **false** Annulla l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="b413b-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="b413b-119">Una volta avviata l'acquisizione, questa funzione di callback verrà chiamata spesso con *nState* impostato su CONTROLCALLBACK Capture \_ per consentire all'applicazione di terminare l'acquisizione restituendo **false**.</span><span class="sxs-lookup"><span data-stu-id="b413b-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b413b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b413b-120">Requirements</span></span>



| <span data-ttu-id="b413b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b413b-121">Requirement</span></span> | <span data-ttu-id="b413b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b413b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b413b-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b413b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b413b-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b413b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b413b-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b413b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b413b-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b413b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b413b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b413b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b413b-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b413b-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b413b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b413b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b413b-130">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="b413b-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b413b-131">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="b413b-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





