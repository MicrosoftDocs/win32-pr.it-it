---
title: Utilizzo dell'elemento Stroke
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web Workshop, elemento Stroke
- progettazione di pagine Web, elemento Stroke
- Vector Markup Language (la), elemento Stroke
- LA (Vector Markup Language), elemento Stroke
- grafica vettoriale, elemento Stroke
- Stroke-elemento
- Elementi la, Stroke
- Forme la, elemento Stroke
- Vector Markup Language (la), attributo proprietà DashStyle
- LA (Vector Markup Language), attributo proprietà DashStyle
- grafica vettoriale, attributo proprietà DashStyle
- attributo proprietà DashStyle
- Vector Markup Language (la), attributo della proprietà Opacity
- LA (Vector Markup Language), attributo della proprietà Opacity
- Vector graphics, attributo Property Opacity
- attributo della proprietà Opacity
- Vector Markup Language (la), attributo proprietà LineStyle
- LA (Vector Markup Language), attributo proprietà LineStyle
- grafica vettoriale, attributo proprietà LineStyle
- attributo proprietà LineStyle
- Vector Markup Language (la), attributo proprietà joinstyle
- LA (Vector Markup Language), attributo proprietà joinstyle
- grafica vettoriale, attributo proprietà joinstyle
- attributo proprietà joinstyle
- Vector Markup Language (la), attributo proprietà elemento FillType
- LA (Vector Markup Language), attributo proprietà elemento FillType
- grafica vettoriale, attributo proprietà elemento FillType
- attributo proprietà elemento FillType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b58e02945884ea63ad1be01e67cfc156951cd5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339102"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="8bd38-132">Utilizzo dell'elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="8bd38-132">Using the Stroke Element</span></span>

<span data-ttu-id="8bd38-133">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8bd38-133">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8bd38-134">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8bd38-134">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8bd38-135">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8bd38-135">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8bd38-136">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8bd38-136">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8bd38-137">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8bd38-137">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8bd38-138">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8bd38-138">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8bd38-139">Uso di `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="8bd38-139">Using `<stroke>`</span></span>

<span data-ttu-id="8bd38-140">Come si è appreso, è possibile usare gli attributi di proprietà **StrokeColor** e **StrokeWeight** di una forma predefinita, ad esempio `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --per specificare il colore e il peso del contorno di una forma.</span><span class="sxs-lookup"><span data-stu-id="8bd38-140">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="8bd38-141">In questo argomento verrà illustrato come disegnare una forma con una struttura più avanzata.</span><span class="sxs-lookup"><span data-stu-id="8bd38-141">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="8bd38-142">`<stroke>` `<shape>` Per descrivere come disegnare il contorno della forma, è possibile inserire il sottoelemento all'interno dell'elemento della forma, o `<shapetype>` o di qualsiasi elemento Shape predefinito.</span><span class="sxs-lookup"><span data-stu-id="8bd38-142">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="8bd38-143">È quindi possibile usare gli attributi delle proprietà, ad esempio [DashStyle](#dashstyle), [Opacity](#opacity), [LineStyle](#linestyle), [joinstyle](#joinstyle), [elemento FillType](#filltype) , del `<stroke>` sottoelemento per personalizzare il contorno.</span><span class="sxs-lookup"><span data-stu-id="8bd38-143">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="8bd38-144">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="8bd38-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="8bd38-145">DashStyle</span><span class="sxs-lookup"><span data-stu-id="8bd38-145">dashstyle</span></span>

<span data-ttu-id="8bd38-146">È possibile usare l'attributo della proprietà **DashStyle** del `<stroke>` sottoelemento per disegnare una struttura con diversi stili di tratteggio.</span><span class="sxs-lookup"><span data-stu-id="8bd38-146">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="8bd38-147">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="8bd38-147">**Examples:**</span></span>

<span data-ttu-id="8bd38-148">Se si specifica `<v:stroke dashstyle="solid" />` all'interno dell' `<line>` elemento, è possibile creare una linea continua, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-148">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 byte)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="8bd38-150">Se si imposta l'attributo della proprietà **DashStyle** su "dot", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-150">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 byte)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="8bd38-152">Se si imposta l'attributo della proprietà **DashStyle** su "Dash", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-152">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 byte)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="8bd38-154">Se si imposta l'attributo della proprietà **DashStyle** su "DashDot", è possibile creare una riga con uno stile tratteggiato e tratteggiato, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-154">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 byte)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="8bd38-156">Se si imposta l'attributo della proprietà **DashStyle** su "longdash", è possibile creare una riga con stile tratteggiato lungo, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-156">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 byte)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="8bd38-158">Se si imposta l'attributo della proprietà **DashStyle** su "longdashdot", è possibile creare una linea con uno stile tratteggiato lungo e tratteggiato, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-158">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 byte)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="8bd38-160">Se si posiziona `<v:stroke dashstyle="dashdot" />` all'interno dell' `<rect>` elemento, è possibile creare un rettangolo con un contorno tratteggiato e tratteggiato, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-160">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 byte)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="8bd38-162">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="8bd38-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="8bd38-163">opacità</span><span class="sxs-lookup"><span data-stu-id="8bd38-163">opacity</span></span>

