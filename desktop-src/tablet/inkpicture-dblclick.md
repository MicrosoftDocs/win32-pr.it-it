---
description: Si verifica quando si fa doppio clic sul controllo InkPicture.
ms.assetid: 5b2a6413-d415-4bf1-a291-35f4c3c5a0dc
title: Evento InkPicture. DblClick (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c3d9bb9125c8142186da969acf6ce03f5f76b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347886"
---
# <a name="inkpicturedblclick-event"></a><span data-ttu-id="d2dae-103">Evento InkPicture. DblClick</span><span class="sxs-lookup"><span data-stu-id="d2dae-103">InkPicture.DblClick event</span></span>

<span data-ttu-id="d2dae-104">Si verifica quando si fa doppio clic sul controllo [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d2dae-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is double-clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2dae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2dae-105">Syntax</span></span>


```C++
void DblClick(
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d2dae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2dae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2dae-107">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d2dae-107">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2dae-108">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="d2dae-108">Whether the event should be canceled for the parent control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2dae-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2dae-109">Return value</span></span>

<span data-ttu-id="d2dae-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d2dae-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2dae-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2dae-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2dae-112">Per distinguere tra i pulsanti sinistro, destro e centrale del mouse, utilizzare gli eventi [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="d2dae-112">To distinguish between the left, right, and middle mouse buttons, use the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="d2dae-113">Se nell'evento [**Click**](inkpicture-click.md) è presente codice, l'evento **DblClick** non verrà mai attivato.</span><span class="sxs-lookup"><span data-stu-id="d2dae-113">If there is code in the [**Click**](inkpicture-click.md) event, the **DblClick** event will never trigger.</span></span>

 

<span data-ttu-id="d2dae-114">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="d2dae-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="d2dae-115">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEDblClick**.</span><span class="sxs-lookup"><span data-stu-id="d2dae-115">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEDblClick**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2dae-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2dae-116">Requirements</span></span>



| <span data-ttu-id="d2dae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2dae-117">Requirement</span></span> | <span data-ttu-id="d2dae-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d2dae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2dae-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2dae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2dae-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d2dae-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d2dae-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2dae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2dae-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d2dae-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d2dae-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2dae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2dae-124"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d2dae-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2dae-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="d2dae-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2dae-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2dae-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d2dae-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2dae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2dae-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d2dae-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




