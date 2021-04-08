---
title: Posizionamento di forme
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web Workshop, posizionamento delle forme
- progettazione di pagine Web, posizionamento di forme
- Vector Markup Language (la), posizionamento delle forme
- LA (Vector Markup Language), posizionamento delle forme
- grafica vettoriale, forme posizionamento
- Forme la, posizionamento
- posizionamento di forme
- Vector Markup Language (la), stile posizione statica
- LA (Vector Markup Language), stile posizione statica
- grafica vettoriale, stile posizione statica
- stile posizione statica
- Vector Markup Language (la), stile posizione relativa
- LA (Vector Markup Language), stile di posizione relativo
- grafica vettoriale, stile posizione relativa
- stile posizione relativa
- Vector Markup Language (la), stile di posizione assoluto
- LA (Vector Markup Language), stile di posizione assoluto
- grafica vettoriale, stile posizione assoluta
- stile posizione assoluta
- Vector Markup Language (la), stile posizione indice z
- LA (Vector Markup Language), stile posizione indice z
- grafica vettoriale, stile posizione indice z
- stile posizione indice z
- Vector Markup Language (la), stile posizione rotazione
- LA (Vector Markup Language), stile posizione rotazione
- grafica vettoriale, stile posizione rotazione
- stile posizione rotazione
- Vector Markup Language (la), Capovolgi stile posizione
- LA (Vector Markup Language), Capovolgi stile posizione
- grafica vettoriale, stile flip position
- Inverti stile posizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8e01d0c7962467b1894f0f4c2c6cd1f6b01509
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046901"
---
# <a name="positioning-shapes"></a><span data-ttu-id="3dd1b-135">Posizionamento di forme</span><span class="sxs-lookup"><span data-stu-id="3dd1b-135">Positioning Shapes</span></span>

