---
title: Uso dell'elemento Fill
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: ed36601d-2e90-412e-ac3f-58324fac300d
keywords:
- Web Workshop, elemento Fill
- progettazione di pagine Web, elemento Fill
- Vector Markup Language (la), elemento Fill
- LA (Vector Markup Language), elemento Fill
- grafica vettoriale, elemento Fill
- Fill (elemento)
- Elementi la, Fill
- Forme la, elemento Fill
- Vector Markup Language (la), riempimento sfumato
- LA (Vector Markup Language), riempimento sfumato
- grafica vettoriale, riempimento sfumato
- Forme la, riempimento sfumatura
- forme con riempimento sfumato
- Vector Markup Language (la), riempimento schema
- LA (Vector Markup Language), riempimento modello
- grafica vettoriale, riempimento schema
- Forme la, riempimento schema
- forme con riempimento di modelli
- Vector Markup Language (la), riempimento immagine
- LA (Vector Markup Language), riempimento immagine
- grafica vettoriale, riempimento immagine
- Forme la, riempimento immagine
- forme con riempimento immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf497a3120f53e24f1cff2bf7084469754bbaf7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104562668"
---
# <a name="using-the-fill-element"></a><span data-ttu-id="83fe0-127">Uso dell'elemento Fill</span><span class="sxs-lookup"><span data-stu-id="83fe0-127">Using the Fill Element</span></span>

<span data-ttu-id="83fe0-128">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="83fe0-128">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="83fe0-129">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="83fe0-129">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="83fe0-130">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="83fe0-130">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="83fe0-131">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="83fe0-131">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="83fe0-132">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="83fe0-132">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="83fe0-133">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="83fe0-133">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="83fe0-134">Come si è appreso, è possibile usare l'attributo della proprietà **FillColor** di un elemento Shape predefinito, ad esempio `<oval>` , `<line>` , `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` , `<arc>` --per specificare il colore usato per riempire la forma.</span><span class="sxs-lookup"><span data-stu-id="83fe0-134">As you've learned, you can use the **fillcolor** property attribute of a predefined shape element -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, `<arc>` -- to specify the color that is used to fill the shape.</span></span> <span data-ttu-id="83fe0-135">In questo argomento verrà illustrato come disegnare una forma riempita con effetti più avanzati.</span><span class="sxs-lookup"><span data-stu-id="83fe0-135">In this topic, we will illustrate how to draw a shape that is filled with more advanced effects.</span></span>

<span data-ttu-id="83fe0-136">È possibile inserire il `<fill>` sottoelemento all'interno dell' `<shape>` elemento della `<shapetype>` forma, o o di qualsiasi elemento della forma predefinito per descrivere la modalità di riempimento della forma.</span><span class="sxs-lookup"><span data-stu-id="83fe0-136">You can place the `<fill>` sub-element inside the `<shape>`, or `<shapetype>`, or any predefined shape element to describe how to fill the shape.</span></span> <span data-ttu-id="83fe0-137">È quindi possibile usare gli attributi di proprietà del `<fill>` sottoelemento per personalizzare l'effetto di riempimento, ad esempio [riempimento sfumato](#gradient-fill), [riempimento schema](#pattern-fill), riempimento [immagine](#picture-fill).</span><span class="sxs-lookup"><span data-stu-id="83fe0-137">You can then use the property attributes of the `<fill>` sub-element to customize the fill effect, such as [gradient fill](#gradient-fill), [pattern fill](#pattern-fill), [picture fill](#picture-fill).</span></span>

<span data-ttu-id="83fe0-138">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="83fe0-138">In this topic:</span></span>

