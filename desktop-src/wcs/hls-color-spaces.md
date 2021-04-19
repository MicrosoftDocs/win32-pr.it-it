---
title: Spazi colori HLS
description: Gli spazi dei colori HLS sono ampiamente usati anche dagli artisti. I componenti di colore sono Hue, Light e Saturation (Chroma).
ms.assetid: 8c80d200-c4d0-4233-8f53-a9637dff9ab2
keywords:
- Windows Color System (WCS), spazi colore HLS
- WCS (sistema di colori Windows), spazi colori HLS
- Gestione colori immagine, spazi colori HLS
- gestione dei colori, spazi dei colori HLS
- colori, spazi colore HLS
- spazi colore, HLS
- Spazi colori HLS
- tonalità
- saturazione
- leggerezza
- saturazione zero
- (HLS)
- HLS (saturazione luminosità tonalità)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613a62d4a998b51f9bfb22bd7431dd8645a72f3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320135"
---
# <a name="hls-color-spaces"></a><span data-ttu-id="671cb-117">Spazi colori HLS</span><span class="sxs-lookup"><span data-stu-id="671cb-117">HLS Color Spaces</span></span>

<span data-ttu-id="671cb-118">Gli [spazi dei colori](c.md) HLS sono ampiamente usati anche dagli artisti.</span><span class="sxs-lookup"><span data-stu-id="671cb-118">HLS [color spaces](c.md) are also widely used by artists.</span></span> <span data-ttu-id="671cb-119">I componenti di colore sono Hue, Light e Saturation (Chroma).</span><span class="sxs-lookup"><span data-stu-id="671cb-119">Its color components are hue, lightness, and saturation (chroma).</span></span>

<span data-ttu-id="671cb-120">Hue ha lo stesso significato del modello HSV, ad eccezione del fatto che un angolo di tinta pari a 0 corrisponde al blu in questo modello.</span><span class="sxs-lookup"><span data-stu-id="671cb-120">Hue has the same meaning as the HSV model, except that a hue angle of 0 corresponds to blue in this model.</span></span> <span data-ttu-id="671cb-121">Magenta è alle 60, il rosso è 120.</span><span class="sxs-lookup"><span data-stu-id="671cb-121">Magenta is at 60, red is at 120.</span></span> <span data-ttu-id="671cb-122">Come per il modello HSV, i colori complementari sono 180 a parte.</span><span class="sxs-lookup"><span data-stu-id="671cb-122">As with the HSV model, complementary colors are 180 apart.</span></span>

<span data-ttu-id="671cb-123">La leggerezza è la quantità di nero o bianco in un colore.</span><span class="sxs-lookup"><span data-stu-id="671cb-123">Lightness is the amount of black or white in a color.</span></span> <span data-ttu-id="671cb-124">L'aumento della luminosità aggiunge il bianco alla tonalità.</span><span class="sxs-lookup"><span data-stu-id="671cb-124">Increasing lightness adds white to the hue.</span></span> <span data-ttu-id="671cb-125">Diminuendo la luminosità, il nero viene aggiunto alla tonalità.</span><span class="sxs-lookup"><span data-stu-id="671cb-125">Decreasing lightness adds black to the hue.</span></span>

<span data-ttu-id="671cb-126">La [saturazione](s.md) nel modello HLS è una misura della "purezza" di una tonalità.</span><span class="sxs-lookup"><span data-stu-id="671cb-126">[Saturation](s.md) in the HLS model is a measure of the "purity" of a hue.</span></span> <span data-ttu-id="671cb-127">Con la riduzione della saturazione, la tonalità diventa più grigia.</span><span class="sxs-lookup"><span data-stu-id="671cb-127">As saturation is decreased, the hue becomes more gray.</span></span> <span data-ttu-id="671cb-128">Un valore di saturazione pari a zero restituisce un valore in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="671cb-128">A saturation value of zero results in a gray-scale value.</span></span>

<span data-ttu-id="671cb-129">La figura seguente è un disegno a linee dello spazio HLS, che è un hexcone doppio.</span><span class="sxs-lookup"><span data-stu-id="671cb-129">The following figure is a line drawing of HLS space, which is a double hexcone.</span></span> <span data-ttu-id="671cb-130">Qualsiasi sezione orizzontale incrociata dello spazio dei colori HLS è un esagono.</span><span class="sxs-lookup"><span data-stu-id="671cb-130">Any horizontal cross section of the HLS color space is a hexagon.</span></span> <span data-ttu-id="671cb-131">HLS è uno spazio di colore normalizzato.</span><span class="sxs-lookup"><span data-stu-id="671cb-131">HLS is a normalized color space.</span></span> <span data-ttu-id="671cb-132">Ovvero i valori di luminosità e saturazione sono compresi tra 0,0 e 1,0 inclusi.</span><span class="sxs-lookup"><span data-stu-id="671cb-132">That is, the lightness and saturation values range from 0.0 to 1.0 inclusive.</span></span> <span data-ttu-id="671cb-133">Hue varia da 0 a 360 inclusi.</span><span class="sxs-lookup"><span data-stu-id="671cb-133">Hue varies from 0 to 360 inclusive.</span></span>

![spazio colore HLS](images/hlsline.png)

<span data-ttu-id="671cb-135">Gli spazi dei colori HLS possono essere dipendenti dal dispositivo o indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="671cb-135">HLS color spaces can be device dependent or device independent.</span></span>

 

 




