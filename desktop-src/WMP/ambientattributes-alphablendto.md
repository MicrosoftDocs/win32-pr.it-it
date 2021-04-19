---
title: AmbientAttributes.alphaBlendTo
description: Il metodo alphaBlendTo regola la proprietà alphaBlend in un determinato periodo di tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- Media Player Windows AmbientAttributes. alphaBlendTo
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326736"
---
# <a name="ambientattributesalphablendto"></a><span data-ttu-id="3a018-104">AmbientAttributes.alphaBlendTo</span><span class="sxs-lookup"><span data-stu-id="3a018-104">AmbientAttributes.alphaBlendTo</span></span>

<span data-ttu-id="3a018-105">Il metodo **alphaBlendTo** regola la proprietà **alphaBlend** in un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="3a018-105">The **alphaBlendTo** method adjusts the **alphaBlend** property over a period of time.</span></span>

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a><span data-ttu-id="3a018-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a018-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a018-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span><span class="sxs-lookup"><span data-stu-id="3a018-107"><span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*</span></span>
</dt> <dd>

<span data-ttu-id="3a018-108">**Numero** (Long) che specifica il nuovo valore di opacità.</span><span class="sxs-lookup"><span data-stu-id="3a018-108">**Number** (long) specifying the new opacity value.</span></span> <span data-ttu-id="3a018-109">L'intervallo è compreso tra 0 (nessuna opacità) e 255 (opacità completa).</span><span class="sxs-lookup"><span data-stu-id="3a018-109">Ranges from 0 (no opacity) to 255 (full opacity).</span></span>

</dd> <dt>

<span data-ttu-id="3a018-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span><span class="sxs-lookup"><span data-stu-id="3a018-110"><span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*</span></span>
</dt> <dd>

<span data-ttu-id="3a018-111">**Numero** (**Long**) che specifica l'intervallo di tempo, in millisecondi, impiegato dall'elemento per modificare l'opacità.</span><span class="sxs-lookup"><span data-stu-id="3a018-111">**Number** (**long**) specifying the time, in milliseconds, that it takes the element to change opacity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a018-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a018-112">Return Value</span></span>

<span data-ttu-id="3a018-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3a018-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a018-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a018-114">Remarks</span></span>

<span data-ttu-id="3a018-115">Questo metodo è utile per far apparire o scomparire elementi gradualmente.</span><span class="sxs-lookup"><span data-stu-id="3a018-115">This method is useful for making elements gradually appear or disappear.</span></span>

<span data-ttu-id="3a018-116">Quando si usa **alphaBlendTo** con un elemento di **testo** che non ha il valore **BackgroundColor** specificato, verrà usato un colore di sfondo nero.</span><span class="sxs-lookup"><span data-stu-id="3a018-116">When you use **alphaBlendTo** with a **TEXT** element that does not have the **backgroundColor** specified, a background color of black will be used.</span></span> <span data-ttu-id="3a018-117">Se il colore di primo piano è anche nero (ovvero il valore predefinito per il *testo*.**foregroundColor**), il testo potrebbe diventare illeggibile.</span><span class="sxs-lookup"><span data-stu-id="3a018-117">If the foreground color is also black (which is the default value for *TEXT*.**foregroundColor**), your text may become unreadable.</span></span> <span data-ttu-id="3a018-118">Per evitare questo problema, specificare sempre l'attributo **BackgroundColor** o impostare **ForegroundColor** su un colore diverso dal nero.</span><span class="sxs-lookup"><span data-stu-id="3a018-118">To prevent this, always specify the **backgroundColor** attribute, or set **foregroundColor** to a color other than black.</span></span>

> [!Note]  
> <span data-ttu-id="3a018-119">Questo attributo non è supportato in Windows 98.</span><span class="sxs-lookup"><span data-stu-id="3a018-119">This attribute is not supported in Windows 98.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3a018-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a018-120">Requirements</span></span>



| <span data-ttu-id="3a018-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a018-121">Requirement</span></span> | <span data-ttu-id="3a018-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3a018-122">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3a018-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3a018-123">Version</span></span><br/> | <span data-ttu-id="3a018-124">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3a018-124">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a018-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a018-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a018-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="3a018-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="3a018-127">**AmbientAttributes. alphaBlend**</span><span class="sxs-lookup"><span data-stu-id="3a018-127">**AmbientAttributes.alphaBlend**</span></span>](ambientattributes-alphablend.md)
</dt> <dt>

[<span data-ttu-id="3a018-128">**Elemento TEXT**</span><span class="sxs-lookup"><span data-stu-id="3a018-128">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="3a018-129">**TESTO. backgroundColor**</span><span class="sxs-lookup"><span data-stu-id="3a018-129">**TEXT.backgroundColor**</span></span>](text-backgroundcolor.md)
</dt> <dt>

[<span data-ttu-id="3a018-130">**TESTO. foregroundColor**</span><span class="sxs-lookup"><span data-stu-id="3a018-130">**TEXT.foregroundColor**</span></span>](text-foregroundcolor.md)
</dt> </dl>

 

 





