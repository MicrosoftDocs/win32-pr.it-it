---
title: Rendering degli Intent
description: Il International Color Consortium (ICC) ha definito quattro valori diversi, detti Intent di rendering.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- Windows Color System (WCS), rendering Intent
- WCS (sistema di colori Windows), rendering Intent
- Gestione colori immagine, rendering Intent
- gestione dei colori, rendering degli Intent
- colori, rendering degli Intent
- rendering degli Intent
- International Color Consortium (ICC)
- IIC (International Color Consortium)
- Finalità immagine
- Finalità grafiche
- Finalità di prova
- Finalità della corrispondenza
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321012"
---
# <a name="rendering-intents"></a><span data-ttu-id="a6be1-115">Rendering degli Intent</span><span class="sxs-lookup"><span data-stu-id="a6be1-115">Rendering Intents</span></span>

<span data-ttu-id="a6be1-116">Il International Color Consortium (ICC) ha definito quattro valori diversi, detti *Intent di rendering*.</span><span class="sxs-lookup"><span data-stu-id="a6be1-116">The International Color Consortium (ICC) has defined four different values called *rendering intents*.</span></span> <span data-ttu-id="a6be1-117">Rappresentano quattro diversi approcci alla creazione di un rendering dei colori.</span><span class="sxs-lookup"><span data-stu-id="a6be1-117">These represent four different approaches to creating a color rendering.</span></span> <span data-ttu-id="a6be1-118">Questi quattro Intent e le costanti usate per fare riferimento a essi nel codice sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6be1-118">These four intents, and the constants used to refer to them in code are as follows.</span></span>



| <span data-ttu-id="a6be1-119">Finalità</span><span class="sxs-lookup"><span data-stu-id="a6be1-119">Intent</span></span>                            | <span data-ttu-id="a6be1-120">Nome ICC</span><span class="sxs-lookup"><span data-stu-id="a6be1-120">ICC Name</span></span>              | <span data-ttu-id="a6be1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6be1-121">Description</span></span>                    |
|-----------------------------------|-----------------------|--------------------------------|
| <span data-ttu-id="a6be1-122">Immagine</span><span class="sxs-lookup"><span data-stu-id="a6be1-122">Picture</span></span> | <span data-ttu-id="a6be1-123">Percettivo</span><span class="sxs-lookup"><span data-stu-id="a6be1-123">Perceptual</span></span>            | <span data-ttu-id="a6be1-124">\_percettivo preventivo</span><span class="sxs-lookup"><span data-stu-id="a6be1-124">INTENT\_PERCEPTUAL</span></span>             |
| <span data-ttu-id="a6be1-125">Graphic</span><span class="sxs-lookup"><span data-stu-id="a6be1-125">Graphic</span></span> | <span data-ttu-id="a6be1-126">Saturazione</span><span class="sxs-lookup"><span data-stu-id="a6be1-126">Saturation</span></span>            | <span data-ttu-id="a6be1-127">\_saturazione preventivo</span><span class="sxs-lookup"><span data-stu-id="a6be1-127">INTENT\_SATURATION</span></span>             |
| <span data-ttu-id="a6be1-128">Proof</span><span class="sxs-lookup"><span data-stu-id="a6be1-128">Proof</span></span>     | <span data-ttu-id="a6be1-129">Colorimetrico relativo</span><span class="sxs-lookup"><span data-stu-id="a6be1-129">Relative Colorimetric</span></span> | <span data-ttu-id="a6be1-130">\_colorimetrico relativo per finalità \_</span><span class="sxs-lookup"><span data-stu-id="a6be1-130">INTENT\_RELATIVE\_COLORIMETRIC</span></span> |
| <span data-ttu-id="a6be1-131">Corrispondenza</span><span class="sxs-lookup"><span data-stu-id="a6be1-131">Match</span></span>     | <span data-ttu-id="a6be1-132">Colorimetrico assoluto</span><span class="sxs-lookup"><span data-stu-id="a6be1-132">Absolute Colorimetric</span></span> | <span data-ttu-id="a6be1-133">\_colorimetrico assoluto \_ preventivo</span><span class="sxs-lookup"><span data-stu-id="a6be1-133">INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> |




 

<span data-ttu-id="a6be1-134">La specifica del formato del profilo ICC versione 3,4, che descrive questi Intent, può essere scaricata da color.org.</span><span class="sxs-lookup"><span data-stu-id="a6be1-134">The ICC Profile Format Specification Version 3.4, which describes these intents, can be downloaded from color.org.</span></span>