<span data-ttu-id="8bd38-164">È possibile usare l'attributo della proprietà **Opacity** del `<stroke>` sottoelemento per disegnare un contorno con diversi stili di opacità.</span><span class="sxs-lookup"><span data-stu-id="8bd38-164">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="8bd38-165">Il valore dell'attributo della proprietà **Opacity** può essere qualsiasi numero compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8bd38-165">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="8bd38-166">Per impostazione predefinita, è 1, che indica l'opacità completa.</span><span class="sxs-lookup"><span data-stu-id="8bd38-166">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="8bd38-167">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="8bd38-167">**Examples:**</span></span>

<span data-ttu-id="8bd38-168">La rappresentazione la seguente crea una riga con opacità completa:</span><span class="sxs-lookup"><span data-stu-id="8bd38-168">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 byte)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="8bd38-170">Se si aggiunge `<v:stroke opacity="0.5" />` all'interno dell' `<line>` elemento, è possibile creare una riga con opacità del 50%, come illustrato nella seguente rappresentazione la:</span><span class="sxs-lookup"><span data-stu-id="8bd38-170">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 byte)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="8bd38-172">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="8bd38-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="8bd38-173">LineStyle</span><span class="sxs-lookup"><span data-stu-id="8bd38-173">linestyle</span></span>

<span data-ttu-id="8bd38-174">È possibile usare l'attributo della proprietà **LineStyle** del `<stroke>` sottoelemento per disegnare un contorno con vari stili di linea.</span><span class="sxs-lookup"><span data-stu-id="8bd38-174">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="8bd38-175">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="8bd38-175">**Examples:**</span></span>

<span data-ttu-id="8bd38-176">Se si specifica `<v:stroke linestyle="single" />` all'interno dell' `<rect>` elemento, è possibile creare un rettangolo con un unico contorno, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-176">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 byte)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="8bd38-178">Se si imposta l'attributo della proprietà **LineStyle** su "thinthin", è possibile creare un rettangolo con il contorno (1:1:1), come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-178">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 byte)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="8bd38-180">Se si imposta l'attributo della proprietà **LineStyle** su "thinthick", è possibile creare un rettangolo con il contorno (1:1:2), come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-180">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 byte)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="8bd38-182">Se si imposta l'attributo della proprietà **LineStyle** su "thickthin", è possibile creare un rettangolo con il contorno (2:1:1), come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-182">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 byte)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="8bd38-184">Se si imposta l'attributo della proprietà **LineStyle** su "thickbetweenthin", è possibile creare un rettangolo con il contorno (1:1:2:1:1), come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-184">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 byte)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="8bd38-186">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="8bd38-186">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="8bd38-187">joinstyle</span><span class="sxs-lookup"><span data-stu-id="8bd38-187">joinstyle</span></span>

<span data-ttu-id="8bd38-188">È possibile usare l'attributo **joinstyle** del `<stroke>` sottoelemento per definire la modalità di Unione delle linee.</span><span class="sxs-lookup"><span data-stu-id="8bd38-188">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="8bd38-189">Ad esempio, per creare una forma con il contorno di un round join, come illustrato nella figura seguente, è possibile specificare `<v:stroke joinstyle="round" />` all'interno dell' `<polyline>` elemento, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-189">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 byte)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="8bd38-191">Se si imposta l'attributo della proprietà **joinstyle** su "smussatura", è possibile creare una forma con il contorno di join smussato, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-191">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="8bd38-193">Se si imposta l'attributo della proprietà **joinstyle** su "Miter", è possibile creare una forma con la struttura ad angolo acuto-join, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-193">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 byte)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="8bd38-195">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="8bd38-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="8bd38-196">elemento FillType</span><span class="sxs-lookup"><span data-stu-id="8bd38-196">filltype</span></span>

<span data-ttu-id="8bd38-197">È possibile usare l'attributo della proprietà **elemento FillType** del `<stroke>` sottoelemento per disegnare un contorno con vari effetti di riempimento.</span><span class="sxs-lookup"><span data-stu-id="8bd38-197">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="8bd38-198">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="8bd38-198">**Examples:**</span></span>

<span data-ttu-id="8bd38-199">Se si specifica `<v:stroke filltype="solid" />` all'interno dell' `<roundrect>` elemento, è possibile creare un rettangolo arrotondato con il contorno con riempimento a tinta unita, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-199">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="8bd38-201">Se si imposta l'attributo della proprietà **elemento FillType** su "pattern", puntare l'attributo della proprietà **src** al percorso del file di immagine del modello e impostare l'attributo della proprietà **color2** sul secondo colore del criterio, è possibile creare un rettangolo arrotondato con un contorno di pattern, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-201">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 byte)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="8bd38-203">Se si imposta l'attributo della proprietà **elemento FillType** su "Tile" e si posiziona l'attributo della proprietà **src** sul percorso del file di immagine, è possibile creare un rettangolo arrotondato con un contorno affiancato, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-203">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 byte)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="8bd38-205">Se si imposta l'attributo della proprietà **elemento FillType** su "frame" e si posiziona l'attributo della proprietà **src** sul percorso del file di immagine, è possibile creare un rettangolo arrotondato con un contorno immagine, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="8bd38-205">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 byte)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="8bd38-207">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="8bd38-207">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 