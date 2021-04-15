---
title: Elemento EQUALIZERSETTINGS
description: Elemento EQUALIZERSETTINGS
ms.assetid: 521f1c95-7904-4085-a8bc-5399d667dfb1
keywords:
- Windows Media Player Skin, elemento EQUALIZERSETTINGS
- interfacce, elemento EQUALIZERSETTINGS
- Elemento EQUALIZERSETTINGS
- riferimento per le interfacce, elemento EQUALIZERSETTINGS
- elementi, EQUALIZERSETTINGS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae20500dfba656450c3102ee80b4a06e089fe8ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515781"
---
# <a name="equalizersettings-element"></a><span data-ttu-id="3a8c7-108">Elemento EQUALIZERSETTINGS</span><span class="sxs-lookup"><span data-stu-id="3a8c7-108">EQUALIZERSETTINGS Element</span></span>

<span data-ttu-id="3a8c7-109">L'elemento **EQUALIZERSETTINGS** fornisce un modo per modificare il equalizzatore grafico e altre impostazioni audio di Windows Media Player usando gli attributi e il metodo elencati qui.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-109">The **EQUALIZERSETTINGS** element provides a way to manipulate the graphic equalizer and other audio settings of Windows Media Player using the attributes and method listed here.</span></span>

<span data-ttu-id="3a8c7-110">L'elemento **EQUALIZERSETTINGS** supporta i seguenti attributi.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-110">The **EQUALIZERSETTINGS** element supports the following attributes.</span></span>



