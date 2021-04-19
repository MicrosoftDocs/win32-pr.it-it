---
title: Spazi colori CMY e CMYK
description: Gli spazi dei colori CMY e CMYK vengono spesso utilizzati per la stampa a colori. Uno spazio colore CMY USA cyan, magenta e Yellow (CMY) come colori primari. Il colore rosso, verde e blu sono i colori secondari.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Color System (WCS), spazi colori CMY
- WCS (sistema di colori Windows), spazi colori CMY
- Gestione colori immagine, spazi colori CMY
- gestione dei colori, spazi colori CMY
- colori, spazi colore CMY
- spazi colore, CMY
- Spazi colori CMY
- Windows Color System (WCS), spazi colore CMYK
- WCS (Windows Color System), spazi colore CMYK
- Gestione colori immagine, spazi colore CMYK
- gestione dei colori, spazi CMYKcolor
- colori, spazi colore CMYK
- spazi colore, CMYK
- Spazi colori CMYK
- ciano
- magenta
- yellow
- cyan magenta giallo (CMY)
- CMY (ciano magenta giallo)
- cyan magenta giallo nero (CMYK)
- CMYK (cyan magenta giallo nero)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52622c929222eb9027b6272137a8b897210697b6
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320123"
---
# <a name="cmy-and-cmyk-color-spaces"></a><span data-ttu-id="1944c-126">Spazi colori CMY e CMYK</span><span class="sxs-lookup"><span data-stu-id="1944c-126">CMY and CMYK Color Spaces</span></span>

<span data-ttu-id="1944c-127">Gli [spazi dei colori](c.md) CMY e CMYK vengono spesso utilizzati per la stampa a colori.</span><span class="sxs-lookup"><span data-stu-id="1944c-127">The CMY and CMYK [color spaces](c.md) are often used in color printing.</span></span> <span data-ttu-id="1944c-128">Uno spazio colore CMY USA cyan, magenta e Yellow (CMY) come [colori primari](p.md).</span><span class="sxs-lookup"><span data-stu-id="1944c-128">A CMY color space uses cyan, magenta, and yellow (CMY) as its [primary colors](p.md).</span></span> <span data-ttu-id="1944c-129">Il colore rosso, verde e blu sono i colori secondari.</span><span class="sxs-lookup"><span data-stu-id="1944c-129">Red, green, and blue are the secondary colors.</span></span>

<span data-ttu-id="1944c-130">Le figure seguenti sono rappresentazioni dei colori dello spazio colore CMY.</span><span class="sxs-lookup"><span data-stu-id="1944c-130">The following figures are color representations of the CMY color space.</span></span> <span data-ttu-id="1944c-131">Lo spazio dei colori CMY è normalizzato.</span><span class="sxs-lookup"><span data-stu-id="1944c-131">The CMY color space is normalized.</span></span>

![cubo dello spazio dei colori CMY al numero massimo](images/cmyclrs1.png)

![cubo dello spazio colore CMY con valori minimi](images/cmyclrs2.png)

<span data-ttu-id="1944c-134">Lo spazio colore CMY è sottrattivo.</span><span class="sxs-lookup"><span data-stu-id="1944c-134">The CMY color space is subtractive.</span></span> <span data-ttu-id="1944c-135">Pertanto, il bianco è a (0,0, 0,0, 0,0) e il nero si trova a (1,0, 1,0, 1,0).</span><span class="sxs-lookup"><span data-stu-id="1944c-135">Therefore, white is at (0.0, 0.0, 0.0) and black is at (1.0, 1.0, 1.0).</span></span> <span data-ttu-id="1944c-136">Se si inizia con il bianco e si sottrae nessun colore, si ottiene il bianco.</span><span class="sxs-lookup"><span data-stu-id="1944c-136">If you start with white and subtract no colors, you get white.</span></span> <span data-ttu-id="1944c-137">Se si inizia con il bianco e si sottraono tutti i colori allo stesso modo, si ottiene il nero.</span><span class="sxs-lookup"><span data-stu-id="1944c-137">If you start with white and subtract all colors equally, you get black.</span></span>

<span data-ttu-id="1944c-138">Lo spazio dei colori CMYK è una variante del modello CMY.</span><span class="sxs-lookup"><span data-stu-id="1944c-138">The CMYK color space is a variation on the CMY model.</span></span> <span data-ttu-id="1944c-139">Aggiunge nero (cyan, magenta, giallo e nero).</span><span class="sxs-lookup"><span data-stu-id="1944c-139">It adds black (Cyan, Magenta, Yellow, and blacK).</span></span> <span data-ttu-id="1944c-140">Lo spazio dei colori CMYK chiude il gap tra teoria e pratica.</span><span class="sxs-lookup"><span data-stu-id="1944c-140">The CMYK color space closes the gap between theory and practice.</span></span> <span data-ttu-id="1944c-141">In teoria, il componente nero aggiuntivo non è necessario.</span><span class="sxs-lookup"><span data-stu-id="1944c-141">In theory, the extra black component is not needed.</span></span> <span data-ttu-id="1944c-142">Tuttavia, l'esperienza con diversi tipi di inchiostri e documenti ha dimostrato che quando i componenti uguali degli inchiostri cyan, magenta e giallo sono misti, il risultato è in genere un marrone scuro, non nero.</span><span class="sxs-lookup"><span data-stu-id="1944c-142">However, experience with various types of inks and papers has shown that when equal components of cyan, magenta, and yellow inks are mixed, the result is usually a dark brown, not black.</span></span> <span data-ttu-id="1944c-143">L'aggiunta di un inchiostro nero alla combinazione risolve questo problema.</span><span class="sxs-lookup"><span data-stu-id="1944c-143">Adding black ink to the mix solves this problem.</span></span>

<span data-ttu-id="1944c-144">Gli spazi dei colori CMY e CMYK possono essere indipendenti dal dispositivo, ma spesso vengono usati in riferimento a un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="1944c-144">The CMY and CMYK colors spaces can be device independent, but most often they are used in reference to a specific device.</span></span>

 

 




