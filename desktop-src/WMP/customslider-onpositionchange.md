---
title: CUSTOMSLIDER. onPositionChange
description: Il gestore dell'evento onPositionChange gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente. | CUSTOMSLIDER. onPositionChange
ms.assetid: d8fe99a2-69ff-4e75-8d7d-506bcb2f75bf
keywords:
- Media Player Windows CUSTOMSLIDER. onPositionChange
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.onPositionChange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3d5547d66ca6dc1b770242301bd95ed010a8d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328414"
---
# <a name="customslideronpositionchange"></a><span data-ttu-id="d9a48-105">CUSTOMSLIDER. onPositionChange</span><span class="sxs-lookup"><span data-stu-id="d9a48-105">CUSTOMSLIDER.onPositionChange</span></span>

<span data-ttu-id="d9a48-106">Il gestore dell'evento **onPositionChange** gestisce un evento che si verifica quando la posizione del dispositivo di scorrimento viene modificata in seguito alla selezione o al trascinamento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9a48-106">The **onPositionChange** event handler handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>

``` syntax
onPositionChange
```

## <a name="remarks"></a><span data-ttu-id="d9a48-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9a48-107">Remarks</span></span>

<span data-ttu-id="d9a48-108">Se la posizione del dispositivo di scorrimento personalizzato cambia in seguito all'attributo **value** modificato nello script, questo evento non viene generato.</span><span class="sxs-lookup"><span data-stu-id="d9a48-108">If the position of the custom slider changes as a result of the **value** attribute being modified in script, this event is not fired.</span></span> <span data-ttu-id="d9a48-109">Per soddisfare questa possibilità, implementare invece il gestore eventi **\_ OnChange del valore** .</span><span class="sxs-lookup"><span data-stu-id="d9a48-109">To accommodate this possibility, implement the **value\_onchange** event handler instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a48-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9a48-110">Requirements</span></span>



| <span data-ttu-id="d9a48-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9a48-111">Requirement</span></span> | <span data-ttu-id="d9a48-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d9a48-112">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d9a48-113">Versione</span><span class="sxs-lookup"><span data-stu-id="d9a48-113">Version</span></span><br/> | <span data-ttu-id="d9a48-114">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d9a48-114">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9a48-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9a48-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a48-116">**Elemento CUSTOMSLIDER**</span><span class="sxs-lookup"><span data-stu-id="d9a48-116">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> </dl>

 

 





