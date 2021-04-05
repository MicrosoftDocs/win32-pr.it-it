---
title: Per attribuire (riga) (la)
description: Per attribuire (riga) (la)
ms.assetid: e4d2afb9-0cad-469d-a388-c1b824d14c04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79246936e4885025d43dfe1fc8cc3b2f144403a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730130"
---
# <a name="to-attribute-linevml"></a><span data-ttu-id="4d3e9-103">Per attribuire (riga) (la)</span><span class="sxs-lookup"><span data-stu-id="4d3e9-103">To Attribute (Line)(VML)</span></span>

<span data-ttu-id="4d3e9-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4d3e9-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4d3e9-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4d3e9-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4d3e9-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4d3e9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4d3e9-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4d3e9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4d3e9-110">Definisce il punto finale di una linea.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-110">Defines the ending point of a line.</span></span> <span data-ttu-id="4d3e9-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-111">Read/write.</span></span> <span data-ttu-id="4d3e9-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-112">**VgVector2D**.</span></span>

<span data-ttu-id="4d3e9-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-113">**Applies To**</span></span>

[<span data-ttu-id="4d3e9-114">Linea</span><span class="sxs-lookup"><span data-stu-id="4d3e9-114">Line</span></span>](msdn-online-vml-line-element.md)

<span data-ttu-id="4d3e9-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-115">**Tag Syntax**</span></span>

<span data-ttu-id="4d3e9-116"><v: *elemento* a = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="4d3e9-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="4d3e9-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-117">**Script Syntax**</span></span>

<span data-ttu-id="4d3e9-118">*element* . to = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="4d3e9-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="4d3e9-119">*espressione* = *elemento*. to</span><span class="sxs-lookup"><span data-stu-id="4d3e9-119">*expression*=*element*.to</span></span>

<span data-ttu-id="4d3e9-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-120">**Remarks**</span></span>

<span data-ttu-id="4d3e9-121">Definisce il punto finale della riga nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-121">Defines the ending point of the line in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="4d3e9-122">Il valore predefinito è 10, 10.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-122">Default is 10,10.</span></span>

<span data-ttu-id="4d3e9-123">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="4d3e9-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="4d3e9-124">**Example**</span></span>

<span data-ttu-id="4d3e9-125">La riga termina in una posizione 100 punta verso il basso e 100 punta a destra dell'angolo superiore sinistro dello spazio padre.</span><span class="sxs-lookup"><span data-stu-id="4d3e9-125">The line ends at a location 100 points down and 100 points to the right of the top left corner of the parent space.</span></span>


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 