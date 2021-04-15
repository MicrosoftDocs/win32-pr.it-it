---
title: Uso di forme predefinite
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, forme predefinite
- progettazione di pagine Web, forme predefinite
- Vector Markup Language (la), forme predefinite
- LA (Vector Markup Language), forme predefinite
- grafica vettoriale, forme predefinite
- Forme la, predefinite
- forme predefinite
- Vector Markup Language (la), elemento Rect
- LA (Vector Markup Language), elemento Rect
- grafica vettoriale, elemento Rect
- elemento Rect
- Elementi la, Rect
- Vector Markup Language (la), elemento RoundRect
- LA (Vector Markup Language), elemento RoundRect
- grafica vettoriale, elemento RoundRect
- elemento RoundRect
- Elementi la, RoundRect
- Vector Markup Language (la), elemento linea
- LA (Vector Markup Language), elemento linea
- grafica vettoriale, elemento linea
- elemento Line
- Elementi la, riga
- Vector Markup Language (la), elemento polilinea
- LA (Vector Markup Language), elemento polilinea
- grafica vettoriale, elemento polilinea
- elemento polilinea
- Elementi la, polilinea
- Vector Markup Language (la), elemento curva
- LA (Vector Markup Language), elemento curva
- grafica vettoriale, elemento curva
- curva-elemento
- Elementi la, curva
- Vector Markup Language (la), elemento Arc
- LA (Vector Markup Language), elemento Arc
- grafica vettoriale, elemento Arc
- elemento Arc
- Elementi la, Arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516882"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="449b7-141">Uso di forme predefinite</span><span class="sxs-lookup"><span data-stu-id="449b7-141">Using Predefined Shapes</span></span>

<span data-ttu-id="449b7-142">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="449b7-142">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="449b7-143">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="449b7-143">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="449b7-144">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="449b7-144">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="449b7-145">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="449b7-145">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="449b7-146">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="449b7-146">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="449b7-147">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="449b7-147">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="449b7-148">Come si è appreso, è possibile usare l' `<oval>` elemento di la per creare un semplice Oval.</span><span class="sxs-lookup"><span data-stu-id="449b7-148">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="449b7-149">LA fornisce molti altri elementi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="449b7-149">VML provides several other predefined elements.</span></span> <span data-ttu-id="449b7-150">In questo argomento verrà illustrato come creare grafica usando questi elementi.</span><span class="sxs-lookup"><span data-stu-id="449b7-150">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="449b7-151">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="449b7-151">In this topic:</span></span>

