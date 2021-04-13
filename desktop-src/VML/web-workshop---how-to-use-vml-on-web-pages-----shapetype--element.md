---
title: Utilizzo dell'elemento TipoForma
description: Utilizzo dell'elemento TipoForma
ms.assetid: ad9e5c00-fbee-4bec-b4cd-075cf5a4d8c7
keywords:
- Web Workshop, elemento TipoForma
- progettazione di pagine Web, elemento TipoForma
- Vector Markup Language (la), elemento TipoForma
- LA (Vector Markup Language), elemento TipoForma
- grafica vettoriale, elemento TipoForma
- elemento TipoForma
- Elementi la, TipoForma
- Forme la, elemento TipoForma
- Vector Markup Language (la), definizione di forme usate di frequente
- LA (Vector Markup Language), definizione di forme usate di frequente
- grafica vettoriale, definizione di forme usate di frequente
- definizione di forme usate di frequente
- LA forme, definizione di uso frequente
- Vector Markup Language (la), creazione di un'istanza di copie di forme
- LA (Vector Markup Language), creazione di un'istanza di copie di forme
- grafica vettoriale, creazione di istanze di copie di forme
- creazione di istanze di copie di forme
- LA forme, creazione di istanze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfa7ec47dde492231e8bcd54f68e4637454613b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474014"
---
# <a name="using-the-shapetype-element"></a><span data-ttu-id="57466-121">Utilizzo dell'elemento TipoForma</span><span class="sxs-lookup"><span data-stu-id="57466-121">Using the Shapetype Element</span></span>

<span data-ttu-id="57466-122">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="57466-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="57466-123">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="57466-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="57466-124">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="57466-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="57466-125">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="57466-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="57466-126">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="57466-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="57466-127">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="57466-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="57466-128">In questo argomento verrà illustrato come usare l' `<shapetype>` elemento per definire le forme usate di frequente e quindi creare un'istanza o creare forme da TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-128">In this topic, we will illustrate how to use the `<shapetype>` element to define your own frequently-used shapes and then instantiate, or create, shapes from the shapetype.</span></span>

<span data-ttu-id="57466-129">Se si desidera disegnare molte forme con proprietà identiche o simili, è noioso se è necessario digitare ripetutamente gli stessi attributi di proprietà per ogni forma.</span><span class="sxs-lookup"><span data-stu-id="57466-129">If you wanted to draw many shapes that have the same or similar properties, it would be tedious if you had to repeatedly type the same property attributes for each shape.</span></span> <span data-ttu-id="57466-130">LA fornisce l' `<shapetype>` elemento in modo che sia possibile definire un prototipo di una forma.</span><span class="sxs-lookup"><span data-stu-id="57466-130">VML provides the `<shapetype>` element so that you can define a prototype of a shape.</span></span> <span data-ttu-id="57466-131">È quindi possibile usare l' `<shape>` elemento per creare un'istanza di molte copie di forme dallo stesso TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-131">You can then use the `<shape>` element to instantiate many copies of shapes from the same shapetype.</span></span>

<span data-ttu-id="57466-132">È possibile seguire i tre passaggi per definire un TipoForma e quindi creare un'istanza di una forma da TipoForma:</span><span class="sxs-lookup"><span data-stu-id="57466-132">You can follow the three steps to define a shapetype, and then instantiate a shape from the shapetype:</span></span>

1.  <span data-ttu-id="57466-133">Digitare un `<shapetype>` elemento e assegnargli un nome specificando l'attributo ID.</span><span class="sxs-lookup"><span data-stu-id="57466-133">Type a `<shapetype>` element and give it a name by specifying the id attribute.</span></span>
2.  <span data-ttu-id="57466-134">Descrivere TipoForma usando i relativi attributi o sottoelementi della proprietà.</span><span class="sxs-lookup"><span data-stu-id="57466-134">Describe the shapetype by using its property attributes or sub-elements.</span></span>
3.  <span data-ttu-id="57466-135">Creare un'istanza di una forma digitando un `<shape>` elemento e fare riferimento all'attributo Type della forma all'attributo ID di TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-135">Instantiate a shape by typing a `<shape>` element, and refer the type attribute of the shape to the id attribute of the shapetype.</span></span>

