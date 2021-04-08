---
description: L'elemento param Specifica il valore di una proprietà in una transizione, un effetto o un altro oggetto SubObject.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876786"
---
# <a name="param-element"></a><span data-ttu-id="08628-103">param (elemento)</span><span class="sxs-lookup"><span data-stu-id="08628-103">param Element</span></span>

> [!Note]  
> <span data-ttu-id="08628-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="08628-104">\[Deprecated.</span></span> <span data-ttu-id="08628-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="08628-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="08628-106">L' `param` elemento specifica il valore di una proprietà in una transizione, un effetto o un altro oggetto SubObject.</span><span class="sxs-lookup"><span data-stu-id="08628-106">The `param` element specifies the value of a property on a transition, effect, or other subobject.</span></span>

## <a name="attributes"></a><span data-ttu-id="08628-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="08628-107">Attributes</span></span>

<span data-ttu-id="08628-108">[**nome**](name-attribute.md), [ **valore**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="08628-108">[**name**](name-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="08628-109">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="08628-109">Parent/Child Information</span></span>



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08628-110">Padre</span><span class="sxs-lookup"><span data-stu-id="08628-110">Parent</span></span>   | <span data-ttu-id="08628-111">[**clip**](clip-element.md), [**effetto**](effect-element.md), [**transizione**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="08628-111">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span> |
| <span data-ttu-id="08628-112">Children</span><span class="sxs-lookup"><span data-stu-id="08628-112">Children</span></span> | <span data-ttu-id="08628-113">[**at**](at-element.md), [ **lineari**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="08628-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>                                               |



 

## <a name="remarks"></a><span data-ttu-id="08628-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="08628-114">Remarks</span></span>

<span data-ttu-id="08628-115">L'attributo **value** specifica il valore della proprietà all'inizio della transizione o dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="08628-115">The **value** attribute specifies the value of the property at the start of the transition or effect.</span></span> <span data-ttu-id="08628-116">Usare l'elemento **at** o **Linear** per specificare i valori modificabili.</span><span class="sxs-lookup"><span data-stu-id="08628-116">Use the **at** or **linear** element to specify changing values.</span></span> <span data-ttu-id="08628-117">Se l'elemento **param** non contiene elementi **at** o **Linear** , il valore rimane costante per la durata dell'effetto o della transizione.</span><span class="sxs-lookup"><span data-stu-id="08628-117">If the **param** element contains no **at** or **linear** elements, the value remains constant over the duration of the effect or transition.</span></span>

> [!Note]  
> <span data-ttu-id="08628-118">Un elemento **param** all'interno di un elemento **clip** non può contenere elementi **at** o **Linear** .</span><span class="sxs-lookup"><span data-stu-id="08628-118">A **param** element inside a **clip** element cannot contain **at** or **linear** elements.</span></span>

 

<span data-ttu-id="08628-119">Molte transizioni supportano una proprietà dello **stato di avanzamento** standard compresa tra 0 e 1,0, che indica la percentuale della transizione che si riflette nell'output.</span><span class="sxs-lookup"><span data-stu-id="08628-119">Many transitions support a standard **Progress** property that ranges from 0 to 1.0, indicating what percentage of the transition is reflected in the output.</span></span> <span data-ttu-id="08628-120">In fase di **esecuzione** = 0,0, la transizione si trova all'inizio della relativa sequenza (interamente la prima immagine video).</span><span class="sxs-lookup"><span data-stu-id="08628-120">At **Progress** = 0.0, the transition is at the beginning of its sequence (entirely the first video image).</span></span> <span data-ttu-id="08628-121">In fase di **esecuzione** = 0,5, la transizione è metà del completamento.</span><span class="sxs-lookup"><span data-stu-id="08628-121">At **Progress** = 0.5, the transition is half complete.</span></span> <span data-ttu-id="08628-122">(Ad esempio, in una cancellazione, in **corso** = 0,5 il limite di transizione è al centro dell'immagine) In fase di **esecuzione** = 1,0, la transizione è completa (interamente la seconda immagine).</span><span class="sxs-lookup"><span data-stu-id="08628-122">(For example, in a wipe, at **Progress** = 0.5 the transition boundary is in the center of the image) At **Progress** = 1.0, the transition is complete (entirely the second image).</span></span> <span data-ttu-id="08628-123">Per impostazione predefinita, le transizioni passano da **Progress** = 0,0 all'inizio della transizione a **Progress** = 1,0 alla fine.</span><span class="sxs-lookup"><span data-stu-id="08628-123">By default, transitions go from **Progress** = 0.0 at the start of the transition to **Progress** = 1.0 at the end.</span></span>

<span data-ttu-id="08628-124">Le altre proprietà sono in genere specifiche di una particolare transizione o effetto.</span><span class="sxs-lookup"><span data-stu-id="08628-124">Other properties are usually specific to one particular transition or effect.</span></span> <span data-ttu-id="08628-125">Ad esempio, la transizione di cancellazione supporta una proprietà **GradientSize** che controlla la larghezza dell'area di transizione.</span><span class="sxs-lookup"><span data-stu-id="08628-125">For example, the wipe transition supports a **GradientSize** property that controls the width of the transition area.</span></span>

<span data-ttu-id="08628-126">Per eseguire una transizione indietro, impostare la proprietà **Progress** su 1,0 all'inizio della transizione e usare l'elemento **Linear** per modificare il valore in 0,0, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="08628-126">To run a transition backward, set the **Progress** property to 1.0 at the start of the transition, and use the **linear** element to change the value to 0.0, as shown in the following example:</span></span>


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a><span data-ttu-id="08628-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="08628-127">Examples</span></span>


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a><span data-ttu-id="08628-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="08628-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08628-129">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="08628-129">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



