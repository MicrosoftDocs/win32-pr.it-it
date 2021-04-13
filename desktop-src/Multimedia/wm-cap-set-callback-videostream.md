---
title: Messaggio di WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ callback \_ VIDEOSTREAM imposta una funzione di callback nell'applicazione.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400256"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="bfe35-104">\_ \_ \_ Messaggio VIDEOSTREAM di richiamata di WM Cap Set \_</span><span class="sxs-lookup"><span data-stu-id="bfe35-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="bfe35-105">Il messaggio **WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM** imposta una funzione di callback nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfe35-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="bfe35-106">AVICap chiama questa procedura durante l'acquisizione del flusso quando un buffer video viene riempito.</span><span class="sxs-lookup"><span data-stu-id="bfe35-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="bfe35-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="bfe35-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="bfe35-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bfe35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfe35-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="bfe35-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="bfe35-110">Puntatore alla funzione di callback del flusso video, di tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="bfe35-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="bfe35-111">Specificare **null** per questo parametro per disabilitare una funzione di callback video-stream installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="bfe35-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfe35-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bfe35-112">Return Value</span></span>

<span data-ttu-id="bfe35-113">Restituisce **true** se l'operazione ha esito **positivo o negativo** se è in corso l'acquisizione di flussi o una sessione di acquisizione a singolo frame.</span><span class="sxs-lookup"><span data-stu-id="bfe35-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfe35-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfe35-114">Remarks</span></span>

<span data-ttu-id="bfe35-115">La finestra di acquisizione chiama la funzione di callback prima di scrivere il frame acquisito su disco.</span><span class="sxs-lookup"><span data-stu-id="bfe35-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="bfe35-116">Questo consente alle applicazioni di modificare il frame se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="bfe35-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="bfe35-117">Se per l'acquisizione di flussi viene usata una funzione di callback del flusso video, la procedura deve essere installata prima di avviare la sessione di acquisizione e deve rimanere abilitata per la durata della sessione.</span><span class="sxs-lookup"><span data-stu-id="bfe35-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="bfe35-118">Può essere disabilitato al termine dell'acquisizione di streaming.</span><span class="sxs-lookup"><span data-stu-id="bfe35-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfe35-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfe35-119">Requirements</span></span>



| <span data-ttu-id="bfe35-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfe35-120">Requirement</span></span> | <span data-ttu-id="bfe35-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bfe35-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bfe35-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfe35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bfe35-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfe35-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bfe35-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfe35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bfe35-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bfe35-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bfe35-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfe35-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfe35-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfe35-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfe35-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfe35-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfe35-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="bfe35-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bfe35-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="bfe35-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





