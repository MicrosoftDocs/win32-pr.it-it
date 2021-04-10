---
title: Attributo TextBoxRect di la
description: Attributo TextBoxRect di la
ms.assetid: 22c3510a-be5f-4357-b288-02d96eae99ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23e955c8dc929a442fe147d5401fd597534242e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046812"
---
# <a name="vml-textboxrect-attribute"></a><span data-ttu-id="76079-103">Attributo TextBoxRect di la</span><span class="sxs-lookup"><span data-stu-id="76079-103">VML TextBoxRect Attribute</span></span>

<span data-ttu-id="76079-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76079-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76079-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="76079-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76079-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="76079-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76079-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="76079-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76079-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76079-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76079-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76079-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76079-110">Definisce una o più caselle di testo all'interno di una forma.</span><span class="sxs-lookup"><span data-stu-id="76079-110">Defines one or more text boxes inside a shape.</span></span> <span data-ttu-id="76079-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="76079-111">Read/write.</span></span> <span data-ttu-id="76079-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="76079-112">**String**.</span></span>

<span data-ttu-id="76079-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="76079-113">**Applies To**</span></span>

[<span data-ttu-id="76079-114">Percorso</span><span class="sxs-lookup"><span data-stu-id="76079-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="76079-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="76079-115">**Tag Syntax**</span></span>

<span data-ttu-id="76079-116"><v: *element* textboxrect = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="76079-116"><v: *element* textboxrect=" *expression* "></span></span>

<span data-ttu-id="76079-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="76079-117">**Script Syntax**</span></span>

<span data-ttu-id="76079-118">*element* . textboxrect = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="76079-118">*element* .textboxrect="*expression*"</span></span>

<span data-ttu-id="76079-119">*espressione* = *elemento*. textboxrect</span><span class="sxs-lookup"><span data-stu-id="76079-119">*expression*=*element*.textboxrect</span></span>

<span data-ttu-id="76079-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="76079-120">**Remarks**</span></span>

<span data-ttu-id="76079-121">Una casella di testo viene definita da uno o più set di numeri che specificano (in ordine) i punti sinistro, superiore, destro e inferiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="76079-121">A textbox is defined by one or more sets of numbers specifying (in order) the left, top, right, and bottom points of the rectangle.</span></span> <span data-ttu-id="76079-122">Più set sono delimitati da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="76079-122">Multiple sets are delimited by a semicolon.</span></span> <span data-ttu-id="76079-123">Il valore predefinito è lo stesso valore della dimensione del rettangolo che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="76079-123">The default value is the same dimension value as the containing rectangle.</span></span> <span data-ttu-id="76079-124">Se è definita più di una casella di testo, i set di quadrupli delimitati da virgole che definiscono ogni casella di testo sono separati da punti e virgola.</span><span class="sxs-lookup"><span data-stu-id="76079-124">If more than one textbox is defined, the comma-delimited quadruple sets that define each textbox are separated by semicolons.</span></span> <span data-ttu-id="76079-125">Normalmente le caselle di testo vengono impostate in set di 1, 2, 3 o 6 rettangoli su una forma.</span><span class="sxs-lookup"><span data-stu-id="76079-125">Normally textboxes come in sets of 1, 2, 3, or 6 rectangles on a shape.</span></span>

<span data-ttu-id="76079-126">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="76079-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="76079-127">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="76079-127">**Example**</span></span>

<span data-ttu-id="76079-128">Una casella di testo di 95 unità per 95 unità è definita e posizionata 5 unità all'interno dell'angolo superiore sinistro della forma.</span><span class="sxs-lookup"><span data-stu-id="76079-128">A textbox of 95 units by 95 units is defined and placed 5 units inside the top left corner of the shape.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "mypath" v="m 1,1 l 1,200, 200,200, 200,1 x e"
   textboxrect="5 5 100 100"/>
   </v:shape>
```



 

 