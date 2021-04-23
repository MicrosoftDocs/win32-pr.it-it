---
description: L'elemento group definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909249"
---
# <a name="group-element"></a><span data-ttu-id="c4ce4-103">Elemento group</span><span class="sxs-lookup"><span data-stu-id="c4ce4-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="c4ce4-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c4ce4-104">\[Deprecated.</span></span> <span data-ttu-id="c4ce4-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4ce4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4ce4-106">**L'elemento** group definisce un gruppo, l'oggetto di primo livello in una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="c4ce4-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="c4ce4-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="c4ce4-107">Attributes</span></span>

<span data-ttu-id="c4ce4-108">[**bitdepth**](bitdepth-attribute.md), [**buffering,**](buffering-attribute.md) [**framerate**](framerate-attribute.md), [**height**](height-attribute.md) [**,**](lock-attribute.md)lock , [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="c4ce4-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="c4ce4-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="c4ce4-109">Parent/Child Information</span></span>



| <span data-ttu-id="c4ce4-110">Label</span><span class="sxs-lookup"><span data-stu-id="c4ce4-110">Label</span></span> | <span data-ttu-id="c4ce4-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c4ce4-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ce4-112">Padre</span><span class="sxs-lookup"><span data-stu-id="c4ce4-112">Parent</span></span>   | [<span data-ttu-id="c4ce4-113">**linea temporale**</span><span class="sxs-lookup"><span data-stu-id="c4ce4-113">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="c4ce4-114">Children</span><span class="sxs-lookup"><span data-stu-id="c4ce4-114">Children</span></span> | <span data-ttu-id="c4ce4-115">[**composito,**](composite-element.md) [**effetto,**](effect-element.md) [**traccia**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="c4ce4-115">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c4ce4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4ce4-116">Remarks</span></span>

<span data-ttu-id="c4ce4-117">`group`All'interno di un elemento, la priorità dei livelli annidati viene determinata in modo implicito dall'ordine in cui appaiono all'interno dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c4ce4-117">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="c4ce4-118">Il primo livello ha la priorità 0 e i livelli successivi hanno valori di priorità crescenti.</span><span class="sxs-lookup"><span data-stu-id="c4ce4-118">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="c4ce4-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="c4ce4-119">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="c4ce4-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c4ce4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ce4-121">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="c4ce4-121">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



