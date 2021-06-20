---
title: Posizionamento di forme
description: Questo articolo descrive il posizionamento delle forme in VML, una funzionalità deprecata a Internet Explorer 9.
ms.assetid: dbd68f54-201a-48dc-a3a9-a8dd42178c11
keywords:
- Web workshop, posizionamento di forme
- progettazione di pagine Web, posizionamento di forme
- Vector Markup Language (VML), posizionamento di forme
- VML (Vector Markup Language),posizionamento di forme
- grafica vettoriale, posizionamento di forme
- forme VML, posizionamento
- posizionamento di forme
- Vector Markup Language (VML), stile di posizione statica
- VML (Vector Markup Language),stile di posizione statica
- grafica vettoriale, stile di posizione statica
- stile di posizione statica
- Vector Markup Language (VML), stile di posizione relativa
- VML (Vector Markup Language),stile di posizione relativa
- grafica vettoriale, stile di posizione relativa
- stile di posizione relativa
- Vector Markup Language (VML), stile di posizione assoluta
- VML (Vector Markup Language),absolute position style
- grafica vettoriale, stile di posizione assoluta
- stile di posizione assoluta
- Vector Markup Language (VML),z-index position style
- VML (Vector Markup Language),z-index position style
- grafica vettoriale, stile di posizione z-index
- Stile di posizione z-index
- Vector Markup Language (VML), stile della posizione di rotazione
- VML (Vector Markup Language),stile della posizione di rotazione
- grafica vettoriale, stile di posizione di rotazione
- stile della posizione di rotazione
- Vector Markup Language (VML), stile di capovolgimento della posizione
- VML (Vector Markup Language),flip position style
- grafica vettoriale, stile posizione capovolgimento
- stile di posizione capovolgimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c96a8de891ed1bbd1b9bfee9eff52ede946247b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407714"
---
# <a name="positioning-shapes"></a><span data-ttu-id="5c348-134">Posizionamento di forme</span><span class="sxs-lookup"><span data-stu-id="5c348-134">Positioning Shapes</span></span>

<span data-ttu-id="5c348-135">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9.</span><span class="sxs-lookup"><span data-stu-id="5c348-135">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5c348-136">Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="5c348-136">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5c348-137">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="5c348-137">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5c348-138">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="5c348-138">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5c348-139">Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="5c348-139">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5c348-140">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="5c348-140">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5c348-141">Si è appreso come disegnare e colorare forme in una pagina Web usando VML.</span><span class="sxs-lookup"><span data-stu-id="5c348-141">You've learned how to draw and color shapes on a Web page using VML.</span></span> <span data-ttu-id="5c348-142">In questo argomento si userà VML per posizionare con precisione la grafica in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="5c348-142">In this topic, you'll use VML to precisely position graphics on a Web page.</span></span>

