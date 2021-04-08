---
description: L'elemento at definisce il valore di un elemento param in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene il parametro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747263"
---
# <a name="at-element"></a><span data-ttu-id="13e75-103">Elemento at</span><span class="sxs-lookup"><span data-stu-id="13e75-103">at Element</span></span>

> [!Note]  
> <span data-ttu-id="13e75-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="13e75-104">\[Deprecated.</span></span> <span data-ttu-id="13e75-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13e75-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13e75-106">L' `at` elemento definisce il valore di un elemento [**param**](param-element.md) in un determinato momento, relativo all'inizio della transizione o dell'effetto che contiene il parametro.</span><span class="sxs-lookup"><span data-stu-id="13e75-106">The `at` element defines the value of a [**param**](param-element.md) element at a particular time, relative to the start of the transition or effect that contains the parameter.</span></span> <span data-ttu-id="13e75-107">L' `at` elemento causa il passaggio improvviso del parametro al nuovo valore nel momento specificato.</span><span class="sxs-lookup"><span data-stu-id="13e75-107">The `at` element causes the parameter to jump abruptly to the new value at the given time.</span></span> <span data-ttu-id="13e75-108">Per una progressione uniforme a un nuovo valore, usare l'elemento [**lineare**](linear-element.md) .</span><span class="sxs-lookup"><span data-stu-id="13e75-108">For a smooth progression to a new value, use the [**linear**](linear-element.md) element.</span></span>

## <a name="attributes"></a><span data-ttu-id="13e75-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="13e75-109">Attributes</span></span>

<span data-ttu-id="13e75-110">[**ora**](time-attribute.md), [ **valore**](value-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="13e75-110">[**time**](time-attribute.md), [**value**](value-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="13e75-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="13e75-111">Parent/Child Information</span></span>



|          |                                |
|----------|--------------------------------|
| <span data-ttu-id="13e75-112">Padre</span><span class="sxs-lookup"><span data-stu-id="13e75-112">Parent</span></span>   | [<span data-ttu-id="13e75-113">**param**</span><span class="sxs-lookup"><span data-stu-id="13e75-113">**param**</span></span>](param-element.md) |
| <span data-ttu-id="13e75-114">Children</span><span class="sxs-lookup"><span data-stu-id="13e75-114">Children</span></span> | <span data-ttu-id="13e75-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="13e75-115">None</span></span>                           |



 

## <a name="examples"></a><span data-ttu-id="13e75-116">Esempi</span><span class="sxs-lookup"><span data-stu-id="13e75-116">Examples</span></span>


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a><span data-ttu-id="13e75-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="13e75-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e75-118">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="13e75-118">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



