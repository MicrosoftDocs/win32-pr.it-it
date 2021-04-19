---
description: L'elemento Effect definisce un oggetto effetto audio o video. Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.
ms.assetid: aedb4491-f1f0-44b3-ad88-3fac8c90144d
title: Elemento Effect (Gdipluseffects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dd31e85407b99c3dffd4417a051be168f7c6d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332050"
---
# <a name="effect-element"></a><span data-ttu-id="b07e5-104">Elemento Effect</span><span class="sxs-lookup"><span data-stu-id="b07e5-104">effect Element</span></span>

> [!Note]  
> <span data-ttu-id="b07e5-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b07e5-105">\[Deprecated.</span></span> <span data-ttu-id="b07e5-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b07e5-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b07e5-107">L' `effect` elemento definisce un oggetto effetto audio o video.</span><span class="sxs-lookup"><span data-stu-id="b07e5-107">The `effect` element defines an audio or video effect object.</span></span> <span data-ttu-id="b07e5-108">Un effetto viene applicato a un singolo flusso, ad esempio una composizione, una traccia o un'origine.</span><span class="sxs-lookup"><span data-stu-id="b07e5-108">An effect is applied to a single stream (such as a composition, track, or source).</span></span>

## <a name="attributes"></a><span data-ttu-id="b07e5-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="b07e5-109">Attributes</span></span>

<span data-ttu-id="b07e5-110">[**CLSID**](clsid-attribute.md), [**Lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**Start**](start-attribute.md), [**Stop**](stop-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="b07e5-110">[**clsid**](clsid-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="b07e5-111">Informazioni padre/figlio</span><span class="sxs-lookup"><span data-stu-id="b07e5-111">Parent/Child Information</span></span>



|          |                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07e5-112">Padre</span><span class="sxs-lookup"><span data-stu-id="b07e5-112">Parent</span></span>   | <span data-ttu-id="b07e5-113">[**composito**](composite-element.md), [**gruppo**](group-element.md), [**clip**](clip-element.md), [**traccia**](track-element.md)</span><span class="sxs-lookup"><span data-stu-id="b07e5-113">[**composite**](composite-element.md), [**group**](group-element.md), [**clip**](clip-element.md), [**track**](track-element.md)</span></span> |
| <span data-ttu-id="b07e5-114">Children</span><span class="sxs-lookup"><span data-stu-id="b07e5-114">Children</span></span> | [<span data-ttu-id="b07e5-115">**param**</span><span class="sxs-lookup"><span data-stu-id="b07e5-115">**param**</span></span>](param-element.md)                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b07e5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b07e5-116">Remarks</span></span>

<span data-ttu-id="b07e5-117">L'attributo **CLSID** specifica l'oggetto SubObject che crea l'effetto.</span><span class="sxs-lookup"><span data-stu-id="b07e5-117">The **clsid** attribute specifies the subobject that creates the effect.</span></span>

## <a name="examples"></a><span data-ttu-id="b07e5-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="b07e5-118">Examples</span></span>


```XML
<effect clsid="{b05a941c-3ce1-11d2-952a-00c04fa34f05}" start="0" stop="32.0" />
```



## <a name="requirements"></a><span data-ttu-id="b07e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b07e5-119">Requirements</span></span>



| <span data-ttu-id="b07e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b07e5-120">Requirement</span></span> | <span data-ttu-id="b07e5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b07e5-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b07e5-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b07e5-122">Header</span></span><br/> | <dl> <span data-ttu-id="b07e5-123"><dt>Gdipluseffects. h</dt></span><span class="sxs-lookup"><span data-stu-id="b07e5-123"><dt>Gdipluseffects.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b07e5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b07e5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07e5-125">Elementi XTL</span><span class="sxs-lookup"><span data-stu-id="b07e5-125">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 




