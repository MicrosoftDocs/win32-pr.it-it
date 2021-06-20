---
title: Uso dell'elemento Stroke
description: Questo articolo descrive l'uso dell'elemento Stroke di VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: e3d9dbe5-e087-4b6f-8318-c7d4485cd502
keywords:
- Web workshop, elemento stroke
- progettazione di pagine Web, elemento stroke
- Vector Markup Language (VML), elemento stroke
- VML (Vector Markup Language),elemento stroke
- grafica vettoriale, elemento stroke
- Elemento stroke
- Elementi VML, tratto
- Forme VML, elemento stroke
- Vector Markup Language (VML), attributo della proprietà dashstyle
- VML (Vector Markup Language),attributo della proprietà dashstyle
- vector graphics,dashstyle - attributo della proprietà
- Attributo della proprietà dashstyle
- Vector Markup Language (VML), attributo della proprietà opacità
- VML (Vector Markup Language),attributo della proprietà opacità
- grafica vettoriale, attributo della proprietà opacità
- Attributo della proprietà opacity
- Vector Markup Language (VML), attributo della proprietà linestyle
- VML (Vector Markup Language),attributo della proprietà linestyle
- Vector Graphics, attributo della proprietà linestyle
- Attributo della proprietà linestyle
- Vector Markup Language (VML), attributo della proprietà joinstyle
- VML (Vector Markup Language),attributo della proprietà joinstyle
- vector graphics,joinstyle - attributo della proprietà
- Attributo della proprietà joinstyle
- Vector Markup Language (VML), attributo della proprietà filltype
- VML (Vector Markup Language),attributo della proprietà filltype
- vector graphics, attributo della proprietà filltype
- Attributo della proprietà filltype
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dff7a4b3bc654063fe8156476cc9c52453247a0b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407844"
---
# <a name="using-the-stroke-element"></a><span data-ttu-id="96882-131">Uso dell'elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="96882-131">Using the Stroke Element</span></span>

<span data-ttu-id="96882-132">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows.</span><span class="sxs-lookup"><span data-stu-id="96882-132">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96882-133">È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="96882-133">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96882-134">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="96882-134">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96882-135">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="96882-135">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96882-136">Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="96882-136">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96882-137">Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="96882-137">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96882-138">Uso di `<stroke>`</span><span class="sxs-lookup"><span data-stu-id="96882-138">Using `<stroke>`</span></span>