| <span data-ttu-id="3a8c7-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="3a8c7-111">Attribute</span></span>                                                          | <span data-ttu-id="3a8c7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a8c7-112">Description</span></span>                                                                                             |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a8c7-113">bande</span><span class="sxs-lookup"><span data-stu-id="3a8c7-113">bands</span></span>](equalizersettings-bands.md)                               | <span data-ttu-id="3a8c7-114">Recupera il numero di bande di frequenza supportate.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-114">Retrieves the number of frequency bands supported.</span></span>                                                      |
| [<span data-ttu-id="3a8c7-115">bypass</span><span class="sxs-lookup"><span data-stu-id="3a8c7-115">bypass</span></span>](equalizersettings-bypass.md)                             | <span data-ttu-id="3a8c7-116">Specifica o recupera un valore che indica se il filtro dell'equalizzatore viene ignorato nel grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-116">Specifies or retrieves a value indicating whether the equalizer filter is bypassed in the filter graph.</span></span> |
| [<span data-ttu-id="3a8c7-117">crossFade</span><span class="sxs-lookup"><span data-stu-id="3a8c7-117">crossFade</span></span>](equalizersettings-crossfade.md)                       | <span data-ttu-id="3a8c7-118">Specifica o recupera un valore che indica se la dissolvenza incrociata è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-118">Specifies or retrieves a value indicating whether cross-fade is enabled.</span></span>                                |
| [<span data-ttu-id="3a8c7-119">crossFadeWindow</span><span class="sxs-lookup"><span data-stu-id="3a8c7-119">crossFadeWindow</span></span>](equalizersettings-crossfadewindow.md)           | <span data-ttu-id="3a8c7-120">Specifica o recupera la quantità di sovrapposizione tra dissolvenza incrociata in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-120">Specifies or retrieves the amount of cross-fade overlap in milliseconds.</span></span>                                |
| [<span data-ttu-id="3a8c7-121">currentPreset</span><span class="sxs-lookup"><span data-stu-id="3a8c7-121">currentPreset</span></span>](equalizersettings-currentpreset.md)               | <span data-ttu-id="3a8c7-122">Specifica o recupera l'indice del set di impostazioni corrente.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-122">Specifies or retrieves the index of the current preset.</span></span>                                                 |
| [<span data-ttu-id="3a8c7-123">currentPresetTitle</span><span class="sxs-lookup"><span data-stu-id="3a8c7-123">currentPresetTitle</span></span>](equalizersettings-currentpresettitle.md)     | <span data-ttu-id="3a8c7-124">Recupera il titolo del set di impostazioni corrente.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-124">Retrieves the title of the current preset.</span></span>                                                              |
| [<span data-ttu-id="3a8c7-125">currentSpeakerName</span><span class="sxs-lookup"><span data-stu-id="3a8c7-125">currentSpeakerName</span></span>](equalizersettings-currentspeakername.md)     | <span data-ttu-id="3a8c7-126">Recupera il nome dell'impostazione del relatore corrente.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-126">Retrieves the name of the current speaker setting.</span></span>                                                      |
| [<span data-ttu-id="3a8c7-127">enableSplineTension</span><span class="sxs-lookup"><span data-stu-id="3a8c7-127">enableSplineTension</span></span>](equalizersettings-enablesplinetension.md)   | <span data-ttu-id="3a8c7-128">Specifica o recupera un valore che indica se la tensione spline è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-128">Specifies or retrieves a value indicating whether spline tension is enabled or disabled.</span></span>                |
| [<span data-ttu-id="3a8c7-129">enhancedAudio</span><span class="sxs-lookup"><span data-stu-id="3a8c7-129">enhancedAudio</span></span>](equalizersettings-enhancedaudio.md)               | <span data-ttu-id="3a8c7-130">Specifica o recupera un valore che indica se l'audio avanzato è attivato.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-130">Specifies or retrieves a value indicating whether enhanced audio is turned on.</span></span>                          |
| [<span data-ttu-id="3a8c7-131">gainLevels</span><span class="sxs-lookup"><span data-stu-id="3a8c7-131">gainLevels</span></span>](equalizersettings-gainlevels.md)                     | <span data-ttu-id="3a8c7-132">Specifica o Recupera il livello di guadagno della banda corrispondente all'indice fornito.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-132">Specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>                  |
| [<span data-ttu-id="3a8c7-133">gainLevel1</span><span class="sxs-lookup"><span data-stu-id="3a8c7-133">gainLevel1</span></span>](equalizersettings-gainlevel1.md)                     | <span data-ttu-id="3a8c7-134">Specifica o Recupera il livello di guadagno della banda 1.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-134">Specifies or retrieves the gain level of band 1.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-135">gainLevel2</span><span class="sxs-lookup"><span data-stu-id="3a8c7-135">gainLevel2</span></span>](equalizersettings-gainlevel2.md)                     | <span data-ttu-id="3a8c7-136">Specifica o Recupera il livello di guadagno della banda 2.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-136">Specifies or retrieves the gain level of band 2.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-137">gainLevel3</span><span class="sxs-lookup"><span data-stu-id="3a8c7-137">gainLevel3</span></span>](equalizersettings-gainlevel3.md)                     | <span data-ttu-id="3a8c7-138">Specifica o Recupera il livello di guadagno della banda 3.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-138">Specifies or retrieves the gain level of band 3.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-139">gainLevel4</span><span class="sxs-lookup"><span data-stu-id="3a8c7-139">gainLevel4</span></span>](equalizersettings-gainlevel4.md)                     | <span data-ttu-id="3a8c7-140">Specifica o Recupera il livello di guadagno della banda 4.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-140">Specifies or retrieves the gain level of band 4.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-141">gainLevel5</span><span class="sxs-lookup"><span data-stu-id="3a8c7-141">gainLevel5</span></span>](equalizersettings-gainlevel5.md)                     | <span data-ttu-id="3a8c7-142">Specifica o Recupera il livello di guadagno della banda 5.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-142">Specifies or retrieves the gain level of band 5.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-143">gainLevel6</span><span class="sxs-lookup"><span data-stu-id="3a8c7-143">gainLevel6</span></span>](equalizersettings-gainlevel6.md)                     | <span data-ttu-id="3a8c7-144">Specifica o Recupera il livello di guadagno della banda 6.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-144">Specifies or retrieves the gain level of band 6.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-145">gainLevel7</span><span class="sxs-lookup"><span data-stu-id="3a8c7-145">gainLevel7</span></span>](equalizersettings-gainlevel7.md)                     | <span data-ttu-id="3a8c7-146">Specifica o Recupera il livello di guadagno della banda 7.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-146">Specifies or retrieves the gain level of band 7.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-147">gainLevel8</span><span class="sxs-lookup"><span data-stu-id="3a8c7-147">gainLevel8</span></span>](equalizersettings-gainlevel8.md)                     | <span data-ttu-id="3a8c7-148">Specifica o Recupera il livello di guadagno della banda 8.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-148">Specifies or retrieves the gain level of band 8.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-149">gainLevel9</span><span class="sxs-lookup"><span data-stu-id="3a8c7-149">gainLevel9</span></span>](equalizersettings-gainlevel9.md)                     | <span data-ttu-id="3a8c7-150">Specifica o Recupera il livello di guadagno della banda 9.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-150">Specifies or retrieves the gain level of band 9.</span></span>                                                        |
| [<span data-ttu-id="3a8c7-151">gainLevel10</span><span class="sxs-lookup"><span data-stu-id="3a8c7-151">gainLevel10</span></span>](equalizersettings-gainlevel10.md)                   | <span data-ttu-id="3a8c7-152">Specifica o Recupera il livello di guadagno della banda 10.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-152">Specifies or retrieves the gain level of band 10.</span></span>                                                       |
| [<span data-ttu-id="3a8c7-153">normalizzazione</span><span class="sxs-lookup"><span data-stu-id="3a8c7-153">normalization</span></span>](equalizersettings-normalization.md)               | <span data-ttu-id="3a8c7-154">Specifica o recupera un valore che indica se la normalizzazione è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-154">Specifies or retrieves a value indicating whether normalization is enabled.</span></span>                             |
| [<span data-ttu-id="3a8c7-155">normalizationAverage</span><span class="sxs-lookup"><span data-stu-id="3a8c7-155">normalizationAverage</span></span>](equalizersettings-normalizationaverage.md) | <span data-ttu-id="3a8c7-156">Recupera il valore di normalizzazione medio.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-156">Retrieves the average normalization value.</span></span>                                                              |
| [<span data-ttu-id="3a8c7-157">normalizationPeak</span><span class="sxs-lookup"><span data-stu-id="3a8c7-157">normalizationPeak</span></span>](equalizersettings-normalizationpeak.md)       | <span data-ttu-id="3a8c7-158">Recupera il valore di normalizzazione del picco.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-158">Retrieves the peak normalization value.</span></span>                                                                 |
| [<span data-ttu-id="3a8c7-159">presetCount</span><span class="sxs-lookup"><span data-stu-id="3a8c7-159">presetCount</span></span>](equalizersettings-presetcount.md)                   | <span data-ttu-id="3a8c7-160">Recupera il numero di set di impostazioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-160">Retrieves the number of presets available.</span></span>                                                              |
| [<span data-ttu-id="3a8c7-161">speakerSize</span><span class="sxs-lookup"><span data-stu-id="3a8c7-161">speakerSize</span></span>](equalizersettings-speakersize.md)                   | <span data-ttu-id="3a8c7-162">Specifica o recupera l'indice della dimensione del relatore corrente.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-162">Specifies or retrieves the index of the current speaker size.</span></span>                                           |
| [<span data-ttu-id="3a8c7-163">splineTension</span><span class="sxs-lookup"><span data-stu-id="3a8c7-163">splineTension</span></span>](equalizersettings-splinetension.md)               | <span data-ttu-id="3a8c7-164">Specifica o recupera la tensione della spline per il controllo dell'equalizzatore.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-164">Specifies or retrieves the spline tension for the equalizer control.</span></span>                                    |
| [<span data-ttu-id="3a8c7-165">truBassLevel</span><span class="sxs-lookup"><span data-stu-id="3a8c7-165">truBassLevel</span></span>](equalizersettings-trubasslevel.md)                 | <span data-ttu-id="3a8c7-166">Specifica o Recupera il livello di TruBass SRS.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-166">Specifies or retrieves the SRS TruBass level.</span></span>                                                           |
| [<span data-ttu-id="3a8c7-167">wowLevel</span><span class="sxs-lookup"><span data-stu-id="3a8c7-167">wowLevel</span></span>](equalizersettings-wowlevel.md)                         | <span data-ttu-id="3a8c7-168">Specifica o Recupera il livello di effetto SRS WOW.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-168">Specifies or retrieves the SRS WOW Effect level.</span></span>                                                        |



 

