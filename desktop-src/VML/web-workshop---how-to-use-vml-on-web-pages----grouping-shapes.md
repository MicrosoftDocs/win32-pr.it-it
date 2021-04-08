---
title: Forme di raggruppamento
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Workshop Web, forme di raggruppamento
- progettazione di pagine Web, raggruppamento di forme
- Vector Markup Language (la), forme di raggruppamento
- LA (Vector Markup Language), forme di raggruppamento
- grafica vettoriale, forme raggruppamento
- LA forme, raggruppamento
- forme di raggruppamento
- Vector Markup Language (la), elemento Group
- LA (Vector Markup Language), elemento Group
- grafica vettoriale, elemento Group
- Elemento group
- Elementi la, gruppo
- Vector Markup Language (la), spazio delle coordinate locale
- LA (Vector Markup Language), spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59eed282094e2d24d2d27e338b93731eaaa1eec0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047262"
---
# <a name="grouping-shapes"></a><span data-ttu-id="23e5f-120">Forme di raggruppamento</span><span class="sxs-lookup"><span data-stu-id="23e5f-120">Grouping Shapes</span></span>

<span data-ttu-id="23e5f-121">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="23e5f-121">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="23e5f-122">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="23e5f-122">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="23e5f-123">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="23e5f-123">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="23e5f-124">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="23e5f-124">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="23e5f-125">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="23e5f-125">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="23e5f-126">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="23e5f-126">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="23e5f-127">Come si è appreso, è possibile creare facilmente singole forme usando la.</span><span class="sxs-lookup"><span data-stu-id="23e5f-127">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="23e5f-128">In questa sezione vengono illustrati i vantaggi derivanti dal raggruppamento di forme e come raggruppare le forme.</span><span class="sxs-lookup"><span data-stu-id="23e5f-128">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="23e5f-129">Se erano presenti molte forme che dovevano essere ridimensionate, spostate o ruotate insieme, sarebbe noioso impostare gli attributi singolarmente per ogni forma.</span><span class="sxs-lookup"><span data-stu-id="23e5f-129">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="23e5f-130">Inoltre, è possibile aumentare il margine per gli errori.</span><span class="sxs-lookup"><span data-stu-id="23e5f-130">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="23e5f-131">Sarebbe opportuno raggruppare le forme, quindi impostare gli attributi per l'intero gruppo.</span><span class="sxs-lookup"><span data-stu-id="23e5f-131">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="23e5f-132">In la è possibile usare l' `<group>` elemento per raggruppare molte forme in modo che possano essere trasformate come un'unica unità.</span><span class="sxs-lookup"><span data-stu-id="23e5f-132">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="23e5f-133">Ad esempio, come illustrato nella seguente rappresentazione la, è possibile raggruppare facilmente due forme.</span><span class="sxs-lookup"><span data-stu-id="23e5f-133">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="23e5f-134">Quando le forme vengono raggruppate, utilizzano lo [spazio delle coordinate locale](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del gruppo.</span><span class="sxs-lookup"><span data-stu-id="23e5f-134">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="23e5f-135">Pertanto, le forme all'interno di un gruppo possono essere ridimensionate e spostate insieme.</span><span class="sxs-lookup"><span data-stu-id="23e5f-135">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="23e5f-136">Per altri esempi, vedere l'argomento usare lo spazio delle coordinate locali.</span><span class="sxs-lookup"><span data-stu-id="23e5f-136">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="23e5f-137">All'interno di un gruppo, è possibile avere tutte le forme o i gruppi desiderati.</span><span class="sxs-lookup"><span data-stu-id="23e5f-137">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="23e5f-138">Quando un gruppo si trova all'interno di un altro gruppo, viene definito "gruppo annidato".</span><span class="sxs-lookup"><span data-stu-id="23e5f-138">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="23e5f-139">Non esiste alcuna limitazione per i livelli di annidamento.</span><span class="sxs-lookup"><span data-stu-id="23e5f-139">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="23e5f-140">Ad esempio, le righe seguenti illustrano un gruppo annidato a 3 livelli.</span><span class="sxs-lookup"><span data-stu-id="23e5f-140">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="23e5f-141">Shape3 e Shape4 sono in GroupC.</span><span class="sxs-lookup"><span data-stu-id="23e5f-141">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="23e5f-142">Shape2 e GroupC sono in GroupB.</span><span class="sxs-lookup"><span data-stu-id="23e5f-142">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="23e5f-143">Shape1 e GroupB si trovano nel gruppo a.</span><span class="sxs-lookup"><span data-stu-id="23e5f-143">Shape1 and GroupB are in GroupA.</span></span>


```HTML
<body>
   <v:group id="GroupA"...>
      <v:shape id="Shape1"...></v:shape>
      <v:group id="GroupB"...>
         <v:shape id="Shape2"...></v:shape>
         <v:group id="GroupC"...>
            <v:shape id="Shape3"...></v:shape>
            <v:shape id="Shape4"...></v:shape>
         </v:group>
      </v:group>
   </v:group>
</body>
```



<span data-ttu-id="23e5f-144">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="23e5f-144">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="23e5f-145">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="23e5f-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="23e5f-146">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="23e5f-146">Summary</span></span>

<span data-ttu-id="23e5f-147">È possibile utilizzare l' `<group>` elemento per raggruppare molte forme in modo che possano essere trasformate come un'unica unità.</span><span class="sxs-lookup"><span data-stu-id="23e5f-147">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 