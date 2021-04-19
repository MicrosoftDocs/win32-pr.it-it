---
title: Conversione colori e corrispondenza colori
description: Il processo di conversione dei colori da uno spazio colore a un altro viene definito conversione di colori.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Color System (WCS), conversione colori
- WCS (sistema di colori Windows), conversione colori
- Gestione colori immagine, conversione colori
- Gestione colori, conversione colori
- colori, conversione colori
- Conversione colori
- Windows Color System (WCS), corrispondenza colori
- WCS (sistema di colori Windows), corrispondenza colori
- Gestione colori immagine, corrispondenza colori
- gestione dei colori, corrispondenza dei colori
- colori, corrispondenza colori
- corrispondenza colori
- Sistema colori Windows (WCS), mapping colori
- WCS (sistema di colori Windows), mapping colori
- Gestione colori immagine, mapping colori
- Gestione colori, mapping colori
- colori, mapping colori
- mapping colori
- punto bianco
- coloranti
- correzione di gamma
- gamma
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320146"
---
# <a name="color-conversion-and-color-matching"></a><span data-ttu-id="fe06c-125">Conversione colori e corrispondenza colori</span><span class="sxs-lookup"><span data-stu-id="fe06c-125">Color Conversion and Color Matching</span></span>

<span data-ttu-id="fe06c-126">Il processo di conversione dei colori da uno [spazio colore](c.md) a un altro viene definito *conversione di colori*.</span><span class="sxs-lookup"><span data-stu-id="fe06c-126">The process of converting colors from one [color space](c.md) to another is called *color conversion*.</span></span> <span data-ttu-id="fe06c-127">Tutti i colori in uno spazio colore sono fissi rispetto al [punto bianco](w.md)dello spazio dei colori.</span><span class="sxs-lookup"><span data-stu-id="fe06c-127">All colors in a color space are fixed relative to the color space's [white point](w.md).</span></span> <span data-ttu-id="fe06c-128">Poiché il punto bianco di uno spazio di colore varia da dispositivo a dispositivo, è necessario trovare una corrispondenza tra il colore convertito e il colore più vicino a quello visuale nello spazio dei colori di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe06c-128">Since the white point of a color space varies from device to device, a converted color must then be matched to its visually closest color in the destination color space.</span></span> <span data-ttu-id="fe06c-129">Questo processo è denominato *mapping dei colori*.</span><span class="sxs-lookup"><span data-stu-id="fe06c-129">This process is called *color mapping*.</span></span>

<span data-ttu-id="fe06c-130">Se, ad esempio, si dispone di un'immagine digitale creata sullo schermo, potrebbe trovarsi in uno spazio di colore RGB dipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe06c-130">For example, if you have a digital image that you created on your display, it may be in a device-dependent RGB color space.</span></span> <span data-ttu-id="fe06c-131">Se si desidera stamparlo su una stampante, è necessario convertirlo nello spazio dei colori della stampante.</span><span class="sxs-lookup"><span data-stu-id="fe06c-131">If you want to print it on a printer, it must be converted to the printer's color space.</span></span> <span data-ttu-id="fe06c-132">Poiché la stampante usa probabilmente uno spazio colore CMYK dipendente dal dispositivo, tutti i valori RGB devono essere convertiti in CYMK.</span><span class="sxs-lookup"><span data-stu-id="fe06c-132">Since the printer probably uses a device-dependent CMYK color space, all RGB values must be converted to CYMK.</span></span> <span data-ttu-id="fe06c-133">Si tratta della [conversione di colori](c.md).</span><span class="sxs-lookup"><span data-stu-id="fe06c-133">This is [color conversion](c.md).</span></span> <span data-ttu-id="fe06c-134">Una volta specificati i valori in termini di spazio CYMK, è necessario che corrispondano al colore più vicino che la stampante può produrre.</span><span class="sxs-lookup"><span data-stu-id="fe06c-134">Once the values are specified in terms of the CYMK space, they need to be matched to the closest color that the printer can produce.</span></span> <span data-ttu-id="fe06c-135">Questa operazione è denominata mapping dei colori o [corrispondenza dei colori](c.md).</span><span class="sxs-lookup"><span data-stu-id="fe06c-135">This is called color mapping or [color matching](c.md).</span></span>

<span data-ttu-id="fe06c-136">Sia la conversione dei colori che la mappatura dei colori devono prendere in considerazione alcuni fattori specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe06c-136">Both color conversion and color mapping must take into account a number of device-specific factors.</span></span> <span data-ttu-id="fe06c-137">Ad esempio, i blocchi predefiniti delle immagini dello schermo sono pixel.</span><span class="sxs-lookup"><span data-stu-id="fe06c-137">For instance, the building blocks of screen images are pixels.</span></span> <span data-ttu-id="fe06c-138">Ogni pixel ha un numero impostato di bit per archiviare il valore di indice colore o colore.</span><span class="sxs-lookup"><span data-stu-id="fe06c-138">Each pixel has a set number of bits to store its color or color index value.</span></span> <span data-ttu-id="fe06c-139">Il numero di bit per pixel dipende dal tipo di visualizzazione e dall'adattatore di visualizzazione utilizzati e dalla modalità di impostazione dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="fe06c-139">The number of bits per pixel depends on the type of display and display adapter being used, and the mode to which that the adapter is set.</span></span> <span data-ttu-id="fe06c-140">La maggior parte di ogni tipo di stampante usa diversi [coloranti](c.md) e stampa con risoluzioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="fe06c-140">Most every printer type uses different [colorants](c.md) and prints at particular resolutions.</span></span>

<span data-ttu-id="fe06c-141">Inoltre, le caratteristiche di tono fisico di un dispositivo sono spesso diverse in dispositivi diversi.</span><span class="sxs-lookup"><span data-stu-id="fe06c-141">In addition, the physical tone characteristics of a device are often different on different devices.</span></span> <span data-ttu-id="fe06c-142">Se, ad esempio, i colori sono prodotti da monitoraggi computer, è possibile che vengano visualizzati diversi da quelli generati in caso di stampa.</span><span class="sxs-lookup"><span data-stu-id="fe06c-142">For instance, when colors are produced by computer monitors, they can appear different than they would if they were produced on a printing press.</span></span> <span data-ttu-id="fe06c-143">Un fattore di correzione, denominato *correzione gamma*, viene spesso usato per compensare tali differenze.</span><span class="sxs-lookup"><span data-stu-id="fe06c-143">A correction factor, called *gamma correction*, is frequently used to compensate for such differences.</span></span>

<span data-ttu-id="fe06c-144">Il risultato di questi fattori dipendenti dal dispositivo è che ogni dispositivo di colore dispone di un particolare set di colori che può produrre.</span><span class="sxs-lookup"><span data-stu-id="fe06c-144">The result of these device-dependent factors is that each color device has a particular set of colors that it can produce.</span></span> <span data-ttu-id="fe06c-145">Questo set di colori è noto come *gamut*.</span><span class="sxs-lookup"><span data-stu-id="fe06c-145">This color set is known as its *gamut*.</span></span> <span data-ttu-id="fe06c-146">Per eseguire la conversione dei colori e il mapping dei colori, è necessario convertire i colori di un'immagine dallo spazio di colore e dalla gamma del dispositivo di origine allo spazio dei colori del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe06c-146">To perform color conversion and color mapping, the colors in an image must be converted from the color space and gamut of the source device into the color space of the destination device.</span></span> <span data-ttu-id="fe06c-147">Viene quindi abbinata alla gamma del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fe06c-147">They are then matched into the gamut of the destination device.</span></span>

 

 




