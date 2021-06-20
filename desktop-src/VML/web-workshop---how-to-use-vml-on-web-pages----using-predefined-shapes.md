---
title: Uso di forme predefinite
description: Questo articolo descrive l'uso di forme predefinite in VML, una funzionalità deprecata a Internet Explorer Windows 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web workshop, forme predefinite
- progettazione di pagine Web, forme predefinite
- Vector Markup Language (VML), forme predefinite
- VML (Vector Markup Language),forme predefinite
- grafica vettoriale, forme predefinite
- Forme VML, predefinite
- forme predefinite
- Vector Markup Language (VML),elemento rect
- VML (Vector Markup Language),elemento rect
- grafica vettoriale, elemento rect
- Elemento rect
- Elementi VML, rect
- Vector Markup Language (VML),elemento roundrect
- VML (Vector Markup Language),elemento roundrect
- grafica vettoriale, elemento roundrect
- roundrect - elemento
- elementi VML, roundrect
- Vector Markup Language (VML),elemento line
- VML (Vector Markup Language),elemento line
- grafica vettoriale, elemento line
- line - elemento
- Elementi VML, riga
- Vector Markup Language (VML),elemento polyline
- VML (Vector Markup Language),elemento polyline
- grafica vettoriale, elemento polilinea
- elemento polyline
- elementi VML, polilinea
- Vector Markup Language (VML),elemento curve
- VML (Vector Markup Language),elemento curve
- grafica vettoriale, elemento curve
- elemento curve
- elementi VML, curva
- Vector Markup Language (VML),elemento arc
- VML (Vector Markup Language),elemento arc
- grafica vettoriale, elemento arc
- elemento arc
- elementi VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407684"
---
# <a name="using-predefined-shapes"></a><span data-ttu-id="96515-140">Uso di forme predefinite</span><span class="sxs-lookup"><span data-stu-id="96515-140">Using Predefined Shapes</span></span>

<span data-ttu-id="96515-141">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9.</span><span class="sxs-lookup"><span data-stu-id="96515-141">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="96515-142">Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="96515-142">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="96515-143">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="96515-143">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="96515-144">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="96515-144">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="96515-145">Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="96515-145">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="96515-146">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="96515-146">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="96515-147">Come si è appreso, è possibile usare `<oval>` l'elemento di VML per creare un semplice ovale.</span><span class="sxs-lookup"><span data-stu-id="96515-147">As you've learned, you can use the `<oval>` element of VML to create a simple oval.</span></span> <span data-ttu-id="96515-148">VML fornisce diversi altri elementi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="96515-148">VML provides several other predefined elements.</span></span> <span data-ttu-id="96515-149">In questo argomento verrà illustrato come disegnare grafica usando questi elementi.</span><span class="sxs-lookup"><span data-stu-id="96515-149">In this topic, we will illustrate how to draw graphics by using these elements.</span></span>

<span data-ttu-id="96515-150">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="96515-150">In this topic:</span></span>