-   [<span data-ttu-id="83fe0-139">Riempimento sfumatura</span><span class="sxs-lookup"><span data-stu-id="83fe0-139">Gradient Fill</span></span>](#gradient-fill)
-   [<span data-ttu-id="83fe0-140">Riempimento modello</span><span class="sxs-lookup"><span data-stu-id="83fe0-140">Pattern Fill</span></span>](#pattern-fill)
-   [<span data-ttu-id="83fe0-141">Riempimento immagine</span><span class="sxs-lookup"><span data-stu-id="83fe0-141">Picture Fill</span></span>](#picture-fill)

## <a name="gradient-fill"></a><span data-ttu-id="83fe0-142">Riempimento sfumatura</span><span class="sxs-lookup"><span data-stu-id="83fe0-142">Gradient Fill</span></span>

<span data-ttu-id="83fe0-143">Per disegnare una forma con riempimento sfumato, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "gradiente" o "gradientRadial", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **Method**, **color2**, **Focus** e **Angle**.</span><span class="sxs-lookup"><span data-stu-id="83fe0-143">To draw a gradient-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "gradient" or "gradientRadial", and then specify other property attributes of the `<fill>` sub-element, such as **method**, **color2**, **focus**, and **angle**.</span></span>

<span data-ttu-id="83fe0-144">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="83fe0-144">**Examples:**</span></span>

<span data-ttu-id="83fe0-145">Per creare una forma con riempimento sfumato orizzontalmente, è possibile impostare l'attributo della proprietà **Type** su "gradiente", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-145">To create a shape that is gradient-filled horizontally, you can set the **type** property attribute to "gradient", as shown in the following VML representation:</span></span>

![horizontal1.gif (3055 byte)](images/horizontal1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="gradient" />
</v:rect>
```




<span data-ttu-id="83fe0-147">Se si modifica l'attributo della proprietà **FillColor** della forma, la forma viene riempita con una sfumatura con un colore diverso.</span><span class="sxs-lookup"><span data-stu-id="83fe0-147">If you change the **fillcolor** property attribute of the shape, the shape is then gradient-filled with a different color.</span></span> <span data-ttu-id="83fe0-148">È possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sottoelemento.</span><span class="sxs-lookup"><span data-stu-id="83fe0-148">You can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element.</span></span> <span data-ttu-id="83fe0-149">Ad esempio, per creare una forma con riempimento sfumato in due colori, è possibile aggiungere un secondo colore specificando l'attributo della proprietà **color2** del `<fill>` sottoelemento, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-149">For example, to create a shape that is gradient-filled in two colors, you can add a second color by specifying the **color2** property attribute of the `<fill>` sub-element, as shown in the following VML representation:</span></span>

![horizontal2.gif (3127 byte)](images/horizontal2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill color2="blue" type="gradient" />
</v:rect>
```




<span data-ttu-id="83fe0-151">È possibile impostare l'attributo della proprietà del **Metodo** su "Linear" o "Sigma" o "any" o "None".</span><span class="sxs-lookup"><span data-stu-id="83fe0-151">You can set the **method** property attribute to "linear" or "sigma" or "any" or "none".</span></span> <span data-ttu-id="83fe0-152">L'effetto della sfumatura è leggermente diverso.</span><span class="sxs-lookup"><span data-stu-id="83fe0-152">The effect of the gradient is slightly different.</span></span> <span data-ttu-id="83fe0-153">Inoltre, è possibile utilizzare l'attributo della proprietà **Angle**,**Focus**,**focussize** o **focusposition** per modificare il modo in cui la sfumatura diventa.</span><span class="sxs-lookup"><span data-stu-id="83fe0-153">Also, you can use the **angle**,**focus**,**focussize**, or **focusposition** property attribute to change how the gradient goes.</span></span>

<span data-ttu-id="83fe0-154">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="83fe0-154">**Examples:**</span></span>

 

<span data-ttu-id="83fe0-155">Per creare una forma con riempimento sfumato verticalmente, è possibile impostare l'attributo della proprietà Angle su Angle = "-90", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-155">To create a shape that is gradient-filled vertically, you can set the angle property attribute to angle="-90", as shown in the following VML representation:</span></span>

![vertical1.gif (3836 byte)](images/vertical1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-90"
type="gradient" />
</v:rect>
```




<span data-ttu-id="83fe0-157">Per creare una forma con riempimento sfumato dalla diagonale verso l'alto, è possibile impostare l'attributo della proprietà **Angle** su Angle = "-135", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-157">To create a shape that is gradient-filled from diagonal moving up, you can set the **angle** property attribute to angle="-135", as shown in the following VML representation:</span></span>

![dialgonalup1.gif (5816 byte)](images/dialgonalup1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-135"
type="gradient" />
</v:rect>
```




<span data-ttu-id="83fe0-159">Per creare una forma con riempimento sfumato dalla diagonale verso il basso, è possibile impostare l'attributo della proprietà **Angle** su Angle = "-45", come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-159">To create a shape that is gradient-filled from diagonal moving down, you can set the **angle** property attribute to angle="-45", as shown in the following VML representation:</span></span>

![diagonaldown1.gif (5753 byte)](images/diagonaldown1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
type="gradient" />
</v:rect>
```




<span data-ttu-id="83fe0-161">Per creare una forma con riempimento sfumato dal centro, è possibile specificare `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"` , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-161">To create a shape that is gradient-filled from the center, you can specify `angle="-45" focus="100%" focusposition=".5, .5" focussize="0, 0" type="gradientRadial"`, as shown in the following VML representation:</span></span>

![fromcenter1.gif (4598 byte)](images/fromcenter1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill method="linear sigma" angle="-45"
focus="100%" focusposition=".5,.5" focussize="0,0"
type="gradientRadial" />
</v:rect>
```




<span data-ttu-id="83fe0-163">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="83fe0-163">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="pattern-fill"></a><span data-ttu-id="83fe0-164">Riempimento modello</span><span class="sxs-lookup"><span data-stu-id="83fe0-164">Pattern Fill</span></span>

<span data-ttu-id="83fe0-165">Per disegnare una forma con riempimento a modelli, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "pattern", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="83fe0-165">To draw a pattern-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "pattern", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="83fe0-166">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="83fe0-166">**Examples:**</span></span>

<span data-ttu-id="83fe0-167">Per creare una forma riempita con un'immagine del modello, è possibile specificare l'attributo della proprietà **Type** su "pattern" e puntare l'attributo della proprietà **src** al percorso del file di immagine del modello, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-167">To create a shape that is filled with a pattern image, you can specify the **type** property attribute to "pattern", and point the **src** property attribute to the location of the pattern image file, as shown in the following VML representation:</span></span>

![pattern1.gif (872 byte)](images/pattern1.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="red">
<v:fill type="pattern" src="image1.gif"/>
</v:rect>
```




<span data-ttu-id="83fe0-169">Se si punta l'attributo della proprietà **src** a un file di modello diverso, è possibile creare una forma con un modello diverso.</span><span class="sxs-lookup"><span data-stu-id="83fe0-169">If you point the **src** property attribute to a different pattern file, you can create a shape that is filled with a different pattern.</span></span> <span data-ttu-id="83fe0-170">Inoltre, è possibile modificare il colore specificando un valore diverso per l'attributo della proprietà **FillColor** o **color2** , come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-170">Also, you can change the color by specifying a different value for the **fillcolor** or **color2** property attribute, as shown in the following VML representation:</span></span>

![pattern2.gif (831 byte)](images/pattern2.gif)


```HTML
<v:rect style='width:120pt;height:80pt' fillcolor="white">
<v:fill type="pattern" src="image2.gif"
color2="blue" />
</v:rect>
```




<span data-ttu-id="83fe0-172">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="83fe0-172">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="picture-fill"></a><span data-ttu-id="83fe0-173">Riempimento immagine</span><span class="sxs-lookup"><span data-stu-id="83fe0-173">Picture Fill</span></span>

<span data-ttu-id="83fe0-174">Per disegnare una forma con riempimento immagine, è possibile impostare l'attributo della proprietà **Type** del `<fill>` sottoelemento su "frame", quindi specificare altri attributi di proprietà del `<fill>` sottoelemento, ad esempio **src** e **color2**.</span><span class="sxs-lookup"><span data-stu-id="83fe0-174">To draw a picture-filled shape, you can set the **type** property attribute of the `<fill>` sub-element to "frame", and then specify other property attributes of the `<fill>` sub-element, such as **src** and **color2**.</span></span>

<span data-ttu-id="83fe0-175">**Esempi:**</span><span class="sxs-lookup"><span data-stu-id="83fe0-175">**Examples:**</span></span>

<span data-ttu-id="83fe0-176">Per creare una forma compilata con un file di immagine, è possibile specificare l'attributo della proprietà **Type** su "frame", quindi puntare l'attributo della proprietà **src** al percorso del file di immagine, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="83fe0-176">To create a shape that is filled with a picture file, you can specify the **type** property attribute to "frame", and then point the **src** property attribute to the location of the picture file, as shown in the following VML representation:</span></span>

![picture1.gif (8496 byte)](images/picture1.gif)


```HTML
<v:oval style='width:120pt;height:90pt' strokecolor="red"
strokeweight="2.5pt">
<v:fill type="frame" src="image1.jpg" />
</v:oval>
```




<span data-ttu-id="83fe0-178">È possibile creare facilmente una forma riempita con un'immagine diversa puntando l'attributo della proprietà **src** a un altro file.</span><span class="sxs-lookup"><span data-stu-id="83fe0-178">You can easily create a shape that is filled with a different picture by pointing the **src** property attribute to another file.</span></span>

<span data-ttu-id="83fe0-179">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span><span class="sxs-lookup"><span data-stu-id="83fe0-179">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858394) .</span></span>

 

 