## <a name="picture-intent"></a><span data-ttu-id="a6be1-135">Finalità immagine</span><span class="sxs-lookup"><span data-stu-id="a6be1-135">Picture Intent</span></span>

<span data-ttu-id="a6be1-136">Chiamata finalità percettiva nella clausola di specifica ICC 4,9, un intento dell'immagine causa la compressione o l'espansione della [gamma](./g.md) completa dell'immagine per riempire la gamma del dispositivo di destinazione, in modo che il bilanciamento del grigio venga mantenuto, ma l'accuratezza colorimetrico potrebbe non essere mantenuta.</span><span class="sxs-lookup"><span data-stu-id="a6be1-136">Called perceptual intent in the ICC specification clause 4.9, a Picture intent causes the full [gamut](./g.md) of the image to be compressed or expanded to fill the gamut of the destination device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span>

<span data-ttu-id="a6be1-137">In altre parole, se determinati colori in un'immagine non rientrano nell'intervallo di colori di cui il dispositivo di output può eseguire il rendering, lo scopo dell'immagine comporterà la regolazione di tutti i colori dell'immagine, in modo che ogni colore nell'immagine rientri nell'intervallo di cui è possibile eseguire il rendering e che la relazione tra i colori venga mantenuta il più possibile.</span><span class="sxs-lookup"><span data-stu-id="a6be1-137">In other words, if certain colors in an image fall outside of the range of colors that the output device can render, the picture intent will cause all the colors in the image to be adjusted so that the every color in the image falls within the range that can be rendered and so that the relationship between colors is preserved as much as possible.</span></span>

<span data-ttu-id="a6be1-138">Questo scopo è particolarmente adatto per la visualizzazione di fotografie e immagini ed è in genere lo scopo predefinito.</span><span class="sxs-lookup"><span data-stu-id="a6be1-138">This intent is most suitable for display of photographs and images, and is generally the default intent.</span></span>

## <a name="graphic-intent"></a><span data-ttu-id="a6be1-139">Finalità grafiche</span><span class="sxs-lookup"><span data-stu-id="a6be1-139">Graphic Intent</span></span>

<span data-ttu-id="a6be1-140">La clausola ICC Specification 4,12 chiama lo scopo grafico a scopo di [saturazione](s.md) .</span><span class="sxs-lookup"><span data-stu-id="a6be1-140">The ICC specification clause 4.12 calls the Graphic intent a [saturation](s.md) intent.</span></span> <span data-ttu-id="a6be1-141">Conserva il Chroma dei colori nell'immagine al possibile costo di [tonalità](h.md) e [luminosità](l.md).</span><span class="sxs-lookup"><span data-stu-id="a6be1-141">It preserves the chroma of colors in the image at the possible expense of [hue](h.md) and [lightness](l.md).</span></span>

<span data-ttu-id="a6be1-142">L'implementazione di questa finalità rimane alquanto problematica e il TPI continua a funzionare sui metodi per ottenere gli effetti desiderati.</span><span class="sxs-lookup"><span data-stu-id="a6be1-142">Implementation of this intent remains somewhat problematic, and the ICC is still working on methods to achieve the desired effects.</span></span>

<span data-ttu-id="a6be1-143">Questo scopo è particolarmente adatto per la grafica aziendale, ad esempio i grafici, in cui è più importante che i colori siano vividi e contrastino tra loro invece che con un colore specifico.</span><span class="sxs-lookup"><span data-stu-id="a6be1-143">This intent is most suitable for business graphics such as charts, where it is more important that the colors be vivid and contrast well with each other rather than a specific color.</span></span>

## <a name="proof-intent"></a><span data-ttu-id="a6be1-144">Finalità di prova</span><span class="sxs-lookup"><span data-stu-id="a6be1-144">Proof Intent</span></span>

<span data-ttu-id="a6be1-145">Il tentativo di prova, denominato intento colorimetrico nella specifica ICC, viene definito in modo tale che tutti i colori che non rientrano nell'intervallo di cui può essere eseguito il rendering del dispositivo di output vengano adattati al colore più vicino di cui è possibile eseguire il rendering, mentre tutti gli altri colori rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="a6be1-145">The Proof intent, called the colorimetric intent in the ICC specification, is defined such that any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span>

<span data-ttu-id="a6be1-146">Lo scopo della prova non mantiene il [punto bianco](w.md).</span><span class="sxs-lookup"><span data-stu-id="a6be1-146">Proof intent does not preserve the [white point](w.md).</span></span>

