---
title: Utilizzo dell'elemento Image
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 444c0b21-35f0-4e2d-ab6d-87a88229d9d2
keywords:
- Web Workshop, elemento Image
- progettazione di pagine Web, elemento Image
- Vector Markup Language (la), elemento Image
- LA (Vector Markup Language), elemento Image
- Vector graphics, elemento Image
- Elemento image
- Elementi la, image
- Forme la, elemento Image
- Vector Markup Language (la), attributi della proprietà Crop
- LA (Vector Markup Language), attributi della proprietà Crop
- grafica vettoriale, attributi della proprietà Crop
- Forme la, attributi della proprietà Crop
- attributi della proprietà Crop
- Vector Markup Language (la), Acquisisci attributo proprietà
- LA (Vector Markup Language), Acquisisci attributo proprietà
- graphics vettoriale, Acquisisci attributo proprietà
- LA forme, Acquisisci attributo proprietà
- Acquisisci attributo proprietà
- Vector Markup Language (la), contrasto
- LA (Vector Markup Language), contrasto
- grafica vettoriale, contrasto
- Forme la, contrasto
- Vector Markup Language (la), attributo proprietà blacklevel
- LA (Vector Markup Language), attributo proprietà blacklevel
- grafica vettoriale, attributo proprietà blacklevel
- Forme la, attributo proprietà blacklevel
- attributo proprietà blacklevel
- Vector Markup Language (la), luminosità
- LA (Vector Markup Language), luminosità
- grafica vettoriale, luminosità
- Forme la, luminosità
- Vector Markup Language (la), attributo della proprietà di scala di grigi
- LA (Vector Markup Language), attributo della proprietà di scala di grigi
- grafica vettoriale, attributo Proprietà scala di grigi
- Forme la, attributo proprietà scale di grigi
- attributo della proprietà di scala di grigi
- Vector Markup Language (la), attributo di proprietà gamma
- LA (Vector Markup Language), attributo di proprietà gamma
- grafica vettoriale, attributo di proprietà gamma
- Forme la, attributo di proprietà gamma
- attributo della proprietà gamma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820039ff76f3685eeea7a65e2bbc01578abbe581
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517049"
---
# <a name="using-the-image-element"></a><span data-ttu-id="a9135-145">Utilizzo dell'elemento Image</span><span class="sxs-lookup"><span data-stu-id="a9135-145">Using the Image Element</span></span>

<span data-ttu-id="a9135-146">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a9135-146">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a9135-147">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a9135-147">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a9135-148">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a9135-148">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a9135-149">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a9135-149">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a9135-150">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a9135-150">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a9135-151">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a9135-151">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a9135-152">Uso di `<image>`</span><span class="sxs-lookup"><span data-stu-id="a9135-152">Using `<image>`</span></span>

<span data-ttu-id="a9135-153">In questo argomento verrà illustrato come utilizzare l' `<image>` elemento per visualizzare immagini con diversi effetti speciali.</span><span class="sxs-lookup"><span data-stu-id="a9135-153">In this topic, we will illustrate how to use the `<image>` element to display pictures with various special effects.</span></span>

<span data-ttu-id="a9135-154">Se si vuole visualizzare un'immagine che è stata caricata da un'origine esterna, in genere si usa l' `<img>` elemento fornito in HTML, quindi si posiziona l'attributo della proprietà **src** sul percorso del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="a9135-154">If you wanted to display a picture that was loaded from an external source, you would usually use the `<img>` element provided in HTML, and then point the **src** property attribute to the location of the image file.</span></span>

