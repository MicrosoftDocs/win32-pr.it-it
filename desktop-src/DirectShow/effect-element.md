---
description: L'elemento effect definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento effect (Gdipluseffects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c925e61578857415bb22248a9ad2b1df27cdac
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908659"
---
# <a name="effect-element"></a><span data-ttu-id="13847-104">Elemento effect</span><span class="sxs-lookup"><span data-stu-id="13847-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="13847-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="13847-105">\[Deprecated.</span></span> <span data-ttu-id="13847-106">Questa API potrebbe essere rimossa dalle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13847-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="13847-107">`effect`L'elemento definisce un oggetto effetto audio o video.</span><span class="sxs-lookup"><span data-stu-id="13847-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="13847-108">Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.</span><span class="sxs-lookup"><span data-stu-id="13847-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="13847-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="13847-109">Attributes</span></span>

<span data-ttu-id="13847-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="13847-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="13847-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="13847-111">Parent/Child Information</span></span>



| <span data-ttu-id="13847-112">Label</span><span class="sxs-lookup"><span data-stu-id="13847-112">Label</span></span> | <span data-ttu-id="13847-113">Valore</span><span class="sxs-lookup"><span data-stu-id="13847-113">Value</span></span> |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13847-114">Padre</span><span class="sxs-lookup"><span data-stu-id="13847-114">Parent</span></span>   | <span data-ttu-id="13847-115">[**composite,**](composite-element.md) [**group,**](group-element.md) [**clip,**](clip-element.md) [**track**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="13847-115">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="13847-116">Children</span><span class="sxs-lookup"><span data-stu-id="13847-116">Children</span></span> | [<span data-ttu-id="13847-117">**Param**</span><span class="sxs-lookup"><span data-stu-id="13847-117">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="13847-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="13847-118">Remarks</span></span>

<span data-ttu-id="13847-119">**L'attributo clsid** specifica il sottooggetto che crea l'effetto.</span><span class="sxs-lookup"><span data-stu-id="13847-119">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="13847-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="13847-120">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="13847-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13847-121">Requirements</span></span>



| <span data-ttu-id="13847-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="13847-122">Requirement</span></span> | <span data-ttu-id="13847-123">Valore</span><span class="sxs-lookup"><span data-stu-id="13847-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="13847-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13847-124">Header</span></span><br/> | <dl> <span data-ttu-id="13847-125"><dt>Gdipluseffects.h</dt></span><span class="sxs-lookup"><span data-stu-id="13847-125"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13847-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13847-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13847-127">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="13847-127">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




