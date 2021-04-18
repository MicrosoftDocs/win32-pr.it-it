---
title: Attributo CoordSize di la
description: Attributo CoordSize di la
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299858"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="e3f04-103">Attributo CoordSize di la</span><span class="sxs-lookup"><span data-stu-id="e3f04-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="e3f04-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e3f04-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3f04-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e3f04-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3f04-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e3f04-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3f04-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e3f04-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3f04-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3f04-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3f04-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3f04-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3f04-110">Specifica le unità orizzontali e verticali del rettangolo che delimita una forma.</span><span class="sxs-lookup"><span data-stu-id="e3f04-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="e3f04-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e3f04-111">Read/write.</span></span> <span data-ttu-id="e3f04-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="e3f04-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="e3f04-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e3f04-113">**Applies To**</span></span>

[<span data-ttu-id="e3f04-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="e3f04-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e3f04-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e3f04-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3f04-116"><v: *element* coordsize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e3f04-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="e3f04-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e3f04-117">**Script Syntax**</span></span>

<span data-ttu-id="e3f04-118">*element* . coordsize = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="e3f04-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="e3f04-119">*espressione* = *elemento*. coordsize</span><span class="sxs-lookup"><span data-stu-id="e3f04-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="e3f04-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e3f04-120">**Remarks**</span></span>

<span data-ttu-id="e3f04-121">Se non specificato, le dimensioni della coordinata corrispondono al riquadro delimitatore della forma.</span><span class="sxs-lookup"><span data-stu-id="e3f04-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="e3f04-122">Si noti che questo attributo è un vettore e che le unità sono relative alla lunghezza e alla larghezza del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e3f04-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="e3f04-123">Si noti inoltre che è possibile effettuare il mapping tra **coordsize** e il rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="e3f04-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="e3f04-124">Assicurarsi che la **larghezza coordsize** e l' **altezza coordsize** corrispondano alla larghezza e all' **altezza** dello **stile** , se non si vuole distorcere la forma.</span><span class="sxs-lookup"><span data-stu-id="e3f04-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="e3f04-125">Durante lo scripting, poiché si tratta di un vettore 2D, è possibile accedere separatamente ai valori x e y e determinare anche il tipo di unità previste.</span><span class="sxs-lookup"><span data-stu-id="e3f04-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="e3f04-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e3f04-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3f04-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e3f04-127">**Example**</span></span>

<span data-ttu-id="e3f04-128">La forma è 100 punti alti e 100 punti di larghezza, ma ogni unità orizzontale e verticale nello spazio delle coordinate è 1/10 di un punto.</span><span class="sxs-lookup"><span data-stu-id="e3f04-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="e3f04-129">[Esempio di attributo CoordSize](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e3f04-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="e3f04-130">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="e3f04-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 