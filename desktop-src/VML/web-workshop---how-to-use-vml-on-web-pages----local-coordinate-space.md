---
title: Utilizzo dello spazio delle coordinate locale
description: Utilizzo dello spazio delle coordinate locale
ms.assetid: 8b5bc176-878f-4391-ab03-3f1c0e7713c3
keywords:
- Web Workshop, spazio delle coordinate locale
- progettazione di pagine Web, spazio delle coordinate locale
- Vector Markup Language (la), spazio delle coordinate locale
- LA (Vector Markup Language), spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
- Forme la, spazio delle coordinate locale
- Vector Markup Language (la), forme di raggruppamento
- LA (Vector Markup Language), forme di raggruppamento
- grafica vettoriale, forme raggruppamento
- LA forme, raggruppamento
- forme di raggruppamento
- Vector Markup Language (la), ridimensionamento delle forme
- LA (Vector Markup Language), ridimensionamento delle forme
- grafica vettoriale, forme di ridimensionamento
- LA forme, ridimensionamento
- ridimensionamento di forme
- Vector Markup Language (la), forme di ridimensionamento
- LA (Vector Markup Language), forme di ridimensionamento
- grafica vettoriale, forme di ridimensionamento
- Forme la, ridimensionamento
- ridimensionamento di forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c82d77ce16ae60bfc1249125d25b1139aeb8f44e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729735"
---
# <a name="using-local-coordinate-space"></a><span data-ttu-id="a8cd4-125">Utilizzo dello spazio delle coordinate locale</span><span class="sxs-lookup"><span data-stu-id="a8cd4-125">Using Local Coordinate Space</span></span>

<span data-ttu-id="a8cd4-126">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-126">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a8cd4-127">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-127">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a8cd4-128">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-128">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a8cd4-129">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-129">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a8cd4-130">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-130">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a8cd4-131">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-131">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a8cd4-132">Come si è appreso, è possibile specificare gli attributi di stile **larghezza** e **altezza** per definire le dimensioni di una casella contenitore in cui verrà eseguito il rendering del contenuto di una forma o di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-132">As you've learned, you can specify the **width** and **height** style attributes to define the size of a containing box within which the contents of a shape or group will be rendered.</span></span> <span data-ttu-id="a8cd4-133">In questo argomento verrà illustrato lo spazio delle coordinate locali e il modo in cui viene usato in la per ridimensionare le forme.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-133">In this topic, we will explain what Local Coordinate Space is, and how it is used in VML to scale shapes.</span></span>

<span data-ttu-id="a8cd4-134">Se è stato richiesto di creare un rettangolo da un pollice a due pollici su una porzione di carta della griglia, la prima cosa da capire è dove iniziare (il punto di origine).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-134">If you were asked to draw a one-inch by two-inch rectangle on a piece of grid paper, the first thing you would figure out is where to start (the originating point).</span></span> <span data-ttu-id="a8cd4-135">Viene quindi illustrato come eseguire il mapping di un pollice alle celle del documento della griglia (la coordinata).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-135">Then, you would figure out how to map one inch to the cells of the grid paper (the coordinate).</span></span>

<span data-ttu-id="a8cd4-136">Analogamente, quando viene eseguito il rendering del contenuto di una forma o di un gruppo all'interno della casella contenitore in una pagina Web, è necessario definire il punto di origine e la coordinata.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-136">Similarly, when the contents of a shape or group are rendered inside its containing box on a Web page, the originating point and the coordinate must be defined.</span></span> <span data-ttu-id="a8cd4-137">LA fornisce spazio delle coordinate locale per consentire a ogni forma o gruppo di definire il proprio punto di origine e coordinata.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-137">VML provides Local Coordinate Space to allow each shape or group to define its own originating point and coordinate.</span></span> <span data-ttu-id="a8cd4-138">Se non si specifica uno spazio delle coordinate, verrà utilizzato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-138">If you don't specify a coordinate space, the default one will be used.</span></span> <span data-ttu-id="a8cd4-139">Per impostazione predefinita, l'origine inizia dall'angolo superiore sinistro della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-139">By default, the origination starts at the top-left corner of the containing box.</span></span>