<span data-ttu-id="57466-136">Si digitano, ad esempio, le righe seguenti per creare un TipoForma denominato "forme":</span><span class="sxs-lookup"><span data-stu-id="57466-136">For example, you type the following lines to create a shapetype called "MyShape":</span></span>


```HTML
<v:shapetype id="MyShape" >
</v:shapetype>
```



<span data-ttu-id="57466-137">Modificare quindi il TipoForma impostando alcuni attributi delle proprietà, ad esempio `fillcolor="red" strokecolor="blue"` .</span><span class="sxs-lookup"><span data-stu-id="57466-137">Then, you alter the shapetype by setting some property attributes, such as `fillcolor="red" strokecolor="blue"`.</span></span> <span data-ttu-id="57466-138">In alternativa, è possibile usare sottoelementi all'interno di TipoForma, ad esempio, `<path>` `<fill>` , `<stroke>` (si parlerà di tali sottoelementi negli argomenti successivi).</span><span class="sxs-lookup"><span data-stu-id="57466-138">Or, you can use sub-elements inside the shapetype, such as `<path>`, `<fill>`, `<stroke>` (we will talk about those sub-elements in later topics).</span></span>


```HTML
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue"...>
</v:shapetype>
```



<span data-ttu-id="57466-139">Quindi, si crea un'istanza di una forma da TipoForma "forme" specificando `type="#MyShape"` , come illustrato nella seguente rappresentazione la.</span><span class="sxs-lookup"><span data-stu-id="57466-139">Then, you instantiate a shape from the shapetype "MyShape" by specifying `type="#MyShape"`, as shown in the following VML representation.</span></span> <span data-ttu-id="57466-140">Questa forma eredita tutte le proprietà da TipoForma "forma" e viene visualizzata all'interno della casella che lo contiene a una dimensione di 100 per 80.</span><span class="sxs-lookup"><span data-stu-id="57466-140">This shape inherits all properties from the shapetype "MyShape", and is displayed within its containing box at a size of 100 by 80.</span></span>


```HTML
<v:shape type="#MyShape" style='width:100;height:80'/>
```



<span data-ttu-id="57466-141">È possibile creare un'istanza di un'altra forma da TipoForma "forme" specificando `type="#MyShape"` e sovrascrivendo alcune proprietà, ad esempio `fillcolor="maroon"` , come illustrato nella rappresentazione la seguente.</span><span class="sxs-lookup"><span data-stu-id="57466-141">You can instantiate another shape from the shapetype "MyShape" by specifying `type="#MyShape"` and overwrite some properties, such as `fillcolor="maroon"`, as shown in the following VML representation.</span></span> <span data-ttu-id="57466-142">Questa forma eredita tutte le proprietà da TipoForma "Shape" ad eccezione della proprietà FillColor e viene visualizzata all'interno della casella che lo contiene a una dimensione di 70 per 90.</span><span class="sxs-lookup"><span data-stu-id="57466-142">This shape inherits all properties from the shapetype "MyShape" except the fillcolor property, and is displayed within its containing box at a size of 70 by 90.</span></span>


```HTML
<v:shape type="#MyShape" fillcolor="maroon"
style='width:70; height:90'/>
```



<span data-ttu-id="57466-143">Di seguito è illustrata la rappresentazione la completa per l'esempio precedente:</span><span class="sxs-lookup"><span data-stu-id="57466-143">Here is the complete VML representation for the preceding example:</span></span>

![\-1.gif tipo1 (477 byte)](images/type1-1.gif)![\-2.gif tipo1 (471 byte)](images/type1-2.gif)


