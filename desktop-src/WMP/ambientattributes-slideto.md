---
title: AmbientAttributes.slideTo
description: Il metodo slideTo sposta il controllo in una nuova posizione. Il controllo viene spostato in modo non lineare nel periodo di tempo specificato.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Media Player Windows AmbientAttributes. slideTo
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332148"
---
# <a name="ambientattributesslideto"></a><span data-ttu-id="cab98-105">AmbientAttributes.slideTo</span><span class="sxs-lookup"><span data-stu-id="cab98-105">AmbientAttributes.slideTo</span></span>

<span data-ttu-id="cab98-106">Il metodo **slideTo** sposta il controllo in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="cab98-106">The **slideTo** method moves the control to a new location.</span></span> <span data-ttu-id="cab98-107">Il controllo viene spostato in modo non lineare nel periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="cab98-107">The control moves in a non-linear fashion over the specified time period.</span></span>

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a><span data-ttu-id="cab98-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cab98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cab98-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="cab98-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="cab98-110">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Left** del controllo.</span><span class="sxs-lookup"><span data-stu-id="cab98-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="cab98-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="cab98-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="cab98-112">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Top** del controllo.</span><span class="sxs-lookup"><span data-stu-id="cab98-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="cab98-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="cab98-113"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="cab98-114">**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="cab98-114">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cab98-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cab98-115">Return Value</span></span>

<span data-ttu-id="cab98-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="cab98-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cab98-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cab98-117">Remarks</span></span>

<span data-ttu-id="cab98-118">Questo metodo è diverso da **MoveTo**, che crea un movimento lineare durante lo spostamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="cab98-118">This method is different from **moveTo**, which creates a linear motion when moving the control.</span></span> <span data-ttu-id="cab98-119">Il movimento non lineare creato da questo metodo è un movimento scorrevole che accelera da una velocità pari a zero all'inizio del movimento e rallenta fino a zero alla fine, arrivando a un punto di arresto.</span><span class="sxs-lookup"><span data-stu-id="cab98-119">The non-linear motion created by this method is a sliding motion that accelerates from a speed of zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="cab98-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cab98-120">Requirements</span></span>



| <span data-ttu-id="cab98-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cab98-121">Requirement</span></span> | <span data-ttu-id="cab98-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cab98-122">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="cab98-123">Versione</span><span class="sxs-lookup"><span data-stu-id="cab98-123">Version</span></span><br/> | <span data-ttu-id="cab98-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="cab98-124">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cab98-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cab98-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cab98-126">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="cab98-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="cab98-127">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="cab98-127">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="cab98-128">**AmbientAttributes. MoveTo**</span><span class="sxs-lookup"><span data-stu-id="cab98-128">**AmbientAttributes.moveTo**</span></span>](ambientattributes-moveto.md)
</dt> <dt>

[<span data-ttu-id="cab98-129">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="cab98-129">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> </dl>

 

 