<span data-ttu-id="a8cd4-140">Ad esempio, la rappresentazione la per l'ovale rosso riportato di seguito non specifica gli attributi delle proprietà **coordsize** e **coordorigin** .</span><span class="sxs-lookup"><span data-stu-id="a8cd4-140">For example, the VML representation for the red oval shown below doesn't specify the **coordsize** and **coordorigin** property attributes.</span></span> <span data-ttu-id="a8cd4-141">Viene pertanto utilizzato uno spazio delle coordinate locale predefinito.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-141">Therefore, a default local coordinate space is used.</span></span> <span data-ttu-id="a8cd4-142">La dimensione dell'ovale è 100 punti (larghezza) di 75 punti (altezza).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-142">The size of the oval is 100 points (width) by 75 points (height).</span></span> <span data-ttu-id="a8cd4-143">È possibile ridimensionare l'ovale specificando una larghezza o un'altezza diversa, come illustrato nell'argomento [forme di scala](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) .</span><span class="sxs-lookup"><span data-stu-id="a8cd4-143">You can resize the oval by specifying a different width or height, as you've learned in the [Scale Shapes](web-workshop---how-to-use-vml-on-web-pages----scaling-shapes.md) topic.</span></span>

![oval1.gif (627 byte)](images/oval1.gif)


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red">
</v:oval>
```





<span data-ttu-id="a8cd4-145">Quando la forma diventa più complessa o quando si desidera raggruppare più forme e ridimensionarle insieme, è necessario utilizzare la funzionalità spazio delle coordinate locale disponibile in la.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-145">When the shape becomes more complicated, or when you would like to group several shapes and scale them together, you should use the Local Coordinate Space feature provided in VML.</span></span>

<span data-ttu-id="a8cd4-146">Per ogni forma o gruppo, è possibile usare gli attributi delle proprietà **coordsize** e **coordorigin** per definire lo spazio delle coordinate locali della forma o del gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-146">For each shape or group, you can use the **coordsize** and **coordorigin** property attributes to define the shape's or group's local coordinate space.</span></span> <span data-ttu-id="a8cd4-147">L'attributo **coordsize** specifica il numero di unità lungo la larghezza e l'altezza della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-147">The **coordsize** attribute specifies the number of units along the width and the height of the containing box.</span></span> <span data-ttu-id="a8cd4-148">L'attributo **coordorigin** definisce la coordinata nell'angolo superiore sinistro della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-148">The **coordorigin** attribute defines the coordinate at the top left corner of the containing box.</span></span> <span data-ttu-id="a8cd4-149">Tutte le informazioni relative alla posizione, ad esempio larghezza, altezza, sinistra, superiore, percorso e così via, sono espresse in termini di unità nello spazio delle coordinate locali.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-149">All position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span>

<span data-ttu-id="a8cd4-150">Ad esempio, come illustrato nella seguente rappresentazione la, `width: 100pt; height: 100pt;` definisce la dimensione della casella contenitore affinché la forma sia 100 punti per 100 punti.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-150">For example, as shown in the following VML representation, `width: 100pt; height: 100pt;` defines the size of the containing box for the shape to be 100 points by 100 points.</span></span>

![cord1.gif (836 byte)](images/cord1.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt; width:100pt; height:100pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





-   <span data-ttu-id="a8cd4-152">`coordsize="21600,21600"` definisce la dimensione dello spazio delle coordinate locale affinché la forma sia 21600 unità per 21600 unità.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-152">`coordsize="21600,21600"` defines the size of the Local Coordinate Space for the shape to be 21600 units by 21600 units.</span></span> <span data-ttu-id="a8cd4-153">Pertanto, un'unità nello spazio delle coordinate locale equivale a 1/216 punto.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-153">Therefore, one unit in the Local Coordinate Space is equivalent to 1/216 point.</span></span>
-   <span data-ttu-id="a8cd4-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` definisce il contorno della forma come forma a rombo.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-154">`path="m10800,0l0,10800,10800,21600,21600,10800xe"` defines the outline of the shape as a diamond shape.</span></span> <span data-ttu-id="a8cd4-155">Come è stato appreso, tutte le informazioni relative alla posizione, ad esempio larghezza, altezza, sinistra, superiore, percorso e così via, sono espresse in termini di unità nello spazio delle coordinate locali.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-155">As we've learned, all position-related information (such as width, height, left, top, path, etc.) is expressed in terms of the unit in Local Coordinate Space.</span></span> <span data-ttu-id="a8cd4-156">Pertanto, 10800 in `<path>` significa 10800 unità, che equivale a 50 punti.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-156">Therefore, 10800 in the `<path>` means 10800 units, which is equivalent to 50 points.</span></span>