<span data-ttu-id="96882-139">Come si è appreso, è possibile usare gli attributi di proprietà **strokecolor** e **strokeweight** di una forma predefinita, ad esempio , , , , , , per specificare il colore e lo spessore del contorno di una `<oval>` `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma.</span><span class="sxs-lookup"><span data-stu-id="96882-139">As you've learned, you can use the **strokecolor** and **strokeweight** property attributes of a predefined shape -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color and weight of a shape's outline.</span></span> <span data-ttu-id="96882-140">In questo argomento verrà illustrato come disegnare una forma con una struttura più avanzata.</span><span class="sxs-lookup"><span data-stu-id="96882-140">In this topic, we will illustrate how to draw a shape that has a more advanced outline.</span></span>

<span data-ttu-id="96882-141">È possibile inserire il sotto-elemento all'interno di , o o qualsiasi elemento forma predefinito per descrivere come disegnare il `<stroke>` `<shape>` `<shapetype>` contorno della forma.</span><span class="sxs-lookup"><span data-stu-id="96882-141">You can place the `<stroke>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to draw the outline of the shape.</span></span> <span data-ttu-id="96882-142">È quindi possibile usare gli attributi della proprietà, ad esempio [dashstyle,](#dashstyle) [opacity,](#opacity) [linestyle,](#linestyle) [joinstyle,](#joinstyle) [filltype,](#filltype) del sotto-elemento per personalizzare `<stroke>` la struttura.</span><span class="sxs-lookup"><span data-stu-id="96882-142">You can then use the property attributes -- for example, [dashstyle](#dashstyle), [opacity](#opacity), [linestyle](#linestyle), [joinstyle](#joinstyle), [filltype](#filltype) -- of the `<stroke>` sub-element to customize the outline.</span></span>

<span data-ttu-id="96882-143">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96882-143">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="dashstyle"></a><span data-ttu-id="96882-144">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="96882-144">dashstyle</span></span>

<span data-ttu-id="96882-145">È possibile usare **l'attributo della** proprietà dashstyle del `<stroke>` sotto-elemento per disegnare un contorno con vari stili di tratteggio.</span><span class="sxs-lookup"><span data-stu-id="96882-145">You can use the **dashstyle** property attribute of the `<stroke>` sub-element to draw an outline with various dash styles.</span></span>

<span data-ttu-id="96882-146">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="96882-146">**Examples:**</span></span>

<span data-ttu-id="96882-147">Se si specifica `<v:stroke dashstyle="solid" />` all'interno `<line>` dell'elemento , è possibile creare una linea continua, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-147">If you specify `<v:stroke dashstyle="solid" />` inside the `<line>` element, you can create a solid line, as shown in the following VML representation:</span></span>

![solid.gif (96 byte)](images/solid.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="solid" />
</v:line>
```





<span data-ttu-id="96882-149">Se si modifica l'attributo della proprietà **dashstyle** in "dot", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-149">If you change the **dashstyle** property attribute to "dot", you can create a dotted line, as shown in the following VML representation:</span></span>

![dot.gif (144 byte)](images/dot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dot" />
</v:line>
```





<span data-ttu-id="96882-151">Se si modifica l'attributo della proprietà **dashstyle** in "dash", è possibile creare una linea tratteggiata, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-151">If you change the **dashstyle** property attribute to "dash", you can create a dash line, as shown in the following VML representation:</span></span>

![dash.gif (137 byte)](images/dash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dash" />
</v:line>
```





<span data-ttu-id="96882-153">Se si modifica l'attributo della proprietà **dashstyle** in "dashdot", è possibile creare una linea con uno stile tratteggiato e punteggiato, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-153">If you change the **dashstyle** property attribute to "dashdot", you can create a line with a dashed and dotted style, as shown in the following VML representation:</span></span>

![dashdot.gif (145 byte)](images/dashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="dashdot" />
</v:line>
```





<span data-ttu-id="96882-155">Se si modifica l'attributo della proprietà **dashstyle** in "longdash", è possibile creare una linea con uno stile tratteggiato lungo, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-155">If you change the **dashstyle** property attribute to "longdash", you can create a line with a long dashed style, as shown in the following VML representation:</span></span>

![longdash.gif (123 byte)](images/longdash.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdash" />
</v:line>
```





<span data-ttu-id="96882-157">Se si modifica l'attributo della proprietà **dashstyle** in "longdashdot", è possibile creare una linea con uno stile tratteggiato e punteggiato lungo, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-157">If you change the **dashstyle** property attribute to "longdashdot", you can create a line with a long dashed and dotted style, as shown in the following VML representation:</span></span>

![longdashdot.gif (135 byte)](images/longdashdot.gif)


```HTML
<v:line style='position:relative;' from="20pt,20pt" to="200pt,20pt"
strokecolor="red" strokeweight="2pt">
<v:stroke dashstyle="longdashdot" />
</v:line>
```





<span data-ttu-id="96882-159">Se si posiziona all'interno dell'elemento , è possibile creare un rettangolo con un contorno tratteggiato e punteggiato, come illustrato nella `<v:stroke dashstyle="dashdot" />` `<rect>` rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-159">If you place `<v:stroke dashstyle="dashdot" />` inside the `<rect>` element, you can create a rectangle that has a dashed and dotted outline, as shown in the following VML representation:</span></span>

![rect.gif (615 byte)](images/rect.gif)


```HTML
<v:rect style='width:100pt;height:80pt' strokecolor="red" strokeweight="2pt"/>
<v:stroke dashstyle="dashdot" />
</v:rect>
```





<span data-ttu-id="96882-161">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96882-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="opacity"></a><span data-ttu-id="96882-162">opacità</span><span class="sxs-lookup"><span data-stu-id="96882-162">opacity</span></span>

<span data-ttu-id="96882-163">È possibile usare **l'attributo della proprietà opacità** del sotto-elemento per disegnare un `<stroke>` contorno con vari stili di opacità.</span><span class="sxs-lookup"><span data-stu-id="96882-163">You can use the **opacity** property attribute of the `<stroke>` sub-element to draw an outline with various opacity styles.</span></span> <span data-ttu-id="96882-164">Il valore **dell'attributo della proprietà di opacità** può essere qualsiasi numero compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="96882-164">The value for the **opacity** property attribute can be any number between 0 to 1.</span></span> <span data-ttu-id="96882-165">Per impostazione predefinita, è 1, che indica l'opacità completa.</span><span class="sxs-lookup"><span data-stu-id="96882-165">By default, it is 1, indicating full opacity.</span></span>

<span data-ttu-id="96882-166">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="96882-166">**Examples:**</span></span>

<span data-ttu-id="96882-167">La rappresentazione VML seguente crea una riga con opacità completa:</span><span class="sxs-lookup"><span data-stu-id="96882-167">The following VML representation creates a line with full opacity:</span></span>

![line1.gif (96 byte)](images/line1.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
</v:line>
```





<span data-ttu-id="96882-169">Se si aggiunge all'interno dell'elemento , è possibile creare una riga con `<v:stroke opacity="0.5" />` opacità del 50%, come illustrato nella `<line>` rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-169">If you add `<v:stroke opacity="0.5" />` inside the `<line>` element, you can create a line with 50% opacity, as shown in the following VML representation:</span></span>

![line2.gif (108 byte)](images/line2.gif)


```HTML
<v:line style='position:relative;' from="20pt,50pt" to="200pt,50pt" strokecolor="red"
strokeweight="2pt">
<v:stroke opacity="0.5" />
</v:line>
```





<span data-ttu-id="96882-171">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96882-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="linestyle"></a><span data-ttu-id="96882-172">Linestyle</span><span class="sxs-lookup"><span data-stu-id="96882-172">linestyle</span></span>

<span data-ttu-id="96882-173">È possibile usare **l'attributo della** proprietà linestyle del `<stroke>` sotto-elemento per disegnare un contorno con vari stili di linea.</span><span class="sxs-lookup"><span data-stu-id="96882-173">You can use the **linestyle** property attribute of the `<stroke>` sub-element to draw an outline with various line styles.</span></span>

<span data-ttu-id="96882-174">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="96882-174">**Examples:**</span></span>

<span data-ttu-id="96882-175">Se si specifica all'interno dell'elemento , è possibile creare un rettangolo con un singolo `<v:stroke linestyle="single" />` `<rect>` contorno, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-175">If you specify `<v:stroke linestyle="single" />` inside the `<rect>` element, you can create a rectangle with a single outline, as shown in the following VML representation:</span></span>

![single.gif (537 byte)](images/single.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red" strokeweight="10pt">
<v:stroke linestyle="single" />
</v:rect>
```





<span data-ttu-id="96882-177">Se si modifica l'attributo della proprietà **linestyle** in "thinthin", è possibile creare un rettangolo con il contorno (1:1:1), come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-177">If you change the **linestyle** property attribute to "thinthin", you can create a rectangle with the outline (1:1:1), as shown in the following VML representation:</span></span>

![thinthin.gif (642 byte)](images/thinthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthin" />
</v:rect>
```





<span data-ttu-id="96882-179">Se si modifica l'attributo della proprietà **linestyle** in "thinthick", è possibile creare un rettangolo con il contorno (1:1:2), come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-179">If you change the **linestyle** property attribute to "thinthick", you can create a rectangle with the outline (1:1:2), as shown in the following VML representation:</span></span>

![thinthick.gif (646 byte)](images/thinthick.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thinthick" />
</v:rect>
```





<span data-ttu-id="96882-181">Se si modifica l'attributo della proprietà **linestyle** in "thickthin", è possibile creare un rettangolo con il contorno (2:1:1), come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-181">If you change the **linestyle** property attribute to "thickthin", you can create a rectangle with the outline (2:1:1), as shown in the following VML representation:</span></span>

![thickthin.gif (676 byte)](images/thickthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickthin" />
</v:rect>
```





<span data-ttu-id="96882-183">Se si modifica l'attributo della proprietà **linestyle** in "thickbetweenthin", è possibile creare un rettangolo con il contorno (1:1:2:1:1), come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-183">If you change the **linestyle** property attribute to "thickbetweenthin", you can create a rectangle with the outline (1:1:2:1:1), as shown in the following VML representation:</span></span>

![thickbthin.gif (669 byte)](images/thickbthin.gif)


```HTML
<v:rect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="10pt">
<v:stroke linestyle="thickbetweenthin" />
</v:rect>
```





<span data-ttu-id="96882-185">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96882-185">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="joinstyle"></a><span data-ttu-id="96882-186">joinstyle</span><span class="sxs-lookup"><span data-stu-id="96882-186">joinstyle</span></span>

<span data-ttu-id="96882-187">È possibile usare **l'attributo joinstyle** del `<stroke>` sotto-elemento per definire la modalità di unione delle linee.</span><span class="sxs-lookup"><span data-stu-id="96882-187">You can use the **joinstyle** attribute of the `<stroke>` sub-element to define how lines are joined together.</span></span>

<span data-ttu-id="96882-188">Ad esempio, per creare una forma con la struttura round join, come illustrato nella figura seguente, è possibile specificare all'interno dell'elemento , come illustrato nella rappresentazione `<v:stroke joinstyle="round" />` `<polyline>` VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-188">For example, to create a shape that has the round-join outline, as shown in the following illustration, you can specify `<v:stroke joinstyle="round" />` inside the `<polyline>` element, as shown in the following VML representation:</span></span>

![round.gif (660 byte)](images/round.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="round" />
</v:polyline>
```





<span data-ttu-id="96882-190">Se si modifica l'attributo della proprietà **joinstyle** in "smussatura", è possibile creare una forma con il contorno smussato, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-190">If you change the **joinstyle** property attribute to "bevel", you can create a shape that has the bevel-join outline, as shown in the following VML representation:</span></span>

![bevel.gif (650 byte)](images/bevel.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="bevel" />
</v:polyline>
```





<span data-ttu-id="96882-192">Se si modifica l'attributo della proprietà **joinstyle** in "miter", è possibile creare una forma con la struttura miter-join, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-192">If you change the **joinstyle** property attribute to "miter", you can create a shape that has the miter-join outline, as shown in the following VML representation:</span></span>

![miter.gif (702 byte)](images/miter.gif)


```HTML
<v:polyline
points="81pt,54pt,126pt,54pt,126pt,27pt,180pt,63pt,126pt,90pt,126pt,1in,81pt,1in"
strokecolor="red" strokeweight="20pt">
<v:stroke joinstyle="miter" />
</v:polyline>
```





<span data-ttu-id="96882-194">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96882-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="filltype"></a><span data-ttu-id="96882-195">filltype</span><span class="sxs-lookup"><span data-stu-id="96882-195">filltype</span></span>

<span data-ttu-id="96882-196">È possibile usare **l'attributo della** proprietà filltype del `<stroke>` sotto-elemento per disegnare un contorno con vari effetti di riempimento.</span><span class="sxs-lookup"><span data-stu-id="96882-196">You can use the **filltype** property attribute of the `<stroke>` sub-element to draw an outline with various fill effects.</span></span>

<span data-ttu-id="96882-197">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="96882-197">**Examples:**</span></span>

<span data-ttu-id="96882-198">Se si specifica all'interno dell'elemento , è possibile creare un rettangolo arrotondato con il contorno con riempimento a tinta unita, come illustrato nella `<v:stroke filltype="solid" />` `<roundrect>` rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-198">If you specify `<v:stroke filltype="solid" />` inside the `<roundrect>` element, you can create a rounded rectangle with the solid-filled outline, as shown in the following VML representation:</span></span>

![solid.gif (701 byte)](images/solidborder.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="solid" />
</v:roundrect>
```





<span data-ttu-id="96882-200">Se si modifica l'attributo della proprietà **filltype** in "pattern", si punta l'attributo della proprietà **src** alla posizione del file di immagine del modello e si imposta l'attributo della proprietà **color2** sul secondo colore del motivo, è possibile creare un rettangolo arrotondato con un contorno di motivo, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-200">If you change the **filltype** property attribute to "pattern", point the **src** property attribute to the location of the pattern image file, and set the **color2** property attribute to the second pattern color, you can create a rounded rectangle with a pattern outline, as shown in the following VML representation:</span></span>

![pattern.gif (1055 byte)](images/pattern.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="pattern" src="image.gif"
color2="green" />
</v:roundrect>
```





<span data-ttu-id="96882-202">Se si modifica l'attributo della proprietà **filltype** in "tile" e si punta l'attributo della proprietà **src** alla posizione del file di immagine, è possibile creare un rettangolo arrotondato con un contorno affiancato, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-202">If you change the **filltype** property attribute to "tile" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a tiled outline, as shown in the following VML representation:</span></span>

![tile.gif (6617 byte)](images/tile.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="tile" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="96882-204">Se si modifica l'attributo della proprietà **filltype** in "frame" e si punta l'attributo della proprietà **src** alla posizione del file di immagine, è possibile creare un rettangolo arrotondato con un contorno immagine, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96882-204">If you change the **filltype** property attribute to "frame" and point the **src** property attribute to the location of the image file, you can create a rounded rectangle with a picture outline, as shown in the following VML representation:</span></span>

![frame.gif (6203 byte)](images/frame.gif)


```HTML
<v:roundrect style='width:120pt;height:80pt' strokecolor="red"
strokeweight="15pt">
<v:stroke filltype="frame" src="image2.gif" />
</v:roundrect>
```





<span data-ttu-id="96882-206">Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span><span class="sxs-lookup"><span data-stu-id="96882-206">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858395) .</span></span>

 

 