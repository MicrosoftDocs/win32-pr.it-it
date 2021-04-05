---
description: Si verifica quando il controllo InkPicture viene ridimensionato (quando cambiano i valori della proprietà Width e/o Height).
ms.assetid: 436db420-f9ea-46f1-b922-c8663371edd5
title: Evento InkPicture. Resize (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c4c5df298658f6ac98ddbf8fc00873f6f22dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057992"
---
# <a name="inkpictureresize-event"></a><span data-ttu-id="28faf-103">Evento InkPicture. Resize</span><span class="sxs-lookup"><span data-stu-id="28faf-103">InkPicture.Resize event</span></span>

<span data-ttu-id="28faf-104">Si verifica quando il controllo [InkPicture](inkpicture-control-reference.md) viene ridimensionato (quando cambiano i valori della proprietà Width e/o Height).</span><span class="sxs-lookup"><span data-stu-id="28faf-104">Occurs when the [InkPicture](inkpicture-control-reference.md) control is resized (when the Width and/or Height property values change).</span></span>

## <a name="syntax"></a><span data-ttu-id="28faf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28faf-105">Syntax</span></span>


```C++
void Resize(
   long Left,
   long Top,
   long Right,
   long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="28faf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28faf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28faf-107">*Sinistra*</span><span class="sxs-lookup"><span data-stu-id="28faf-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="28faf-108">Il numero di pixel del lato sinistro della finestra che contiene il controllo a sinistra del controllo.</span><span class="sxs-lookup"><span data-stu-id="28faf-108">The number of pixels from the left side of the window that contains the control to the left side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="28faf-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="28faf-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="28faf-110">Il numero di pixel dalla parte superiore della finestra che contiene il controllo nella parte superiore del controllo.</span><span class="sxs-lookup"><span data-stu-id="28faf-110">The number of pixels from the top of the window that contains the control to the top of the control.</span></span>

</dd> <dt>

<span data-ttu-id="28faf-111">*Ok*</span><span class="sxs-lookup"><span data-stu-id="28faf-111">*Right*</span></span> 
</dt> <dd>

<span data-ttu-id="28faf-112">Il numero di pixel dal lato sinistro della finestra che contiene il controllo sul lato destro del controllo.</span><span class="sxs-lookup"><span data-stu-id="28faf-112">The number of pixels from the left side of the window that contains the control to the right side of the control.</span></span>

</dd> <dt>

<span data-ttu-id="28faf-113">*Ultimo*</span><span class="sxs-lookup"><span data-stu-id="28faf-113">*Bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="28faf-114">Il numero di pixel dalla parte superiore della finestra che contiene il controllo nella parte inferiore del controllo.</span><span class="sxs-lookup"><span data-stu-id="28faf-114">The number of pixels from the top of the window that contains the control to the bottom of the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28faf-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28faf-115">Return value</span></span>

<span data-ttu-id="28faf-116">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="28faf-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="28faf-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="28faf-117">Remarks</span></span>

<span data-ttu-id="28faf-118">La nuova larghezza del controllo in pixel sarà uguale alla differenza tra i parametri *destro* e *sinistro* .</span><span class="sxs-lookup"><span data-stu-id="28faf-118">The new width of the control in pixels will be equal to the difference between the *Right* and *Left* parameters.</span></span> <span data-ttu-id="28faf-119">Analogamente, la nuova altezza sarà uguale alla differenza tra *Bottom* e *Top*.</span><span class="sxs-lookup"><span data-stu-id="28faf-119">Likewise, the new height will be equal to the difference between *Bottom* and *Top*.</span></span>

<span data-ttu-id="28faf-120">Questo metodo di evento è definito nell'interfaccia **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="28faf-120">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="28faf-121">L'interfaccia **\_ IInkPictureEvents** implementa l'interfaccia IDispatch con un identificatore di **DISPID \_ IPEResize**.</span><span class="sxs-lookup"><span data-stu-id="28faf-121">The **\_IInkPictureEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IPEResize**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28faf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28faf-122">Requirements</span></span>



| <span data-ttu-id="28faf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="28faf-123">Requirement</span></span> | <span data-ttu-id="28faf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="28faf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28faf-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28faf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="28faf-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="28faf-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="28faf-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28faf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="28faf-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="28faf-128">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="28faf-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28faf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="28faf-130"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="28faf-130"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="28faf-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="28faf-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="28faf-132"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28faf-132"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="28faf-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28faf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28faf-134">InkPicture</span><span class="sxs-lookup"><span data-stu-id="28faf-134">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




