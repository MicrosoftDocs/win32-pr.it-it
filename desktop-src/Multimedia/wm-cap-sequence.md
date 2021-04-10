---
title: Messaggio di WM_CAP_SEQUENCE (VFW. h)
description: Il \_ \_ messaggio sequenza di WM Cap avvia il flusso di video e l'acquisizione audio in un file. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964363"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="df436-105">\_ \_ Messaggio sequenza Cap WM</span><span class="sxs-lookup"><span data-stu-id="df436-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="df436-106">Il **messaggio \_ \_ sequenza di WM Cap** avvia il flusso di video e l'acquisizione audio in un file.</span><span class="sxs-lookup"><span data-stu-id="df436-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="df436-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .</span><span class="sxs-lookup"><span data-stu-id="df436-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="df436-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df436-108">Return Value</span></span>

<span data-ttu-id="df436-109">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="df436-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="df436-110">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="df436-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="df436-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="df436-111">Remarks</span></span>

<span data-ttu-id="df436-112">Se si desidera modificare i parametri che controllano l'acquisizione di flussi, utilizzare il messaggio di [**\_ installazione della sequenza di \_ serie \_ \_ WM Cap**](wm-cap-set-sequence-setup.md) prima di avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="df436-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="df436-113">Per impostazione predefinita, la finestra di acquisizione non consente l'esecuzione di altre applicazioni durante l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="df436-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="df436-114">Per eseguire l'override di questa impostazione, impostare il membro **fYield** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) su **true** oppure installare una funzione di callback yield.</span><span class="sxs-lookup"><span data-stu-id="df436-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="df436-115">Durante l'acquisizione di flussi, la finestra di acquisizione può facoltativamente inviare notifiche all'applicazione di tipi specifici di condizioni.</span><span class="sxs-lookup"><span data-stu-id="df436-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="df436-116">Per installare le procedure di callback per queste notifiche, usare i messaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="df436-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="df436-117">**\_errore di \_ callback del set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df436-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="df436-118">**\_stato di \_ callback per set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df436-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="df436-119">**\_rendimento di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="df436-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="df436-120">**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="df436-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="df436-121">**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="df436-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="df436-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df436-122">Requirements</span></span>



| <span data-ttu-id="df436-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="df436-123">Requirement</span></span> | <span data-ttu-id="df436-124">Valore</span><span class="sxs-lookup"><span data-stu-id="df436-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="df436-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df436-125">Minimum supported client</span></span><br/> | <span data-ttu-id="df436-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df436-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="df436-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df436-127">Minimum supported server</span></span><br/> | <span data-ttu-id="df436-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="df436-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="df436-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df436-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="df436-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="df436-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df436-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df436-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df436-132">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="df436-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="df436-133">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="df436-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





