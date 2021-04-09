---
title: Commutatori
description: Commutatori
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixer audio, controlli
- mixer audio, commutatori
- mixer, controlli
- mixer, commutatori
- Cambia controlli
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Controllo booleano
- Button (controllo)
- controllo on/off
- controllo mono
- controllo della sonorità
- controllo avanzato stereo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872398"
---
# <a name="switches"></a><span data-ttu-id="ec62c-115">Commutatori</span><span class="sxs-lookup"><span data-stu-id="ec62c-115">Switches</span></span>

<span data-ttu-id="ec62c-116">I controlli commutatore sono due opzioni di stato.</span><span class="sxs-lookup"><span data-stu-id="ec62c-116">The switch controls are two-state switches.</span></span> <span data-ttu-id="ec62c-117">Questi controlli utilizzano la [**struttura \_ booleana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) per recuperare e impostare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="ec62c-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="ec62c-118">Nella tabella seguente vengono descritti i tipi di opzioni.</span><span class="sxs-lookup"><span data-stu-id="ec62c-118">The following table describes the types of switches.</span></span>



| <span data-ttu-id="ec62c-119">Controllo</span><span class="sxs-lookup"><span data-stu-id="ec62c-119">Control</span></span>         | <span data-ttu-id="ec62c-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec62c-120">Description</span></span>                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec62c-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="ec62c-121">Boolean</span></span>         | <span data-ttu-id="ec62c-122">Opzione generica.</span><span class="sxs-lookup"><span data-stu-id="ec62c-122">The generic switch.</span></span> <span data-ttu-id="ec62c-123">Può essere impostato su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="ec62c-123">It can be set to **TRUE** or **FALSE**.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="ec62c-124">Pulsante</span><span class="sxs-lookup"><span data-stu-id="ec62c-124">Button</span></span>          | <span data-ttu-id="ec62c-125">Impostare su **true** per tutti i pulsanti che devono essere gestiti dal driver come se fossero stati premuti.</span><span class="sxs-lookup"><span data-stu-id="ec62c-125">Set to **TRUE** for all buttons that the driver should handle as though they had been pressed.</span></span> <span data-ttu-id="ec62c-126">Se il valore è **false**, non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="ec62c-126">If the value is **FALSE**, no action is taken.</span></span>                                                                                         |
| <span data-ttu-id="ec62c-127">Attivato/Disattivato</span><span class="sxs-lookup"><span data-stu-id="ec62c-127">On/Off</span></span>          | <span data-ttu-id="ec62c-128">Opzione alternativa rappresentata da un elemento grafico diverso da quello usato per l'opzione booleana.</span><span class="sxs-lookup"><span data-stu-id="ec62c-128">An alternative switch that is represented by a graphic other than the one used for the Boolean switch.</span></span> <span data-ttu-id="ec62c-129">Può essere impostata su ON o OFF.</span><span class="sxs-lookup"><span data-stu-id="ec62c-129">It can be set to ON or OFF.</span></span>                                                                                                    |
| <span data-ttu-id="ec62c-130">Disattiva audio</span><span class="sxs-lookup"><span data-stu-id="ec62c-130">Mute</span></span>            | <span data-ttu-id="ec62c-131">Disattiva una linea audio (evitando il flusso di dati della linea) o consente la riproduzione dei dati audio.</span><span class="sxs-lookup"><span data-stu-id="ec62c-131">Mutes an audio line (suppressing the data flow of the line) or allows the audio data to play.</span></span> <span data-ttu-id="ec62c-132">Questa opzione viene spesso usata per consentire il controllo delle linee che si nutrono nel mixer.</span><span class="sxs-lookup"><span data-stu-id="ec62c-132">This switch is frequently used to help control the lines feeding into the mixer.</span></span>                                                        |
| <span data-ttu-id="ec62c-133">Mono</span><span class="sxs-lookup"><span data-stu-id="ec62c-133">Mono</span></span>            | <span data-ttu-id="ec62c-134">Passa dall'output mono a quello stereo per una linea audio stereo.</span><span class="sxs-lookup"><span data-stu-id="ec62c-134">Switches between mono and stereo output for a stereo audio line.</span></span> <span data-ttu-id="ec62c-135">Impostare su OFF per riprodurre i dati stereo come canali separati.</span><span class="sxs-lookup"><span data-stu-id="ec62c-135">Set to OFF to play stereo data as separate channels.</span></span> <span data-ttu-id="ec62c-136">Impostare su ON per combinare i dati di entrambi i canali in una linea audio mono.</span><span class="sxs-lookup"><span data-stu-id="ec62c-136">Set to ON to combine data from both channels into a mono audio line.</span></span>                                            |
| <span data-ttu-id="ec62c-137">Sonorità</span><span class="sxs-lookup"><span data-stu-id="ec62c-137">Loudness</span></span>        | <span data-ttu-id="ec62c-138">Aumenta i bassi volumi bassi per una linea audio.</span><span class="sxs-lookup"><span data-stu-id="ec62c-138">Boosts low-volume bass for an audio line.</span></span> <span data-ttu-id="ec62c-139">Impostare su ON per aumentare i bassi volume basso.</span><span class="sxs-lookup"><span data-stu-id="ec62c-139">Set to ON to boost low-volume bass.</span></span> <span data-ttu-id="ec62c-140">Impostare su OFF per impostare i livelli di volume sul normale.</span><span class="sxs-lookup"><span data-stu-id="ec62c-140">Set to OFF to set volume levels to normal.</span></span> <span data-ttu-id="ec62c-141">La quantità di Boost è specifica dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ec62c-141">The amount of boost is hardware specific.</span></span> <span data-ttu-id="ec62c-142">Per ulteriori informazioni, vedere la documentazione relativa al dispositivo mixer.</span><span class="sxs-lookup"><span data-stu-id="ec62c-142">For more information, see the documentation for your mixer device.</span></span> |
| <span data-ttu-id="ec62c-143">Enhanced Stereo</span><span class="sxs-lookup"><span data-stu-id="ec62c-143">Stereo Enhanced</span></span> | <span data-ttu-id="ec62c-144">Aumenta la separazione stereo.</span><span class="sxs-lookup"><span data-stu-id="ec62c-144">Increases stereo separation.</span></span> <span data-ttu-id="ec62c-145">Impostare su ON per aumentare la separazione stereo.</span><span class="sxs-lookup"><span data-stu-id="ec62c-145">Set to ON to increase stereo separation.</span></span> <span data-ttu-id="ec62c-146">Impostare su OFF per nessun miglioramento.</span><span class="sxs-lookup"><span data-stu-id="ec62c-146">Set to OFF for no enhancement.</span></span>                                                                                                                                  |



 

 

 