-   [<span data-ttu-id="96515-151">Rect</span><span class="sxs-lookup"><span data-stu-id="96515-151">rect</span></span>](#roundrect)
-   [<span data-ttu-id="96515-152">roundrect</span><span class="sxs-lookup"><span data-stu-id="96515-152">roundrect</span></span>](#roundrect)
-   [<span data-ttu-id="96515-153">Linea</span><span class="sxs-lookup"><span data-stu-id="96515-153">line</span></span>](#polyline)
-   [<span data-ttu-id="96515-154">Polilinea</span><span class="sxs-lookup"><span data-stu-id="96515-154">polyline</span></span>](#polyline)
-   [<span data-ttu-id="96515-155">curva</span><span class="sxs-lookup"><span data-stu-id="96515-155">curve</span></span>](#curve)
-   [<span data-ttu-id="96515-156">Arco</span><span class="sxs-lookup"><span data-stu-id="96515-156">arc</span></span>](#arc)
-   [<span data-ttu-id="96515-157">Summary</span><span class="sxs-lookup"><span data-stu-id="96515-157">Summary</span></span>](#summary)

## <a name="rect"></a><span data-ttu-id="96515-158">rect</span><span class="sxs-lookup"><span data-stu-id="96515-158">rect</span></span>

<span data-ttu-id="96515-159">È possibile usare `<rect>` l'elemento per disegnare un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="96515-159">You can use the `<rect>` element to draw a rectangle.</span></span> <span data-ttu-id="96515-160">È quindi possibile personalizzare il rettangolo specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="96515-160">You can then customize the rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="96515-161">Ad esempio, è possibile disegnare un rettangolo riempito di blu specificando **fillcolor**="blue" e assegnargli un contorno rosso di 3,5 punti specificando **strokecolor**="red" **strokeweight**="3.5pt", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-161">For example, you can draw a rectangle that is filled with blue by specifying **fillcolor**="blue", and give it a 3.5-point red outline by specifying **strokecolor**="red" **strokeweight**="3.5pt", as shown in the following VML representation:</span></span>

![rect1.gif (485 byte)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





<span data-ttu-id="96515-163">Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="96515-163">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span> <span data-ttu-id="96515-164">Nota: la specifica VML non ha un segnalibro per `<rect>` l'elemento .</span><span class="sxs-lookup"><span data-stu-id="96515-164">(Note: The VML specification doesn't have a bookmark for the `<rect>` element.)</span></span>

<span data-ttu-id="96515-165">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-165">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="roundrect"></a><span data-ttu-id="96515-166">roundrect</span><span class="sxs-lookup"><span data-stu-id="96515-166">roundrect</span></span>

<span data-ttu-id="96515-167">È possibile usare `<roundrect>` l'elemento per disegnare un rettangolo con angoli arrotondati.</span><span class="sxs-lookup"><span data-stu-id="96515-167">You can use the `<roundrect>` element to draw a rectangle with rounded corners.</span></span> <span data-ttu-id="96515-168">È quindi possibile personalizzare il rettangolo arrotondato specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="96515-168">You can then customize the rounded rectangle by specifying different property attributes.</span></span>

<span data-ttu-id="96515-169">Ad esempio, è possibile disegnare un rettangolo con angoli arrotondati pari al 30% della metà della dimensione più piccola del rettangolo specificando **arcsize**="0.3", riempirlo di giallo specificando **fillcolor**="yellow" e assegnargli un contorno rosso a 2 punti specificando **strokecolor**="red" **strokeweight**="2pt", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-169">For example, you can draw a rectangle that has rounded corners 30% of half the smaller dimension of the rectangle by specifying **arcsize**="0.3", fill it with yellow by specifying **fillcolor**="yellow", and give it a 2-point red outline by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![roundrect1.gif (622 byte)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="96515-171">Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span><span class="sxs-lookup"><span data-stu-id="96515-171">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .</span></span>

<span data-ttu-id="96515-172">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="line"></a><span data-ttu-id="96515-173">line</span><span class="sxs-lookup"><span data-stu-id="96515-173">line</span></span>

<span data-ttu-id="96515-174">È possibile usare `<line>` l'elemento per creare una linea retta.</span><span class="sxs-lookup"><span data-stu-id="96515-174">You can use the `<line>` element to create a straight line.</span></span> <span data-ttu-id="96515-175">È quindi possibile personalizzare la riga specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="96515-175">You can then customize the line by specifying different property attributes.</span></span>

<span data-ttu-id="96515-176">Ad esempio, è possibile disegnare una linea orizzontale specificando da ="20pt,20pt" a ="100pt,20pt" e impostarla su 2 punti e sul rosso specificando **strokecolor**="red" **strokeweight**="2pt", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-176">For example, you can draw a horizontal line by specifying **from**="20pt,20pt" **to**="100pt,20pt", and make it 2-point and red by specifying **strokecolor**="red" **strokeweight**="2pt", as shown in the following VML representation:</span></span>

![line1.gif (88 byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="96515-178">È possibile disegnare una linea verticale o diagonale specificando semplicemente valori diversi per gli attributi delle proprietà **from** e **to,** come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-178">You can draw a vertical or diagonal line by simply specifying different values for the **from** and **to** property attributes, as shown in the following VML representation:</span></span>

![line2.gif (86 byte)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





<span data-ttu-id="96515-180">Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span><span class="sxs-lookup"><span data-stu-id="96515-180">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .</span></span>

<span data-ttu-id="96515-181">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-181">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="polyline"></a><span data-ttu-id="96515-182">Polilinea</span><span class="sxs-lookup"><span data-stu-id="96515-182">polyline</span></span>

<span data-ttu-id="96515-183">È possibile usare `<polyline>` l'elemento per definire le forme create da segmenti di linea connessi.</span><span class="sxs-lookup"><span data-stu-id="96515-183">You can use the `<polyline>` element to define shapes that are created from connected line segments.</span></span> <span data-ttu-id="96515-184">È quindi possibile personalizzare la forma specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="96515-184">You can then customize the shape by specifying different property attributes.</span></span>

<span data-ttu-id="96515-185">Ad esempio, per disegnare la forma illustrata nell'immagine seguente, è possibile digitare la rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-185">For example, to draw the shape shown in the following picture, you can type the following VML representation:</span></span>

![polyline1.gif (957 byte)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="96515-187">Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span><span class="sxs-lookup"><span data-stu-id="96515-187">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .</span></span>

<span data-ttu-id="96515-188">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-188">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="curve"></a><span data-ttu-id="96515-189">curva</span><span class="sxs-lookup"><span data-stu-id="96515-189">curve</span></span>

<span data-ttu-id="96515-190">È possibile usare `<curve>` l'elemento per disegnare una curva di Bézier cubica.</span><span class="sxs-lookup"><span data-stu-id="96515-190">You can use the `<curve>` element to draw a cubic bézier curve.</span></span> <span data-ttu-id="96515-191">È quindi possibile personalizzare la curva specificando attributi di proprietà diversi.</span><span class="sxs-lookup"><span data-stu-id="96515-191">You can then customize the curve by specifying different property attributes.</span></span>

<span data-ttu-id="96515-192">Ad esempio, per disegnare una curva come illustrato nell'immagine seguente, è possibile digitare la rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-192">For example, to draw a curve as shown in the following picture, you can type the following VML representation:</span></span>

![curve1.gif (992 byte)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





<span data-ttu-id="96515-194">Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span><span class="sxs-lookup"><span data-stu-id="96515-194">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .</span></span>

<span data-ttu-id="96515-195">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="arc"></a><span data-ttu-id="96515-196">arco</span><span class="sxs-lookup"><span data-stu-id="96515-196">arc</span></span>

<span data-ttu-id="96515-197">È possibile usare `<arc>` l'elemento per disegnare un arco definito come segmento di un ovale.</span><span class="sxs-lookup"><span data-stu-id="96515-197">You can use the `<arc>` element to draw an arc that is defined as a segment of an oval.</span></span> <span data-ttu-id="96515-198">L'arco è definito dall'intersezione dell'ovale con i vettori di raggio iniziale e finale specificati dagli angoli.</span><span class="sxs-lookup"><span data-stu-id="96515-198">The arc is defined by the intersection of the oval with the start and end radius vectors given by the angles.</span></span> <span data-ttu-id="96515-199">Gli angoli vengono calcolati usando le proprietà di un cerchio (larghezza uguale all'altezza), quindi ridimensionati in modo orizzontale in base alla larghezza e all'altezza desiderate.</span><span class="sxs-lookup"><span data-stu-id="96515-199">The angles are calculated by using the properties of a circle (width equal to height), then scaled anisotropically to the desired width and height.</span></span>

<span data-ttu-id="96515-200">Ad esempio, è possibile disegnare un arco che inizia da 0 gradi e termina a 90 gradi specificando **startangle**="0" **endangle**="90", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-200">For example, you can draw an arc that starts at 0 degrees and ends at 90 degrees by specifying **startangle**="0" **endangle**="90", as shown in the following VML representation:</span></span>

![arc1.gif (410 byte)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





<span data-ttu-id="96515-202">È possibile modificare l'arco specificando valori **startangle** ed **endangle** diversi, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="96515-202">You can change the arc by specifying different **startangle** and **endangle** values, as shown in the following VML representation:</span></span>

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





<span data-ttu-id="96515-205">Per altre informazioni su questo elemento, vedere la specifica [VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span><span class="sxs-lookup"><span data-stu-id="96515-205">For more information about this element, see the [VML specification](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .</span></span>

<span data-ttu-id="96515-206">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="96515-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="96515-207">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="96515-207">Summary</span></span>

<span data-ttu-id="96515-208">È possibile usare elementi predefiniti vml, ad esempio , , , , , e per disegnare facilmente grafica in una pagina Web e quindi personalizzare tali elementi grafici modificando semplicemente gli attributi `<oval>` `<line>` delle `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` proprietà.</span><span class="sxs-lookup"><span data-stu-id="96515-208">You can use VML predefined elements such as `<oval>`, `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` to easily draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span>

 

 