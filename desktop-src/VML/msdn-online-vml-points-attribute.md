---
title: Attributo punti la
description: Attributo punti la
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046839"
---
# <a name="vml-points-attribute"></a><span data-ttu-id="e515b-103">Attributo punti la</span><span class="sxs-lookup"><span data-stu-id="e515b-103">VML Points Attribute</span></span>

<span data-ttu-id="e515b-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e515b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e515b-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="e515b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e515b-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="e515b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e515b-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="e515b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e515b-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e515b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e515b-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e515b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e515b-110">Definisce un set di punti che costituiscono una polilinea.</span><span class="sxs-lookup"><span data-stu-id="e515b-110">Defines a set of points that make up a polyline.</span></span> <span data-ttu-id="e515b-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e515b-111">Read/write.</span></span> <span data-ttu-id="e515b-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="e515b-112">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .</span></span>

<span data-ttu-id="e515b-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="e515b-113">**Applies To**</span></span>

[<span data-ttu-id="e515b-114">Polilinea</span><span class="sxs-lookup"><span data-stu-id="e515b-114">Polyline</span></span>](msdn-online-vml-polyline-element.md)

<span data-ttu-id="e515b-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="e515b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e515b-116"><v: *elemento* Points = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="e515b-116"><v: *element* points=" *expression* "></span></span>

<span data-ttu-id="e515b-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="e515b-117">**Script Syntax**</span></span>

<span data-ttu-id="e515b-118">*element* . Points = "*Expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="e515b-118">*element* .points="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="e515b-119">*espressione* = *elemento*. Points</span><span class="sxs-lookup"><span data-stu-id="e515b-119">*expression*=*element*.points</span></span>

<span data-ttu-id="e515b-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="e515b-120">**Remarks**</span></span>

<span data-ttu-id="e515b-121">Definisce un set di segmenti di linea retta costituiti da una serie di punti.</span><span class="sxs-lookup"><span data-stu-id="e515b-121">Defines a set of straight line segments that are composed of a series of points.</span></span> <span data-ttu-id="e515b-122">Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="e515b-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="e515b-123">Il valore predefinito è "0, 0 10, 10".</span><span class="sxs-lookup"><span data-stu-id="e515b-123">The default value is "0,0 10,10".</span></span> <span data-ttu-id="e515b-124">Si noti che le virgole non sono necessarie, ma rendono più semplice la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="e515b-124">Note that commas are not required, but they make for easier readability.</span></span>

<span data-ttu-id="e515b-125">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="e515b-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="e515b-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="e515b-126">**Example**</span></span>

<span data-ttu-id="e515b-127">La polilinea inizia in corrispondenza del punto 10, 10 e termina con 100.100, con i valori in punti.</span><span class="sxs-lookup"><span data-stu-id="e515b-127">The polyline starts at the point 10,10 and ends at 100,100, with the valuesin points.</span></span>


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 