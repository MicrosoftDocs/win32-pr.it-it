---
title: Supporto per la filigrana
description: Supporto per la filigrana
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, supporto per la filigrana
- Windows Media Format SDK, digital watermarking
- ASF (Advanced Systems Format), supporto per la filigrana
- ASF (Advanced Systems Format), supporto per la filigrana
- Formato Advanced Systems (ASF), digital watermarking
- ASF (Advanced Systems Format), digital watermarking
- Windows Media Format SDK, DMO
- ASF (Advanced Systems Format), DMO
- ASF (Advanced Systems Format), DMO
- Windows Media Format SDK, interfaccia IWMWatermarkInfo
- Advanced Systems Format (ASF), interfaccia IWMWatermarkInfo
- ASF (formato avanzato dei sistemi), interfaccia IWMWatermarkInfo
- watermarking, informazioni
- filigrana digitale
- DMO (DirectX Media Object), informazioni
- DMO (oggetto multimediale DirectX), informazioni
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299433"
---
# <a name="watermarking-support"></a><span data-ttu-id="80b70-120">Supporto per la filigrana</span><span class="sxs-lookup"><span data-stu-id="80b70-120">Watermarking Support</span></span>

<span data-ttu-id="80b70-121">Il watermark digitale è un modo per incorporare il copyright o altre informazioni nei dati di un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="80b70-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="80b70-122">Le tecniche per la filigrana variano notevolmente da una soluzione all'altra.</span><span class="sxs-lookup"><span data-stu-id="80b70-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="80b70-123">La forma più semplice di filigrana è semplicemente l'aggiunta di un'immagine di identificazione a ogni frame di un flusso video.</span><span class="sxs-lookup"><span data-stu-id="80b70-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="80b70-124">Le stazioni televisive utilizzano spesso questa tecnica per inserire un logo semi-trasparente in un angolo inferiore della trasmissione.</span><span class="sxs-lookup"><span data-stu-id="80b70-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="80b70-125">Le forme più sofisticate di filigrana digitale sono impercettibili per l'utente che guarda o ascolta il contenuto.</span><span class="sxs-lookup"><span data-stu-id="80b70-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="80b70-126">Windows Media Format SDK supporta l'uso di digital watermarking [*DMOS*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="80b70-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="80b70-127">In pratica, un sistema di filigrana è molto simile a un codec: accetta esempi di supporti, esegue algoritmi sui dati e restituisce gli esempi modificati.</span><span class="sxs-lookup"><span data-stu-id="80b70-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="80b70-128">Quando si specifica un sistema di filigrana per un flusso, l'oggetto writer include il DMO nell'elaborazione degli esempi di input.</span><span class="sxs-lookup"><span data-stu-id="80b70-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="80b70-129">Quando si configura un flusso per la filigrana, è necessario specificare le informazioni di configurazione di filigrana.</span><span class="sxs-lookup"><span data-stu-id="80b70-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="80b70-130">I valori di configurazione saranno diversi a seconda del valore DMO per la filigrana.</span><span class="sxs-lookup"><span data-stu-id="80b70-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="80b70-131">L'oggetto DMO usato dovrebbe essere dotato di istruzioni che descrivono i valori di configurazione supportati.</span><span class="sxs-lookup"><span data-stu-id="80b70-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="80b70-132">Per informazioni sulle impostazioni usate per specificare un sistema di filigrana, vedere [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="80b70-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="80b70-133">È possibile programmare l'applicazione per enumerare il DMOs di filigrana installato nel computer client.</span><span class="sxs-lookup"><span data-stu-id="80b70-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="80b70-134">Per ulteriori informazioni, vedere l'interfaccia [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .</span><span class="sxs-lookup"><span data-stu-id="80b70-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80b70-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="80b70-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80b70-136">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="80b70-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




