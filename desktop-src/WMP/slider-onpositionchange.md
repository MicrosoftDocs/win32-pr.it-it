---
title: SLIDER. onPositionChange
description: Il gestore dell'evento onPositionChange gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente. | SLIDER. onPositionChange
ms.assetid: c18e9a49-9576-42ae-9f30-249c44d40f41
keywords:
- Media Player Windows SLIDER. onPositionChange
topic_type:
- apiref
api_name:
- SLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68faa9e7addd85b9b5f02b8a6c445e7ddf54e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330721"
---
# <a name="slideronpositionchange"></a><span data-ttu-id="0062b-105">SLIDER. onPositionChange</span><span class="sxs-lookup"><span data-stu-id="0062b-105">SLIDER.onPositionChange</span></span>

<span data-ttu-id="0062b-106">Il gestore dell'evento **onPositionChange** gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0062b-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="0062b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="0062b-107">Remarks</span></span>

<span data-ttu-id="0062b-108">Se la posizione del dispositivo di scorrimento cambia in seguito all'attributo **value** modificato nello script, questo evento non viene generato.</span><span class="sxs-lookup"><span data-stu-id="0062b-108">If the position of the slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="0062b-109">Per soddisfare questa possibilità, implementare invece il gestore eventi **\_ OnChange del valore** .</span><span class="sxs-lookup"><span data-stu-id="0062b-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="0062b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0062b-110">Requirements</span></span>



| <span data-ttu-id="0062b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="0062b-111">Requirement</span></span> | <span data-ttu-id="0062b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="0062b-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0062b-113">Versione</span><span class="sxs-lookup"><span data-stu-id="0062b-113">Version</span></span><br/> | <span data-ttu-id="0062b-114">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="0062b-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0062b-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0062b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0062b-116">**Elemento SLIDER**</span><span class="sxs-lookup"><span data-stu-id="0062b-116">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





