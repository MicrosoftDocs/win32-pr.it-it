---
title: Disegno di forme di base
description: Questo articolo descrive il disegno di forme di base in VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- Web workshop, disegno di forme
- progettazione di pagine Web, disegno di forme
- Vector Markup Language (VML), disegno di forme
- VML (Vector Markup Language),disegno di forme
- grafica vettoriale, disegno di forme
- disegno di forme
- forme VML, disegno
- Vector Markup Language (VML),XML
- VML (Vector Markup Language),XML
- grafica vettoriale,XML
- Vector Markup Language (VML),CSS2
- VML (Vector Markup Language),CSS2
- grafica vettoriale,CSS2
- Vector Markup Language (VML), elementi
- VML (Vector Markup Language),elements
- grafica vettoriale, elementi
- elementi VML, disegno di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00701e8ac77bd5bda7156c04ca25427d131646bf
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407734"
---
# <a name="drawing-basic-shapes"></a><span data-ttu-id="ac415-120">Disegno di forme di base</span><span class="sxs-lookup"><span data-stu-id="ac415-120">Drawing Basic Shapes</span></span>

<span data-ttu-id="ac415-121">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows.</span><span class="sxs-lookup"><span data-stu-id="ac415-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ac415-122">È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ac415-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ac415-123">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ac415-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ac415-124">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="ac415-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ac415-125">Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ac415-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ac415-126">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ac415-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ac415-127">In questo argomento verrà illustrato quanto sia semplice disegnare una forma usando VML.</span><span class="sxs-lookup"><span data-stu-id="ac415-127">In this topic, we will illustrate how easy it is to draw a shape using VML.</span></span>

<span data-ttu-id="ac415-128">Per creare un ovale rosso in una pagina Web, come illustrato nell'immagine seguente, è possibile disegnare l'ovale usando uno strumento di modifica grafica, salvare il disegno come bitmap e quindi inserire la bitmap nella pagina Web:</span><span class="sxs-lookup"><span data-stu-id="ac415-128">To create a red oval on a Web page, as shown in the following picture, you can draw the oval by using a graphic edit tool, save your drawing as a bitmap, and then insert the bitmap on your Web page:</span></span>

![oval1.gif (627 byte)](images/oval1.gif)

<span data-ttu-id="ac415-130">In alternativa, è possibile usare VML per disegnare grafica.</span><span class="sxs-lookup"><span data-stu-id="ac415-130">Alternatively, you can use VML to draw graphics.</span></span> <span data-ttu-id="ac415-131">Nell'esempio precedente è possibile digitare le righe seguenti nell'area della pagina Web per `<BODY>` disegnare l'ovale rosso:</span><span class="sxs-lookup"><span data-stu-id="ac415-131">In the preceding example, you can type the following lines in the `<BODY>` region of your Web page to draw the red oval:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