<span data-ttu-id="3dd1b-136">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-136">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3dd1b-137">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-137">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3dd1b-138">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-138">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3dd1b-139">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-139">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3dd1b-140">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3dd1b-140">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3dd1b-141">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3dd1b-141">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3dd1b-142">Si è appreso come creare e colorare forme in una pagina Web usando la.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-142">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="3dd1b-143">In questo argomento verrà usato la per posizionare con precisione la grafica in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-143">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="3dd1b-144">LA utilizza la stessa sintassi definita nelle sezioni [modello di riquadro](https://www.w3.org/TR/PR-CSS2/box.mdl) e [modello di rendering visivo](https://www.w3.org/TR/PR-CSS2/visuren.mdl) di [CSS2](https://www.w3.org/TR/PR-CSS2/) per posizionare le forme in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-144">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="3dd1b-145">È possibile usare [static](#static), [relativa](#relative)o [Absolute](#absolute) per determinare la posizione in cui si trova il punto di base in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-145">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="3dd1b-146">È quindi possibile usare gli attributi di stile **superiore** e **sinistro** per specificare l'offset dal punto di base in cui verrà posizionata la casella contenitore per la forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-146">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="3dd1b-147">È inoltre possibile utilizzare [z-index](#z-index) per specificare l'ordine z delle forme in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-147">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="3dd1b-148">Inoltre, la fornisce [rotazione](#rotation) e [Capovolgi](#flip) per ruotare o capovolgere le forme.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-148">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="3dd1b-149">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="3dd1b-149">In this topic:</span></span>

-   [<span data-ttu-id="3dd1b-150">static</span><span class="sxs-lookup"><span data-stu-id="3dd1b-150">static</span></span>](#static)
-   [<span data-ttu-id="3dd1b-151">relative</span><span class="sxs-lookup"><span data-stu-id="3dd1b-151">relative</span></span>](#relative)
-   [<span data-ttu-id="3dd1b-152">absolute</span><span class="sxs-lookup"><span data-stu-id="3dd1b-152">absolute</span></span>](#absolute)
-   [<span data-ttu-id="3dd1b-153">indice z</span><span class="sxs-lookup"><span data-stu-id="3dd1b-153">z-index</span></span>](#z-index)
-   [<span data-ttu-id="3dd1b-154">rotazione</span><span class="sxs-lookup"><span data-stu-id="3dd1b-154">rotation</span></span>](#rotation)
-   [<span data-ttu-id="3dd1b-155">flip</span><span class="sxs-lookup"><span data-stu-id="3dd1b-155">flip</span></span>](#flip)
-   [<span data-ttu-id="3dd1b-156">Summary</span><span class="sxs-lookup"><span data-stu-id="3dd1b-156">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="3dd1b-157">static</span><span class="sxs-lookup"><span data-stu-id="3dd1b-157">static</span></span>

<span data-ttu-id="3dd1b-158">Lo stile di posizione predefinito è statico, che indica ai browser di posizionare la forma in corrispondenza del punto corrente, ovvero il punto di base, nel flusso di testo e ignorare le impostazioni negli attributi di stile **superiore** e **sinistro** .</span><span class="sxs-lookup"><span data-stu-id="3dd1b-158">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="3dd1b-159">Nella rappresentazione la seguente, ad esempio, il rosso ovale viene posizionato immediatamente dopo il testo "inizio della forma:", come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="3dd1b-159">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![\-ps.gif Shape1 (2123 byte)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="3dd1b-161">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-161">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="3dd1b-162">relative</span><span class="sxs-lookup"><span data-stu-id="3dd1b-162">relative</span></span>

<span data-ttu-id="3dd1b-163">L'impostazione dell'attributo di stile position su "relativa" consente di posizionare la casella contenitore con un offset dal punto corrente (il punto di base) nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-163">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="3dd1b-164">L'offset è determinato dalle impostazioni negli attributi di stile **superiore** e **sinistro** .</span><span class="sxs-lookup"><span data-stu-id="3dd1b-164">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="3dd1b-165">Tenere presente che la casella contenitore che è posizionata come relativa occupa spazio nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-165">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="3dd1b-166">Nella rappresentazione la seguente, ad esempio, il rosso ovale è posizionato a 20 punti da sinistra e 10 punti dalla parte superiore rispetto al punto corrente nel flusso di testo, come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="3dd1b-166">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 byte)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="3dd1b-168">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-168">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="3dd1b-169">assoluto</span><span class="sxs-lookup"><span data-stu-id="3dd1b-169">absolute</span></span>

<span data-ttu-id="3dd1b-170">Impostando l'attributo di stile position su "Absolute" è possibile posizionare la casella contenente una distanza esatta dall'angolo superiore sinistro (il punto di base) del relativo elemento padre, ovvero l'elemento posizionato che contiene la forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-170">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="3dd1b-171">Tenere presente che la casella contenitore che è posizionata come assoluta non occupi spazio nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-171">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="3dd1b-172">Nella rappresentazione la seguente, ad esempio, il rosso ovale è contenuto all'interno dell' `<body>` elemento (l'intera pagina Web); Pertanto, il punto di base si trova nell'angolo superiore sinistro della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-172">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="3dd1b-173">La casella contenitore per l'ovale è posizionata esattamente a 20 punti da sinistra e 10 punti dalla parte superiore rispetto all'angolo superiore sinistro della pagina Web, come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="3dd1b-173">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 byte)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="3dd1b-175">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-175">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="3dd1b-176">indice z</span><span class="sxs-lookup"><span data-stu-id="3dd1b-176">z-index</span></span>

<span data-ttu-id="3dd1b-177">È possibile posizionare una forma che si sovrappone a un'altra forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-177">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="3dd1b-178">In genere, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-178">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="3dd1b-179">In la è possibile controllare l'ordine z usando l'attributo di stile **z-index** .</span><span class="sxs-lookup"><span data-stu-id="3dd1b-179">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="3dd1b-180">Il valore di questo attributo può essere zero, un numero intero positivo o un numero intero negativo.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-180">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="3dd1b-181">Il grafico con un valore di indice z più grande viene visualizzato sopra l'elemento grafico con un valore di indice z inferiore.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-181">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="3dd1b-182">Quando entrambi i grafici hanno lo stesso valore di indice z, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-182">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="3dd1b-183">Nella rappresentazione la seguente, ad esempio, il rosso ovale viene visualizzato sopra il rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-183">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="3dd1b-184">Questo è dovuto al fatto che il valore dell'indice z dell'ovale rosso è maggiore del valore dell'indice z del rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-184">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 byte)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="3dd1b-186">Se si modifica l'indice z, come illustrato nella seguente rappresentazione la, il rosso ovale si sposta dietro il rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-186">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 byte)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="3dd1b-188">Se si specifica un numero intero negativo, è possibile usare z-index per posizionare la grafica dietro il normale flusso di testo, come illustrato nella rappresentazione la seguente.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-188">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 byte)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="3dd1b-190">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-190">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="3dd1b-191">rotazione</span><span class="sxs-lookup"><span data-stu-id="3dd1b-191">rotation</span></span>

<span data-ttu-id="3dd1b-192">È possibile utilizzare l'attributo di stile **Rotation** per specificare il numero di gradi per cui si desidera che una forma accenda l'asse.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-192">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="3dd1b-193">Un valore positivo indica una rotazione in senso orario; un valore negativo indica una rotazione in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-193">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="3dd1b-194">Ad esempio, se si specifica **Style**='... Rotation: 90', è possibile ruotare la forma 90 gradi in senso orario.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-194">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="3dd1b-195">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-195">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="3dd1b-196">flip</span><span class="sxs-lookup"><span data-stu-id="3dd1b-196">flip</span></span>

<span data-ttu-id="3dd1b-197">È possibile utilizzare l'attributo **Flip** Style per capovolgere una forma sull'asse x o y in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="3dd1b-197">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="3dd1b-198">Valore</span><span class="sxs-lookup"><span data-stu-id="3dd1b-198">Value</span></span> | <span data-ttu-id="3dd1b-199">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dd1b-199">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="3dd1b-200">x</span><span class="sxs-lookup"><span data-stu-id="3dd1b-200">x</span></span>     | <span data-ttu-id="3dd1b-201">Capovolgere la forma ruotata sull'asse y (Inverti le coordinate x)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-201">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="3dd1b-202">y</span><span class="sxs-lookup"><span data-stu-id="3dd1b-202">y</span></span>     | <span data-ttu-id="3dd1b-203">Capovolgere la forma ruotata sull'asse x (coordinate y invertite)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-203">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="3dd1b-204">Nella proprietà Flip è possibile specificare sia x che y.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-204">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="3dd1b-205">Ad esempio, se si digita **Style**='... Flip: x y. la forma viene invertita sia sull'asse x che su quello y.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-205">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="3dd1b-206">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="3dd1b-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="3dd1b-207">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="3dd1b-207">Summary</span></span>

<span data-ttu-id="3dd1b-208">In base a quanto appreso, è possibile posizionare con precisione una forma in una pagina Web attenendosi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="3dd1b-208">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="3dd1b-209">Decidere dove si desidera che la forma venga visualizzata in una pagina Web e la dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-209">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="3dd1b-210">Specificare **Style**=' position: relativa (o relativa)' per determinare il punto di base.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-210">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="3dd1b-211">Utilizzare **Left** e **Top** per specificare l'offset dal punto di base.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-211">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="3dd1b-212">Usare **Width** e **Height** per specificare la dimensione della casella contenitore per la forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-212">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="3dd1b-213">Utilizzare **z-index** per specificare l'ordine z della forma.</span><span class="sxs-lookup"><span data-stu-id="3dd1b-213">Use **z-index** to specify the z-order of the shape.</span></span>

 

 