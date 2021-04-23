---
description: L'elemento at definisce il valore di un elemento param in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909829"
---
# <a name="at-element"></a><span data-ttu-id="7a706-103">Elemento at</span><span class="sxs-lookup"><span data-stu-id="7a706-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="7a706-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="7a706-104">\[Deprecated.</span></span> <span data-ttu-id="7a706-105">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7a706-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7a706-106">L'elemento definisce il valore di un elemento `at` [**param**](param-element.md) in un determinato momento, rispetto all'inizio della transizione o dell'effetto che contiene il parametro .</span><span class="sxs-lookup"><span data-stu-id="7a706-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="7a706-107">L'elemento fa sì che il parametro salti improvvisamente `at` al nuovo valore all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="7a706-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="7a706-108">Per una progressione uniforme a un nuovo valore, usare [**l'elemento lineare.**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="7a706-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="7a706-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="7a706-109">Attributes</span></span>

<span data-ttu-id="7a706-110">[**time**](time-attribute.md), [ **value**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="7a706-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="7a706-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="7a706-111">Parent/Child Information</span></span>



| <span data-ttu-id="7a706-112">Label</span><span class="sxs-lookup"><span data-stu-id="7a706-112">Label</span></span> | <span data-ttu-id="7a706-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7a706-113">Value</span></span> |
|----------|--------------------------------|
| <span data-ttu-id="7a706-114">Padre</span><span class="sxs-lookup"><span data-stu-id="7a706-114">Parent</span></span>   | [<span data-ttu-id="7a706-115">**Param**</span><span class="sxs-lookup"><span data-stu-id="7a706-115">**param**</span></span>](param-element.md) |
| <span data-ttu-id="7a706-116">Children</span><span class="sxs-lookup"><span data-stu-id="7a706-116">Children</span></span> | <span data-ttu-id="7a706-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="7a706-117">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="7a706-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="7a706-118">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="7a706-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7a706-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a706-120">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="7a706-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



