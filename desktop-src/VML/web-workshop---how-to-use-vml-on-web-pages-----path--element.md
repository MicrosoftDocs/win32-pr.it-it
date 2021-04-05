---
title: Utilizzo dell'elemento Path
description: Utilizzo dell'elemento Path
ms.assetid: fd7924e7-f94f-4bc9-aa45-02cf8f9bac9b
keywords:
- Web Workshop, elemento Path
- progettazione di pagine Web, elemento Path
- Vector Markup Language (la), elemento Path
- LA (Vector Markup Language), elemento Path
- Vector graphics, elemento Path
- path-elemento
- Elementi la, percorso
- Forme la, elemento Path
- Vector Markup Language (la), personalizzazione delle strutture delle forme
- LA (Vector Markup Language), personalizzazione delle strutture delle forme
- grafica vettoriale, personalizzazione delle strutture delle forme
- LA forme, personalizzazione di strutture
- personalizzazione delle strutture delle forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba82d0ab946ef8937b68b4934f9c4d928bd25225
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729751"
---
# <a name="using-the-path-element"></a><span data-ttu-id="b584b-116">Utilizzo dell'elemento Path</span><span class="sxs-lookup"><span data-stu-id="b584b-116">Using the Path Element</span></span>

<span data-ttu-id="b584b-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b584b-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b584b-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b584b-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b584b-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b584b-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b584b-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b584b-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b584b-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b584b-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b584b-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b584b-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b584b-123">Si è appreso che è possibile usare gli elementi di forma predefiniti di la, ad esempio `<oval>` ,, `<line>` `<polyline>` , `<curve>` , `<rect>` , e, `<roundrect>` `<arc>` per disegnare una forma.</span><span class="sxs-lookup"><span data-stu-id="b584b-123">You've learned that you can use the VML predefined shape elements -- such as `<oval>` , `<line>`, `<polyline>`, `<curve>`, `<rect>`, `<roundrect>`, and `<arc>` -- to draw a shape.</span></span> <span data-ttu-id="b584b-124">In questo argomento verrà illustrato come utilizzare il `<path>` sottoelemento per personalizzare il contorno di una forma.</span><span class="sxs-lookup"><span data-stu-id="b584b-124">In this topic, we will illustrate how to use the `<path>` sub-element to customize the outline of a shape.</span></span>

<span data-ttu-id="b584b-125">È possibile inserire il `<path>` sottoelemento all'interno dell' `<shape>` `<shapetype>` elemento o.</span><span class="sxs-lookup"><span data-stu-id="b584b-125">You can place the `<path>` sub-element inside the `<shape>` or `<shapetype>` element.</span></span> <span data-ttu-id="b584b-126">È quindi possibile usare gli attributi di proprietà del `<path>` sottoelemento per personalizzare il contorno della forma.</span><span class="sxs-lookup"><span data-stu-id="b584b-126">You can then use the property attributes of the `<path>` sub-element to customize the outline of the shape.</span></span>

<span data-ttu-id="b584b-127">Per disegnare la forma personalizzata illustrata nell'immagine seguente, ad esempio, è possibile usare il `<path>` sottoelemento per definire il contorno della forma, come illustrato nella rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="b584b-127">For example, to draw the customized shape illustrated in the following picture, you can use the `<path>` sub-element to define the outline of the shape, as shown in the following VML representation:</span></span>

![shape1.gif (1301 byte)](images/shape1p.gif)


```HTML
<body>
<v:shape style='width:250;height:250' strokecolor="red" strokeweight="1.5pt"
fillcolor="blue" coordorigin="0 0" coordsize="200 200">
<v:path v="m 8,65 l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155,
92,121, 42,155, 60,100 x e"/>
</v:shape>
</body>
```





-   <span data-ttu-id="b584b-129">I valori `m 8,65` indicano che il disegno inizia in corrispondenza del punto (8, 65).</span><span class="sxs-lookup"><span data-stu-id="b584b-129">The values `m 8,65` indicate that the drawing starts at the point (8,65).</span></span>
-   <span data-ttu-id="b584b-130">I valori `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicano che una linea retta inizia in corrispondenza del punto corrente (8, 65) e termina in corrispondenza del punto specificato (72, 65), che diventa il nuovo punto corrente.</span><span class="sxs-lookup"><span data-stu-id="b584b-130">The values `l 72,65, 92,11, 112,65, 174,65, 122,100, 142,155, 92,121, 42,155, 60,100` indicate that a straight line begins at the current point (8, 65) and ends at the given point (72, 65), which becomes the new current point.</span></span> <span data-ttu-id="b584b-131">Una nuova riga inizia in corrispondenza del punto corrente (72, 65) e termina in corrispondenza del punto specificato, che diventa il nuovo punto corrente e così via, fino al punto finale (60, 100).</span><span class="sxs-lookup"><span data-stu-id="b584b-131">A new line begins at the current point (72, 65) and ends at the given point, which becomes the new current point, and so on, to the final point (60, 100).</span></span>
-   <span data-ttu-id="b584b-132">`x` indica che il percorso si chiuderà con una linea retta che inizia in corrispondenza del punto corrente (60, 100) e termina in corrispondenza del punto originale (8, 65).</span><span class="sxs-lookup"><span data-stu-id="b584b-132">`x` indicates that the path will close by a straight line that starts at the current point (60, 100) and ends at the original point (8, 65).</span></span>
-   <span data-ttu-id="b584b-133">`e` indica l'arresto del disegno.</span><span class="sxs-lookup"><span data-stu-id="b584b-133">`e` indicates stop drawing.</span></span>

<span data-ttu-id="b584b-134">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span><span class="sxs-lookup"><span data-stu-id="b584b-134">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858391) .</span></span>

 

 