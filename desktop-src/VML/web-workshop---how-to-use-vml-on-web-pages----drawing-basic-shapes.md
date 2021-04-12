---
title: Disegno di forme di base
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web Workshop, disegno di forme
- progettazione di pagine Web, disegno di forme
- Vector Markup Language (la), disegno di forme
- LA (Vector Markup Language), disegno di forme
- grafica vettoriale, forme disegno
- disegno di forme
- LA forme, disegno
- Vector Markup Language (la), XML
- LA (Vector Markup Language), XML
- grafica vettoriale, XML
- Vector Markup Language (la), CSS2
- LA (Vector Markup Language), CSS2
- grafica vettoriale, CSS2
- Vector Markup Language (la), elementi
- LA (Vector Markup Language), elementi
- grafica vettoriale, elementi
- Elementi la, disegno di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474011"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="49028-121">Disegno di forme di base</span><span class="sxs-lookup"><span data-stu-id="49028-121">Drawing Basic Shapes</span></span>

<span data-ttu-id="49028-122">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="49028-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="49028-123">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="49028-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="49028-124">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="49028-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="49028-125">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="49028-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="49028-126">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="49028-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="49028-127">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="49028-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="49028-128">In questo argomento verrà illustrato quanto sia facile disegnare una forma usando la.</span><span class="sxs-lookup"><span data-stu-id="49028-128">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="49028-129">Per creare un Oval rosso in una pagina Web, come illustrato nell'immagine seguente, è possibile disegnare l'ovale usando uno strumento di modifica grafico, salvare il disegno come bitmap e quindi inserire la bitmap nella pagina Web:</span><span class="sxs-lookup"><span data-stu-id="49028-129">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 byte)](images/oval1.gif)

<span data-ttu-id="49028-131">In alternativa, è possibile usare la per creare grafica.</span><span class="sxs-lookup"><span data-stu-id="49028-131">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="49028-132">Nell'esempio precedente, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web per creare l'ovale rosso:</span><span class="sxs-lookup"><span data-stu-id="49028-132">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="49028-133">`<v:...>` e `</v:...>` sono i tag di inizio e di fine nella [sintassi XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="49028-133">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="49028-134">fornisce [informazioni CSS](#css-information).</span><span class="sxs-lookup"><span data-stu-id="49028-134">provides [CSS information](#css-information).</span></span> <span data-ttu-id="49028-135">**Oval** e **FillColor**= "Red" sono [elementi la](#vml-elements).</span><span class="sxs-lookup"><span data-stu-id="49028-135">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="49028-136">È possibile modificare la grafica semplicemente modificando gli attributi delle proprietà in la.</span><span class="sxs-lookup"><span data-stu-id="49028-136">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="49028-137">Nell'esempio precedente, se si passa `fillcolor="red"` a `fillcolor="blue"` , come illustrato nella seguente rappresentazione la, il rosso ovale cambierà in blu:</span><span class="sxs-lookup"><span data-stu-id="49028-137">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="49028-138">I browser che supportano la possono eseguire il rendering e la visualizzazione della grafica rappresentata in la senza dover scaricare file di immagine separati.</span><span class="sxs-lookup"><span data-stu-id="49028-138">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="49028-139">La maggior parte degli elementi grafici rappresentati in la viene sottoposta a rendering più velocemente nei browser e richiedono meno spazio su disco e tempi di download</span><span class="sxs-lookup"><span data-stu-id="49028-139">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="49028-140">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="49028-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="49028-141">Struttura XML</span><span class="sxs-lookup"><span data-stu-id="49028-141">XML Structure</span></span>

<span data-ttu-id="49028-142">LA viene formattato in base alle regole di Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="49028-142">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="49028-143">Qualsiasi parser XML standard può analizzare la e passare i dati risultanti a un processore specifico di la.</span><span class="sxs-lookup"><span data-stu-id="49028-143">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="49028-144">Per fare in modo che i browser sappiano come passare i dati a un processore specifico di la, è necessario digitare alcune informazioni, ad esempio [spazi dei nomi](web-workshop---how-to-use-vml-on-web-pages----appendix.md) e [oggetti personalizzati incorporati](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span><span class="sxs-lookup"><span data-stu-id="49028-144">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="49028-145">È quindi possibile usare la per digitare elementi grafici nell' `<BODY>` area così come è stato fatto nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="49028-145">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="49028-146">Il `"v:"` prefisso in ogni tag XML identifica il tag come la.</span><span class="sxs-lookup"><span data-stu-id="49028-146">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="49028-147">Il `"v:"` prefisso nell' `<BODY>` area deve essere coerente con `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="49028-147">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="49028-148">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="49028-148">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="49028-149">Informazioni CSS</span><span class="sxs-lookup"><span data-stu-id="49028-149">CSS Information</span></span>

<span data-ttu-id="49028-150">LA utilizza [Cascading Style Sheets, livello 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) per determinare le dimensioni della grafica e per posizionare la grafica in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="49028-150">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="49028-151">Nell'esempio precedente è stata specificata la dimensione dell'ovale come 100 punti (larghezza) per 75 punti (altezza) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="49028-151">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="49028-152">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="49028-152">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="49028-153">Elementi la</span><span class="sxs-lookup"><span data-stu-id="49028-153">VML Elements</span></span>

<span data-ttu-id="49028-154">Nell'esempio precedente è stato usato un elemento predefinito la `<oval>` per creare un Oval.</span><span class="sxs-lookup"><span data-stu-id="49028-154">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="49028-155">È stato quindi usato l'attributo della proprietà **FillColor** dell' `<oval>` elemento per riempire l'ovale con il rosso.</span><span class="sxs-lookup"><span data-stu-id="49028-155">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="49028-156">In base ai tag di [inizio, tag finali e tag Empty-Element](https://www.w3.org/TR/REC-xml#sec-starttags) della [specifica XML 1,0](https://www.w3.org/TR/REC-xml), i tag degli elementi vuoti possono essere usati per qualsiasi elemento senza contenuto.</span><span class="sxs-lookup"><span data-stu-id="49028-156">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="49028-157">Ad esempio, come illustrato nella seguente rappresentazione la, non è presente alcun contenuto (sottoelemento) nell' `<oval>` elemento.</span><span class="sxs-lookup"><span data-stu-id="49028-157">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="49028-158">(Si noti che lo **stile** e **FillColor** sono gli attributi dell' `<oval>` elemento, non sono sottoelementi).</span><span class="sxs-lookup"><span data-stu-id="49028-158">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="49028-159">Pertanto, è possibile utilizzare il tag elemento vuoto, come illustrato nella seguente rappresentazione la, per rappresentare lo stesso elemento della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="49028-159">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="49028-160">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="49028-160">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="49028-161">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="49028-161">Summary</span></span>

<span data-ttu-id="49028-162">È possibile usare la per creare elementi grafici in una pagina Web e quindi personalizzare tali elementi semplicemente modificando gli attributi delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="49028-162">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="49028-163">Inoltre, la maggior parte dei grafici rappresentati in la viene sottoposta a rendering più velocemente nei browser e non è più tempo di download e spazio su disco</span><span class="sxs-lookup"><span data-stu-id="49028-163">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 