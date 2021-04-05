---
title: Funzioni di callback AVICap
description: Funzioni di callback AVICap
ms.assetid: d238a238-9702-4ba6-92bd-5ef1605b4983
keywords:
- Classe AVICap, funzioni di callback
- Funzioni di callback di AVICap, informazioni
- Messaggio WM_CAP_SET_CALLBACK_CAPCONTROL
- Messaggio WM_CAP_SET_CALLBACK_ERROR
- Messaggio WM_CAP_SET_CALLBACK_FRAME
- Messaggio WM_CAP_SET_CALLBACK_STATUS
- Messaggio WM_CAP_SET_CALLBACK_VIDEOSTREAM
- Messaggio WM_CAP_SET_CALLBACK_WAVESTREAM
- Messaggio WM_CAP_SET_CALLBACK_YIELD
- capSetCallbackOnCapControl (macro)
- capSetCallbackOnErrormacro
- capSetCallbackOnFrame (macro)
- capSetCallbackOnStatus (macro)
- capSetCallbackOnVideoStream (macro)
- capSetCallbackOnWaveStream (macro)
- capSetCallbackOnYield (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9edf96a6ff5b359acb6ef6d6a302b798742ffb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955803"
---
# <a name="avicap-callback-functions"></a><span data-ttu-id="da765-119">Funzioni di callback AVICap</span><span class="sxs-lookup"><span data-stu-id="da765-119">AVICap Callback Functions</span></span>

<span data-ttu-id="da765-120">L'applicazione può registrare le funzioni di callback con una finestra di acquisizione per notificare all'applicazione quando lo stato viene modificato, quando si verificano errori, quando i fotogrammi video e i buffer audio diventano disponibili e vengono restituiti durante l'acquisizione del flusso.</span><span class="sxs-lookup"><span data-stu-id="da765-120">Your application can register callback functions with a capture window to have it notify your application when the status changes, when errors occur, when video frame and audio buffers become available, and to yield during streaming capture.</span></span> <span data-ttu-id="da765-121">I messaggi seguenti impostano la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="da765-121">The following messages set the callback function.</span></span>



| <span data-ttu-id="da765-122">Message</span><span class="sxs-lookup"><span data-stu-id="da765-122">Message</span></span>                                                                        | <span data-ttu-id="da765-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da765-123">Description</span></span>                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da765-124">**\_CAPCONTROL di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="da765-124">**WM\_CAP\_SET\_CALLBACK\_CAPCONTROL**</span></span>](wm-cap-set-callback-capcontrol.md)   | <span data-ttu-id="da765-125">Specifica la funzione di callback nell'applicazione chiamata per fornire un controllo preciso sull'inizio e la fine dell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="da765-125">Specifies the callback function in the application called to give precise control over capture start and end.</span></span> <span data-ttu-id="da765-126">È anche possibile usare la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-126">You can also use the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro to send this message.</span></span>                   |
| [<span data-ttu-id="da765-127">**\_errore di \_ callback del set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da765-127">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)             | <span data-ttu-id="da765-128">Specifica la funzione di callback nell'applicazione chiamata quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="da765-128">Specifies the callback function in the application called when an error occurs.</span></span> <span data-ttu-id="da765-129">È anche possibile usare la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-129">You can also use the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro to send this message.</span></span>                                                           |
| [<span data-ttu-id="da765-130">**\_frame di \_ \_ callback \_ per set di estremità WM**</span><span class="sxs-lookup"><span data-stu-id="da765-130">**WM\_CAP\_SET\_CALLBACK\_FRAME**</span></span>](wm-cap-set-callback-frame.md)             | <span data-ttu-id="da765-131">Specifica la funzione di callback nell'applicazione chiamata quando vengono acquisiti i frame di anteprima.</span><span class="sxs-lookup"><span data-stu-id="da765-131">Specifies the callback function in the application called when preview frames are captured.</span></span> <span data-ttu-id="da765-132">È anche possibile usare la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-132">You can also use the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro to send this message.</span></span>                                               |
| [<span data-ttu-id="da765-133">**\_stato di \_ callback per set di estremità WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da765-133">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)           | <span data-ttu-id="da765-134">Specifica la funzione di callback nell'applicazione chiamata quando lo stato cambia.</span><span class="sxs-lookup"><span data-stu-id="da765-134">Specifies the callback function in the application called when the status changes.</span></span> <span data-ttu-id="da765-135">È anche possibile usare la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-135">You can also use the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro to send this message.</span></span>                                                      |
| [<span data-ttu-id="da765-136">**\_VIDEOSTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="da765-136">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md) | <span data-ttu-id="da765-137">Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer video.</span><span class="sxs-lookup"><span data-stu-id="da765-137">Specifies the callback function in the application called during streaming capture when a new video buffer becomes available.</span></span> <span data-ttu-id="da765-138">È anche possibile usare la macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-138">You can also use the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro to send this message.</span></span> |
| [<span data-ttu-id="da765-139">**\_WAVESTREAM di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="da765-139">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)   | <span data-ttu-id="da765-140">Specifica la funzione di callback nell'applicazione chiamata durante l'acquisizione del flusso quando diventa disponibile un nuovo buffer audio.</span><span class="sxs-lookup"><span data-stu-id="da765-140">Specifies the callback function in the application called during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="da765-141">È anche possibile usare la macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-141">You can also use the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro to send this message.</span></span>   |
| [<span data-ttu-id="da765-142">**\_rendimento di \_ \_ callback set di estremità \_ WM**</span><span class="sxs-lookup"><span data-stu-id="da765-142">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)             | <span data-ttu-id="da765-143">Specifica la funzione di callback nell'applicazione chiamata quando cede durante l'acquisizione di flussi.</span><span class="sxs-lookup"><span data-stu-id="da765-143">Specifies the callback function in the application called when yielding during streaming capture.</span></span> <span data-ttu-id="da765-144">È anche possibile usare la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) per inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="da765-144">You can also use the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro to send this message.</span></span>                                         |



 

<span data-ttu-id="da765-145">Negli argomenti seguenti vengono descritte le diverse funzioni di callback, le notifiche inviate alle funzioni e i relativi utilizzi.</span><span class="sxs-lookup"><span data-stu-id="da765-145">The following topics describe the different callback functions, the notifications sent to the functions, and their uses.</span></span>

 

 




