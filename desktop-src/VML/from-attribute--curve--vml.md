---
title: Attributo from (curve) (la)
description: Attributo from (curve) (la)
ms.assetid: 70e940c1-3fa8-4a30-9ca8-584483cea485
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d5f78dee46192efed48172a7d1f4d9cc77582f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399633"
---
# <a name="from-attribute-curvevml"></a><span data-ttu-id="504c2-103">Attributo from (curve) (la)</span><span class="sxs-lookup"><span data-stu-id="504c2-103">From Attribute (Curve)(VML)</span></span>

<span data-ttu-id="504c2-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="504c2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="504c2-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="504c2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="504c2-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="504c2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="504c2-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="504c2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="504c2-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="504c2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="504c2-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="504c2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="504c2-110">Definisce il punto iniziale di una curva.</span><span class="sxs-lookup"><span data-stu-id="504c2-110">Defines the starting point of a curve.</span></span> <span data-ttu-id="504c2-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="504c2-111">Read/write.</span></span> <span data-ttu-id="504c2-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="504c2-112">**VgVector2D**.</span></span>

<span data-ttu-id="504c2-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="504c2-113">**Applies To**</span></span>

[<span data-ttu-id="504c2-114">Curva</span><span class="sxs-lookup"><span data-stu-id="504c2-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="504c2-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="504c2-115">**Tag Syntax**</span></span>

<span data-ttu-id="504c2-116"><v: *elemento* da = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="504c2-116"><v: *element* from=" *expression* "></span></span>

<span data-ttu-id="504c2-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="504c2-117">**Script Syntax**</span></span>

<span data-ttu-id="504c2-118">*element* . from = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="504c2-118">*element* .from="*expression*"</span></span>

<span data-ttu-id="504c2-119">*espressione* = *elemento*. from</span><span class="sxs-lookup"><span data-stu-id="504c2-119">*expression*=*element*.from</span></span>

<span data-ttu-id="504c2-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="504c2-120">**Remarks**</span></span>

<span data-ttu-id="504c2-121">Definisce il punto iniziale di una curva di Bezier cubica nello spazio delle coordinate dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="504c2-121">Defines the starting point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="504c2-122">Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="504c2-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="504c2-123">Il valore predefinito è 0, 0.</span><span class="sxs-lookup"><span data-stu-id="504c2-123">Default is 0,0.</span></span>

<span data-ttu-id="504c2-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="504c2-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="504c2-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="504c2-125">**Example**</span></span>

<span data-ttu-id="504c2-126">La curva è sorridente.</span><span class="sxs-lookup"><span data-stu-id="504c2-126">The curve is smiling.</span></span> <span data-ttu-id="504c2-127">Inizia a sinistra e termina a destra.</span><span class="sxs-lookup"><span data-stu-id="504c2-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="504c2-128">I due punti di controllo si trovano lungo il modo in cui è possibile estrarre la curva per dare l'impressione di sorridere.</span><span class="sxs-lookup"><span data-stu-id="504c2-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```



 

 