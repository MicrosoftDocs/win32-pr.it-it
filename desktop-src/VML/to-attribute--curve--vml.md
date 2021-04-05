---
title: Attributo to (curve) (la)
description: Attributo to (curve) (la)
ms.assetid: 61469921-5095-4cb6-b032-f3e250874958
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c0c9a858ff2cc8304ffacefb1cae477614e470
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872938"
---
# <a name="to-attribute-curvevml"></a><span data-ttu-id="44b83-103">Attributo to (curve) (la)</span><span class="sxs-lookup"><span data-stu-id="44b83-103">To Attribute (Curve)(VML)</span></span>

<span data-ttu-id="44b83-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="44b83-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="44b83-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="44b83-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="44b83-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="44b83-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="44b83-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="44b83-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="44b83-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="44b83-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="44b83-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="44b83-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="44b83-110">Definisce il punto finale di una curva.</span><span class="sxs-lookup"><span data-stu-id="44b83-110">Defines the ending point of a curve.</span></span> <span data-ttu-id="44b83-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="44b83-111">Read/write.</span></span> <span data-ttu-id="44b83-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="44b83-112">**VgVector2D**.</span></span>

<span data-ttu-id="44b83-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="44b83-113">**Applies To**</span></span>

[<span data-ttu-id="44b83-114">Curva</span><span class="sxs-lookup"><span data-stu-id="44b83-114">Curve</span></span>](msdn-online-vml-curve-element.md)

<span data-ttu-id="44b83-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="44b83-115">**Tag Syntax**</span></span>

<span data-ttu-id="44b83-116"><v: *elemento* a = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="44b83-116"><v: *element* to=" *expression* "></span></span>

<span data-ttu-id="44b83-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="44b83-117">**Script Syntax**</span></span>

<span data-ttu-id="44b83-118">*element* . to = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="44b83-118">*element* .to="*expression*"</span></span>

<span data-ttu-id="44b83-119">*espressione* = *elemento*. to</span><span class="sxs-lookup"><span data-stu-id="44b83-119">*expression*=*element*.to</span></span>

<span data-ttu-id="44b83-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="44b83-120">**Remarks**</span></span>

<span data-ttu-id="44b83-121">Definisce il punto finale di una curva di Bezier cubica nello spazio delle coordinate dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="44b83-121">Defines the ending point of a cubic bezier curve in the coordinate space of the parent element.</span></span> <span data-ttu-id="44b83-122">Se l'elemento padre non è un elemento la, l' [unità](msdn-online-vml-units.md) predefinita è un pixel, ma è possibile specificare anche in cm, mm, PT, PC.</span><span class="sxs-lookup"><span data-stu-id="44b83-122">If the parent is not a VML element, the default [unit](msdn-online-vml-units.md) is a pixel (but in, cm, mm, pt, pc may also be specified).</span></span> <span data-ttu-id="44b83-123">Il valore predefinito è 30, 20.</span><span class="sxs-lookup"><span data-stu-id="44b83-123">Default is 30,20.</span></span>

<span data-ttu-id="44b83-124">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="44b83-124">**VML Standard Attribute**</span></span>

<span data-ttu-id="44b83-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="44b83-125">**Example**</span></span>

<span data-ttu-id="44b83-126">La curva è sorridente.</span><span class="sxs-lookup"><span data-stu-id="44b83-126">The curve is smiling.</span></span> <span data-ttu-id="44b83-127">Inizia a sinistra e termina a destra.</span><span class="sxs-lookup"><span data-stu-id="44b83-127">It starts at the left and ends at the right.</span></span> <span data-ttu-id="44b83-128">I due punti di controllo si trovano lungo il modo in cui è possibile estrarre la curva per dare l'impressione di sorridere.</span><span class="sxs-lookup"><span data-stu-id="44b83-128">The two control points are situated along the way so as to pull the curve down to give the appearance of a smile.</span></span>


```HTML
   <v:curve id="mycurve"
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```



 

 