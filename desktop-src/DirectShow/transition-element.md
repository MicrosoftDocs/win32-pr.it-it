---
description: L'elemento Transition definisce un oggetto di transizione. Una transizione è una trasformazione di due input che consente di eseguire una transizione da un flusso a un altro (ad esempio un composto o una traccia).
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Transition (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313408"
---
# <a name="transition-element"></a><span data-ttu-id="be00f-104">Transition (elemento)</span><span class="sxs-lookup"><span data-stu-id="be00f-104">transition Element</span></span>

> [!Note]  
> <span data-ttu-id="be00f-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="be00f-105">\[Deprecated.</span></span> <span data-ttu-id="be00f-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be00f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be00f-107">L' `transition` elemento definisce un oggetto di transizione.</span><span class="sxs-lookup"><span data-stu-id="be00f-107">The `transition` element defines a transition object.</span></span> <span data-ttu-id="be00f-108">Una transizione è una trasformazione di due input che consente di eseguire una transizione da un flusso a un altro (ad esempio un composto o una traccia).</span><span class="sxs-lookup"><span data-stu-id="be00f-108">A transition is a two-input transform that results in a transition from one stream (such as a composite or track) to another.</span></span>

## <a name="attributes"></a><span data-ttu-id="be00f-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="be00f-109">Attributes</span></span>

<span data-ttu-id="be00f-110">[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="be00f-110">[**clsid**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="be00f-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="be00f-111">Parent/Child Information</span></span>



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| <span data-ttu-id="be00f-112">Padre</span><span class="sxs-lookup"><span data-stu-id="be00f-112">Parent</span></span>   | <span data-ttu-id="be00f-113">[**composto**](composite-element.md), [ **traccia**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="be00f-113">[**composite**](composite-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="be00f-114">Children</span><span class="sxs-lookup"><span data-stu-id="be00f-114">Children</span></span> | [<span data-ttu-id="be00f-115">**param**</span><span class="sxs-lookup"><span data-stu-id="be00f-115">**param**</span></span>](param-element.md)                                         |



 

## <a name="remarks"></a><span data-ttu-id="be00f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="be00f-116">Remarks</span></span>

<span data-ttu-id="be00f-117">L'attributo **CLSID** specifica il sottooggetto che crea la transizione.</span><span class="sxs-lookup"><span data-stu-id="be00f-117">The **clsid** attribute specifies the subobject that creates the transition.</span></span>

## <a name="examples"></a><span data-ttu-id="be00f-118">Esempi</span><span class="sxs-lookup"><span data-stu-id="be00f-118">Examples</span></span>


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a><span data-ttu-id="be00f-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="be00f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be00f-120">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="be00f-120">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



