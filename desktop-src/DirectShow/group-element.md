---
description: L'elemento Group definisce un gruppo, ovvero l'oggetto di primo livello in una sequenza temporale.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965820"
---
# <a name="group-element"></a><span data-ttu-id="3e27a-103">Elemento Group</span><span class="sxs-lookup"><span data-stu-id="3e27a-103">group Element</span></span>

> [!Note]  
> <span data-ttu-id="3e27a-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3e27a-104">\[Deprecated.</span></span> <span data-ttu-id="3e27a-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3e27a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3e27a-106">L'elemento **Group** definisce un gruppo, ovvero l'oggetto di primo livello in una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="3e27a-106">The **group** element defines a group, the top-level object in a timeline.</span></span>

## <a name="attributes"></a><span data-ttu-id="3e27a-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="3e27a-107">Attributes</span></span>

<span data-ttu-id="3e27a-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**Height**](height-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Name**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**SamplingRate**](samplingrate-attribute.md), [**Type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**Width**](width-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="3e27a-108">[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="3e27a-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="3e27a-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e27a-110">Padre</span><span class="sxs-lookup"><span data-stu-id="3e27a-110">Parent</span></span>   | [<span data-ttu-id="3e27a-111">**sequenza temporale**</span><span class="sxs-lookup"><span data-stu-id="3e27a-111">**timeline**</span></span>](timeline-element.md)                                                                     |
| <span data-ttu-id="3e27a-112">Children</span><span class="sxs-lookup"><span data-stu-id="3e27a-112">Children</span></span> | <span data-ttu-id="3e27a-113">[**composto**](composite-element.md), [**effetto**](effect-element.md), [**traccia**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="3e27a-113">[**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3e27a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e27a-114">Remarks</span></span>

<span data-ttu-id="3e27a-115">All'interno di un `group` elemento, la priorità dei livelli annidati viene determinata in modo implicito in base all'ordine in cui vengono visualizzati all'interno dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="3e27a-115">Within a `group` element, the priority of nested layers is determined implicitly by the order they appear within the element.</span></span> <span data-ttu-id="3e27a-116">Il primo livello ha priorità 0 e i livelli successivi hanno valori di priorità sempre maggiori.</span><span class="sxs-lookup"><span data-stu-id="3e27a-116">The first layer has priority 0, and subsequent layers have increasing priority values.</span></span>

## <a name="examples"></a><span data-ttu-id="3e27a-117">Esempi</span><span class="sxs-lookup"><span data-stu-id="3e27a-117">Examples</span></span>


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a><span data-ttu-id="3e27a-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3e27a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e27a-119">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="3e27a-119">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



