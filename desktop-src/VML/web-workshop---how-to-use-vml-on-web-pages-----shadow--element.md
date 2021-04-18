---
title: Utilizzo dell'elemento Shadow
description: Utilizzo dell'elemento Shadow
ms.assetid: 905df226-6232-4e1c-8a9c-f4d4c50b13fa
keywords:
- Web Workshop, elemento Shadow
- progettazione di pagine Web, elemento Shadow
- Vector Markup Language (la), elemento Shadow
- LA (Vector Markup Language), elemento Shadow
- grafica vettoriale, elemento Shadow
- elemento Shadow
- Elementi la, ombreggiatura
- Forme la, elemento Shadow
- Vector Markup Language (la), disegno con effetti di ombreggiatura
- LA (Vector Markup Language), disegno con effetti di ombreggiatura
- grafica vettoriale, disegno con effetti di ombreggiatura
- LA forme, disegno con effetti ombreggiatura
- disegno con effetti di ombreggiatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe32651fbeab6b84b49a40bae05a08ba3d9c33a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399626"
---
# <a name="using-the-shadow-element"></a><span data-ttu-id="3dcef-116">Utilizzo dell'elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="3dcef-116">Using the Shadow Element</span></span>

<span data-ttu-id="3dcef-117">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3dcef-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3dcef-118">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3dcef-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3dcef-119">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3dcef-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3dcef-120">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3dcef-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3dcef-121">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3dcef-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3dcef-122">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3dcef-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3dcef-123">In questo argomento verrà illustrato come utilizzare il `<shadow>` sottoelemento per disegnare una forma con diversi effetti di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="3dcef-123">In this topic, we will illustrate how to use the `<shadow>` sub-element to draw a shape that has various shadow effects.</span></span>

<span data-ttu-id="3dcef-124">È possibile inserire il `<shadow>` sottoelemento all'interno `<shape>` di, `<shapetype>` o qualsiasi elemento della forma predefinito per disegnare una forma con un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="3dcef-124">You can place the `<shadow>` sub-element inside the `<shape>`, `<shapetype>`, or any predefined shape element to draw a shape with a shadow.</span></span> <span data-ttu-id="3dcef-125">È quindi possibile usare gli attributi di proprietà del `<shadow>` sottoelemento per personalizzare l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="3dcef-125">You can then use the property attributes of the `<shadow>` sub-element to customize the shadow.</span></span>

<span data-ttu-id="3dcef-126">Ad esempio, per creare una forma con un'ombreggiatura, come illustrato nell'immagine seguente, è possibile digitare le righe seguenti nell' `<BODY>` area della pagina Web:</span><span class="sxs-lookup"><span data-stu-id="3dcef-126">For example, to create a shape with a shadow, as shown in the following picture, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![shape1.gif (887 byte)](images/shape1.gif)


```HTML
<v:oval style='width:120pt;height:80pt;' fillcolor="red">
<v:shadow on="t" type="perspective"
origin=".5,.5" offset="0,0"
matrix=",-92680f,,,,-95367431641e-17"/>
</v:oval>
```





-   <span data-ttu-id="3dcef-128">`on="t"` e `type="perspective"` indicano di attivare l'ombreggiatura usando il tipo di prospettiva.</span><span class="sxs-lookup"><span data-stu-id="3dcef-128">`on="t"` and `type="perspective"` indicate to turn on the shadow using the perspective type.</span></span>
-   <span data-ttu-id="3dcef-129">L' **origine** e l' **offset** indicano dove si desidera creare l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="3dcef-129">The **origin** and **offset** indicate where to draw the shadow.</span></span>
-   <span data-ttu-id="3dcef-130">`matrix="..."` Specifica la matrice di trasformazione della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="3dcef-130">`matrix="..."` specifies the perspective transform matrix.</span></span>

<span data-ttu-id="3dcef-131">Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span><span class="sxs-lookup"><span data-stu-id="3dcef-131">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858396) .</span></span>

 

 