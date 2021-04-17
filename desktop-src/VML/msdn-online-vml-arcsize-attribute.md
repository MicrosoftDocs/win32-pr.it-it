---
title: Attributo ArcSize di la
description: Attributo ArcSize di la
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300022"
---
# <a name="vml-arcsize-attribute"></a><span data-ttu-id="4c185-103">Attributo ArcSize di la</span><span class="sxs-lookup"><span data-stu-id="4c185-103">VML ArcSize Attribute</span></span>

<span data-ttu-id="4c185-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4c185-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4c185-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="4c185-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4c185-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="4c185-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4c185-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="4c185-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4c185-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4c185-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4c185-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4c185-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4c185-110">Definisce la quantità di arrotondamento per un rettangolo arrotondato.</span><span class="sxs-lookup"><span data-stu-id="4c185-110">Defines the amount of roundness for a rounded rectangle.</span></span> <span data-ttu-id="4c185-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4c185-111">Read/write.</span></span> <span data-ttu-id="4c185-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4c185-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="4c185-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="4c185-113">**Applies To**</span></span>

[<span data-ttu-id="4c185-114">RoundRect</span><span class="sxs-lookup"><span data-stu-id="4c185-114">RoundRect</span></span>](msdn-online-vml-roundrect-element.md)

<span data-ttu-id="4c185-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="4c185-115">**Tag Syntax**</span></span>

<span data-ttu-id="4c185-116"><v: *element* arcsize = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4c185-116"><v: *element* arcsize=" *expression* "></span></span>

<span data-ttu-id="4c185-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="4c185-117">**Script Syntax**</span></span>

<span data-ttu-id="4c185-118">*element* . arcSize = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="4c185-118">*element* .arcSize="*expression*"</span></span>

<span data-ttu-id="4c185-119">*espressione* = *elemento*. arcSize</span><span class="sxs-lookup"><span data-stu-id="4c185-119">*expression*=*element*.arcSize</span></span>

<span data-ttu-id="4c185-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="4c185-120">**Remarks**</span></span>

<span data-ttu-id="4c185-121">Definisce gli angoli arrotondati di un rettangolo arrotondato come percentuale della metà della dimensione minore della lunghezza e della larghezza di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="4c185-121">Defines the rounded corners of a rounded rectangle as a percentage of half the smaller dimension of the length and width of a rectangle.</span></span> <span data-ttu-id="4c185-122">0% avrebbe gli angoli quadrati e il 100% costituirebbe angoli circolari.</span><span class="sxs-lookup"><span data-stu-id="4c185-122">0% would have square corners, and 100% would form circular corners.</span></span> <span data-ttu-id="4c185-123">Un quadrato con un valore **ArcSize** di 1,0 sarebbe un cerchio.</span><span class="sxs-lookup"><span data-stu-id="4c185-123">A square with an **ArcSize** value of 1.0 would be a circle.</span></span> <span data-ttu-id="4c185-124">Il valore predefinito è 0,2 (20%).</span><span class="sxs-lookup"><span data-stu-id="4c185-124">The default value is 0.2 (20%).</span></span>

<span data-ttu-id="4c185-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="4c185-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="4c185-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="4c185-126">**Example**</span></span>

<span data-ttu-id="4c185-127">Il rettangolo arrotondato viene disegnato con angoli stretti e arrotondati.</span><span class="sxs-lookup"><span data-stu-id="4c185-127">The rounded rectangle is drawn with tight-but-rounded corners.</span></span>


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 