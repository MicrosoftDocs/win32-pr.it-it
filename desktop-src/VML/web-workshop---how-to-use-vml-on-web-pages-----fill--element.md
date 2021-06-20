---
title: Uso dell'elemento Fill
description: Questo articolo descrive l'uso dell'elemento Fill di VML, una funzionalità deprecata a Internet Explorer 9 di Windows.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web workshop, elemento fill
- progettazione di pagine Web, elemento fill
- Vector Markup Language (VML), elemento fill
- VML (Vector Markup Language),elemento fill
- grafica vettoriale, elemento fill
- elemento fill
- elementi VML, riempimento
- Forme VML, elemento fill
- Vector Markup Language (VML), riempimento sfumato
- VML (Vector Markup Language),riempimento sfumato
- grafica vettoriale, riempimento sfumato
- Forme VML, riempimento sfumato
- Forme con riempimento sfumato
- Vector Markup Language (VML), riempimento a motivo
- VML (Vector Markup Language),riempimento a motivo
- grafica vettoriale, riempimento a motivo
- Forme VML, riempimento a motivo
- forme con riempimento a motivo
- Vector Markup Language (VML), riempimento immagine
- VML (Vector Markup Language),riempimento immagine
- grafica vettoriale, riempimento immagine
- Forme VML, riempimento immagine
- Forme con riempimento a immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb243e4896443fd36a1b22c2ac3a0ab0bedfb2b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407794"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="ea993-126">Uso dell'elemento Fill</span><span class="sxs-lookup"><span data-stu-id="ea993-126">Using the Fill Element</span></span>

<span data-ttu-id="ea993-127">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer 9 di Windows.</span><span class="sxs-lookup"><span data-stu-id="ea993-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ea993-128">È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ea993-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ea993-129">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ea993-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ea993-130">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="ea993-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ea993-131">Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ea993-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ea993-132">Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ea993-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ea993-133">Come si è appreso, è possibile usare l'attributo della proprietà **fillcolor** di un elemento forma predefinito, ad esempio , , , , , per specificare il colore usato per riempire `<oval>` la `<line>` `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` forma.</span><span class="sxs-lookup"><span data-stu-id="ea993-133">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="ea993-134">In questo argomento verrà illustrato come disegnare una forma riempita con effetti più avanzati.</span><span class="sxs-lookup"><span data-stu-id="ea993-134">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="ea993-135">È possibile inserire il sotto-elemento all'interno di , o o qualsiasi elemento di forma predefinito per descrivere `<fill>` `<shape>` come riempire la `<shapetype>` forma.</span><span class="sxs-lookup"><span data-stu-id="ea993-135">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="ea993-136">È quindi possibile usare gli attributi della proprietà del sotto-elemento per personalizzare l'effetto di riempimento, ad esempio il riempimento sfumato, il riempimento a `<fill>` [motivi,](#pattern-fill)il [riempimento immagine.](#picture-fill) [](#gradient-fill)</span><span class="sxs-lookup"><span data-stu-id="ea993-136">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="ea993-137">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="ea993-137">In this topic:</span></span>