<span data-ttu-id="a9135-155">In alternativa, è possibile usare l' `<image>` elemento fornito in la.</span><span class="sxs-lookup"><span data-stu-id="a9135-155">Alternatively you can use the `<image>` element provided in VML.</span></span> <span data-ttu-id="a9135-156">Quando si usa l' `<image>` elemento, è possibile creare un solo file di immagine e quindi visualizzare l'immagine in modo diverso modificando gli attributi delle proprietà dell' `<image>` elemento.</span><span class="sxs-lookup"><span data-stu-id="a9135-156">When you use the `<image>` element, you can create only one image file and then display the image differently by altering the property attributes of the `<image>` element.</span></span> <span data-ttu-id="a9135-157">Inoltre, l' `<image>` elemento fornisce diversi effetti speciali che non è possibile eseguire utilizzando semplicemente l' `<img>` elemento HTML, ad esempio [ritaglio](#crop), [contrasto](#contrast), [luminosità](#brightness), [gamma](#gamma)e [scala di grigi](#grayscale).</span><span class="sxs-lookup"><span data-stu-id="a9135-157">Also, the `<image>` element provides several special effects that you can't do by simply using the `<img>` element of HTML, such as [cropping](#crop), [contrast](#contrast), [brightness](#brightness), [gamma](#gamma), and [grayscale](#grayscale).</span></span>

<span data-ttu-id="a9135-158">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="a9135-158">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="crop"></a><span data-ttu-id="a9135-159">raccolto</span><span class="sxs-lookup"><span data-stu-id="a9135-159">crop</span></span>

<span data-ttu-id="a9135-160">È possibile usare gli attributi di proprietà **CropBottom**, **CropTop**, **CropLeft** e **CropRight** dell' `<image>` elemento per visualizzare immagini diverse ritagliate dallo stesso file di immagine.</span><span class="sxs-lookup"><span data-stu-id="a9135-160">You can use the **cropbottom**, **croptop**, **cropleft**, and **cropright** property attributes of the `<image>` element to display different pictures that are cropped from the same image file.</span></span>

<span data-ttu-id="a9135-161">Il valore di questi attributi di ritaglio rappresenta il taglio percentuale dal bordo dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="a9135-161">The value of these crop attributes represents the percentage cut from the edge of the picture.</span></span> <span data-ttu-id="a9135-162">Il valore può essere qualsiasi numero compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="a9135-162">The value can be any number between 0 to 1.</span></span> <span data-ttu-id="a9135-163">Per impostazione predefinita, il valore è impostato su 0, che indica nessun ritaglio dal bordo.</span><span class="sxs-lookup"><span data-stu-id="a9135-163">By default, the value is set to 0, indicating no crop from the edge.</span></span> <span data-ttu-id="a9135-164">Il valore 0,1 indica un ritaglio del 10% dal bordo, il valore 0,15 indica un ritaglio del 15% dal bordo e così via.</span><span class="sxs-lookup"><span data-stu-id="a9135-164">The value 0.1 indicates a cropping of 10 percent from the edge, The value 0.15 indicates a cropping of 15 percent from the edge, and so on.</span></span>

<span data-ttu-id="a9135-165">Per visualizzare, ad esempio, cinque immagini ritagliate dallo stesso file di immagine, è possibile usare l' `<image>` elemento e specificare valori di ritaglio diversi, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9135-165">For example, to display five pictures that are all cropped from the same image file, you can use the `<image>` element and specify different crop values, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image1 (1969 byte)](images/image1-2.jpg)![\-3.jpg image1 (1148 byte)](images/image1-3.jpg)![\-4.jpg image1 (1686 byte)](images/image1-4.jpg)![\-5.jpg image1 (1364 byte)](images/image1-5.jpg)


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





<span data-ttu-id="a9135-171">La prima immagine, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` , non ha alcun valore di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a9135-171">The first image, `<v:image style='width:100pt;height:80pt' src="image1.jpg" />`, doesn't have any crop value.</span></span> <span data-ttu-id="a9135-172">Pertanto, il 100% dell'immagine originale viene visualizzato con una dimensione di 100 punti per 80 punti.</span><span class="sxs-lookup"><span data-stu-id="a9135-172">Therefore, 100 percent of the original image is displayed at a size of 100 points by 80 points.</span></span>

<span data-ttu-id="a9135-173">La seconda immagine, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>` , presenta alcuni valori di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a9135-173">The second image, `<v:image style='width:85pt;height:64pt' src="image1.jpg" cropbottom="0.2" cropright="0.15"/>`, has some crop values.</span></span> <span data-ttu-id="a9135-174">`cropbottom="0.2"` indica che il 20% dell'immagine verrà ritagliato dalla parte inferiore; `cropright="0.15"` indica che il 15% dell'immagine verrà ritagliato dal bordo destro.</span><span class="sxs-lookup"><span data-stu-id="a9135-174">`cropbottom="0.2"` indicates that 20 percent of the picture will be cropped from the bottom; `cropright="0.15"` indicates that 15 percent of the picture will be cropped from the right edge.</span></span> <span data-ttu-id="a9135-175">L'immagine rimanente viene quindi visualizzata con una dimensione di 85 punti per 64 punti.</span><span class="sxs-lookup"><span data-stu-id="a9135-175">The remaining picture is then displayed at a size of 85 points by 64 points.</span></span>

<span data-ttu-id="a9135-176">Analogamente, le immagini terzo, quarto e quinto hanno alcuni valori di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a9135-176">Similarly the third, fourth, and fifth images have some crop values.</span></span> <span data-ttu-id="a9135-177">L'immagine originale viene ritagliata in base ai valori di ritaglio e viene quindi visualizzata in base al valore della larghezza e dell'altezza.</span><span class="sxs-lookup"><span data-stu-id="a9135-177">The original picture is cropped according to the crop values, and is then displayed according to the value of width and height.</span></span>

<span data-ttu-id="a9135-178">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="a9135-178">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="contrast"></a><span data-ttu-id="a9135-179">elevato</span><span class="sxs-lookup"><span data-stu-id="a9135-179">contrast</span></span>

<span data-ttu-id="a9135-180">È possibile usare l'attributo della proprietà **Gain** dell' `<image>` elemento per visualizzare varie immagini con diverse impostazioni di contrasto.</span><span class="sxs-lookup"><span data-stu-id="a9135-180">You can use the **gain** property attribute of the `<image>` element to display various pictures that have different contrast settings.</span></span>

<span data-ttu-id="a9135-181">Il valore dell'attributo della proprietà **Gain** può essere qualsiasi numero.</span><span class="sxs-lookup"><span data-stu-id="a9135-181">The value of the **gain** property attribute can be any number.</span></span> <span data-ttu-id="a9135-182">Per impostazione predefinita, il valore è 1, che indica l'uso dello stesso contrasto dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="a9135-182">By default, the value is 1, indicating the use of the same contrast as the original image.</span></span> <span data-ttu-id="a9135-183">Il valore 0 indica nessun contrasto.</span><span class="sxs-lookup"><span data-stu-id="a9135-183">The value 0 indicates no contrast.</span></span> <span data-ttu-id="a9135-184">Maggiore è il numero, maggiore è il contrasto.</span><span class="sxs-lookup"><span data-stu-id="a9135-184">The larger the number, the higher the contrast.</span></span>

<span data-ttu-id="a9135-185">Ad esempio, per visualizzare cinque immagini con impostazioni di contrasto diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso per l'attributo **Gain** Property, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9135-185">For example, to display five pictures that have different contrast settings, you can use the `<image>` element and set a different value for the **gain** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg Image2 (270 byte)](images/image2-2.jpg)![\-3.jpg Image2 (1919 byte)](images/image2-3.jpg)![\-4.jpg Image2 (3143 byte)](images/image2-4.jpg)![\-5.jpg Image2 (1724 byte)](images/image2-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=0.5 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=3 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gain=-0.4 />
```





<span data-ttu-id="a9135-191">Quando l'attributo **Gain** Property è impostato su 0, l'intera immagine diventa grigio perché non esiste alcun contrasto.</span><span class="sxs-lookup"><span data-stu-id="a9135-191">When the **gain** property attribute is set to 0, the entire image becomes gray because there is no contrast.</span></span> <span data-ttu-id="a9135-192">Il contrasto è più evidente quando l'attributo della proprietà **Gain** è impostato su 3 rispetto a quando è impostato su 0,5.</span><span class="sxs-lookup"><span data-stu-id="a9135-192">The contrast is more noticeable when the **gain** property attribute is set to 3 than when it is set to 0.5.</span></span> <span data-ttu-id="a9135-193">Il contrasto viene invertito quando l'attributo della proprietà **Gain** è impostato su un valore negativo, ad esempio-0,4.</span><span class="sxs-lookup"><span data-stu-id="a9135-193">The contrast is reversed when the **gain** property attribute is set to a negative value such as -0.4.</span></span>

<span data-ttu-id="a9135-194">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="a9135-194">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="brightness"></a><span data-ttu-id="a9135-195">luminosità</span><span class="sxs-lookup"><span data-stu-id="a9135-195">brightness</span></span>

<span data-ttu-id="a9135-196">È possibile usare l'attributo della proprietà **blacklevel** dell' `<image>` elemento per visualizzare varie immagini con impostazioni di luminosità diverse.</span><span class="sxs-lookup"><span data-stu-id="a9135-196">You can use the **blacklevel** property attribute of the `<image>` element to display various pictures that have different brightness settings.</span></span>

<span data-ttu-id="a9135-197">Il valore dell'attributo della proprietà **blacklevel** può essere qualsiasi valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="a9135-197">The value of the **blacklevel** property attribute can be any value between 0 to 1.</span></span> <span data-ttu-id="a9135-198">Per impostazione predefinita, il valore è 0, che indica che il livello di luminosità nell'immagine originale viene mantenuto.</span><span class="sxs-lookup"><span data-stu-id="a9135-198">By default, the value is 0, indicating that the level of brightness in the original image is preserved.</span></span> <span data-ttu-id="a9135-199">Il valore 1 indica il livello massimo di luminosità.</span><span class="sxs-lookup"><span data-stu-id="a9135-199">The value 1 indicates the highest level of brightness.</span></span>

<span data-ttu-id="a9135-200">Ad esempio, per visualizzare cinque immagini con impostazioni di luminosità diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso per l'attributo della proprietà **blacklevel** , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9135-200">For example, to display five pictures that have different brightness settings, you can use the `<image>` element and set a different value for the **blacklevel** property attribute, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image3 (2579 byte)](images/image3-2.jpg)![\-3.jpg image3 (2330 byte)](images/image3-3.jpg)![\-4.jpg image3 (2727 byte)](images/image3-4.jpg)![\-5.jpg image3 (2435 byte)](images/image3-5.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.1 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=0.2 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.05 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" blacklevel=-0.15 />
```





<span data-ttu-id="a9135-206">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="a9135-206">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="grayscale"></a><span data-ttu-id="a9135-207">scala di grigi</span><span class="sxs-lookup"><span data-stu-id="a9135-207">grayscale</span></span>

<span data-ttu-id="a9135-208">È possibile usare l'attributo della proprietà **scala di grigi** dell' `<image>` elemento per visualizzare immagini con o senza scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="a9135-208">You can use the **grayscale** property attribute of the `<image>` element to display pictures with or without grayscale.</span></span>

<span data-ttu-id="a9135-209">Il valore dell'attributo della proprietà **scala di grigi** può essere true o false.</span><span class="sxs-lookup"><span data-stu-id="a9135-209">The value of the **grayscale** property attribute can be either true or false.</span></span> <span data-ttu-id="a9135-210">Per impostazione predefinita, il valore è impostato su false in modo che l'immagine venga visualizzata in colore.</span><span class="sxs-lookup"><span data-stu-id="a9135-210">By default, the value is set to false so that the image will be displayed in color.</span></span> <span data-ttu-id="a9135-211">Se il valore è impostato su true, l'immagine verrà visualizzata in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="a9135-211">If the value is set to true, the image will be displayed in grayscale.</span></span>

<span data-ttu-id="a9135-212">Come illustrato nell'immagine seguente, ad esempio, la prima immagine usa l'impostazione predefinita (false) dell'attributo di scala di grigi ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span><span class="sxs-lookup"><span data-stu-id="a9135-212">For example, as shown in the following picture, the first image uses the default setting (false)of the grayscale attribute (`<v:image style='width:100pt;height:80pt' src="image1.jpg" />` ).</span></span> <span data-ttu-id="a9135-213">Pertanto, l'immagine viene visualizzata in colore.</span><span class="sxs-lookup"><span data-stu-id="a9135-213">Therefore, the picture is displayed in color.</span></span>

<span data-ttu-id="a9135-214">La seconda immagine imposta l'attributo scala di grigi su true ( `<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span><span class="sxs-lookup"><span data-stu-id="a9135-214">The second image sets the grayscale attribute to true (`<v:image style='width:100pt;height:80pt' src="image1.jpg" grayscale=true />` ).</span></span> <span data-ttu-id="a9135-215">Pertanto, l'immagine viene visualizzata in scala di grigi, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9135-215">Therefore, the picture is displayed in grayscale, as shown in the following VML representation:</span></span>

![image1.jpg (5770 byte)](images/image1.jpg)![\-2.jpg image4 (2138 byte)](images/image4-2.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg"
grayscale=true />
```





<span data-ttu-id="a9135-218">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="a9135-218">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="gamma"></a><span data-ttu-id="a9135-219">gamma</span><span class="sxs-lookup"><span data-stu-id="a9135-219">gamma</span></span>

<span data-ttu-id="a9135-220">È possibile usare l'attributo di proprietà **gamma** dell' `<image>` elemento per visualizzare immagini con impostazioni gamma diverse.</span><span class="sxs-lookup"><span data-stu-id="a9135-220">You can use the **gamma** property attribute of the `<image>` element to display pictures that have different gamma settings.</span></span>

<span data-ttu-id="a9135-221">Il valore dell'attributo della proprietà gamma può essere qualsiasi valore compreso tra 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="a9135-221">The value of the gamma property attribute can be any value between 0 and 1.</span></span> <span data-ttu-id="a9135-222">Per impostazione predefinita, il valore è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="a9135-222">By default, the value is set to 1.</span></span>

<span data-ttu-id="a9135-223">Per visualizzare, ad esempio, tre immagini con impostazioni gamma diverse, è possibile usare l' `<image>` elemento e impostare un valore diverso dell'attributo della proprietà **gamma** , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a9135-223">For example, to display three pictures that have different gamma settings, you can use the `<image>` element and set a different value of the **gamma** property attribute, as shown in the following VML representation:</span></span>

![\-1.jpg image5 (2714 byte)](images/image5-1.jpg)![\-2.jpg image5 (2729 byte)](images/image5-2.jpg)![\-3.jpg image5 (2726 byte)](images/image5-3.jpg)


```HTML
<v:image style='width:100pt;height:80pt' src="image1.jpg" />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0 />
<v:image style='width:100pt;height:80pt' src="image1.jpg" gamma=0.5 />
```





<span data-ttu-id="a9135-227">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span><span class="sxs-lookup"><span data-stu-id="a9135-227">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858408) .</span></span>

 

 