<span data-ttu-id="a8cd4-157">Quando si vuole ridimensionare questa forma a rombo, è sufficiente specificare una larghezza o un'altezza diversa, ovvero non è necessario modificare alcun valore in `<path>` .</span><span class="sxs-lookup"><span data-stu-id="a8cd4-157">When you want to resize this diamond shape, simply specify a different width or height -- that's it; you don't have to change any value in the `<path>`.</span></span> <span data-ttu-id="a8cd4-158">Per questa forma complicata, se non si utilizza la funzionalità spazio delle coordinate locale, sarà necessario modificare ogni valore in `<path>` ogni volta che si desidera ridimensionarlo.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-158">For this complicated shape, if you didn't use the Local Coordinate Space feature, you would have to change every value in the `<path>` whenever you wanted to resize it.</span></span>

<span data-ttu-id="a8cd4-159">È ad esempio possibile ridimensionare la forma a rombo semplicemente specificando una larghezza o un'altezza diversa, come illustrato nella seguente rappresentazione la:</span><span class="sxs-lookup"><span data-stu-id="a8cd4-159">For example, you can scale the diamond shape by simply specifying a different width or height, as shown in the following VML representation:</span></span>

![cord2.gif (1692 byte)](images/cord2.gif)


```HTML
<v:shape style='position:relative;left:10pt;top:5pt;width:200pt; height:200pt;'
coordsize="21600,21600" path="m10800,0l0,10800,10800,21600,21600,10800xe"
fillcolor="red" strokecolor="blue" strokeweight="2pt">
</v:shape>
```





<span data-ttu-id="a8cd4-161">È inoltre possibile utilizzare lo spazio delle coordinate locale nell' `<group>` elemento in modo che il contenuto di tutte le forme all'interno del gruppo venga ridimensionato in base alla stessa coordinata.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-161">You can also use Local Coordinate Space in the `<group>` element so that the contents of all shapes within the group are scaled together according to the same coordinate.</span></span> <span data-ttu-id="a8cd4-162">Quindi, ogni volta che si desidera ridimensionare o spostare un gruppo di forme, è sufficiente modificare la larghezza e l'altezza oppure le impostazioni **coordsize** e **coordorigin** del gruppo.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-162">Then, whenever you want to scale or move a group of shapes, simply change the width and height, or **coordsize** and **coordorigin** settings, of the group.</span></span>

<span data-ttu-id="a8cd4-163">Ad esempio, nella seguente rappresentazione la, `<v:group style='... width:200pt;height:200pt;'>` definisce la dimensione della casella contenitore affinché il gruppo sia 200 punti per 200 punti.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-163">For example, in the following VML representation, `<v:group style='... width:200pt;height:200pt;'>` defines the size of the containing box for the group to be 200 points by 200 points.</span></span>

![cord3.gif (645 byte)](images/cord3.gif)


```HTML
<v:group style='position:relative;left:1pt;top:2pt;width:200pt; height:200pt;'
coordsize="1000,1000" coordorigin="-500,-500">
<v:oval style='position:relative;left:0;top:0;width:400;height:300;' fillcolor="red" />
<v:roundrect style='position:relative;left:0;top:0;width:250;height:200;' fillcolor="green" />
</v:group>
```





-   <span data-ttu-id="a8cd4-165">`coordsize="1000,1000"` definisce la dimensione dello spazio delle coordinate locale affinché il gruppo sia 1000 unità per 1000 unità.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-165">`coordsize="1000,1000"` defines the size of the Local Coordinate Space for the group to be 1000 units by 1000 units.</span></span> <span data-ttu-id="a8cd4-166">Pertanto, 1 unità nello spazio delle coordinate locale equivale a 1/5 punto.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-166">Therefore, 1 unit in the Local Coordinate Space is equivalent to 1/5 point.</span></span>
-   <span data-ttu-id="a8cd4-167">`coordorigin="-500,-500"` definisce l'angolo superiore sinistro della casella contenitore in modo che sia "-500,-500".</span><span class="sxs-lookup"><span data-stu-id="a8cd4-167">`coordorigin="-500,-500"` defines the top left corner of the containing box to be "-500, -500".</span></span> <span data-ttu-id="a8cd4-168">Pertanto, il sistema di coordinate all'interno della casella contenitore è compreso tra-500 e 500 lungo l'asse x e-500 a 500 lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-168">Therefore, the coordinate system inside the containing box ranges from -500 to 500 along the x-axis, and -500 to 500 along the y-axis.</span></span> <span data-ttu-id="a8cd4-169">In altre parole, il centro della casella contenitore è "0, 0".</span><span class="sxs-lookup"><span data-stu-id="a8cd4-169">In other words, the center of the containing box is "0, 0".</span></span>
-   <span data-ttu-id="a8cd4-170">`<v:oval style='... width:400;height:300;'>` definisce la dimensione della casella che lo contiene per il rosso ovale da 400 unità (larghezza) per 300 unità (altezza).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-170">`<v:oval style='... width:400;height:300;'>` defines the size of the containing box for the red oval to be 400 units (width) by 300 units (height).</span></span> <span data-ttu-id="a8cd4-171">Poiché un'unità nello spazio delle coordinate locale equivale a 1/5 punti, la dimensione della casella contenitore per l'ovale rosso è 80 punti (larghezza) di 60 punti (altezza).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-171">Because one unit in the Local Coordinate Space is equivalent to 1/5 point, the size of the containing box for the red oval is 80 points (width) by 60 points (height).</span></span>

