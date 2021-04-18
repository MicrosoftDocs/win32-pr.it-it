---
title: AmbientAttributes. MoveTo
description: Il metodo MoveTo sposta il controllo in una nuova posizione a una velocità lineare.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Media Player di Windows AmbientAttributes. MoveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327170"
---
# <a name="ambientattributesmoveto"></a><span data-ttu-id="d7dca-104">AmbientAttributes. MoveTo</span><span class="sxs-lookup"><span data-stu-id="d7dca-104">AmbientAttributes.moveTo</span></span>

<span data-ttu-id="d7dca-105">Il metodo **MoveTo** sposta il controllo in una nuova posizione a una velocità lineare.</span><span class="sxs-lookup"><span data-stu-id="d7dca-105">The **moveTo** method moves the control to a new location at a linear speed.</span></span>

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a><span data-ttu-id="d7dca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7dca-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span><span class="sxs-lookup"><span data-stu-id="d7dca-107"><span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*</span></span>
</dt> <dd>

<span data-ttu-id="d7dca-108">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Left** del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7dca-108">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d7dca-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span><span class="sxs-lookup"><span data-stu-id="d7dca-109"><span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*</span></span>
</dt> <dd>

<span data-ttu-id="d7dca-110">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Top** del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7dca-110">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="d7dca-111"><span id="time"></span><span id="TIME"></span>*tempo*</span><span class="sxs-lookup"><span data-stu-id="d7dca-111"><span id="time"></span><span id="TIME"></span>*time*</span></span>
</dt> <dd>

<span data-ttu-id="d7dca-112">**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="d7dca-112">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7dca-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7dca-113">Return Value</span></span>

<span data-ttu-id="d7dca-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d7dca-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7dca-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7dca-115">Remarks</span></span>

<span data-ttu-id="d7dca-116">Questo metodo è utile per gli elementi di **Sottovisualizzazione** animati (ad esempio, se l'utente fa clic su un vassoio e i controlli scorrono verso il basso).</span><span class="sxs-lookup"><span data-stu-id="d7dca-116">This method is useful for animated **SUBVIEW** elements (for example, if the user clicks a tray and the controls slide down).</span></span>

<span data-ttu-id="d7dca-117">Questo metodo crea un movimento lineare durante lo spostamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="d7dca-117">This method creates a linear motion when moving the control.</span></span> <span data-ttu-id="d7dca-118">Questo comportamento è diverso da **slideTo**, che consente di creare un movimento non lineare.</span><span class="sxs-lookup"><span data-stu-id="d7dca-118">This differs from **slideTo**, which creates a non-linear motion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7dca-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7dca-119">Requirements</span></span>



| <span data-ttu-id="d7dca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7dca-120">Requirement</span></span> | <span data-ttu-id="d7dca-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d7dca-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d7dca-122">Versione</span><span class="sxs-lookup"><span data-stu-id="d7dca-122">Version</span></span><br/> | <span data-ttu-id="d7dca-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d7dca-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7dca-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7dca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7dca-125">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="d7dca-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7dca-126">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="d7dca-126">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="d7dca-127">**AmbientAttributes.slideTo**</span><span class="sxs-lookup"><span data-stu-id="d7dca-127">**AmbientAttributes.slideTo**</span></span>](ambientattributes-slideto.md)
</dt> <dt>

[<span data-ttu-id="d7dca-128">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="d7dca-128">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





