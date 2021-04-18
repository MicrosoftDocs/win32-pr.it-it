---
description: L'elemento lineare definisce il valore di un elemento param in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene l'elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento Linear (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324786"
---
# <a name="linear-element"></a><span data-ttu-id="7d406-103">Elemento lineare</span><span class="sxs-lookup"><span data-stu-id="7d406-103">linear Element</span></span>

> [!Note]  
> <span data-ttu-id="7d406-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7d406-104">\[Deprecated.</span></span> <span data-ttu-id="7d406-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d406-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d406-106">L'elemento lineare definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene l'elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="7d406-106">The linear element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the **param** element.</span></span> <span data-ttu-id="7d406-107">L' `linear` elemento fa in modo che il parametro effettui una transizione uniforme dal valore precedente al nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="7d406-107">The `linear` element causes the parameter to make a smooth transition from its previous value to the new value.</span></span> <span data-ttu-id="7d406-108">Per passare immediatamente a un nuovo valore, usare l'elemento [**at**](at-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7d406-108">For an instantaneous jump to a new value, use the [**at**](at-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="7d406-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="7d406-109">Attributes</span></span>

<span data-ttu-id="7d406-110">[**ora**](time-attribute.md), [ **valore**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7d406-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7d406-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="7d406-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="7d406-112">Padre</span><span class="sxs-lookup"><span data-stu-id="7d406-112">Parent</span></span>   | [<span data-ttu-id="7d406-113">**param**</span><span class="sxs-lookup"><span data-stu-id="7d406-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="7d406-114">Children</span><span class="sxs-lookup"><span data-stu-id="7d406-114">Children</span></span> | <span data-ttu-id="7d406-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="7d406-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="7d406-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="7d406-116">Examples</span></span>


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a><span data-ttu-id="7d406-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d406-117">Requirements</span></span>



| <span data-ttu-id="7d406-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d406-118">Requirement</span></span> | <span data-ttu-id="7d406-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7d406-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d406-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d406-120">Header</span></span><br/> | <dl> <span data-ttu-id="7d406-121"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d406-121"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d406-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d406-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d406-123">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="7d406-123">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




