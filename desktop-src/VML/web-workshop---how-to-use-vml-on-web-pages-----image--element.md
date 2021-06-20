---
title: Uso dell'elemento Image
description: Questo articolo descrive l'uso dell'elemento Image in VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web workshop, elemento image
- progettazione di pagine Web, elemento image
- Vector Markup Language (VML), elemento image
- VML (Vector Markup Language),elemento image
- grafica vettoriale, elemento image
- Elemento image
- elementi VML, immagine
- Forme VML, elemento image
- Vector Markup Language (VML), attributi delle proprietà crop
- VML (Vector Markup Language),attributi delle proprietà crop
- grafica vettoriale, attributi delle proprietà di ritaglio
- Forme VML, attributi delle proprietà di ritaglio
- Attributi delle proprietà di ritaglio
- Vector Markup Language (VML), ottenere l'attributo della proprietà
- VML (Vector Markup Language),ottenere l'attributo della proprietà
- grafica vettoriale, attributo della proprietà gain
- Forme VML,ottenere l'attributo della proprietà
- Attributo della proprietà gain
- Vector Markup Language (VML), contrasto
- VML (Vector Markup Language),contrasto
- grafica vettoriale, contrasto
- Forme VML,contrasto
- Vector Markup Language (VML), attributo della proprietà blacklevel
- VML (Vector Markup Language),attributo della proprietà blacklevel
- vector graphics,blacklevel - attributo della proprietà
- Forme VML, attributo della proprietà blacklevel
- Attributo della proprietà blacklevel
- Vector Markup Language (VML), luminosità
- VML (Vector Markup Language),luminosità
- grafica vettoriale, luminosità
- Forme VML, luminosità
- Vector Markup Language (VML), attributo della proprietà grayscale
- VML (Vector Markup Language),attributo della proprietà grayscale
- grafica vettoriale, attributo della proprietà grayscale
- Forme VML, attributo della proprietà grayscale
- Attributo della proprietà grayscale
- Vector Markup Language (VML), attributo della proprietà gamma
- VML (Vector Markup Language),attributo della proprietà gamma
- grafica vettoriale, attributo della proprietà gamma
- Forme VML, attributo della proprietà gamma
- Attributo della proprietà gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572acef76afc42e02f476ca1825ef2541f596380
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407804"
---
# <a name="using-the-image-element"></a><span data-ttu-id="e9964-144">Uso dell'elemento Image</span><span class="sxs-lookup"><span data-stu-id="e9964-144">Using the Image Element</span></span>

<span data-ttu-id="e9964-145">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows.</span><span class="sxs-lookup"><span data-stu-id="e9964-145">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e9964-146">È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e9964-146">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e9964-147">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e9964-147">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e9964-148">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="e9964-148">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e9964-149">Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e9964-149">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e9964-150">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e9964-150">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e9964-151">Uso di `<image>`</span><span class="sxs-lookup"><span data-stu-id="e9964-151">Using `<image>`</span></span>

<span data-ttu-id="e9964-152">In questo argomento verrà illustrato come usare l'elemento `<image>` per visualizzare immagini con vari effetti speciali.</span><span class="sxs-lookup"><span data-stu-id="e9964-152">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="e9964-153">Se si desidera visualizzare un'immagine caricata da un'origine esterna, in genere si usa l'elemento fornito in HTML e quindi si punta l'attributo della proprietà src al percorso del file di `<img>` immagine. </span><span class="sxs-lookup"><span data-stu-id="e9964-153">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="e9964-154">In alternativa, è possibile usare `<image>` l'elemento fornito in VML.</span><span class="sxs-lookup"><span data-stu-id="e9964-154">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="e9964-155">Quando si usa l'elemento , è possibile creare un solo file di immagine e quindi visualizzare l'immagine in modo diverso modificando gli attributi `<image>` delle proprietà `<image>` dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e9964-155">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="e9964-156">Inoltre, l'elemento fornisce diversi effetti speciali che non è possibile eseguire semplicemente usando l'elemento HTML, ad esempio il ritaglio, il `<image>` `<img>` [](#crop) [contrasto,](#contrast) [](#brightness)la luminosità, la [gamma](#gamma)e la scala di [grigi.](#grayscale)</span><span class="sxs-lookup"><span data-stu-id="e9964-156">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="e9964-157">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e9964-157">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="e9964-158">Raccolto</span><span class="sxs-lookup"><span data-stu-id="e9964-158">crop</span></span>