```HTML
<body>
<v:shapetype id="MyShape" fillcolor="red" strokecolor="blue" coordsize="21600,21600"
path="m10860,2187c10451,1746,9529,1018,9015,730,7865,152,6685,,5415,,4175,
152,2995,575,1967,1305,1150,2187,575,3222,242,4220,,5410,242,6560,575,7597l10860,
21600,20995,7597c21480,6560,21600,5410,21480,4220,21115,3222,20420,2187,19632,
1305,18575,575,17425,152,16275,,15005,,13735,152,12705,730,12176,1018,11254,1746,
10860,2187xe">
</v:shapetype>
<v:shape type="#MyShape" style='width:100;height:80;'/>
<v:shape type="#MyShape" style='width:70;height:90;' fillcolor="maroon"/>
</body>
```





<span data-ttu-id="57466-146">Come appreso, quando viene creata un'istanza di una forma da un TipoForma, eredita tutti gli attributi della proprietà da TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-146">As you've learned, when a shape is instantiated from a shapetype, it inherits all of the property attributes from the shapetype.</span></span> <span data-ttu-id="57466-147">È possibile sovrascrivere alcuni o tutti gli attributi ereditati ridefinendo gli attributi all'interno dell' `<shape>` elemento.</span><span class="sxs-lookup"><span data-stu-id="57466-147">You can overwrite some or all of the inherited attributes by redefining attributes inside the `<shape>` element.</span></span> <span data-ttu-id="57466-148">Tenere presente che l'ereditarietà è un solo livello.</span><span class="sxs-lookup"><span data-stu-id="57466-148">Be aware that the inheritance is only one level.</span></span> <span data-ttu-id="57466-149">Questo perché solo un `<shape>` elemento può fare riferimento a un `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="57466-149">This is because only a `<shape>` element can reference a `<shapetype>` element.</span></span> <span data-ttu-id="57466-150">Un `<shapetype>` elemento non può fare riferimento A un altro `<shapetype>` elemento.</span><span class="sxs-lookup"><span data-stu-id="57466-150">A `<shapetype>` element cannot reference another `<shapetype>` element.</span></span>

<span data-ttu-id="57466-151">Inoltre, un TipoForma non appartiene ad alcun gruppo.</span><span class="sxs-lookup"><span data-stu-id="57466-151">Also, a shapetype doesn't belong to any group.</span></span> <span data-ttu-id="57466-152">Pertanto, l' `<shapetype>` elemento può essere visualizzato da solo o all'interno di un `<group>` elemento.</span><span class="sxs-lookup"><span data-stu-id="57466-152">Therefore, the `<shapetype>` element can appear by itself or inside a `<group>` element.</span></span> <span data-ttu-id="57466-153">È possibile disporre di molte forme all'interno di gruppi diversi che fanno riferimento allo stesso TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-153">You can have many shapes inside different groups that reference the same shapetype.</span></span> <span data-ttu-id="57466-154">Se un TipoForma viene visualizzato all'interno di un gruppo, una forma che vive in un altro gruppo può comunque fare riferimento a questo TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-154">If a shapetype appears inside a group, a shape living in another group can still reference this shapetype.</span></span>

<span data-ttu-id="57466-155">Nella rappresentazione la seguente, ad esempio, Rect1 e rect2 sono in GroupA e Rect3 è in GroupB.</span><span class="sxs-lookup"><span data-stu-id="57466-155">For example, in the following VML representation, Rect1 and Rect2 are in GroupA, and Rect3 is in GroupB.</span></span> <span data-ttu-id="57466-156">Viene creata un'istanza di tutti e tre i rettangoli da forma TipoForma.</span><span class="sxs-lookup"><span data-stu-id="57466-156">All three rectangles are instantiated from MyShape shapetype.</span></span>


```HTML
<body>
...
<v:shapetype id="MyShape" fillcolor="blue" strokecolor="red"...>
</v:shapetype>

<v:group id="GroupA"...>
<v:shape id="Rect1" type="#MyShape" .../>
<v:shape id="Rect2" type="#MyShape" strokecolor="black".../>
</v:group>

<v:group id="GroupB"...>
<v:shape id="Rect3" type="#MyShape" fillcolor="green".../>
</v:group>
...
</body>
```



<span data-ttu-id="57466-157">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span><span class="sxs-lookup"><span data-stu-id="57466-157">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858387) .</span></span>

 

 