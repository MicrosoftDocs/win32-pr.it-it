---
description: L'elemento transition definisce un oggetto transition. Una transizione è una trasformazione a due input che comporta una transizione da un flusso (ad esempio una composita o una traccia) a un altro.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60bf6b915a393ab153f0e94862cb5ed72dd3424c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910039"
---
# <a name="transition-element"></a><span data-ttu-id="ff02c-104">Elemento transition</span><span class="sxs-lookup"><span data-stu-id="ff02c-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="ff02c-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="ff02c-105">\[Deprecated.</span></span> <span data-ttu-id="ff02c-106">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ff02c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ff02c-107">`transition`L'elemento definisce un oggetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="ff02c-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="ff02c-108">Una transizione è una trasformazione a due input che comporta una transizione da un flusso (ad esempio una composita o una traccia) a un altro.</span><span class="sxs-lookup"><span data-stu-id="ff02c-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="ff02c-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="ff02c-109">Attributes</span></span>

<span data-ttu-id="ff02c-110">[**clsid**](clsid-attribute.md), cutpoint , [**cutpoint**](cutpoint-attribute.md) [**,**](lock-attribute.md) [**cutonly**](cutsonly-attribute.md), lock , [**mute**](mute-attribute.md), start , [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md) [](start-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="ff02c-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="ff02c-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="ff02c-111">Parent/Child Information</span></span>



| <span data-ttu-id="ff02c-112">Label</span><span class="sxs-lookup"><span data-stu-id="ff02c-112">Label</span></span> | <span data-ttu-id="ff02c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ff02c-113">Value</span></span> |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="ff02c-114">Padre</span><span class="sxs-lookup"><span data-stu-id="ff02c-114">Parent</span></span>   | <span data-ttu-id="ff02c-115">[**composito,**](composite-element.md) [ **traccia**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="ff02c-115">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="ff02c-116">Children</span><span class="sxs-lookup"><span data-stu-id="ff02c-116">Children</span></span> | [<span data-ttu-id="ff02c-117">**Param**</span><span class="sxs-lookup"><span data-stu-id="ff02c-117">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="ff02c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff02c-118">Remarks</span></span>

<span data-ttu-id="ff02c-119">**L'attributo clsid** specifica il sottooggetto che crea la transizione.</span><span class="sxs-lookup"><span data-stu-id="ff02c-119">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="ff02c-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="ff02c-120">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="ff02c-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff02c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff02c-122">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="ff02c-122">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



