---
description: Si verifica quando un utente fa clic sul controllo InkPicture.
ms.assetid: 326bac37-2d5d-434b-916c-8a675bab5052
title: Evento InkPicture. Click (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1dd90cd69555f65531f5ab2684f886dab23e191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884373"
---
# <a name="inkpictureclick-event"></a><span data-ttu-id="6e0c6-103">Evento InkPicture. Click</span><span class="sxs-lookup"><span data-stu-id="6e0c6-103">InkPicture.Click event</span></span>

<span data-ttu-id="6e0c6-104">Si verifica quando un utente fa clic sul controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0c6-104">Occurs when a user clicks the [InkPicture](inkpicture-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e0c6-105">Syntax</span></span>


```C++
void Click();
```



## <a name="parameters"></a><span data-ttu-id="6e0c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e0c6-106">Parameters</span></span>

<span data-ttu-id="6e0c6-107">Questo evento non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e0c6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e0c6-108">Return value</span></span>

<span data-ttu-id="6e0c6-109">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e0c6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e0c6-110">Remarks</span></span>

<span data-ttu-id="6e0c6-111">Se si fa clic su un controllo, vengono generati eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) oltre all'evento click.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-111">Clicking a control generates [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events in addition to the Click event.</span></span>

> [!Note]  
> <span data-ttu-id="6e0c6-112">Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="6e0c6-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span>

 

<span data-ttu-id="6e0c6-113">Se nell'evento **Click** è presente codice, l'evento [**DblClick**](inkpicture-dblclick.md) non verrà mai attivato, perché l'evento **Click** è il primo evento da attivare tra i due.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-113">If there is code in the **Click** event, the [**DblClick**](inkpicture-dblclick.md) event will never trigger, because the **Click** event is the first event to trigger between the two.</span></span> <span data-ttu-id="6e0c6-114">Di conseguenza, il clic del mouse viene intercettato dall'evento **Click** , quindi l'evento **DblClick** non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-114">As a result, the mouse click is intercepted by the **Click** event, so the **DblClick** event doesn't occur.</span></span>

<span data-ttu-id="6e0c6-115">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="6e0c6-115">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="6e0c6-116">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEClick**.</span><span class="sxs-lookup"><span data-stu-id="6e0c6-116">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0c6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e0c6-117">Requirements</span></span>



| <span data-ttu-id="6e0c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e0c6-118">Requirement</span></span> | <span data-ttu-id="6e0c6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6e0c6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0c6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0c6-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6e0c6-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6e0c6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e0c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0c6-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6e0c6-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6e0c6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e0c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e0c6-125"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c6-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6e0c6-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e0c6-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e0c6-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e0c6-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6e0c6-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e0c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0c6-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6e0c6-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




