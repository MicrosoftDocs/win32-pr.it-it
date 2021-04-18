---
title: Attributo Control1 di la
description: Attributo Control1 di la
ms.assetid: 4a304936-4da8-4197-b7f3-d89551de0c85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88516592c371a19a7a3b001a708c507d3103927a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299824"
---
# <a name="vml-control1-attribute"></a><span data-ttu-id="3f2cf-103">Attributo Control1 di la</span><span class="sxs-lookup"><span data-stu-id="3f2cf-103">VML Control1 Attribute</span></span>

<span data-ttu-id="3f2cf-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3f2cf-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3f2cf-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3f2cf-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3f2cf-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3f2cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3f2cf-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3f2cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3f2cf-110">Definisce il primo punto di controllo di una curva di Bezier.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-110">Defines the first control point of a bezier curve.</span></span> <span data-ttu-id="3f2cf-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-111">Read/write.</span></span> <span data-ttu-id="3f2cf-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-112">**VgVector2D**.</span></span>

<span data-ttu-id="3f2cf-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="3f2cf-113">**Applies To**</span></span>

[<span data-ttu-id="3f2cf-114">Curva</span><span class="sxs-lookup"><span data-stu-id="3f2cf-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="3f2cf-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="3f2cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="3f2cf-116"><v: *element* Control1 = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="3f2cf-116"><v: *element* control1=" *expression* "></span></span>

<span data-ttu-id="3f2cf-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="3f2cf-117">**Script Syntax**</span></span>

<span data-ttu-id="3f2cf-118">*element* . Control1 = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="3f2cf-118">*element* .control1="*expression*"</span></span>

<span data-ttu-id="3f2cf-119">*espressione* = *elemento*. Control1</span><span class="sxs-lookup"><span data-stu-id="3f2cf-119">*expression*=*element*.control1</span></span>

<span data-ttu-id="3f2cf-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="3f2cf-120">**Remarks**</span></span>

<span data-ttu-id="3f2cf-121">Definisce il primo punto di controllo di una curva di Bezier cubica nello spazio delle coordinate dell'elemento padre. Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-121">Defines the first control point of a cubic bezier curve in the coordinate space of the parent element.If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="3f2cf-122">Il valore predefinito è 10, 10.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-122">Default is 10,10.</span></span>

<span data-ttu-id="3f2cf-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="3f2cf-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3f2cf-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="3f2cf-124">**Example**</span></span>

<span data-ttu-id="3f2cf-125">La curva è sorridente.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-125">The curve is smiling.</span></span> <span data-ttu-id="3f2cf-126">Inizia a sinistra e termina a destra.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-126">It starts at the left and ends at the right.</span></span> <span data-ttu-id="3f2cf-127">I due punti di controllo si trovano lungo il modo in cui è possibile estrarre la curva per dare l'impressione di sorridere.</span><span class="sxs-lookup"><span data-stu-id="3f2cf-127">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,10pt" control2="70pt,10pt">
   </v:curve>
```





 

 