<span data-ttu-id="ac415-132">`<v:...>` e `</v:...>` sono il tag di inizio e il tag di fine nella [sintassi XML](#xml-structure).`style='width:100pt; height:75pt'`</span><span class="sxs-lookup"><span data-stu-id="ac415-132">`<v:...>` and `</v:...>` are the start tag and end tag in [XML syntax](#xml-structure).`style='width:100pt; height:75pt'`</span></span> <span data-ttu-id="ac415-133">fornisce [informazioni CSS.](#css-information)</span><span class="sxs-lookup"><span data-stu-id="ac415-133">provides [CSS information](#css-information).</span></span> <span data-ttu-id="ac415-134">**oval** e **fillcolor**="red" sono [elementi VML.](#vml-elements)</span><span class="sxs-lookup"><span data-stu-id="ac415-134">**oval** and **fillcolor**="red" are [VML elements](#vml-elements).</span></span>

<span data-ttu-id="ac415-135">È possibile modificare la grafica modificando semplicemente gli attributi delle proprietà in VML.</span><span class="sxs-lookup"><span data-stu-id="ac415-135">You can alter the graphics by simply changing their property attributes in VML.</span></span> <span data-ttu-id="ac415-136">Nell'esempio precedente, se si modifica in , come illustrato nella rappresentazione `fillcolor="red"` `fillcolor="blue"` VML seguente, l'ovale rosso cambierà in blu:</span><span class="sxs-lookup"><span data-stu-id="ac415-136">In the preceding example, if you change `fillcolor="red"` to `fillcolor="blue"`, as shown in the following VML representation, the red oval will change to blue:</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





<span data-ttu-id="ac415-137">I browser che supportano VML possono eseguire il rendering e visualizzare la grafica rappresentata in VML senza dover scaricare file di immagine separati.</span><span class="sxs-lookup"><span data-stu-id="ac415-137">Browsers that support VML can render and display the graphics represented in VML without having to download separate image files.</span></span> <span data-ttu-id="ac415-138">La maggior parte della grafica rappresentata in VML viene visualizzata più velocemente nei browser e richiede meno spazio su disco e tempo di download.</span><span class="sxs-lookup"><span data-stu-id="ac415-138">Most graphics represented in VML are rendered faster in browsers, and require less disk space and download time.</span></span>

<span data-ttu-id="ac415-139">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ac415-139">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="xml-structure"></a><span data-ttu-id="ac415-140">Struttura XML</span><span class="sxs-lookup"><span data-stu-id="ac415-140">XML Structure</span></span>

<span data-ttu-id="ac415-141">VmL viene formattato in base alle regole di Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="ac415-141">VML is formatted according to the rules of Extensible Markup Language (XML).</span></span> <span data-ttu-id="ac415-142">Qualsiasi parser XML standard può analizzare VML e consegnare i dati risultanti a un processore specifico di VML.</span><span class="sxs-lookup"><span data-stu-id="ac415-142">Any standard XML parser can parse VML and hand off the resulting data to a VML-specific processor.</span></span> <span data-ttu-id="ac415-143">Per consentire ai browser di sapere come consegnare i dati a un processore [](web-workshop---how-to-use-vml-on-web-pages----appendix.md) specifico di VML, è necessario digitare alcune informazioni, ad esempio spazi dei nomi e [oggetti personalizzati incorporati.](web-workshop---how-to-use-vml-on-web-pages----appendix.md)</span><span class="sxs-lookup"><span data-stu-id="ac415-143">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as [namespaces](web-workshop---how-to-use-vml-on-web-pages----appendix.md) and [embedded custom objects](web-workshop---how-to-use-vml-on-web-pages----appendix.md).</span></span> <span data-ttu-id="ac415-144">È quindi possibile usare VML per digitare grafica nell'area esattamente `<BODY>` come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="ac415-144">You can then use VML to type graphics in the `<BODY>` region just as you did in the preceding example.</span></span>

<span data-ttu-id="ac415-145">Il `"v:"` prefisso in ogni tag XML identifica il tag come VML.</span><span class="sxs-lookup"><span data-stu-id="ac415-145">The `"v:"` prefix on each XML tag identifies the tag as VML.</span></span> <span data-ttu-id="ac415-146">Il `"v:"` prefisso `<BODY>` nell'area deve essere coerente con `<html xmlns:v="...">` .</span><span class="sxs-lookup"><span data-stu-id="ac415-146">The `"v:"` prefix in the `<BODY>` region should be consistent with `<html xmlns:v="...">`.</span></span>

<span data-ttu-id="ac415-147">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ac415-147">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="css-information"></a><span data-ttu-id="ac415-148">Informazioni CSS</span><span class="sxs-lookup"><span data-stu-id="ac415-148">CSS Information</span></span>

<span data-ttu-id="ac415-149">VML usa [Cascading Style Sheets livello 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) per determinare le dimensioni della grafica e per posizionare la grafica in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="ac415-149">VML uses [Cascading Style Sheets, Level 2 (CSS2)](https://www.w3.org/TR/PR-CSS2/) to determine the size of the graphics and to position the graphics on a Web page.</span></span> <span data-ttu-id="ac415-150">Nell'esempio precedente la dimensione dell'ovale è stata specificata come 100 punti (larghezza) per 75 punti (altezza) ( `style='width:100pt;height:75pt'` ).</span><span class="sxs-lookup"><span data-stu-id="ac415-150">In the preceding example, we specified the size of the oval as 100 points (width) by 75 points (height) (`style='width:100pt;height:75pt'` ).</span></span>

<span data-ttu-id="ac415-151">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ac415-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vml-elements"></a><span data-ttu-id="ac415-152">Elementi VML</span><span class="sxs-lookup"><span data-stu-id="ac415-152">VML Elements</span></span>

<span data-ttu-id="ac415-153">Nell'esempio precedente è stato usato un elemento predefinito VML `<oval>` per disegnare un ovale.</span><span class="sxs-lookup"><span data-stu-id="ac415-153">In the preceding example, we used a VML predefined `<oval>` element to draw an oval.</span></span> <span data-ttu-id="ac415-154">È stato quindi usato **l'attributo della** proprietà fillcolor dell'elemento `<oval>` per riempire l'ovale con rosso.</span><span class="sxs-lookup"><span data-stu-id="ac415-154">We then used the **fillcolor** property attribute of the `<oval>` element to fill the oval with red.</span></span>

<span data-ttu-id="ac415-155">In base alla sezione Tag di [inizio,](https://www.w3.org/TR/REC-xml#sec-starttags) Tag di fine e Tag Empty-Element della specifica [XML 1.0,](https://www.w3.org/TR/REC-xml)i tag di elemento vuoto possono essere usati per qualsiasi elemento senza contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac415-155">Based upon the [Start-Tags, End-Tags, and Empty-Element Tags](https://www.w3.org/TR/REC-xml#sec-starttags) section of [XML 1.0 specification](https://www.w3.org/TR/REC-xml), empty-element tags may be used for any element that has no content.</span></span> <span data-ttu-id="ac415-156">Ad esempio, come illustrato nella rappresentazione VML seguente, all'interno dell'elemento non è presente alcun contenuto `<oval>` (sotto-elemento).</span><span class="sxs-lookup"><span data-stu-id="ac415-156">For example, as shown in the following VML representation, there is no content (sub-element) within the `<oval>` element.</span></span> <span data-ttu-id="ac415-157">Si noti che **lo stile e** il colore di **riempimento** sono gli attributi `<oval>` dell'elemento, non sono elementi secondari.</span><span class="sxs-lookup"><span data-stu-id="ac415-157">(Note that the **style** and **fillcolor** are the attributes of the `<oval>` element; they are not sub-elements.)</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



<span data-ttu-id="ac415-158">È quindi possibile usare il tag empty-element, come illustrato nella rappresentazione VML seguente, per rappresentare la stessa cosa della riga precedente.</span><span class="sxs-lookup"><span data-stu-id="ac415-158">Therefore, you can use the empty-element tag, as shown in the following VML representation, to represent the same thing as the above line.</span></span>


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



<span data-ttu-id="ac415-159">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ac415-159">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="ac415-160">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="ac415-160">Summary</span></span>

<span data-ttu-id="ac415-161">È possibile usare VML per disegnare grafica in una pagina Web e quindi personalizzarne gli attributi modificando semplicemente gli attributi delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="ac415-161">You can use VML to draw graphics on a Web page, and then customize those graphics by simply changing their property attributes.</span></span> <span data-ttu-id="ac415-162">Inoltre, la maggior parte della grafica rappresentata in VML viene visualizzata più velocemente nei browser e richiede meno tempo di download e spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="ac415-162">Also, most graphics represented in VML are rendered faster in browsers, and take less download time and disk space.</span></span>

 

 