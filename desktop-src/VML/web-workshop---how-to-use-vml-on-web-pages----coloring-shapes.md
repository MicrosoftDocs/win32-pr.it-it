---
title: Colorazione delle forme
description: Questo articolo descrive la colorazione delle forme in VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Web workshop, colorazione di forme
- progettazione di pagine Web, colorazione di forme
- Vector Markup Language (VML), colorazione delle forme
- VML (Vector Markup Language), colorazione delle forme
- grafica vettoriale, colorazione di forme
- forme VML, colorazione
- colorare le forme
- Vector Markup Language (VML), nomi dei colori delle parole chiave
- VML (Vector Markup Language),nomi dei colori delle parole chiave
- grafica vettoriale, nomi dei colori delle parole chiave
- nomi dei colori delle parole chiave
- Vector Markup Language (VML), triplette RGB
- VML (Vector Markup Language),triplette RGB
- grafica vettoriale, triplette RGB
- Triplette RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c203debd01d4234ae58900a023944511f9fc73c1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407744"
---
# <a name="coloring-shapes"></a><span data-ttu-id="c66b8-118">Colorazione delle forme</span><span class="sxs-lookup"><span data-stu-id="c66b8-118">Coloring Shapes</span></span>

<span data-ttu-id="c66b8-119">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows.</span><span class="sxs-lookup"><span data-stu-id="c66b8-119">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c66b8-120">È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="c66b8-120">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c66b8-121">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="c66b8-121">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c66b8-122">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="c66b8-122">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c66b8-123">Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c66b8-123">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c66b8-124">Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c66b8-124">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c66b8-125">Come accennato nelle sezioni precedenti, è possibile usare "red" per rappresentare un colore in rosso, "blu" per rappresentare un colore in blu e così via.</span><span class="sxs-lookup"><span data-stu-id="c66b8-125">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="c66b8-126">In questo argomento verrà illustrato come disegnare forme in qualsiasi colore desiderato.</span><span class="sxs-lookup"><span data-stu-id="c66b8-126">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="c66b8-127">VML estende la sintassi dei colori HTML e CSS.</span><span class="sxs-lookup"><span data-stu-id="c66b8-127">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="c66b8-128">Quando il tipo di attributo di un elemento VML è color, ad esempio **fillcolor** e **strokecolor,** è possibile esprimere il colore usando un nome di colore della parola chiave o una [tripletta RGB.](#rgb-triplet) [](#keyword-color-name)</span><span class="sxs-lookup"><span data-stu-id="c66b8-128">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="c66b8-129">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="c66b8-129">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="c66b8-130">Nome colore parola chiave</span><span class="sxs-lookup"><span data-stu-id="c66b8-130">Keyword Color Name</span></span>

<span data-ttu-id="c66b8-131">HTML 4.0 definisce un elenco di nomi di colori delle parole chiave.</span><span class="sxs-lookup"><span data-stu-id="c66b8-131">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="c66b8-132">Si tratta di acqua, nero, blu, fucsia, grigio, verde, calce, maioon, blu, blu, viola, rosso, argento, verde acqua, bianco e giallo.</span><span class="sxs-lookup"><span data-stu-id="c66b8-132">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="c66b8-133">Il valore RGB per questi 16 colori è definito nella specifica [HTML 4.0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="c66b8-133">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="c66b8-134">Ad esempio, è possibile disegnare un rettangolo pieno di giallo specificando e assegnandogli un contorno blu specificando , come illustrato nella rappresentazione `fillcolor="yellow"` `strokecolor="blue"` VML seguente:</span><span class="sxs-lookup"><span data-stu-id="c66b8-134">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 byte)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="c66b8-136">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="c66b8-136">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="c66b8-137">Tripletta RGB</span><span class="sxs-lookup"><span data-stu-id="c66b8-137">RGB Triplet</span></span>

<span data-ttu-id="c66b8-138">Se il colore non è un [nome](#keyword-color-name)di colore della parola chiave, è possibile esprimere il colore come tripletta decimale RGB o tripletta esadecimale RGB.</span><span class="sxs-lookup"><span data-stu-id="c66b8-138">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="c66b8-139">Con le triplette RGB, è possibile specificare i valori per i componenti rosso, verde e blu del colore, impostando ogni componente su un valore compreso tra 0 e 255 in decimale o da 00 a FF in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="c66b8-139">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="c66b8-140">Ad esempio, è possibile creare un rettangolo riempito con un colore personalizzato con un valore RGB pari a 253, 249, 186 in formato decimale specificando o , come illustrato nella rappresentazione `fillcolor="rgb(253,249, 186)"` `fillcolor="#FDF9BA"` VML seguente.</span><span class="sxs-lookup"><span data-stu-id="c66b8-140">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="c66b8-141">In formato esadecimale, il valore 253 diventa FD, 249 diventa F9 e 186 diventa BA.</span><span class="sxs-lookup"><span data-stu-id="c66b8-141">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 byte)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="c66b8-143">Se il RGB in formato esadecimale ha un modello come XXYYZZ, è possibile abbreviarlo in XYZ.</span><span class="sxs-lookup"><span data-stu-id="c66b8-143">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="c66b8-144">Ad esempio, \# "66FF99" può essere scritto come \# "6F9".</span><span class="sxs-lookup"><span data-stu-id="c66b8-144">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="c66b8-145">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="c66b8-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="c66b8-146">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="c66b8-146">Summary</span></span>

<span data-ttu-id="c66b8-147">In VML è possibile rappresentare un colore in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="c66b8-147">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="c66b8-148">fillcolor="blue"</span><span class="sxs-lookup"><span data-stu-id="c66b8-148">fillcolor="blue"</span></span>
2.  <span data-ttu-id="c66b8-149">fillcolor="rgb(0,0,255)"</span><span class="sxs-lookup"><span data-stu-id="c66b8-149">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="c66b8-150">fillcolor=" \# 0000ff"</span><span class="sxs-lookup"><span data-stu-id="c66b8-150">fillcolor="\#0000ff"</span></span>

 

 