<span data-ttu-id="3a8c7-169">L'elemento **EQUALIZERSETTINGS** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-169">The **EQUALIZERSETTINGS** element supports the following methods.</span></span>



| <span data-ttu-id="3a8c7-170">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a8c7-170">Method</span></span>                                                 | <span data-ttu-id="3a8c7-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a8c7-171">Description</span></span>                                                          |
|--------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3a8c7-172">nextPreset</span><span class="sxs-lookup"><span data-stu-id="3a8c7-172">nextPreset</span></span>](equalizersettings-nextpreset.md)         | <span data-ttu-id="3a8c7-173">Applica il set di impostazioni di equalizzatore successivo.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-173">Applies the next equalizer preset.</span></span>                                   |
| [<span data-ttu-id="3a8c7-174">presetTitle</span><span class="sxs-lookup"><span data-stu-id="3a8c7-174">presetTitle</span></span>](equalizersettings-presettitle.md)       | <span data-ttu-id="3a8c7-175">Recupera il nome del set di impostazioni dell'equalizzatore con l'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-175">Retrieves the name of the equalizer preset with the specified index.</span></span> |
| [<span data-ttu-id="3a8c7-176">previousPreset</span><span class="sxs-lookup"><span data-stu-id="3a8c7-176">previousPreset</span></span>](equalizersettings-previouspreset.md) | <span data-ttu-id="3a8c7-177">Applica il set di impostazioni di equalizzatore precedente.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-177">Applies the previous equalizer preset.</span></span>                               |
| [<span data-ttu-id="3a8c7-178">reset</span><span class="sxs-lookup"><span data-stu-id="3a8c7-178">reset</span></span>](equalizersettings-reset.md)                   | <span data-ttu-id="3a8c7-179">Reimposta i livelli di guadagno di tutte le bande su zero decibel.</span><span class="sxs-lookup"><span data-stu-id="3a8c7-179">Resets the gain levels of all bands to zero decibels.</span></span>                |



 

<span data-ttu-id="3a8c7-180">L'elemento **EQUALIZERSETTINGS** può implementare i gestori eventi [ \_ OnChange dell'attributo](attribute-onchange.md) .</span><span class="sxs-lookup"><span data-stu-id="3a8c7-180">The **EQUALIZERSETTINGS** element can implement the [attribute\_onchange](attribute-onchange.md) event handlers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a8c7-181">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a8c7-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a8c7-182">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="3a8c7-182">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




