---
description: L'elemento param specifica il valore di una proprietà su una transizione, un effetto o un altro oggetto secondario.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909039"
---
# <a name="param-element"></a><span data-ttu-id="4cee1-103">Elemento param</span><span class="sxs-lookup"><span data-stu-id="4cee1-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="4cee1-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4cee1-104">\[Deprecated.</span></span> <span data-ttu-id="4cee1-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4cee1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4cee1-106">`param`L'elemento specifica il valore di una proprietà su una transizione, un effetto o un altro oggetto secondario.</span><span class="sxs-lookup"><span data-stu-id="4cee1-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="4cee1-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="4cee1-107">Attributes</span></span>

<span data-ttu-id="4cee1-108">[**name**](name-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="4cee1-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="4cee1-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="4cee1-109">Parent/Child Information</span></span>



| <span data-ttu-id="4cee1-110">Label</span><span class="sxs-lookup"><span data-stu-id="4cee1-110">Label</span></span> | <span data-ttu-id="4cee1-111">Valore</span><span class="sxs-lookup"><span data-stu-id="4cee1-111">Value</span></span> |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cee1-112">Padre</span><span class="sxs-lookup"><span data-stu-id="4cee1-112">Parent</span></span>   | <span data-ttu-id="4cee1-113">[**clip,**](clip-element.md) [**effetto,**](effect-element.md) [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="4cee1-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="4cee1-114">Children</span><span class="sxs-lookup"><span data-stu-id="4cee1-114">Children</span></span> | <span data-ttu-id="4cee1-115">[**in**](at-element.md), [ **lineare**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="4cee1-115">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="4cee1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="4cee1-116">Remarks</span></span>

<span data-ttu-id="4cee1-117">**L'attributo** value specifica il valore della proprietà all'inizio della transizione o dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4cee1-117">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="4cee1-118">Usare **l'elemento at** **o linear** per specificare i valori che cambiano.</span><span class="sxs-lookup"><span data-stu-id="4cee1-118">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="4cee1-119">Se **l'elemento param** non contiene **elementi at o** **lineari,** il valore rimane costante per la durata dell'effetto o della transizione.</span><span class="sxs-lookup"><span data-stu-id="4cee1-119">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="4cee1-120">Un **elemento param all'interno** di un **elemento clip** non può **contenere elementi in corrispondenza di** o **lineari.**</span><span class="sxs-lookup"><span data-stu-id="4cee1-120">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="4cee1-121">Molte transizioni supportano una proprietà **Progress** standard che è compreso tra 0 e 1,0, che indica la percentuale della transizione riflessa nell'output.</span><span class="sxs-lookup"><span data-stu-id="4cee1-121">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="4cee1-122">In **Progress** = 0.0 la transizione si trova all'inizio della sequenza (interamente la prima immagine video).</span><span class="sxs-lookup"><span data-stu-id="4cee1-122">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="4cee1-123">In **Progress** = 0,5 la transizione è metà completa.</span><span class="sxs-lookup"><span data-stu-id="4cee1-123">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="4cee1-124">Ad esempio, in una cancellazione, in **Progress** = 0,5 il limite di transizione si trova al centro dell'immagine. In **Progress** = 1.0 la transizione è completa (interamente la seconda immagine).</span><span class="sxs-lookup"><span data-stu-id="4cee1-124">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="4cee1-125">Per impostazione predefinita, le transizioni passano da **Progress** = 0.0 all'inizio della transizione a **Progress** = 1.0 alla fine.</span><span class="sxs-lookup"><span data-stu-id="4cee1-125">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="4cee1-126">Altre proprietà sono in genere specifiche di una particolare transizione o effetto.</span><span class="sxs-lookup"><span data-stu-id="4cee1-126">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="4cee1-127">Ad esempio, la transizione di cancellazione supporta una **proprietà GradientSize** che controlla la larghezza dell'area di transizione.</span><span class="sxs-lookup"><span data-stu-id="4cee1-127">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="4cee1-128">Per eseguire una transizione all'indietro, impostare la proprietà **Progress** su 1.0 all'inizio della transizione e usare l'elemento **lineare** per impostare il valore su 0,0, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="4cee1-128">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="4cee1-129">Esempi</span><span class="sxs-lookup"><span data-stu-id="4cee1-129">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="4cee1-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4cee1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cee1-131">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="4cee1-131">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