<span data-ttu-id="e9964-159">È possibile usare gli attributi delle proprietà **cropbottom**, **croptop**, **cropleft** e **cropright** dell'elemento per visualizzare immagini diverse ritagliate dallo `<image>` stesso file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e9964-159">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="e9964-160">Il valore di questi attributi di ritaglio rappresenta la percentuale di taglio dal bordo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e9964-160">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="e9964-161">Il valore può essere qualsiasi numero compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="e9964-161">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="e9964-162">Per impostazione predefinita, il valore è impostato su 0, a indicare che non viene ritagliato dal bordo.</span><span class="sxs-lookup"><span data-stu-id="e9964-162">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="e9964-163">Il valore 0,1 indica un ritaglio del 10% dal bordo, Il valore 0,15 indica un ritaglio del 15% dal bordo e così via.</span><span class="sxs-lookup"><span data-stu-id="e9964-163">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="e9964-164">Ad esempio, per visualizzare cinque immagini tutte ritagliate dallo stesso file di immagine, è possibile usare l'elemento e specificare valori di ritaglio diversi, come illustrato nella rappresentazione `<image>` VML seguente:</span><span class="sxs-lookup"><span data-stu-id="e9964-164">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![image1 \-2.jpg (1969 byte)](images/image1-2.jpg)![image1 \-3.jpg (1148 byte)](images/image1-3.jpg)![image1 \-4.jpg (1686 byte)](images/image1-4.jpg)![image1 \-5.jpg (1364 byte)](images/image1-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:85pt;height:64pt' src="image1.jpg"
cropbottom="0.2" cropright="0.15"/>
<v:image style='width:50pt;height:44pt' src="image1.jpg"
cropbottom="0.45" cropleft="0.5"/>
<v:image style='width:80pt;height:56pt' src="image1.jpg"
croptop="0.3" cropright="0.2"/>
<v:image style='width:70pt;height:48pt' src="image1.jpg"
croptop="0.4" cropleft="0.3"/>
```





<span data-ttu-id="e9964-170">La prima immagine, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , non ha alcun valore di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="e9964-170">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="e9964-171">Di conseguenza, il 100% dell'immagine originale viene visualizzato con dimensioni di 100 punti per 80 punti.</span><span class="sxs-lookup"><span data-stu-id="e9964-171">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="e9964-172">La seconda immagine, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , ha alcuni valori di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="e9964-172">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="e9964-173">`cropbottom="0.2"` indica che il 20% dell'immagine verrà ritagliato dal basso; `cropright="0.15"` indica che il 15% dell'immagine verrà ritagliato dal bordo destro.</span><span class="sxs-lookup"><span data-stu-id="e9964-173">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="e9964-174">L'immagine rimanente viene quindi visualizzata con una dimensione di 85 punti per 64 punti.</span><span class="sxs-lookup"><span data-stu-id="e9964-174">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="e9964-175">Analogamente, la terza, la quarta e la quinta immagine hanno alcuni valori di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="e9964-175">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="e9964-176">L'immagine originale viene ritagliata in base ai valori di ritaglio e quindi visualizzata in base al valore di larghezza e altezza.</span><span class="sxs-lookup"><span data-stu-id="e9964-176">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="e9964-177">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e9964-177">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="e9964-178">elevato</span><span class="sxs-lookup"><span data-stu-id="e9964-178">contrast</span></span>

<span data-ttu-id="e9964-179">È possibile usare **l'attributo della** proprietà gain dell'elemento per visualizzare diverse immagini con impostazioni `<image>` di contrasto diverse.</span><span class="sxs-lookup"><span data-stu-id="e9964-179">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="e9964-180">Il valore **dell'attributo della proprietà gain** può essere qualsiasi numero.</span><span class="sxs-lookup"><span data-stu-id="e9964-180">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="e9964-181">Per impostazione predefinita, il valore è 1, che indica l'uso dello stesso contrasto dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="e9964-181">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="e9964-182">Il valore 0 indica nessun contrasto.</span><span class="sxs-lookup"><span data-stu-id="e9964-182">The value 0 indicates no contrast.</span></span> <span data-ttu-id="e9964-183">Maggiore è il numero, maggiore è il contrasto.</span><span class="sxs-lookup"><span data-stu-id="e9964-183">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="e9964-184">Ad esempio, per visualizzare cinque immagini con impostazioni di contrasto diverse, è possibile usare l'elemento e impostare un valore diverso per l'attributo della proprietà gain, come illustrato nella rappresentazione `<image>` VML seguente: </span><span class="sxs-lookup"><span data-stu-id="e9964-184">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![image2 \-2.jpg (270 byte)](images/image2-2.jpg)![image2 \-3.jpg (1919 byte)](images/image2-3.jpg)![image2 \-4.jpg (3143 byte)](images/image2-4.jpg)![image2 \-5.jpg (1724 byte)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="e9964-190">Quando **l'attributo della** proprietà gain è impostato su 0, l'intera immagine diventa grigia perché non è presente alcun contrasto.</span><span class="sxs-lookup"><span data-stu-id="e9964-190">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="e9964-191">Il contrasto è più evidente quando **l'attributo della** proprietà gain è impostato su 3 rispetto a quando è impostato su 0,5.</span><span class="sxs-lookup"><span data-stu-id="e9964-191">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="e9964-192">Il contrasto viene invertito quando **l'attributo della** proprietà gain è impostato su un valore negativo, ad esempio -0,4.</span><span class="sxs-lookup"><span data-stu-id="e9964-192">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="e9964-193">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e9964-193">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="e9964-194">luminosità</span><span class="sxs-lookup"><span data-stu-id="e9964-194">brightness</span></span>

<span data-ttu-id="e9964-195">È possibile usare **l'attributo della proprietà blacklevel** dell'elemento `<image>` per visualizzare varie immagini con impostazioni di luminosità diverse.</span><span class="sxs-lookup"><span data-stu-id="e9964-195">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="e9964-196">Il valore **dell'attributo della proprietà blacklevel** può essere qualsiasi valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="e9964-196">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="e9964-197">Per impostazione predefinita, il valore è 0, a indicare che il livello di luminosità nell'immagine originale viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="e9964-197">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="e9964-198">Il valore 1 indica il livello massimo di luminosità.</span><span class="sxs-lookup"><span data-stu-id="e9964-198">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="e9964-199">Ad esempio, per visualizzare cinque immagini con impostazioni di luminosità diverse, è possibile usare l'elemento e impostare un valore diverso per l'attributo della proprietà blacklevel, come illustrato nella rappresentazione `<image>` VML seguente: </span><span class="sxs-lookup"><span data-stu-id="e9964-199">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![image3 \-2.jpg (2579 byte)](images/image3-2.jpg)![image3 \-3.jpg (2330 byte)](images/image3-3.jpg)![image3 \-4.jpg (2727 byte)](images/image3-4.jpg)![image3 \-5.jpg (2435 byte)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="e9964-205">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e9964-205">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="e9964-206">scala di grigi</span><span class="sxs-lookup"><span data-stu-id="e9964-206">grayscale</span></span>

<span data-ttu-id="e9964-207">È possibile usare **l'attributo della proprietà grayscale** dell'elemento `<image>` per visualizzare immagini con o senza gradazioni di grigio.</span><span class="sxs-lookup"><span data-stu-id="e9964-207">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="e9964-208">Il valore **dell'attributo della proprietà grayscale** può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="e9964-208">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="e9964-209">Per impostazione predefinita, il valore è impostato su false in modo che l'immagine verrà visualizzata a colori.</span><span class="sxs-lookup"><span data-stu-id="e9964-209">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="e9964-210">Se il valore è impostato su true, l'immagine verrà visualizzata in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="e9964-210">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="e9964-211">Ad esempio, come illustrato nell'immagine seguente, la prima immagine usa l'impostazione predefinita (false) dell'attributo della scala di grigi ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="e9964-211">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="e9964-212">Di conseguenza, l'immagine viene visualizzata a colori.</span><span class="sxs-lookup"><span data-stu-id="e9964-212">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="e9964-213">La seconda immagine imposta l'attributo della scala di grigi su true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="e9964-213">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="e9964-214">Di conseguenza, l'immagine viene visualizzata in scala di grigi, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="e9964-214">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![image4 \-2.jpg (2138 byte)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="e9964-217">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="e9964-217">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="e9964-218">gamma</span><span class="sxs-lookup"><span data-stu-id="e9964-218">gamma</span></span>

<span data-ttu-id="e9964-219">È possibile usare **l'attributo della** proprietà gamma dell'elemento per visualizzare immagini con impostazioni `<image>` gamma diverse.</span><span class="sxs-lookup"><span data-stu-id="e9964-219">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="e9964-220">Il valore dell'attributo della proprietà gamma può essere qualsiasi valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="e9964-220">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="e9964-221">Per impostazione predefinita, il valore è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="e9964-221">By default, the value is set to 1.</span></span>

<span data-ttu-id="e9964-222">Ad esempio, per visualizzare tre immagini con impostazioni gamma diverse, è possibile usare l'elemento e impostare un valore diverso dell'attributo della proprietà gamma, come illustrato nella rappresentazione `<image>` VML seguente: </span><span class="sxs-lookup"><span data-stu-id="e9964-222">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![image5 \-1.jpg (2714 byte)](images/image5-1.jpg)![image5 \-2.jpg (2729 byte)](images/image5-2.jpg)![image5 \-3.jpg (2726 byte)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="e9964-226">Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="e9964-226">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 