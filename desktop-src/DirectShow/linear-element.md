---
description: L'elemento lineare definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene l'elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910089"
---
# <a name="linear-element"></a><span data-ttu-id="4a2ea-103">Elemento linear</span><span class="sxs-lookup"><span data-stu-id="4a2ea-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="4a2ea-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-104">\[Deprecated.</span></span> <span data-ttu-id="4a2ea-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4a2ea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a2ea-106">L'elemento lineare definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene **l'elemento param.**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="4a2ea-107">`linear`L'elemento fa sì che il parametro esere una transizione uniforme dal valore precedente al nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="4a2ea-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="4a2ea-108">Per un passaggio istantaneo a un nuovo valore, usare [**l'elemento at.**](at-element.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ea-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="4a2ea-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="4a2ea-109">Attributes</span></span>

<span data-ttu-id="4a2ea-110">[**time**](time-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="4a2ea-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="4a2ea-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="4a2ea-111">Parent/Child Information</span></span>



| <span data-ttu-id="4a2ea-112">Label</span><span class="sxs-lookup"><span data-stu-id="4a2ea-112">Label</span></span> | <span data-ttu-id="4a2ea-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4a2ea-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="4a2ea-114">Padre</span><span class="sxs-lookup"><span data-stu-id="4a2ea-114">Parent</span></span>   | [<span data-ttu-id="4a2ea-115">**Param**</span><span class="sxs-lookup"><span data-stu-id="4a2ea-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="4a2ea-116">Children</span><span class="sxs-lookup"><span data-stu-id="4a2ea-116">Children</span></span> | <span data-ttu-id="4a2ea-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="4a2ea-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="4a2ea-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="4a2ea-118">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="4a2ea-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a2ea-119">Requirements</span></span>



| <span data-ttu-id="4a2ea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2ea-120">Requirement</span></span> | <span data-ttu-id="4a2ea-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4a2ea-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2ea-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a2ea-122">Header</span></span><br/> | <dl> <span data-ttu-id="4a2ea-123"><dt>Camerauicontrol.h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2ea-123"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2ea-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a2ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2ea-125">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="4a2ea-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




