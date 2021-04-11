---
title: Messaggio di WM_CAP_SEQUENCE_NOFILE (VFW. h)
description: Il \_ messaggio WM Cap \_ Sequence \_ nofile avvia l'acquisizione video di streaming senza scrivere dati in un file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119134"
---
# <a name="wm_cap_sequence_nofile-message"></a><span data-ttu-id="d86ed-105">\_ \_ \_ Messaggio nofile sequenza Cap WM</span><span class="sxs-lookup"><span data-stu-id="d86ed-105">WM\_CAP\_SEQUENCE\_NOFILE message</span></span>

<span data-ttu-id="d86ed-106">Il messaggio **WM \_ Cap \_ Sequence \_ nofile** avvia l'acquisizione video di streaming senza scrivere dati in un file.</span><span class="sxs-lookup"><span data-stu-id="d86ed-106">The **WM\_CAP\_SEQUENCE\_NOFILE** message initiates streaming video capture without writing data to a file.</span></span> <span data-ttu-id="d86ed-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) .</span><span class="sxs-lookup"><span data-stu-id="d86ed-107">You can send this message explicitly or by using the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro.</span></span>


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="d86ed-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d86ed-108">Return Value</span></span>

<span data-ttu-id="d86ed-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d86ed-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86ed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="d86ed-110">Remarks</span></span>

<span data-ttu-id="d86ed-111">Questo messaggio è utile in combinazione con le funzioni di callback flusso video o waveform-flusso audio che consentono all'applicazione di usare direttamente i dati video e audio.</span><span class="sxs-lookup"><span data-stu-id="d86ed-111">This message is useful in conjunction with video stream or waveform-audio stream callback functions that let your application use the video and audio data directly.</span></span>

<span data-ttu-id="d86ed-112">Se si desidera modificare i parametri che controllano l'acquisizione di flussi, utilizzare il messaggio di [**\_ installazione della sequenza di \_ serie \_ \_ WM Cap**](wm-cap-set-sequence-setup.md) prima di avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d86ed-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="d86ed-113">Per impostazione predefinita, la finestra di acquisizione non consente l'esecuzione di altre applicazioni durante l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d86ed-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="d86ed-114">Per eseguire l'override di questa impostazione, impostare il membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) su **true** oppure installare una funzione di callback yield.</span><span class="sxs-lookup"><span data-stu-id="d86ed-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="d86ed-115">Durante l'acquisizione di flussi, la finestra di acquisizione può facoltativamente inviare notifiche all'applicazione di tipi specifici di condizioni.</span><span class="sxs-lookup"><span data-stu-id="d86ed-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="d86ed-116">Per installare le procedure di callback per queste notifiche, usare i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d86ed-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="d86ed-117">**\_errore di \_ callback del set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d86ed-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="d86ed-118">**\_stato di \_ callback per set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d86ed-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="d86ed-119">**\_rendimento di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d86ed-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="d86ed-120">**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d86ed-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="d86ed-121">**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="d86ed-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="d86ed-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d86ed-122">Requirements</span></span>



| <span data-ttu-id="d86ed-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86ed-123">Requirement</span></span> | <span data-ttu-id="d86ed-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d86ed-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d86ed-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d86ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d86ed-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d86ed-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d86ed-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d86ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d86ed-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d86ed-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d86ed-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d86ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d86ed-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86ed-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86ed-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d86ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86ed-132">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d86ed-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d86ed-133">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="d86ed-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





