---
title: Attributo from (line) (la)
description: Attributo from (line) (la)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730007"
---
# <a name="from-attribute-linevml"></a><span data-ttu-id="8a938-103">Attributo from (line) (la)</span><span class="sxs-lookup"><span data-stu-id="8a938-103">From Attribute (Line)(VML)</span></span>

<span data-ttu-id="8a938-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8a938-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8a938-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="8a938-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8a938-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="8a938-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8a938-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="8a938-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8a938-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8a938-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8a938-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8a938-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8a938-110">Definisce il punto iniziale di una linea.</span><span class="sxs-lookup"><span data-stu-id="8a938-110">Defines the starting point of a line.</span></span> <span data-ttu-id="8a938-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8a938-111">Read/write.</span></span> <span data-ttu-id="8a938-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="8a938-112">**VgVector2D**.</span></span>

<span data-ttu-id="8a938-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="8a938-113">**Applies To**</span></span>

[<span data-ttu-id="8a938-114">Linea</span><span class="sxs-lookup"><span data-stu-id="8a938-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="8a938-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="8a938-115">**Tag Syntax**</span></span>

<span data-ttu-id="8a938-116"><v: *elemento* da = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="8a938-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="8a938-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="8a938-117">**Script Syntax**</span></span>

<span data-ttu-id="8a938-118">*element* . from = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="8a938-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="8a938-119">*espressione* = *elemento*. from</span><span class="sxs-lookup"><span data-stu-id="8a938-119">*expression*=*element*.from</span></span>

<span data-ttu-id="8a938-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="8a938-120">**Remarks**</span></span>

<span data-ttu-id="8a938-121">Definisce il punto iniziale della riga nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="8a938-121">Defines the starting point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="8a938-122">Il valore predefinito è 0, 0.</span><span class="sxs-lookup"><span data-stu-id="8a938-122">Default is 0,0.</span></span>

<span data-ttu-id="8a938-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="8a938-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8a938-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="8a938-124">**Example**</span></span>

<span data-ttu-id="8a938-125">La riga inizia in una posizione 10 punta verso il basso e 10 punta a destra dell'angolo superiore sinistro dello spazio padre.</span><span class="sxs-lookup"><span data-stu-id="8a938-125">The line starts at a location 10 points down and 10 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 