-   [<span data-ttu-id="449b7-152">Rect</span><span class="sxs-lookup"><span data-stu-id="449b7-152">rect</span></span>](#roundrect)
-   [<span data-ttu-id="449b7-153">RoundRect</span><span class="sxs-lookup"><span data-stu-id="449b7-153">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="449b7-154">linea</span><span class="sxs-lookup"><span data-stu-id="449b7-154">line</span></span>](#polyline)
-   [<span data-ttu-id="449b7-155">polilinea</span><span class="sxs-lookup"><span data-stu-id="449b7-155">polyline</span></span>](#polyline)
-   [<span data-ttu-id="449b7-156">curva</span><span class="sxs-lookup"><span data-stu-id="449b7-156">curve</span></span>](#curve)
-   [<span data-ttu-id="449b7-157">arco</span><span class="sxs-lookup"><span data-stu-id="449b7-157">arc</span></span>](#arc)
-   [<span data-ttu-id="449b7-158">Summary</span><span class="sxs-lookup"><span data-stu-id="449b7-158">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="449b7-159">rect</span><span class="sxs-lookup"><span data-stu-id="449b7-159">rect</span></span>

<span data-ttu-id="449b7-160">`<rect>`Per creare un rettangolo, è possibile usare l'elemento.</span><span class="sxs-lookup"><span data-stu-id="449b7-160">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="449b7-161">È quindi possibile personalizzare il rettangolo specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="449b7-161">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="449b7-162">Ad esempio, è possibile disegnare un rettangolo che viene riempito con blu specificando **FillColor**= "Blue" e assegnargli un contorno rosso a 3,5 punti specificando **StrokeColor**= "Red" **StrokeWeight**= "3.5 pt", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-162">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 byte)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="449b7-164">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="449b7-164">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="449b7-165">Nota: la specifica la non dispone di un segnalibro per l' `<rect>` elemento.</span><span class="sxs-lookup"><span data-stu-id="449b7-165">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="449b7-166">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-166">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="449b7-167">RoundRect</span><span class="sxs-lookup"><span data-stu-id="449b7-167">roundrect</span></span>

<span data-ttu-id="449b7-168">È possibile utilizzare l' `<roundrect>` elemento per creare un rettangolo con angoli arrotondati.</span><span class="sxs-lookup"><span data-stu-id="449b7-168">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="449b7-169">È quindi possibile personalizzare il rettangolo arrotondato specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="449b7-169">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="449b7-170">È possibile, ad esempio, disegnare un rettangolo con angoli arrotondati del 30% della metà della dimensione più piccola del rettangolo specificando **arcsize**= "0,3", riempirlo con il giallo specificando **FillColor**= "Yellow" e assegnargli un contorno rosso a 2 punte specificando **StrokeColor**= "Red" **StrokeWeight**= "2PT", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-170">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 byte)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="449b7-172">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="449b7-172">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="449b7-173">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-173">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="449b7-174">line</span><span class="sxs-lookup"><span data-stu-id="449b7-174">line</span></span>

<span data-ttu-id="449b7-175">È possibile usare l' `<line>` elemento per creare una linea retta.</span><span class="sxs-lookup"><span data-stu-id="449b7-175">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="449b7-176">È quindi possibile personalizzare la riga specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="449b7-176">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="449b7-177">Ad esempio, è possibile creare una linea orizzontale specificando **from**= "20pt, 20pt" **a**= "100PT, 20pt" e impostarla su 2-Point e Red specificando **StrokeColor**= "Red" **StrokeWeight**= "2PT", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-177">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="449b7-179">È possibile creare una linea verticale o diagonale semplicemente specificando valori diversi per gli attributi di proprietà **from** e **to** , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-179">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 byte)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="449b7-181">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="449b7-181">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="449b7-182">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-182">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="449b7-183">polilinea</span><span class="sxs-lookup"><span data-stu-id="449b7-183">polyline</span></span>

<span data-ttu-id="449b7-184">È possibile utilizzare l' `<polyline>` elemento per definire forme create da segmenti di linea connessi.</span><span class="sxs-lookup"><span data-stu-id="449b7-184">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="449b7-185">È quindi possibile personalizzare la forma specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="449b7-185">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="449b7-186">Per disegnare la forma illustrata nell'immagine seguente, ad esempio, è possibile digitare la rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-186">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 byte)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="449b7-188">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="449b7-188">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="449b7-189">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="449b7-190">curva</span><span class="sxs-lookup"><span data-stu-id="449b7-190">curve</span></span>

<span data-ttu-id="449b7-191">È possibile usare l' `<curve>` elemento per creare una curva di Bézier cubica.</span><span class="sxs-lookup"><span data-stu-id="449b7-191">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="449b7-192">È quindi possibile personalizzare la curva specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="449b7-192">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="449b7-193">Ad esempio, per creare una curva come illustrato nell'immagine seguente, è possibile digitare la rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-193">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 byte)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="449b7-195">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="449b7-195">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="449b7-196">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-196">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="449b7-197">arco</span><span class="sxs-lookup"><span data-stu-id="449b7-197">arc</span></span>

<span data-ttu-id="449b7-198">È possibile utilizzare l' `<arc>` elemento per creare un arco definito come segmento di un Oval.</span><span class="sxs-lookup"><span data-stu-id="449b7-198">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="449b7-199">L'arco è definito dall'intersezione dell'ovale con i vettori RADIUS iniziale e finale specificati dagli angoli.</span><span class="sxs-lookup"><span data-stu-id="449b7-199">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="449b7-200">Gli angoli vengono calcolati usando le proprietà di un cerchio (larghezza uguale a altezza), quindi ridimensionato in modo anisotropico fino alla larghezza e all'altezza desiderate.</span><span class="sxs-lookup"><span data-stu-id="449b7-200">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="449b7-201">Ad esempio, è possibile creare un arco che inizia con 0 gradi e termina con 90 gradi specificando **startAngle** **= "0",** ovvero "90", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-201">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 byte)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="449b7-203">È possibile modificare l'arco specificando **valori diversi** per **startAngle** e indicizzazione, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="449b7-203">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

![arc2.gif (608 byte)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 byte)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="449b7-206">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="449b7-206">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="449b7-207">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="449b7-207">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="449b7-208">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="449b7-208">Summary</span></span>

<span data-ttu-id="449b7-209">È possibile utilizzare gli elementi predefiniti la, ad esempio `<oval>` ,, `<line>` `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` e `<arc>` per creare facilmente la grafica in una pagina Web e quindi personalizzare tali immagini cambiando semplicemente gli attributi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="449b7-209">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 