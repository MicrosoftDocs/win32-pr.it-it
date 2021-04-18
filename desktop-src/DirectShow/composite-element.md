---
description: L'elemento composito definisce una composizione, un oggetto contenitore per le tracce e altre composizioni nidificate.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303824"
---
# <a name="composite-element"></a><span data-ttu-id="1df13-103">Elemento composite</span><span class="sxs-lookup"><span data-stu-id="1df13-103">composite Element</span></span>

> [!Note]  
> <span data-ttu-id="1df13-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="1df13-104">\[Deprecated.</span></span> <span data-ttu-id="1df13-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1df13-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1df13-106">L' `composite` elemento definisce una composizione, un oggetto contenitore per le tracce e altre composizioni nidificate.</span><span class="sxs-lookup"><span data-stu-id="1df13-106">The `composite` element defines a composition, a container object for tracks and other nested compositions.</span></span>

## <a name="attributes"></a><span data-ttu-id="1df13-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="1df13-107">Attributes</span></span>

<span data-ttu-id="1df13-108">[**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="1df13-108">[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="1df13-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="1df13-109">Parent/Child Information</span></span>



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1df13-110">Padre</span><span class="sxs-lookup"><span data-stu-id="1df13-110">Parent</span></span>   | <span data-ttu-id="1df13-111">`composite`, [ **gruppo**](group-element.md)</span><span class="sxs-lookup"><span data-stu-id="1df13-111">`composite`, [**group**](group-element.md)</span></span>                                                                             |
| <span data-ttu-id="1df13-112">Children</span><span class="sxs-lookup"><span data-stu-id="1df13-112">Children</span></span> | <span data-ttu-id="1df13-113">`composite`, [**effetto**](effect-element.md), [**traccia**](track-element.md), [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="1df13-113">`composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1df13-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1df13-114">Remarks</span></span>

<span data-ttu-id="1df13-115">All'interno di un `composite` elemento, la priorità dei livelli annidati viene determinata in modo implicito in base all'ordine in cui vengono visualizzati all'interno dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1df13-115">Within a `composite` element, the priority of nested layers is determined implicitly by the order in which they appear within the element.</span></span> <span data-ttu-id="1df13-116">Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità sempre maggiori.</span><span class="sxs-lookup"><span data-stu-id="1df13-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="1df13-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="1df13-117">Examples</span></span>


```XML
<composite> </composite>
```



## <a name="see-also"></a><span data-ttu-id="1df13-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1df13-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1df13-119">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="1df13-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