<span data-ttu-id="5c348-143">VML usa la stessa sintassi definita nelle sezioni Box Model (Modello [box)](https://www.w3.org/TR/PR-CSS2/box.mdl) e [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) (Modello di rendering visivo) di [CSS2](https://www.w3.org/TR/PR-CSS2/) per posizionare le forme in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="5c348-143">VML uses the same syntax defined in the [Box Model](https://www.w3.org/TR/PR-CSS2/box.mdl) and [Visual Rendering Model](https://www.w3.org/TR/PR-CSS2/visuren.mdl) sections of [CSS2](https://www.w3.org/TR/PR-CSS2/) to position shapes on a Web page.</span></span> <span data-ttu-id="5c348-144">È possibile usare [static](#static), [relative](#relative)o [absolute](#absolute) per determinare dove si trova il punto di base in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="5c348-144">You can use [static](#static), [relative](#relative), or [absolute](#absolute) to determine where the base point is located on a Web page.</span></span> <span data-ttu-id="5c348-145">È quindi possibile usare  gli **attributi** di stile superiore e sinistro per specificare l'offset dal punto di base in cui verrà posizionata la casella contenitore per la forma.</span><span class="sxs-lookup"><span data-stu-id="5c348-145">You can then use the **top** and **left** style attributes to specify the offset from the base point at which the containing box for the shape will be positioned.</span></span>

<span data-ttu-id="5c348-146">È anche possibile usare [z-index](#z-index) per specificare l'ordine z delle forme in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="5c348-146">You can also use [z-index](#z-index) to specify the z-order of shapes on a Web page.</span></span>

<span data-ttu-id="5c348-147">VmL offre inoltre la [rotazione](#rotation) e il [capovolgimento](#flip) per ruotare o capovolgere le forme.</span><span class="sxs-lookup"><span data-stu-id="5c348-147">In addition, VML provides [rotation](#rotation) and [flip](#flip) to rotate or flip shapes.</span></span>

<span data-ttu-id="5c348-148">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="5c348-148">In this topic:</span></span>

-   [<span data-ttu-id="5c348-149">static</span><span class="sxs-lookup"><span data-stu-id="5c348-149">static</span></span>](#static)
-   [<span data-ttu-id="5c348-150">relative</span><span class="sxs-lookup"><span data-stu-id="5c348-150">relative</span></span>](#relative)
-   [<span data-ttu-id="5c348-151">absolute</span><span class="sxs-lookup"><span data-stu-id="5c348-151">absolute</span></span>](#absolute)
-   [<span data-ttu-id="5c348-152">z-index</span><span class="sxs-lookup"><span data-stu-id="5c348-152">z-index</span></span>](#z-index)
-   [<span data-ttu-id="5c348-153">Rotazione</span><span class="sxs-lookup"><span data-stu-id="5c348-153">rotation</span></span>](#rotation)
-   [<span data-ttu-id="5c348-154">flip</span><span class="sxs-lookup"><span data-stu-id="5c348-154">flip</span></span>](#flip)
-   [<span data-ttu-id="5c348-155">Summary</span><span class="sxs-lookup"><span data-stu-id="5c348-155">Summary</span></span>](#summary)

## <a name="static"></a><span data-ttu-id="5c348-156">static</span><span class="sxs-lookup"><span data-stu-id="5c348-156">static</span></span>

<span data-ttu-id="5c348-157">Lo stile di posizione predefinito è statico, che indica ai browser di posizionare la forma in corrispondenza del  punto  corrente (il punto di base) nel flusso di testo e ignorare le impostazioni negli attributi di stile superiore e sinistro.</span><span class="sxs-lookup"><span data-stu-id="5c348-157">The default position style is static, which instructs browsers to position the shape at the current point (the base point) in the text flow and ignore the settings in the **top** and **left** style attributes.</span></span>

<span data-ttu-id="5c348-158">Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene posizionato immediatamente dopo il testo "Beginning of the shape:", come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="5c348-158">For example, in the following VML representation, the red oval is positioned immediately after the text "Beginning of the shape:", as shown in the following picture:</span></span>

![shape1 \-ps.gif (2123 byte)](images/shape1-ps.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='width:80pt;height:90pt' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="5c348-160">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="relative"></a><span data-ttu-id="5c348-161">relative</span><span class="sxs-lookup"><span data-stu-id="5c348-161">relative</span></span>

<span data-ttu-id="5c348-162">L'impostazione dell'attributo di stile della posizione su "relative" consente di posizionare la casella contenitore con un offset dal punto corrente (il punto di base) nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="5c348-162">Setting the position style attribute to "relative" allows you to place the containing box with an offset from the current point (the base point) in the text flow.</span></span> <span data-ttu-id="5c348-163">L'offset è determinato dalle impostazioni negli attributi di stile **superiore** **e** sinistro.</span><span class="sxs-lookup"><span data-stu-id="5c348-163">The offset is determined by the settings in the **top** and **left** style attributes.</span></span> <span data-ttu-id="5c348-164">Tenere presente che la casella contenitore posizionata come relativa occupa spazio nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="5c348-164">Be aware that the containing box that is positioned as relative takes up space in the text flow.</span></span>

<span data-ttu-id="5c348-165">Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene posizionato 20 punti da sinistra e 10 punti dall'alto rispetto al punto corrente nel flusso di testo, come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="5c348-165">For example, in the following VML representation, the red oval is positioned 20 points from the left and 10 points from the top relative to the current point in the text flow, as shown in the following picture:</span></span>

![shape3.gif (2048 byte)](images/shape3.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;width:80pt;
height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="5c348-167">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-167">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="absolute"></a><span data-ttu-id="5c348-168">assoluto</span><span class="sxs-lookup"><span data-stu-id="5c348-168">absolute</span></span>

<span data-ttu-id="5c348-169">L'impostazione dell'attributo di stile della posizione su "absolute" consente di posizionare la casella contenitore a una distanza esatta dall'angolo superiore sinistro (il punto di base) dell'elemento padre (l'elemento posizionato che contiene la forma).</span><span class="sxs-lookup"><span data-stu-id="5c348-169">Setting the position style attribute to "absolute" allows you to place the containing box an exact distance from the top left corner (the base point) of its parent element (the positioned element that contains the shape).</span></span> <span data-ttu-id="5c348-170">Tenere presente che la casella contenitore posizionata come assoluta non richiede spazio nel flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="5c348-170">Be aware that the containing box that is positioned as absolute doesn't take up space in the text flow.</span></span>

<span data-ttu-id="5c348-171">Nella rappresentazione VML seguente, ad esempio, l'ovale rosso è contenuto all'interno dell'elemento (l'intera pagina Web). Pertanto, il punto di base si trova nell'angolo superiore sinistro della `<body>` pagina Web.</span><span class="sxs-lookup"><span data-stu-id="5c348-171">For example, in the following VML representation, the red oval is contained within the `<body>` element (the entire Web page); therefore, the base point is at the top left corner of the Web page.</span></span> <span data-ttu-id="5c348-172">La casella contenitore per l'ovale è posizionata esattamente a 20 punti da sinistra e a 10 punti dall'alto, rispetto all'angolo superiore sinistro della pagina Web, come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="5c348-172">The containing box for the oval is positioned exactly 20 points from the left and 10 points from the top, relative to the top left corner of the Web page, as shown in the following picture:</span></span>

![shape2.gif (2006 byte)](images/shape2.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt
width:80pt; height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="5c348-174">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-174">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="z-index"></a><span data-ttu-id="5c348-175">indice z</span><span class="sxs-lookup"><span data-stu-id="5c348-175">z-index</span></span>

<span data-ttu-id="5c348-176">È possibile posizionare una forma che si sovrappone a un'altra forma.</span><span class="sxs-lookup"><span data-stu-id="5c348-176">It is possible to position a shape that overlaps another shape.</span></span> <span data-ttu-id="5c348-177">In genere, il grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="5c348-177">Normally, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="5c348-178">In VML è possibile controllare l'ordine z usando **l'attributo di stile z-index.**</span><span class="sxs-lookup"><span data-stu-id="5c348-178">In VML, you can control the z-order by using the **z-index** style attribute.</span></span> <span data-ttu-id="5c348-179">Il valore di questo attributo può essere zero, un numero intero positivo o un numero intero negativo.</span><span class="sxs-lookup"><span data-stu-id="5c348-179">The value of this attribute can be zero, a positive integer, or a negative integer.</span></span> <span data-ttu-id="5c348-180">L'elemento grafico con un valore z-index maggiore viene visualizzato sopra l'elemento grafico con un valore z-index più piccolo.</span><span class="sxs-lookup"><span data-stu-id="5c348-180">The graphic that has a larger z-index value is displayed on top of the graphic that has a smaller z-index value.</span></span> <span data-ttu-id="5c348-181">Quando entrambi gli elementi grafici hanno lo stesso valore z-index, l'elemento grafico elencato per ultimo nel codice HTML viene visualizzato nella parte superiore.</span><span class="sxs-lookup"><span data-stu-id="5c348-181">When both graphics have the same z-index value, the graphic that is listed last in the HTML code appears on top.</span></span>

<span data-ttu-id="5c348-182">Nella rappresentazione VML seguente, ad esempio, l'ovale rosso viene visualizzato sopra il rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="5c348-182">For example, in the following VML representation, the red oval is displayed on top of the blue rectangle.</span></span> <span data-ttu-id="5c348-183">Questo perché il valore z-index dell'ovale rosso è maggiore del valore z-index del rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="5c348-183">This is because the z-index value of the red oval is greater than the z-index value of the blue rectangle.</span></span>

![shape4.gif (572 byte)](images/shape4.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index: 1'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt; z-index:0' fillcolor="blue" />
```





<span data-ttu-id="5c348-185">Se si modifica l'indice z, come illustrato nella rappresentazione VML seguente, l'ovale rosso si sposterà dietro il rettangolo blu.</span><span class="sxs-lookup"><span data-stu-id="5c348-185">If you change the z-index, as shown in the following VML representation, the red oval would move behind the blue rectangle.</span></span>

![shape5.gif (469 byte)](images/shape5.gif)


```HTML
<v:oval
style='position:relative;left:10pt;top:20pt;width:100pt; height:80pt;z-index:0'
fillcolor="red" />
<v:rect style='position:relative;left:10pt;top:45pt;width:100pt; height:80pt;z-index:1'
fillcolor="blue" />
```





<span data-ttu-id="5c348-187">Se si specifica un numero intero negativo, è possibile usare z-index per posizionare la grafica dietro il normale flusso di testo, come illustrato nella rappresentazione VML seguente.</span><span class="sxs-lookup"><span data-stu-id="5c348-187">If you supply a negative integer, you can use z-index to position graphics behind the normal text flow, as shown in the following VML representation.</span></span>

![shape6.gif (2125 byte)](images/shape6.gif)


```HTML
<body>
Beginning of the shape:
<v:oval style='position:relative;left:20pt;top:10pt;z-index:-1;
width:80pt;height:90pt;' fillcolor="red" />
End.
</body>
```





<span data-ttu-id="5c348-189">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-189">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="rotation"></a><span data-ttu-id="5c348-190">Rotazione</span><span class="sxs-lookup"><span data-stu-id="5c348-190">rotation</span></span>

<span data-ttu-id="5c348-191">È possibile usare **l'attributo di** stile di rotazione per specificare quanti gradi si vuole che una forma accerti il relativo asse.</span><span class="sxs-lookup"><span data-stu-id="5c348-191">You can use the **rotation** style attribute to specify how many degrees you want a shape to turn on its axis.</span></span> <span data-ttu-id="5c348-192">Un valore positivo indica una rotazione in senso orario; un valore negativo indica una rotazione in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="5c348-192">A positive value indicates a clockwise rotation; a negative value indicates a counter-clockwise rotation.</span></span>

<span data-ttu-id="5c348-193">Ad esempio, se si specifica **style**='... rotation:90', è possibile ruotare la forma di 90 gradi in senso orario.</span><span class="sxs-lookup"><span data-stu-id="5c348-193">For example, if you specify **style**='... rotation:90', you can rotate the shape 90 degrees clockwise.</span></span>

<span data-ttu-id="5c348-194">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="flip"></a><span data-ttu-id="5c348-195">flip</span><span class="sxs-lookup"><span data-stu-id="5c348-195">flip</span></span>

<span data-ttu-id="5c348-196">È possibile usare **l'attributo dello** stile di capovolgimento per capovolgere una forma sul relativo asse x o y in base alla tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="5c348-196">You can use the **flip** style attribute to flip a shape on its x or y axis according to the following table:</span></span>



| <span data-ttu-id="5c348-197">Valore</span><span class="sxs-lookup"><span data-stu-id="5c348-197">Value</span></span> | <span data-ttu-id="5c348-198">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c348-198">Description</span></span>                                                  |
|-------|--------------------------------------------------------------|
| <span data-ttu-id="5c348-199">x</span><span class="sxs-lookup"><span data-stu-id="5c348-199">x</span></span>     | <span data-ttu-id="5c348-200">Capovolgere la forma ruotata intorno all'asse y (inverti x ordinate)</span><span class="sxs-lookup"><span data-stu-id="5c348-200">Flip the rotated shape about the y axis (invert x ordinates)</span></span> |
| <span data-ttu-id="5c348-201">y</span><span class="sxs-lookup"><span data-stu-id="5c348-201">y</span></span>     | <span data-ttu-id="5c348-202">Capovolgere la forma ruotata intorno all'asse x (inverte ordinate y)</span><span class="sxs-lookup"><span data-stu-id="5c348-202">Flip the rotated shape about the x axis (invert y ordinates)</span></span> |



 

<span data-ttu-id="5c348-203">Sia x che y possono essere specificati nella proprietà flip.</span><span class="sxs-lookup"><span data-stu-id="5c348-203">Both x and y may be specified in the flip property.</span></span>

<span data-ttu-id="5c348-204">Ad esempio, se si digita **style**='... flip:x y', la forma verrà capovolta sia sull'asse x che sull'asse y.</span><span class="sxs-lookup"><span data-stu-id="5c348-204">For example, if you type **style**='... flip:x y', you will flip the shape on both its x and y axis.</span></span>

<span data-ttu-id="5c348-205">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="5c348-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="5c348-206">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="5c348-206">Summary</span></span>

<span data-ttu-id="5c348-207">In base a quanto appreso, è possibile posizionare con precisione una forma in una pagina Web seguendo questa procedura:</span><span class="sxs-lookup"><span data-stu-id="5c348-207">Based on what you've learned, you can precisely position a shape on a Web page by following these steps:</span></span>

1.  <span data-ttu-id="5c348-208">Decidere dove si vuole che la forma venga visualizzata in una pagina Web e le dimensioni della forma.</span><span class="sxs-lookup"><span data-stu-id="5c348-208">Decide where you want the shape to appear on a Web page, and the size of the shape.</span></span>
2.  <span data-ttu-id="5c348-209">Specificare **style**='position:relative (or relative)' per determinare il punto di base.</span><span class="sxs-lookup"><span data-stu-id="5c348-209">Specify **style**='position:relative (or relative)' to determine the base point.</span></span>
3.  <span data-ttu-id="5c348-210">Usare **left** e **top** per specificare l'offset dal punto di base.</span><span class="sxs-lookup"><span data-stu-id="5c348-210">Use **left** and **top** to specify the offset from the base point.</span></span>
4.  <span data-ttu-id="5c348-211">Usare **larghezza** e **altezza** per specificare le dimensioni della casella contenitore per la forma.</span><span class="sxs-lookup"><span data-stu-id="5c348-211">Use **width** and **height** to specify the size of the containing box for the shape.</span></span>
5.  <span data-ttu-id="5c348-212">Usare **z-index** per specificare l'ordine z della forma.</span><span class="sxs-lookup"><span data-stu-id="5c348-212">Use **z-index** to specify the z-order of the shape.</span></span>

 

 