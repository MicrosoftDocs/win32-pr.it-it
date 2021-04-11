---
title: Colori delle forme
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- Workshop Web, forme colorazione
- progettazione di pagine Web, colorazione di forme
- Vector Markup Language (la), forme colorazione
- LA (Vector Markup Language), forme colorazione
- grafica vettoriale, forme colorazione
- Forme la, colorazione
- colori delle forme
- Vector Markup Language (la), nomi dei colori delle parole chiave
- LA (Vector Markup Language), nomi di colori delle parole chiave
- grafica vettoriale, nomi dei colori delle parole chiave
- nomi dei colori delle parole chiave
- Vector Markup Language (la), triple RGB
- LA (Vector Markup Language), triple RGB
- grafica vettoriale, triplette RGB
- Triplette RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1257c5f5b0cf8021658820f09de6e87099f0a52b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047047"
---
# <a name="coloring-shapes"></a><span data-ttu-id="e2ccf-119">Colori delle forme</span><span class="sxs-lookup"><span data-stu-id="e2ccf-119">Coloring Shapes</span></span>

<span data-ttu-id="e2ccf-120">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e2ccf-121">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e2ccf-122">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e2ccf-123">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e2ccf-124">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e2ccf-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e2ccf-125">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e2ccf-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e2ccf-126">Come indicato nelle sezioni precedenti, è possibile usare "Red" per rappresentare un colore in rosso, "blu" per rappresentare un colore in blu e così via.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-126">As we mentioned in earlier sections, you can use "red" to represent a color in red, "blue" to represent a color in blue, and so on.</span></span> <span data-ttu-id="e2ccf-127">In questo argomento verrà illustrato come creare forme nei colori desiderati.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-127">In this topic, we will illustrate how to draw shapes in any color you want.</span></span>

<span data-ttu-id="e2ccf-128">LA estende la sintassi di colore HTML e CSS.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-128">VML extends HTML and CSS color syntax.</span></span> <span data-ttu-id="e2ccf-129">Quando il tipo di attributo di un elemento la è color, ad esempio **FillColor** e **StrokeColor** , è possibile esprimere il colore usando un [nome di colore della parola chiave](#keyword-color-name) o una [tripletta RGB](#rgb-triplet).</span><span class="sxs-lookup"><span data-stu-id="e2ccf-129">When the attribute type of a VML element is color -- such as **fillcolor** and **strokecolor** -- you can express the color by using either a [keyword color name](#keyword-color-name) or an [RGB triplet](#rgb-triplet).</span></span>

<span data-ttu-id="e2ccf-130">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e2ccf-130">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="keyword-color-name"></a><span data-ttu-id="e2ccf-131">Nome colore parola chiave</span><span class="sxs-lookup"><span data-stu-id="e2ccf-131">Keyword Color Name</span></span>

<span data-ttu-id="e2ccf-132">HTML 4,0 definisce un elenco di nomi di colori delle parole chiave.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-132">HTML 4.0 defines a list of keyword color names.</span></span> <span data-ttu-id="e2ccf-133">Sono Aqua, black, Blue, fucsia, grigio, verde, lime, Maroon, Navy, olive, Purple, Red, Silver, alzavola, White e Yellow.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-133">They are aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow.</span></span> <span data-ttu-id="e2ccf-134">Il valore RGB per questi 16 colori è definito nella [specifica HTML 4,0](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span><span class="sxs-lookup"><span data-stu-id="e2ccf-134">The RGB value for these 16 colors are defined in [HTML 4.0 specification](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) .</span></span>

<span data-ttu-id="e2ccf-135">Ad esempio, è possibile disegnare un rettangolo riempito con il giallo specificando `fillcolor="yellow"` e assegnargli un contorno blu specificando `strokecolor="blue"` , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="e2ccf-135">For example, you can draw a rectangle filled with yellow by specifying `fillcolor="yellow"`, and give it a blue outline by specifying `strokecolor="blue"`, as shown in the following VML representation:</span></span>

![color1.gif (305 byte)](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





<span data-ttu-id="e2ccf-137">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e2ccf-137">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rgb-triplet"></a><span data-ttu-id="e2ccf-138">Tripletta RGB</span><span class="sxs-lookup"><span data-stu-id="e2ccf-138">RGB Triplet</span></span>

<span data-ttu-id="e2ccf-139">Se il colore non è un [nome di colore di parola chiave](#keyword-color-name), è possibile esprimere il colore come una tripletta decimale RGB o una tripletta esadecimale RGB.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-139">If the color is not a [keyword color name](#keyword-color-name), you can express the color as either an RGB decimal triplet or an RGB hexadecimal triplet.</span></span> <span data-ttu-id="e2ccf-140">Con le triplette RGB è possibile specificare i valori per i componenti rosso, verde e blu del colore, impostando ogni componente su un valore compreso tra 0 e 255 in decimale oppure 00 con FF in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-140">With RGB triplets, you can specify values for the red, green, and blue components of the color, setting each component to a value ranging from 0 through 255 in decimal, or 00 through FF in hexadecimal.</span></span>

<span data-ttu-id="e2ccf-141">È ad esempio possibile creare un rettangolo con un colore personalizzato con un valore RGB 253, 249, 186 in Decimal specificando `fillcolor="rgb(253,249, 186)"` o `fillcolor="#FDF9BA"` , come illustrato nella rappresentazione la seguente.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-141">For example, you can create a rectangle that is filled with a customized color with an RGB value of 253, 249, 186 in decimal by specifying either `fillcolor="rgb(253,249, 186)"` or `fillcolor="#FDF9BA"`, as shown in the following VML representation.</span></span> <span data-ttu-id="e2ccf-142">In esadecimale, il valore 253 diventa FD, 249 diventa F9 e 186 diventa BA.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-142">In hexadecimal, the value 253 becomes FD, 249 becomes F9, and 186 becomes BA.</span></span>

![color2.gif (305 byte)](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





<span data-ttu-id="e2ccf-144">Se l'oggetto RGB in formato esadecimale ha un modello, ad esempio XXYYZZ, è possibile abbreviare l'oggetto con XYZ.</span><span class="sxs-lookup"><span data-stu-id="e2ccf-144">If the RGB in hexadecimal has a pattern such as XXYYZZ, you can abbreviate it to XYZ.</span></span> <span data-ttu-id="e2ccf-145">Ad esempio, " \# 66FF99" può essere scritto come " \# 6F9".</span><span class="sxs-lookup"><span data-stu-id="e2ccf-145">For example, "\#66FF99" can be written out as "\#6F9".</span></span>

<span data-ttu-id="e2ccf-146">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e2ccf-146">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="e2ccf-147">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="e2ccf-147">Summary</span></span>

<span data-ttu-id="e2ccf-148">In la è possibile rappresentare un colore in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2ccf-148">In VML, you can represent a color in one of the following formats:</span></span>

1.  <span data-ttu-id="e2ccf-149">FillColor = "blu"</span><span class="sxs-lookup"><span data-stu-id="e2ccf-149">fillcolor="blue"</span></span>
2.  <span data-ttu-id="e2ccf-150">FillColor = "RGB (0, 0255)"</span><span class="sxs-lookup"><span data-stu-id="e2ccf-150">fillcolor="rgb(0,0,255)"</span></span>
3.  <span data-ttu-id="e2ccf-151">FillColor = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="e2ccf-151">fillcolor="\#0000ff"</span></span>

 

 