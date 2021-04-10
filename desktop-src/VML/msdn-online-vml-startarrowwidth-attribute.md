---
title: Attributo StartArrowWidth di la
description: Attributo StartArrowWidth di la
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728538"
---
# <a name="vml-startarrowwidth-attribute"></a><span data-ttu-id="b9989-103">Attributo StartArrowWidth di la</span><span class="sxs-lookup"><span data-stu-id="b9989-103">VML StartArrowWidth Attribute</span></span>

<span data-ttu-id="b9989-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b9989-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b9989-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="b9989-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b9989-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="b9989-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b9989-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="b9989-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b9989-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b9989-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b9989-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b9989-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b9989-110">Definisce la larghezza della freccia per l'inizio di una riga.</span><span class="sxs-lookup"><span data-stu-id="b9989-110">Defines the arrowhead width for the start of a line.</span></span> <span data-ttu-id="b9989-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="b9989-111">Read/write.</span></span> <span data-ttu-id="b9989-112">**VgArrowheadWidth**.</span><span class="sxs-lookup"><span data-stu-id="b9989-112">**VgArrowheadWidth**.</span></span>

<span data-ttu-id="b9989-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="b9989-113">**Applies To**</span></span>

[<span data-ttu-id="b9989-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="b9989-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="b9989-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="b9989-115">**Tag Syntax**</span></span>

<span data-ttu-id="b9989-116"><v: *element* startarrowwidth = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="b9989-116"><v: *element* startarrowwidth=" *expression* "></span></span>

<span data-ttu-id="b9989-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="b9989-117">**Script Syntax**</span></span>

<span data-ttu-id="b9989-118">*element* . startarrowwidth = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="b9989-118">*element* .startarrowwidth="*expression*"</span></span>

<span data-ttu-id="b9989-119">*espressione* = *elemento*. startarrowwidth</span><span class="sxs-lookup"><span data-stu-id="b9989-119">*expression*=*element*.startarrowwidth</span></span>

<span data-ttu-id="b9989-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="b9989-120">**Remarks**</span></span>

<span data-ttu-id="b9989-121">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="b9989-121">Values include:</span></span>

-   <span data-ttu-id="b9989-122">Limitare</span><span class="sxs-lookup"><span data-stu-id="b9989-122">Narrow</span></span>
-   <span data-ttu-id="b9989-123">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9989-123">Medium (default)</span></span>
-   <span data-ttu-id="b9989-124">Largo</span><span class="sxs-lookup"><span data-stu-id="b9989-124">Wide</span></span>

<span data-ttu-id="b9989-125">Attributo standard la</span><span class="sxs-lookup"><span data-stu-id="b9989-125">VML Standard Attribute</span></span>

<span data-ttu-id="b9989-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="b9989-126">**Example**</span></span>

<span data-ttu-id="b9989-127">Una linea viene disegnata con un'ampia freccia classica all'inizio del tratto.</span><span class="sxs-lookup"><span data-stu-id="b9989-127">A line is drawn with a wide classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 