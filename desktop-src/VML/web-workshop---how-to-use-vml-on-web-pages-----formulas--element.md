---
title: Utilizzo dell'elemento formules
description: Utilizzo dell'elemento formules
ms.assetid: f5a381b4-4132-4b66-b41a-3cada26b41e2
keywords:
- Web Workshop, elemento formule
- progettazione di pagine Web, elemento formule
- Vector Markup Language (la), elemento formule
- LA (Vector Markup Language), elemento formule
- graphics vettoriale, elemento formule
- elemento formules
- Elementi la, formule
- Forme la, elemento formule
- Vector Markup Language (la), definizione dei percorsi per le forme
- LA (Vector Markup Language), definizione dei percorsi per le forme
- grafica vettoriale, definizione dei percorsi per le forme
- LA forme, definizione di percorsi
- definizione dei percorsi per le forme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85ce4ebb6eea05895edf974e3ca86b1fa2ad923
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046803"
---
# <a name="using-the-formulas-element"></a><span data-ttu-id="a98a7-116">Utilizzo dell'elemento formules</span><span class="sxs-lookup"><span data-stu-id="a98a7-116">Using the Formulas Element</span></span>

<span data-ttu-id="a98a7-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a98a7-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a98a7-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="a98a7-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a98a7-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="a98a7-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a98a7-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="a98a7-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a98a7-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a98a7-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a98a7-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a98a7-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a98a7-123">In questo argomento verrà illustrato come utilizzare il `<formulas>` sottoelemento per definire un percorso regolabile per una forma.</span><span class="sxs-lookup"><span data-stu-id="a98a7-123">In this topic, we will illustrate how to use the `<formulas>` sub-element to define an adjustable path for a shape.</span></span>

<span data-ttu-id="a98a7-124">È possibile inserire il <formulas> sottoelemento all'interno `<shape>` o `<shapetype>` per definire formule che possono variare il percorso di una forma.</span><span class="sxs-lookup"><span data-stu-id="a98a7-124">You can place the <formulas> sub-element inside `<shape>` or `<shapetype>` to define formulas that can vary the path of a shape.</span></span> <span data-ttu-id="a98a7-125">All'interno del `<formulas>` sottoelemento, un sottoelemento **f** definisce una formula in modo che un valore venga valutato in base alla formula.</span><span class="sxs-lookup"><span data-stu-id="a98a7-125">Inside the `<formulas>` sub-element, one **f** sub-element defines one formula so that one value is evaluated based upon that formula.</span></span> <span data-ttu-id="a98a7-126">Ad esempio, la formula `<v:f eqn="prod 10 4 5"/>` definisce un valore equivalente a "10 x 4/5".</span><span class="sxs-lookup"><span data-stu-id="a98a7-126">For example, the formula, `<v:f eqn="prod 10 4 5"/>` defines a value that is equivalent to "10 x 4 / 5".</span></span>

<span data-ttu-id="a98a7-127">È possibile inserire molti elementi secondari **f** all'interno `<formulas>` di un sottoelemento.</span><span class="sxs-lookup"><span data-stu-id="a98a7-127">You can place many **f** sub-elements inside one`<formulas>` sub-element.</span></span> <span data-ttu-id="a98a7-128">Le formule possono fare riferimento ai valori definiti in precedenza in altre formule all'interno dello stesso `<formulas>` sottoelemento.</span><span class="sxs-lookup"><span data-stu-id="a98a7-128">Formulas can reference the values that are defined earlier in other formulas within the same `<formulas>` sub-element.</span></span> <span data-ttu-id="a98a7-129">Il valore definito nella prima formula può essere indicato come @0 , il valore definito nella seconda formula può essere definito come @1 e così via...</span><span class="sxs-lookup"><span data-stu-id="a98a7-129">The value that is defined in the first formula can be referred to as @0, the value that is defined in the second formula can be referred to as @1, and so on.</span></span>

<span data-ttu-id="a98a7-130">Inoltre, è possibile specificare l'attributo di proprietà **ADJ** dell' `<shape>` elemento, ad esempio ADJ = "100, 200, 150".</span><span class="sxs-lookup"><span data-stu-id="a98a7-130">In addition, you can specify the **adj** property attribute of the `<shape>` element, such as adj="100, 200, 150".</span></span> <span data-ttu-id="a98a7-131">All'interno dell' `<formulas>` elemento è quindi possibile fare riferimento a tali valori nell'elenco **ADJ** .</span><span class="sxs-lookup"><span data-stu-id="a98a7-131">Inside the `<formulas>` element, you can then reference those values in the **adj** list.</span></span> <span data-ttu-id="a98a7-132">Il primo valore (100) nell'elenco **ADJ** può essere definito come \# 0, il secondo valore (200) può essere definito come \# 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="a98a7-132">The first value (100) in the **adj** list can be referred to as \#0, the second value (200) can be referred to as \#1, and so on.</span></span>

