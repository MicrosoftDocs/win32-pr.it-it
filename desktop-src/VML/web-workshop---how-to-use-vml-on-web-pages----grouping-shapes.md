---
title: Raggruppamento di forme
description: Questo articolo descrive il raggruppamento di forme in VML, una funzionalità deprecata a Internet Explorer Windows 9.
ms.assetid: 469c9e4d-d1ae-4285-b2cb-ac833ebe59ff
keywords:
- Workshop Web, raggruppamento di forme
- progettazione di pagine Web, raggruppamento di forme
- Vector Markup Language (VML), raggruppamento di forme
- VML (Vector Markup Language),raggruppamento di forme
- grafica vettoriale, raggruppamento di forme
- forme VML, raggruppamento
- raggruppamento di forme
- Vector Markup Language (VML),elemento group
- VML (Vector Markup Language),elemento group
- grafica vettoriale, elemento group
- Elemento group
- elementi VML, gruppo
- Vector Markup Language (VML), spazio delle coordinate locale
- VML (Vector Markup Language),spazio delle coordinate locale
- grafica vettoriale, spazio delle coordinate locale
- spazio delle coordinate locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e0c3073f55d23c15734b5d5ddfa886e7291530
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407704"
---
# <a name="grouping-shapes"></a><span data-ttu-id="07e6b-119">Raggruppamento di forme</span><span class="sxs-lookup"><span data-stu-id="07e6b-119">Grouping Shapes</span></span>

<span data-ttu-id="07e6b-120">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9.</span><span class="sxs-lookup"><span data-stu-id="07e6b-120">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="07e6b-121">Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="07e6b-121">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="07e6b-122">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="07e6b-122">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="07e6b-123">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="07e6b-123">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="07e6b-124">Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="07e6b-124">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="07e6b-125">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="07e6b-125">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="07e6b-126">Come si è appreso, è possibile disegnare facilmente singole forme usando VML.</span><span class="sxs-lookup"><span data-stu-id="07e6b-126">As you've learned, you can easily draw individual shapes by using VML.</span></span> <span data-ttu-id="07e6b-127">In questa sezione verranno illustrati i vantaggi del raggruppamento delle forme e verrà illustrato come raggruppare le forme.</span><span class="sxs-lookup"><span data-stu-id="07e6b-127">In this section, we will explain the benefits of grouping shapes together, and how to group shapes.</span></span>

<span data-ttu-id="07e6b-128">Se si hanno molte forme che devono essere ridimensionate, spostate o ruotate insieme, può essere noioso impostare gli attributi singolarmente per ogni forma.</span><span class="sxs-lookup"><span data-stu-id="07e6b-128">If you had many shapes that needed to be scaled, moved, or rotated together, you would find it tedious to set the attributes individually for each shape.</span></span> <span data-ttu-id="07e6b-129">Inoltre, è possibile aumentare il margine per gli errori.</span><span class="sxs-lookup"><span data-stu-id="07e6b-129">Plus you would raise your margin for errors.</span></span> <span data-ttu-id="07e6b-130">Sarebbe meglio raggruppare le forme e quindi impostare gli attributi per l'intero gruppo.</span><span class="sxs-lookup"><span data-stu-id="07e6b-130">It would be better if you could group the shapes, and then set the attributes for the entire group.</span></span>

<span data-ttu-id="07e6b-131">In VML è possibile usare l'elemento per raggruppare più forme in modo che possano `<group>` essere trasformate come un'unica unità.</span><span class="sxs-lookup"><span data-stu-id="07e6b-131">In VML, you can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span> <span data-ttu-id="07e6b-132">Ad esempio, come illustrato nella rappresentazione VML seguente, è possibile raggruppare facilmente due forme.</span><span class="sxs-lookup"><span data-stu-id="07e6b-132">For example, as shown in the following VML representation, you can easily group two shapes together.</span></span>


```HTML
<v:group id="GroupA" style='position:relative;left:10pt;top:20pt;
width:150pt;height:100pt; ...>
   <v:shape id="Shape1"...></v:shape>
   <v:shape id="Shape2"...></v:shape>
</v:group>
```



<span data-ttu-id="07e6b-133">Quando le forme vengono raggruppate, usano lo [spazio delle coordinate locale](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) del gruppo.</span><span class="sxs-lookup"><span data-stu-id="07e6b-133">When shapes are grouped, they use the [local coordinate space](web-workshop---how-to-use-vml-on-web-pages----local-coordinate-space.md) of the group.</span></span> <span data-ttu-id="07e6b-134">Di conseguenza, le forme all'interno di un gruppo possono essere ridimensionate e spostate insieme.</span><span class="sxs-lookup"><span data-stu-id="07e6b-134">Therefore, shapes within a group can be scaled and moved together.</span></span> <span data-ttu-id="07e6b-135">Verranno visualizzati altri esempi nell'argomento Usare lo spazio delle coordinate locali.</span><span class="sxs-lookup"><span data-stu-id="07e6b-135">You will see more examples in the Use Local Coordinate Space topic.</span></span>

<span data-ttu-id="07e6b-136">All'interno di un gruppo è possibile avere tutte le forme o i gruppi desiderati.</span><span class="sxs-lookup"><span data-stu-id="07e6b-136">Inside a group, you can have as many shapes or groups as you want.</span></span> <span data-ttu-id="07e6b-137">Quando un gruppo si trova all'interno di un altro gruppo, viene chiamato "gruppo annidato".</span><span class="sxs-lookup"><span data-stu-id="07e6b-137">When a group is inside another group, it is called a "nested group".</span></span> <span data-ttu-id="07e6b-138">Non esiste alcuna limitazione ai livelli di annidamento.</span><span class="sxs-lookup"><span data-stu-id="07e6b-138">There is no limitation on the levels of nesting.</span></span>

<span data-ttu-id="07e6b-139">Ad esempio, le righe seguenti illustrano un gruppo annidato a 3 livelli.</span><span class="sxs-lookup"><span data-stu-id="07e6b-139">For example, the following lines demonstrate a 3-level nested group.</span></span> <span data-ttu-id="07e6b-140">Shape3 e Shape4 sono in GroupC.</span><span class="sxs-lookup"><span data-stu-id="07e6b-140">Shape3 and Shape4 are in GroupC.</span></span> <span data-ttu-id="07e6b-141">Shape2 e GroupC sono in GroupB.</span><span class="sxs-lookup"><span data-stu-id="07e6b-141">Shape2 and GroupC are in GroupB.</span></span> <span data-ttu-id="07e6b-142">Shape1 e GroupB sono in GroupA.</span><span class="sxs-lookup"><span data-stu-id="07e6b-142">Shape1 and GroupB are in GroupA.</span></span>


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



<span data-ttu-id="07e6b-143">Per altre informazioni su questo elemento, vedere la [specifica VML](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span><span class="sxs-lookup"><span data-stu-id="07e6b-143">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858388) .</span></span>

<span data-ttu-id="07e6b-144">[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="07e6b-144">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="summary"></a><span data-ttu-id="07e6b-145">Riepilogo</span><span class="sxs-lookup"><span data-stu-id="07e6b-145">Summary</span></span>

<span data-ttu-id="07e6b-146">È possibile usare `<group>` l'elemento per raggruppare più forme in modo che possano essere trasformate come un'unica unità.</span><span class="sxs-lookup"><span data-stu-id="07e6b-146">You can use the `<group>` element to group many shapes together so that they can be transformed as one unit.</span></span>

 

 