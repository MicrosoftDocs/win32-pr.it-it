---
title: Messaggio di WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: Il \_ \_ \_ \_ messaggio di stato del callback di WM Cap imposta una funzione di callback dello stato nell'applicazione. AVICap chiama questa procedura ogni volta che lo stato della finestra di acquisizione cambia. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- WM_CAP_SET_CALLBACK_STATUS messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475491"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="d8327-106">Messaggio di stato del callback di WM \_ Cap \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="d8327-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="d8327-107">Il messaggio di **\_ stato del \_ \_ callback \_ di WM Cap** imposta una funzione di callback dello stato nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8327-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="d8327-108">AVICap chiama questa procedura ogni volta che lo stato della finestra di acquisizione cambia.</span><span class="sxs-lookup"><span data-stu-id="d8327-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="d8327-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="d8327-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="d8327-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8327-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8327-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="d8327-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="d8327-112">Puntatore alla funzione di callback dello stato di tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="d8327-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="d8327-113">Specificare **null** per questo parametro per disabilitare una funzione di callback dello stato installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d8327-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8327-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8327-114">Return Value</span></span>

<span data-ttu-id="d8327-115">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="d8327-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8327-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8327-116">Remarks</span></span>

<span data-ttu-id="d8327-117">Le applicazioni possono facoltativamente impostare una funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="d8327-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="d8327-118">Se impostata, AVICap chiama questa procedura nelle situazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8327-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="d8327-119">Una sessione di acquisizione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d8327-119">A capture session is completed.</span></span>
-   <span data-ttu-id="d8327-120">Un driver di acquisizione è riuscito a connettersi a una finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d8327-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="d8327-121">Viene creata una tavolozza ottimale.</span><span class="sxs-lookup"><span data-stu-id="d8327-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="d8327-122">Il numero di frame acquisiti viene segnalato.</span><span class="sxs-lookup"><span data-stu-id="d8327-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8327-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8327-123">Requirements</span></span>



| <span data-ttu-id="d8327-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8327-124">Requirement</span></span> | <span data-ttu-id="d8327-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d8327-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8327-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8327-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d8327-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8327-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8327-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8327-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d8327-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8327-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8327-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8327-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8327-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8327-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8327-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8327-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8327-133">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8327-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d8327-134">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d8327-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





