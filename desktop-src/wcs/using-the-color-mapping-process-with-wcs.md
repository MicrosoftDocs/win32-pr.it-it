---
title: Uso del processo di mapping dei colori con WCS
description: Il mapping dei colori WCS è basato sui profili di dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Sistema colori Windows (WCS), mapping colori
- WCS (sistema di colori Windows), mapping colori
- Gestione colori immagine, mapping colori
- Gestione colori, mapping colori
- colori, mapping colori
- mapping colori
- Windows Color System (WCS), profili di dispositivo
- WCS (sistema di colori Windows), profili di dispositivo
- Gestione colori immagine, profili dispositivo
- gestione dei colori, profili di dispositivo
- colori, profili di dispositivo
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- profili di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320133"
---
# <a name="using-the-color-mapping-process-with-wcs"></a><span data-ttu-id="5b137-120">Uso del processo di mapping dei colori con WCS</span><span class="sxs-lookup"><span data-stu-id="5b137-120">Using The Color Mapping Process with WCS</span></span>

<span data-ttu-id="5b137-121">Il mapping dei colori WCS è basato sui [profili di dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="5b137-121">WCS color mapping is based on [device profiles](d.md).</span></span> <span data-ttu-id="5b137-122">Questi vengono forniti dai fornitori di dispositivi hardware a colori e installati durante l'installazione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b137-122">These are supplied by vendors of color hardware devices and installed when a device is installed.</span></span> <span data-ttu-id="5b137-123">Quando il mapping dei colori viene usato da un programma applicativo, WCS accede al profilo del dispositivo dell'immagine per ottenere le informazioni necessarie per convertire l'immagine nei PC.</span><span class="sxs-lookup"><span data-stu-id="5b137-123">When color mapping is used by an application program, WCS accesses the device profile of the image to get the information needed to convert the image to the PCS.</span></span> <span data-ttu-id="5b137-124">La conversione viene eseguita dal CMM.</span><span class="sxs-lookup"><span data-stu-id="5b137-124">The conversion is done by the CMM.</span></span>

<span data-ttu-id="5b137-125">Un profilo di dispositivo può essere incorporato nell'immagine stessa.</span><span class="sxs-lookup"><span data-stu-id="5b137-125">A device profile can be embedded into the image itself.</span></span> <span data-ttu-id="5b137-126">Il profilo del dispositivo si sposta quindi con l'immagine, anche in Internet.</span><span class="sxs-lookup"><span data-stu-id="5b137-126">So the device profile travels with the image, even across the Internet.</span></span> <span data-ttu-id="5b137-127">Un utente non ha bisogno del dispositivo di origine per ottenere un mapping accurato dei colori.</span><span class="sxs-lookup"><span data-stu-id="5b137-127">A user does not need the source device to get an accurate color mapping.</span></span> <span data-ttu-id="5b137-128">Se un'immagine non ha un profilo di dispositivo, lo spazio sRGB viene usato come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5b137-128">If an image does not have a device profile, the sRGB space is used as a default.</span></span> <span data-ttu-id="5b137-129">Per ulteriori informazioni, vedere [utilizzo di gestione colori in Internet](using-color-management-on-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="5b137-129">For more details, see [Using Color Management on the Internet](using-color-management-on-the-internet.md).</span></span>

<span data-ttu-id="5b137-130">Si noti che le applicazioni che utilizzano WCS non devono mai incorporare il profilo sRGB in un'immagine.</span><span class="sxs-lookup"><span data-stu-id="5b137-130">Note that applications which use WCS should never embed the sRGB profile into an image.</span></span> <span data-ttu-id="5b137-131">Lo spazio dei colori di sRGB fornisce uno spazio di colore standardizzato che è portabile in tutti i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="5b137-131">The sRGB color space provides a standardized color space that is portable across all devices.</span></span> <span data-ttu-id="5b137-132">È automaticamente disponibile per gli utenti di Windows 98 e versioni successive, nonché per Windows 2000 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5b137-132">It is automatically available to users of Windows 98 and later as well as Windows 2000 and later.</span></span> <span data-ttu-id="5b137-133">Pertanto, non è necessario spostarsi con l'immagine.</span><span class="sxs-lookup"><span data-stu-id="5b137-133">Therefore, it does not need to travel with the image.</span></span>

<span data-ttu-id="5b137-134">Quando i colori dell'immagine si trovano nei [PC](p.md), WCS accede al profilo di dispositivo del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5b137-134">After the image colors are in the [PCS](p.md), WCS accesses the device profile of the destination device.</span></span> <span data-ttu-id="5b137-135">Ottiene il CMM per convertire i colori dell'immagine dai PC alla gamma del dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5b137-135">It gets the CMM to convert the image colors from PCS to the gamut of the destination device.</span></span>

<span data-ttu-id="5b137-136">Il mapping dei colori più complesso può essere eseguito anche con WCS.</span><span class="sxs-lookup"><span data-stu-id="5b137-136">More complex color mapping can also be done with WCS.</span></span> <span data-ttu-id="5b137-137">Ad esempio, può essere usato per avere un'idea dell'aspetto di un'immagine creata in uno schermo video quando viene stampata su una stampante laser a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="5b137-137">For example, it can be used to get an idea of what an image created on a video display would look like when printed on a high resolution laser printer.</span></span> <span data-ttu-id="5b137-138">L'esempio è più complesso se è presente solo una stampante inkjet standard in cui visualizzarne l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="5b137-138">The example gets more complex if there is only a standard inkjet printer on which to preview it.</span></span> <span data-ttu-id="5b137-139">È possibile convertire l'immagine dalla gamma dello schermo alla gamma della stampante a getto d'inchiostro.</span><span class="sxs-lookup"><span data-stu-id="5b137-139">The image can be converted from the gamut of the display, into the gamut of the inkjet printer.</span></span> <span data-ttu-id="5b137-140">Da qui può essere convertito nella gamma della stampante laser.</span><span class="sxs-lookup"><span data-stu-id="5b137-140">From there it can converted into the gamut of the laser printer.</span></span> <span data-ttu-id="5b137-141">L'immagine risultante può essere stampata sulla stampante a getto d'inchiostro.</span><span class="sxs-lookup"><span data-stu-id="5b137-141">The resulting image can be printed on the inkjet printer.</span></span> <span data-ttu-id="5b137-142">Naturalmente, l'immagine potrebbe essere a una risoluzione superiore quando viene stampata sulla stampante laser con colori.</span><span class="sxs-lookup"><span data-stu-id="5b137-142">Of course the image would be at a higher resolution when printed on the color laser printer.</span></span> <span data-ttu-id="5b137-143">Tuttavia, i colori dell'immagine di correzione stampata sulla stampante inkjet sarebbero una corrispondenza vicina ai colori che la stampante laser avrebbe stampato.</span><span class="sxs-lookup"><span data-stu-id="5b137-143">However, the colors of the proofing image printed on the inkjet printer would be a close match to the colors that the laser printer would print.</span></span>

<span data-ttu-id="5b137-144">Il modo in cui vengono eseguite le conversioni nell'esempio consiste nel convertire i colori dell'immagine dal gamut dello schermo ai PC.</span><span class="sxs-lookup"><span data-stu-id="5b137-144">The way the conversions in the example are accomplished is to convert the image colors from the display's gamut into the PCS.</span></span> <span data-ttu-id="5b137-145">Una volta convertiti i colori delle immagini nei PC, il profilo del dispositivo della stampante inkjet viene usato per trasformarli nella gamma della stampante inkjet.</span><span class="sxs-lookup"><span data-stu-id="5b137-145">After the image colors are converted into the PCS, the device profile of the inkjet printer would be used to transform them into the gamut of the inkjet printer.</span></span> <span data-ttu-id="5b137-146">Successivamente, verrà usata la trasformazione gamut per PC per riportare i colori ai PC.</span><span class="sxs-lookup"><span data-stu-id="5b137-146">Next, the gamut to PCS transform would be used to move the colors back to the PCS.</span></span> <span data-ttu-id="5b137-147">A questo punto, il profilo di dispositivo della stampante laser viene usato per convertire i colori dai PC alla gamma della stampante laser.</span><span class="sxs-lookup"><span data-stu-id="5b137-147">From there, the laser printer's device profile is used to convert the colors from PCS into the gamut of the laser printer.</span></span>

<span data-ttu-id="5b137-148">La possibilità di trasformare facilmente i colori da una gamma di dispositivi ai PC e viceversa consente di riprovare i colori delle immagini per un dispositivo di output di un colore.</span><span class="sxs-lookup"><span data-stu-id="5b137-148">The ability to easily transform colors from a device gamut to the PCS and back again enables image colors intended for one color output device to be proofed on almost any other.</span></span>

<span data-ttu-id="5b137-149">Nell'esempio precedente, la descrizione è leggermente diversa dalla procedura effettiva per maggiore chiarezza.</span><span class="sxs-lookup"><span data-stu-id="5b137-149">In the preceding example, the description varies from the actual procedure somewhat for clarity.</span></span> <span data-ttu-id="5b137-150">In realtà, tutte le trasformazioni indicate nel paragrafo precedente verrebbero concatenate in una singola trasformazione.</span><span class="sxs-lookup"><span data-stu-id="5b137-150">In reality, all of the transformations mentioned in the preceding paragraph would be concatenated into a single transformation.</span></span>

 

 




