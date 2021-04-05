---
description: Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto InkCollector o InkOverlay dispone dello stato attivo.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884937"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="ecf30-103">InkOverlay. MouseWheel (evento)</span><span class="sxs-lookup"><span data-stu-id="ecf30-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="ecf30-104">Si verifica quando viene spostata la rotellina del mouse mentre l'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) dispone dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="ecf30-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf30-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecf30-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ecf30-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecf30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf30-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="ecf30-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ecf30-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="ecf30-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ecf30-111">*Delta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-112">Conteggio con segno del numero di arresti ruotati della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecf30-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="ecf30-113">Un dentello corrisponde a uno scatto della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecf30-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="ecf30-114">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-115">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecf30-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ecf30-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-117">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="ecf30-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ecf30-118">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecf30-119">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="ecf30-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="ecf30-120">Il valore predefinito è **false**, che specifica che l'evento non deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="ecf30-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf30-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecf30-121">Return value</span></span>

<span data-ttu-id="ecf30-122">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ecf30-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf30-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecf30-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ecf30-124">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="ecf30-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ecf30-125">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="ecf30-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="ecf30-126">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="ecf30-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf30-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecf30-127">Requirements</span></span>



| <span data-ttu-id="ecf30-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf30-128">Requirement</span></span> | <span data-ttu-id="ecf30-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ecf30-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf30-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecf30-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf30-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ecf30-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ecf30-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecf30-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf30-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ecf30-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ecf30-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecf30-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf30-135"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ecf30-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ecf30-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecf30-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecf30-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf30-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ecf30-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecf30-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf30-139">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="ecf30-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ecf30-140">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="ecf30-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ecf30-141">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="ecf30-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