-   [<span data-ttu-id="ea993-138">Riempimento sfumato</span><span class="sxs-lookup"><span data-stu-id="ea993-138">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="ea993-139">Riempimento a motivo</span><span class="sxs-lookup"><span data-stu-id="ea993-139">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="ea993-140">Riempimento immagine</span><span class="sxs-lookup"><span data-stu-id="ea993-140">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="ea993-141">Riempimento sfumato</span><span class="sxs-lookup"><span data-stu-id="ea993-141">Gradient Fill</span></span>

<span data-ttu-id="ea993-142">Per disegnare una forma con riempimento sfumato, è possibile impostare l'attributo della proprietà type del sotto-elemento su "gradient" o  `<fill>` "gradientRadial" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio `<fill>` **method**, **color2**, **focus** e **angle**.</span><span class="sxs-lookup"><span data-stu-id="ea993-142">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="ea993-143">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="ea993-143">**Examples:**</span></span>

<span data-ttu-id="ea993-144">Per creare una forma con riempimento sfumato  orizzontalmente, è possibile impostare l'attributo della proprietà type su "gradient", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-144">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 byte)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="ea993-146">Se si modifica **l'attributo della** proprietà fillcolor della forma, la forma viene riempita con una sfumatura con un colore diverso.</span><span class="sxs-lookup"><span data-stu-id="ea993-146">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="ea993-147">È possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sotto-elemento.</span><span class="sxs-lookup"><span data-stu-id="ea993-147">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="ea993-148">Ad esempio, per creare una forma con riempimento sfumato in due colori, è possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del sotto-elemento, come illustrato nella rappresentazione `<fill>` VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-148">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 byte)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="ea993-150">È possibile impostare **l'attributo** della proprietà del metodo su "linear" o "sigma" o "any" o "none".</span><span class="sxs-lookup"><span data-stu-id="ea993-150">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="ea993-151">L'effetto della sfumatura è leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="ea993-151">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="ea993-152">È anche possibile usare l'attributo della proprietà **angle,\*\*\*\*focus,\*\*\*\*focussize** o **focusposition** per modificare il modo in cui va la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="ea993-152">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="ea993-153">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="ea993-153">**Examples:**</span></span>

 

<span data-ttu-id="ea993-154">Per creare una forma con riempimento sfumato verticalmente, è possibile impostare l'attributo della proprietà angle su angle="-90", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-154">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 byte)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="ea993-156">Per creare una forma con riempimento sfumato dalla diagonale verso l'alto, è possibile impostare l'attributo della proprietà **angle** su angle="-135", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-156">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 byte)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="ea993-158">Per creare una forma con riempimento sfumato dalla diagonale verso il basso, è possibile impostare l'attributo della proprietà **angle** su angle="-45", come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-158">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 byte)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="ea993-160">Per creare una forma con riempimento sfumato dal centro, è possibile specificare `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-160">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 byte)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="ea993-162">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ea993-162">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="ea993-163">Riempimento a motivo</span><span class="sxs-lookup"><span data-stu-id="ea993-163">Pattern Fill</span></span>

<span data-ttu-id="ea993-164">Per disegnare una forma con riempimento a  motivo, è possibile impostare l'attributo della proprietà type del sotto-elemento su "pattern" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio src e `<fill>` `<fill>` **color2.** </span><span class="sxs-lookup"><span data-stu-id="ea993-164">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="ea993-165">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="ea993-165">**Examples:**</span></span>

<span data-ttu-id="ea993-166">Per creare una forma riempita con un'immagine  modello, è possibile specificare l'attributo della proprietà type su "pattern" e puntare l'attributo della proprietà **src** alla posizione del file di immagine del modello, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-166">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 byte)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="ea993-168">Se si punta l'attributo della proprietà **src** a un file di criteri diverso, è possibile creare una forma riempita con un modello diverso.</span><span class="sxs-lookup"><span data-stu-id="ea993-168">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="ea993-169">È anche possibile modificare il colore specificando un valore diverso per l'attributo della proprietà **fillcolor** o **color2,** come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-169">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="ea993-171">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="ea993-171">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="ea993-172">Riempimento immagine</span><span class="sxs-lookup"><span data-stu-id="ea993-172">Picture Fill</span></span>

<span data-ttu-id="ea993-173">Per disegnare una forma con riempimento a  immagine, è possibile impostare l'attributo della proprietà type del sotto-elemento su "frame" e quindi specificare altri attributi di proprietà del sotto-elemento, ad esempio src e `<fill>` `<fill>` **color2.** </span><span class="sxs-lookup"><span data-stu-id="ea993-173">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="ea993-174">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="ea993-174">**Examples:**</span></span>

<span data-ttu-id="ea993-175">Per creare una forma riempita con un file  di immagine, è possibile specificare l'attributo della proprietà type su "frame" e quindi puntare l'attributo della proprietà **src** al percorso del file di immagine, come illustrato nella rappresentazione VML seguente:</span><span class="sxs-lookup"><span data-stu-id="ea993-175">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 byte)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="ea993-177">È possibile creare facilmente una forma riempita con un'immagine diversa puntando l'attributo della proprietà **src** a un altro file.</span><span class="sxs-lookup"><span data-stu-id="ea993-177">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="ea993-178">Per altre informazioni su questo elemento, vedere la specifica [VML](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="ea993-178">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 