<span data-ttu-id="a6be1-147">Ad esempio, il bianco bianco di un foglio è più giallo del bianco bianco di un monitor del computer.</span><span class="sxs-lookup"><span data-stu-id="a6be1-147">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="a6be1-148">Un'immagine convertita nella gamma della stampante che usa la finalità colorimetrico relativa comporterebbe la maggiore ingiallimento di tutti i colori.</span><span class="sxs-lookup"><span data-stu-id="a6be1-148">An image converted into the gamut of the printer using relative colorimetric intent would result in all colors becoming more yellow.</span></span> <span data-ttu-id="a6be1-149">Il punto bianco dell'immagine viene spostato in modo che corrisponda al punto bianco della stampante.</span><span class="sxs-lookup"><span data-stu-id="a6be1-149">The white point of the image is moved to match the white point of the printer.</span></span> <span data-ttu-id="a6be1-150">Tutti gli altri colori nell'immagine mantengono la relativa posizione rispetto al punto bianco.</span><span class="sxs-lookup"><span data-stu-id="a6be1-150">All other colors in the image keep their position relative to the white point.</span></span> <span data-ttu-id="a6be1-151">In questo modo viene generata un'immagine che riflette più accuratamente l'aspetto dell'immagine stampata.</span><span class="sxs-lookup"><span data-stu-id="a6be1-151">This produces an image that more accurately reflects what the printed image will look like.</span></span> <span data-ttu-id="a6be1-152">Tuttavia, l'utente può riscontrare una discordanza visiva.</span><span class="sxs-lookup"><span data-stu-id="a6be1-152">However, the user may find it visually disconcerting.</span></span>

## <a name="match-intent"></a><span data-ttu-id="a6be1-153">Finalità della corrispondenza</span><span class="sxs-lookup"><span data-stu-id="a6be1-153">Match Intent</span></span>

<span data-ttu-id="a6be1-154">In uno scopo di corrispondenza, tutti i colori che non rientrano nell'intervallo di cui è possibile eseguire il rendering del dispositivo di output vengono adattati al colore più vicino di cui è possibile eseguire il rendering, mentre tutti gli altri colori rimangono invariati.</span><span class="sxs-lookup"><span data-stu-id="a6be1-154">In a Match intent, any colors that fall outside the range that the output device can render are adjusted to the closest color that can be rendered, while all other colors are left unchanged.</span></span> <span data-ttu-id="a6be1-155">La specifica ICC chiama lo scopo di corrispondenza colorimetrico assoluto.</span><span class="sxs-lookup"><span data-stu-id="a6be1-155">The ICC specification calls the match intent absolute colorimetric intent.</span></span>

<span data-ttu-id="a6be1-156">Lo scopo della corrispondenza conserva il punto bianco.</span><span class="sxs-lookup"><span data-stu-id="a6be1-156">Match intent preserves the white point.</span></span>

<span data-ttu-id="a6be1-157">Ad esempio, il bianco bianco di un foglio è più giallo del bianco bianco di un monitor del computer.</span><span class="sxs-lookup"><span data-stu-id="a6be1-157">For example, the whitest white of a paper is more yellow than the whitest white of a computer monitor.</span></span> <span data-ttu-id="a6be1-158">Un'immagine convertita nella [gamma](./g.md) della stampante con finalità di corrispondenza comporterebbe la conversione di tutti i colori e la corrispondenza nella gamma della stampante.</span><span class="sxs-lookup"><span data-stu-id="a6be1-158">An image converted into the [gamut](./g.md) of the printer using match intent would result in all colors being converted and matched into the gamut of the printer.</span></span> <span data-ttu-id="a6be1-159">Il punto bianco dell'immagine non viene spostato in modo che corrisponda al punto bianco della stampante.</span><span class="sxs-lookup"><span data-stu-id="a6be1-159">The white point of the image is not moved to match the white point of the printer.</span></span> <span data-ttu-id="a6be1-160">Pertanto, la distanza dei colori al punto bianco può variare.</span><span class="sxs-lookup"><span data-stu-id="a6be1-160">Therefore, the distance of the colors to the white point may change.</span></span> <span data-ttu-id="a6be1-161">Questa operazione produce un'immagine che risulta meno visivamente disconcertante per l'utente, ma è anche una versione meno precisa dell'output della stampante.</span><span class="sxs-lookup"><span data-stu-id="a6be1-161">This produces an image that is less visually disconcerting to the user, but is also a less accurate rendition of printer output.</span></span>

 

 