<span data-ttu-id="a8cd4-172">Analogamente, la dimensione della casella contenitore per il RoundRect verde è 50 punti (larghezza) per 40 punti (altezza).</span><span class="sxs-lookup"><span data-stu-id="a8cd4-172">Similarly, the size of the containing box for the green roundrect is 50 points (width) by 40 points (height).</span></span>

<span data-ttu-id="a8cd4-173">Quando si vuole ridimensionare sia il rosso ovale che il RoundRect verde, è sufficiente modificare `<v:group style='... width:200pt;height:200pt;'>` .</span><span class="sxs-lookup"><span data-stu-id="a8cd4-173">When you want to to resize both the red oval and the green roundrect, simply change `<v:group style='... width:200pt;height:200pt;'>`.</span></span> <span data-ttu-id="a8cd4-174">In questo modo, non è necessario modificare singolarmente le dimensioni delle due forme.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-174">That's it -- you don't have to individually change the size of the two shapes.</span></span>

<span data-ttu-id="a8cd4-175">Se, ad esempio, si passa `<v:group style='... width:200pt;height:200pt;'>` a `<v:group style='... width:300pt;height:300pt;'>` , le forme diventano maggiori, come illustrato nell'immagine seguente:</span><span class="sxs-lookup"><span data-stu-id="a8cd4-175">For example, if you change `<v:group style='... width:200pt;height:200pt;'>` to `<v:group style='... width:300pt;height:300pt;'>`, the shapes become larger, as shown in the following picture:</span></span>

![cord4.gif (943 byte)](images/cord4.gif)



<span data-ttu-id="a8cd4-177">Si noterà anche che le forme sono posizionate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-177">You'd also notice that the shapes are located differently.</span></span> <span data-ttu-id="a8cd4-178">Questo è dovuto al fatto che le forme vengono disegnate da "0,0", che si trova al centro della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-178">This is because the shapes are drawn from "0, 0" which is located at the center of the containing box.</span></span> <span data-ttu-id="a8cd4-179">Poiché la casella contenitore è più grande, viene spostato anche il centro della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-179">Because you make the containing box bigger, the center of the containing box is also moved.</span></span>

<span data-ttu-id="a8cd4-180">Se si passa `coordorigin="-500,-500"` a `coordorigin="0,0"` , come illustrato nell'immagine seguente, si noterà che il rosso ovale e il RoundRect verde sono spostati verso l'alto nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-180">If you change `coordorigin="-500,-500"` to `coordorigin="0,0"`, as shown in the following picture, you'll notice that the red oval and the green roundrect are both shifted up to the new location.</span></span> <span data-ttu-id="a8cd4-181">Questo è dovuto al fatto che "0,0" individua ora nell'angolo superiore sinistro della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-181">This is because "0, 0" now locates at the top left corner of the containing box.</span></span>

![cord5.gif (648 byte)](images/cord5.gif)



<span data-ttu-id="a8cd4-183">È anche importante notare che la casella contenitore non stabilisce un'area di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-183">It is also important to note that the containing box does not establish a clipping region.</span></span> <span data-ttu-id="a8cd4-184">La grafica può essere disegnata all'esterno dei limiti della casella contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-184">Graphics may be drawn outside the boundaries of the containing box.</span></span> <span data-ttu-id="a8cd4-185">La casella contenitore serve semplicemente per eseguire il mapping dello spazio delle coordinate locale allo spazio della pagina.</span><span class="sxs-lookup"><span data-stu-id="a8cd4-185">The containing box merely serves to map the local coordinate space to the page space.</span></span>

<span data-ttu-id="a8cd4-186">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span><span class="sxs-lookup"><span data-stu-id="a8cd4-186">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858382) .</span></span>

 

 