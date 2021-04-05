---
title: Attributo CoordOrigin di la
description: Attributo CoordOrigin di la
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872573"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="77013-103">Attributo CoordOrigin di la</span><span class="sxs-lookup"><span data-stu-id="77013-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="77013-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="77013-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77013-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="77013-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77013-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="77013-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77013-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="77013-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77013-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="77013-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77013-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="77013-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77013-110">Specifica l'origine dell'unità di coordinate del rettangolo che delimita una forma.</span><span class="sxs-lookup"><span data-stu-id="77013-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="77013-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="77013-111">Read/write.</span></span> <span data-ttu-id="77013-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="77013-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="77013-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="77013-113">**Applies To**</span></span>

[<span data-ttu-id="77013-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="77013-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="77013-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="77013-115">**Tag Syntax**</span></span>

<span data-ttu-id="77013-116"><v: *element* coordorigin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="77013-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="77013-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="77013-117">**Script Syntax**</span></span>

<span data-ttu-id="77013-118">*element* . coordorigin = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="77013-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="77013-119">*espressione* = *elemento*. coordorigin</span><span class="sxs-lookup"><span data-stu-id="77013-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="77013-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="77013-120">**Remarks**</span></span>

<span data-ttu-id="77013-121">Se non specificato, le coordinate di origine sono (0,0) nell'angolo superiore sinistro del rettangolo di delimitazione della forma.</span><span class="sxs-lookup"><span data-stu-id="77013-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="77013-122">Il valore x di **CoordSize** viene aggiunto al valore x di **CoordOrigin** per determinare l'intervallo dei valori orizzontali.</span><span class="sxs-lookup"><span data-stu-id="77013-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="77013-123">Se, ad esempio, il valore x di **CoordOrigin** è-100 e il valore x di **CoordSize** è 200, le unità orizzontali variano da-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="77013-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="77013-124">Se il valore x di **CoordOrigin** è 100 e il valore x di **CoordSize** è 200, le unità orizzontali variano da 100 a 300, tutte all'interno del rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="77013-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="77013-125">Lo stesso vale per i valori y.</span><span class="sxs-lookup"><span data-stu-id="77013-125">The same is true for the y values.</span></span>

<span data-ttu-id="77013-126">Si noti che questo attributo è un vettore e che le unità sono dello stesso tipo di unità di [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="77013-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="77013-127">Durante lo scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare anche il tipo di unità previste.</span><span class="sxs-lookup"><span data-stu-id="77013-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="77013-128">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="77013-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="77013-129">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="77013-129">**Example**</span></span>

<span data-ttu-id="77013-130">Il centro del rettangolo di delimitazione sarà l'origine (0,0) del percorso per la forma.</span><span class="sxs-lookup"><span data-stu-id="77013-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="77013-131">Poiché **CoordOrigin** è "-500-500" e **CoordSize** è "1000 1000", le unità orizzontali e verticali variano da-500 a + 500.</span><span class="sxs-lookup"><span data-stu-id="77013-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="77013-132">L'angolo sinistro e superiore del tracciato sarà al centro del rettangolo di delimitazione definito dai punti sinistro e superiore, come definito dallo **stile**.</span><span class="sxs-lookup"><span data-stu-id="77013-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="77013-133">[Esempio di attributo CoordOrigin](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="77013-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="77013-134">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="77013-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 