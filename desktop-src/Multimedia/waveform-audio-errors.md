---
title: Errori Waveform-Audio
description: Errori Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- Valori restituiti MCIERR, errori audio e forma d'onda
- Guida di riferimento multimediale, errori audio e forma d'onda
- informazioni di riferimento per i file multimediali, le forme di errore audio
- MCI (Media Control Interface), errori audio e Waveform
- MCI (interfaccia di controllo multimediale), errori audio e Waveform
- informazioni di riferimento per MCI, errori audio e Waveform
- Riferimento a MCI, errori audio e forma d'onda
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- waveform-errori audio
- Forma d'onda MCI-errori audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044309"
---
# <a name="waveform-audio-errors"></a><span data-ttu-id="8dd0a-116">Errori Waveform-Audio</span><span class="sxs-lookup"><span data-stu-id="8dd0a-116">Waveform-Audio Errors</span></span>

<span data-ttu-id="8dd0a-117">I seguenti valori restituiti aggiuntivi vengono definiti per i dispositivi audio e la forma d'onda MCI:</span><span class="sxs-lookup"><span data-stu-id="8dd0a-117">The following additional return values are defined for MCI waveform-audio devices:</span></span>



| <span data-ttu-id="8dd0a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8dd0a-118">Value</span></span>                             | <span data-ttu-id="8dd0a-119">Significato</span><span class="sxs-lookup"><span data-stu-id="8dd0a-119">Meaning</span></span>                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dd0a-120">\_INPUTSINUSE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-120">MCIERR\_WAVE\_INPUTSINUSE</span></span>         | <span data-ttu-id="8dd0a-121">Sono in uso tutti i dispositivi waveform che possono registrare file nel formato corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-121">All waveform devices that can record files in the current format are in use.</span></span> <span data-ttu-id="8dd0a-122">Attendere fino a quando uno di questi dispositivi non è disponibile; quindi, riprovare.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-122">Wait until one of these devices is free; then, try again.</span></span>                              |
| <span data-ttu-id="8dd0a-123">\_INPUTSUNSUITABLE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-123">MCIERR\_WAVE\_INPUTSUNSUITABLE</span></span>    | <span data-ttu-id="8dd0a-124">Nessun dispositivo waveform installato può registrare i file nel formato corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-124">No installed waveform device can record files in the current format.</span></span> <span data-ttu-id="8dd0a-125">Usare l'opzione drivers nel pannello di controllo per installare un dispositivo di registrazione della forma d'onda appropriato.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-125">Use the Drivers option from the Control Panel to install a suitable waveform recording device.</span></span> |
| <span data-ttu-id="8dd0a-126">\_INPUTUNSPECIFIED Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-126">MCIERR\_WAVE\_INPUTUNSPECIFIED</span></span>    | <span data-ttu-id="8dd0a-127">È possibile specificare qualsiasi dispositivo di registrazione della forma d'onda compatibile.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-127">You can specify any compatible waveform recording device.</span></span>                                                                                                           |
| <span data-ttu-id="8dd0a-128">\_OUTPUTSINUSE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-128">MCIERR\_WAVE\_OUTPUTSINUSE</span></span>        | <span data-ttu-id="8dd0a-129">Sono in uso tutti i dispositivi waveform che possono riprodurre file nel formato corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-129">All waveform devices that can play files in the current format are in use.</span></span> <span data-ttu-id="8dd0a-130">Attendere fino a quando uno di questi dispositivi non è disponibile; quindi, riprovare.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-130">Wait until one of these devices is free; then, try again.</span></span>                                |
| <span data-ttu-id="8dd0a-131">\_OUTPUTSUNSUITABLE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-131">MCIERR\_WAVE\_OUTPUTSUNSUITABLE</span></span>   | <span data-ttu-id="8dd0a-132">Nessun dispositivo waveform installato può riprodurre file nel formato corrente.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-132">No installed waveform device can play files in the current format.</span></span> <span data-ttu-id="8dd0a-133">Usare l'opzione drivers nel pannello di controllo per installare un dispositivo waveform adatto.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-133">Use the Drivers option from the Control Panel to install a suitable waveform device.</span></span>             |
| <span data-ttu-id="8dd0a-134">\_OUTPUTUNSPECIFIED Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-134">MCIERR\_WAVE\_OUTPUTUNSPECIFIED</span></span>   | <span data-ttu-id="8dd0a-135">È possibile specificare qualsiasi dispositivo compatibile per la riproduzione di forme d'onda.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-135">You can specify any compatible waveform playback device.</span></span>                                                                                                            |
| <span data-ttu-id="8dd0a-136">\_SETINPUTINUSE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-136">MCIERR\_WAVE\_SETINPUTINUSE</span></span>       | <span data-ttu-id="8dd0a-137">Il dispositivo waveform corrente è in uso.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-137">The current waveform device is in use.</span></span> <span data-ttu-id="8dd0a-138">Attendere fino a quando il dispositivo non è disponibile; quindi, riprovare a impostare il dispositivo per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-138">Wait until the device is free; then, try again to set the device for recording.</span></span>                                              |
| <span data-ttu-id="8dd0a-139">\_SETINPUTUNSUITABLE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-139">MCIERR\_WAVE\_SETINPUTUNSUITABLE</span></span>  | <span data-ttu-id="8dd0a-140">Il dispositivo usato per registrare una forma d'onda non è in grado di riconoscere il formato dati.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-140">The device you are using to record a waveform cannot recognize the data format.</span></span>                                                                                     |
| <span data-ttu-id="8dd0a-141">\_SETOUTPUTINUSE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-141">MCIERR\_WAVE\_SETOUTPUTINUSE</span></span>      | <span data-ttu-id="8dd0a-142">Il dispositivo waveform corrente è in uso.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-142">The current waveform device is in use.</span></span> <span data-ttu-id="8dd0a-143">Attendere fino a quando il dispositivo non è disponibile; quindi, riprovare a impostare il dispositivo per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-143">Wait until the device is free; then, try again to set the device for playback.</span></span>                                               |
| <span data-ttu-id="8dd0a-144">\_SETOUTPUTUNSUITABLE Wave \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="8dd0a-144">MCIERR\_WAVE\_SETOUTPUTUNSUITABLE</span></span> | <span data-ttu-id="8dd0a-145">Il dispositivo utilizzato per riprodurre una forma d'onda non è in grado di riconoscere il formato dati.</span><span class="sxs-lookup"><span data-stu-id="8dd0a-145">The device you are using to playback a waveform cannot recognize the data format.</span></span>                                                                                   |



 

 

 