<span data-ttu-id="a98a7-133">Ad esempio, per creare una faccia sorridente, è possibile digitare la rappresentazione la seguente:</span><span class="sxs-lookup"><span data-stu-id="a98a7-133">For example, to draw a smiling face, you can type the following VML representation:</span></span>

![shape1.gif (735 byte)](images/shape1f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="17520"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





-   <span data-ttu-id="a98a7-135">`adj="17520"` definisce un valore (= 17520).</span><span class="sxs-lookup"><span data-stu-id="a98a7-135">`adj="17520"` defines a value (= 17520).</span></span> <span data-ttu-id="a98a7-136">È possibile fare riferimento a questo valore come \# 0.</span><span class="sxs-lookup"><span data-stu-id="a98a7-136">This value can be referenced as \#0.</span></span>
-   <span data-ttu-id="a98a7-137">La prima formula, `<v:f eqn="sum 33030 0 #0"/>` , definisce il valore (= 33030 + 0- \# 0).</span><span class="sxs-lookup"><span data-stu-id="a98a7-137">The first formula, `<v:f eqn="sum 33030 0 #0"/>`, defines the value (= 33030 + 0 - \#0).</span></span> <span data-ttu-id="a98a7-138">È possibile fare riferimento a questo valore come @0 .</span><span class="sxs-lookup"><span data-stu-id="a98a7-138">This value can be referenced as @0.</span></span>
-   <span data-ttu-id="a98a7-139">La seconda formula, `<v:f eqn="prod #0 4 3"/>` , definisce il valore (= \# 0 \* 4/3).</span><span class="sxs-lookup"><span data-stu-id="a98a7-139">The second formula, `<v:f eqn="prod #0 4 3"/>`, defines the value (= \#0 \* 4 / 3).</span></span> <span data-ttu-id="a98a7-140">È possibile fare riferimento a questo valore come @1 .</span><span class="sxs-lookup"><span data-stu-id="a98a7-140">This value can be referenced as @1.</span></span>
-   <span data-ttu-id="a98a7-141">La terza formula, `<v:f eqn="prod @0 1 3"/>` , definisce il valore (= @0 \* 1/3).</span><span class="sxs-lookup"><span data-stu-id="a98a7-141">The third formula, `<v:f eqn="prod @0 1 3"/>`, defines the value (= @0 \* 1 / 3).</span></span> <span data-ttu-id="a98a7-142">È possibile fare riferimento a questo valore come @2 .</span><span class="sxs-lookup"><span data-stu-id="a98a7-142">This value can be referenced as @2.</span></span>
-   <span data-ttu-id="a98a7-143">La quarta formula, `<v:f eqn="sum @1 0 @2"/>` , definisce il valore (= @1 + 0 -@2 ).</span><span class="sxs-lookup"><span data-stu-id="a98a7-143">The fourth formula, `<v:f eqn="sum @1 0 @2"/>`, defines the value (=@1 + 0 -@2).</span></span> <span data-ttu-id="a98a7-144">È possibile fare riferimento a questo valore come @3 .</span><span class="sxs-lookup"><span data-stu-id="a98a7-144">This value can be referenced as @3.</span></span>
-   <span data-ttu-id="a98a7-145">All'interno dell' `<path>` elemento vengono utilizzati i valori definiti nelle prime ( @0 ) e le quattro @3 formule () per determinare il contorno della forma.</span><span class="sxs-lookup"><span data-stu-id="a98a7-145">Inside the `<path>` element, the values defined in the first (@0) and the fourth (@3) formulas are used to determine the outline of the shape.</span></span>

<span data-ttu-id="a98a7-146">Se si modifica l'elenco **ADJ** , ad esempio `adj="20000"` , verranno modificati anche i valori delle formule che fanno riferimento all'elenco **ADJ** , che influisce sulla faccia sorridente come segue:</span><span class="sxs-lookup"><span data-stu-id="a98a7-146">If you change the **adj** list, such as `adj="20000"`, the values of the formulas that reference the **adj** list will be changed as well, affecting the smiling face as follows:</span></span>

![shape2.gif (765 byte)](images/shape2f.gif)


```HTML
<v:shape style='width:1in;height:1in;' strokecolor="red"
strokeweight="2pt" coordsize="21600,21600" adj="20000"
path="m10800,0qx0,10800,10800,21600,21600,10800,10800,0xe
m7340,6445qx6215,7570,7340,8695,8465,7570,7340,6445xnfe
m14260,6445qx13135,7570,14260,8695,15385,7570,14260,6445xnfe
m4960@0c8853@3,12747@3,16640@0nfe">
<v:formulas>
<v:f eqn="sum 33030 0 #0"/>
<v:f eqn="prod #0 4 3"/>
<v:f eqn="prod @0 1 3"/>
<v:f eqn="sum @1 0 @2"/>
</v:formulas>
</v:shape>
```





<span data-ttu-id="a98a7-148">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span><span class="sxs-lookup"><span data-stu-id="a98a7-148">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858392) .</span></span>

 

 