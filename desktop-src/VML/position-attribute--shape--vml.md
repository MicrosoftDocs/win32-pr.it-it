---
title: Attributo position (Shape) (la)
description: Attributo position (Shape) (la)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399674"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="ab1ff-103">Attributo position (Shape) (la)</span><span class="sxs-lookup"><span data-stu-id="ab1ff-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="ab1ff-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ab1ff-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ab1ff-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ab1ff-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ab1ff-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ab1ff-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ab1ff-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ab1ff-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ab1ff-110">Definisce il tipo di posizionamento utilizzato per inserire un elemento.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="ab1ff-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-111">Read/write.</span></span> <span data-ttu-id="ab1ff-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-112">**String**.</span></span>

<span data-ttu-id="ab1ff-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="ab1ff-113">**Applies To**</span></span>

[<span data-ttu-id="ab1ff-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="ab1ff-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="ab1ff-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="ab1ff-115">**Tag Syntax**</span></span>

<span data-ttu-id="ab1ff-116"><v: *elemento* Style = "position: *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="ab1ff-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="ab1ff-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="ab1ff-117">**Script Syntax**</span></span>

<span data-ttu-id="ab1ff-118">*element* . Style. Position = "*espressione*"</span><span class="sxs-lookup"><span data-stu-id="ab1ff-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="ab1ff-119">*espressione* = *element*. Style. Position</span><span class="sxs-lookup"><span data-stu-id="ab1ff-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="ab1ff-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="ab1ff-120">**Remarks**</span></span>

<span data-ttu-id="ab1ff-121">L'attributo **position** è simile all'attributo **position** HTML standard usato con i fogli di stile.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="ab1ff-122">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="ab1ff-122">Values include:</span></span>



| <span data-ttu-id="ab1ff-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ab1ff-123">Value</span></span>    | <span data-ttu-id="ab1ff-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab1ff-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1ff-125">static</span><span class="sxs-lookup"><span data-stu-id="ab1ff-125">static</span></span>   | <span data-ttu-id="ab1ff-126">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-126">Default.</span></span> <span data-ttu-id="ab1ff-127">L'elemento viene posizionato in base al normale flusso della pagina.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="ab1ff-128">Gli attributi **Top** e **Left** vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="ab1ff-129">Se l'oggetto è ancorato inline, che si verifica solo in Microsoft Word, viene usato questo valore.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="ab1ff-130">assoluto</span><span class="sxs-lookup"><span data-stu-id="ab1ff-130">absolute</span></span> | <span data-ttu-id="ab1ff-131">L'elemento è posizionato in relazione al padre, usando gli attributi **Top** e **Left** .</span><span class="sxs-lookup"><span data-stu-id="ab1ff-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="ab1ff-132">Questo valore viene utilizzato dagli oggetti mobili di Microsoft Word e Microsoft Excel e dalle diapositive di Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="ab1ff-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="ab1ff-133">relative</span><span class="sxs-lookup"><span data-stu-id="ab1ff-133">relative</span></span> | <span data-ttu-id="ab1ff-134">L'elemento viene posizionato in base al normale flusso della pagina, ma vengono utilizzati gli attributi **Top** e **Left** .</span><span class="sxs-lookup"><span data-stu-id="ab1ff-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="ab1ff-135">La sovrapposizione di elementi sovrapposti è regolata dall'attributo **Z-index** .</span><span class="sxs-lookup"><span data-stu-id="ab1ff-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="ab1ff-136">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="ab1ff-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="ab1ff-137">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="ab1ff-137">**Example**</span></span>

<span data-ttu-id="ab1ff-138">La posizione del rettangolo viene visualizzata utilizzando lo stile *relativo* .</span><span class="sxs-lookup"><span data-stu-id="ab1ff-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="ab1ff-139">[Esempio di attributo position](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ab1ff-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="ab1ff-140">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="ab1ff-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 