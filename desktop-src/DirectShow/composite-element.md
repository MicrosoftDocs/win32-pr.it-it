---
description: L'elemento composito definisce una composizione, un oggetto contenitore per tracce e altre composizione annidate.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908839"
---
# <a name="composite-element"></a><span data-ttu-id="512b0-103">Elemento composite</span><span class="sxs-lookup"><span data-stu-id="512b0-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="512b0-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="512b0-104">\[Deprecated.</span></span> <span data-ttu-id="512b0-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="512b0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="512b0-106">`composite`L'elemento definisce una composizione, un oggetto contenitore per tracce e altre composizione annidate.</span><span class="sxs-lookup"><span data-stu-id="512b0-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="512b0-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="512b0-107">Attributes</span></span>

<span data-ttu-id="512b0-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="512b0-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="512b0-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="512b0-109">Parent/Child Information</span></span>



| <span data-ttu-id="512b0-110">Label</span><span class="sxs-lookup"><span data-stu-id="512b0-110">Label</span></span> | <span data-ttu-id="512b0-111">Valore</span><span class="sxs-lookup"><span data-stu-id="512b0-111">Value</span></span> |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="512b0-112">Padre</span><span class="sxs-lookup"><span data-stu-id="512b0-112">Parent</span></span>   | <span data-ttu-id="512b0-113">`composite`, [ **group**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="512b0-113">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="512b0-114">Children</span><span class="sxs-lookup"><span data-stu-id="512b0-114">Children</span></span> | <span data-ttu-id="512b0-115">`composite`, [**effetto**](effect-element.md), [**traccia**](track-element.md), [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="512b0-115">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="512b0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="512b0-116">Remarks</span></span>

<span data-ttu-id="512b0-117">`composite`All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito dall'ordine in cui vengono visualizzati all'interno dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="512b0-117">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="512b0-118">Il primo livello ha la priorità 0 e i livelli successivi hanno valori di priorità crescenti.</span><span class="sxs-lookup"><span data-stu-id="512b0-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="512b0-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="512b0-119">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="512b0-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="512b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512b0-121">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="512b0-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



