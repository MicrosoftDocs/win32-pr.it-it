---
title: AmbientAttributes.moveSizeTo
description: Il metodo moveSizeTo sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione. Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- Media Player Windows AmbientAttributes. moveSizeTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326033"
---
# <a name="ambientattributesmovesizeto"></a><span data-ttu-id="747ff-105">AmbientAttributes.moveSizeTo</span><span class="sxs-lookup"><span data-stu-id="747ff-105">AmbientAttributes.moveSizeTo</span></span>

<span data-ttu-id="747ff-106">Il metodo **moveSizeTo** sposta il controllo e specifica una nuova dimensione per il controllo nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="747ff-106">The **moveSizeTo** method moves the control and specifies a new size for the control in the new location.</span></span> <span data-ttu-id="747ff-107">Il controllo viene spostato e ridimensionato in modo animato nel periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="747ff-107">The control moves and resizes in an animated fashion over the specified time period.</span></span>

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a><span data-ttu-id="747ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="747ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747ff-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span><span class="sxs-lookup"><span data-stu-id="747ff-109"><span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-110">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Left** del controllo.</span><span class="sxs-lookup"><span data-stu-id="747ff-110">**Number** (**long**) specifying the new value for the **left** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="747ff-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span><span class="sxs-lookup"><span data-stu-id="747ff-111"><span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-112">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Top** del controllo.</span><span class="sxs-lookup"><span data-stu-id="747ff-112">**Number** (**long**) specifying the new value for the **top** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="747ff-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span><span class="sxs-lookup"><span data-stu-id="747ff-113"><span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-114">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Width** del controllo.</span><span class="sxs-lookup"><span data-stu-id="747ff-114">**Number** (**long**) specifying the new value for the **width** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="747ff-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span><span class="sxs-lookup"><span data-stu-id="747ff-115"><span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-116">**Number** (**Long**) che specifica il nuovo valore per l'attributo **Height** del controllo.</span><span class="sxs-lookup"><span data-stu-id="747ff-116">**Number** (**long**) specifying the new value for the **height** attribute of the control.</span></span>

</dd> <dt>

<span data-ttu-id="747ff-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span><span class="sxs-lookup"><span data-stu-id="747ff-117"><span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-118">**Numero** (**Long**) che specifica il tempo, in millisecondi, necessario affinché il controllo venga spostato nella nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="747ff-118">**Number** (**long**) specifying the time, in milliseconds, that it takes for the control to move to its new location.</span></span>

</dd> <dt>

<span data-ttu-id="747ff-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span><span class="sxs-lookup"><span data-stu-id="747ff-119"><span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*</span></span>
</dt> <dd>

<span data-ttu-id="747ff-120">**Valore booleano** che specifica il tipo di movimento creato durante lo spostamento del controllo.</span><span class="sxs-lookup"><span data-stu-id="747ff-120">**Boolean** specifying the type of motion created when moving the control.</span></span>



| <span data-ttu-id="747ff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="747ff-121">Value</span></span> | <span data-ttu-id="747ff-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="747ff-122">Description</span></span>                                                             |
|-------|-------------------------------------------------------------------------|
| <span data-ttu-id="747ff-123">true</span><span class="sxs-lookup"><span data-stu-id="747ff-123">true</span></span>  | <span data-ttu-id="747ff-124">Il movimento è non lineare (movimento scorrevole che accelera e decelera).</span><span class="sxs-lookup"><span data-stu-id="747ff-124">Motion is non-linear (sliding motion that accelerates and decelerates).</span></span> |
| <span data-ttu-id="747ff-125">false</span><span class="sxs-lookup"><span data-stu-id="747ff-125">false</span></span> | <span data-ttu-id="747ff-126">Il movimento è lineare.</span><span class="sxs-lookup"><span data-stu-id="747ff-126">Motion is linear.</span></span>                                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747ff-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="747ff-127">Return Value</span></span>

<span data-ttu-id="747ff-128">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="747ff-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="747ff-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="747ff-129">Remarks</span></span>

<span data-ttu-id="747ff-130">Il movimento del controllo può essere lineare o non lineare.</span><span class="sxs-lookup"><span data-stu-id="747ff-130">The motion of the control can be linear or non-linear.</span></span> <span data-ttu-id="747ff-131">Movimento lineare significa che il controllo si sposta a una velocità costante nella nuova posizione, avviando e interrompendo bruscamente.</span><span class="sxs-lookup"><span data-stu-id="747ff-131">Linear motion means the control moves at a constant speed to its new location, starting and stopping abruptly.</span></span> <span data-ttu-id="747ff-132">Quando si specifica un movimento non lineare, viene creato un movimento scorrevole che accelera da zero all'inizio del movimento e rallenta fino a zero alla fine, arrivando a un punto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="747ff-132">When non-linear motion is specified, a sliding motion is created that accelerates from zero at the beginning of the motion and decelerates back to zero at the end, coming to a smooth stop.</span></span>

## <a name="requirements"></a><span data-ttu-id="747ff-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="747ff-133">Requirements</span></span>



| <span data-ttu-id="747ff-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="747ff-134">Requirement</span></span> | <span data-ttu-id="747ff-135">Valore</span><span class="sxs-lookup"><span data-stu-id="747ff-135">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="747ff-136">Versione</span><span class="sxs-lookup"><span data-stu-id="747ff-136">Version</span></span><br/> | <span data-ttu-id="747ff-137">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="747ff-137">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="747ff-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="747ff-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747ff-139">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="747ff-139">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="747ff-140">**AmbientAttributes. Height**</span><span class="sxs-lookup"><span data-stu-id="747ff-140">**AmbientAttributes.height**</span></span>](ambientattributes-height.md)
</dt> <dt>

[<span data-ttu-id="747ff-141">**AmbientAttributes. Left**</span><span class="sxs-lookup"><span data-stu-id="747ff-141">**AmbientAttributes.left**</span></span>](ambientattributes-left.md)
</dt> <dt>

[<span data-ttu-id="747ff-142">**AmbientAttributes.top**</span><span class="sxs-lookup"><span data-stu-id="747ff-142">**AmbientAttributes.top**</span></span>](ambientattributes-top.md)
</dt> <dt>

[<span data-ttu-id="747ff-143">**AmbientAttributes. Width**</span><span class="sxs-lookup"><span data-stu-id="747ff-143">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> </dl>

 

 





