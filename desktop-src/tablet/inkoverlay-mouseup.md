---
description: Si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene rilasciato un pulsante del mouse.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Evento InkOverlay. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16fd3dc5006f43e09e093cb2c474a8578f56c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233183"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="093dd-103">InkOverlay. MouseUp (evento)</span><span class="sxs-lookup"><span data-stu-id="093dd-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="093dd-104">Si verifica quando il puntatore del mouse si trova sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene rilasciato un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="093dd-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="093dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="093dd-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="093dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="093dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="093dd-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="093dd-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093dd-108">Pulsante del mouse rilasciato.</span><span class="sxs-lookup"><span data-stu-id="093dd-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="093dd-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="093dd-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093dd-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="093dd-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="093dd-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="093dd-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093dd-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="093dd-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="093dd-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="093dd-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="093dd-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="093dd-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="093dd-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="093dd-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="093dd-116">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="093dd-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="093dd-117">Il valore predefinito è **false**, che specifica che l'evento non deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="093dd-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="093dd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="093dd-118">Return value</span></span>

<span data-ttu-id="093dd-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="093dd-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="093dd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="093dd-120">Remarks</span></span>

<span data-ttu-id="093dd-121">Per migliorare le prestazioni in tempo reale dell'input penna, nascondere o mostrare il cursore del mouse nei gestori eventi [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="093dd-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="093dd-122">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="093dd-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="093dd-123">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="093dd-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="093dd-124">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="093dd-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="093dd-125">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="093dd-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="093dd-126">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseUp.</span><span class="sxs-lookup"><span data-stu-id="093dd-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="093dd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="093dd-127">Requirements</span></span>



| <span data-ttu-id="093dd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="093dd-128">Requirement</span></span> | <span data-ttu-id="093dd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="093dd-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="093dd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093dd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="093dd-131">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="093dd-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="093dd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="093dd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="093dd-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="093dd-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="093dd-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="093dd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="093dd-135"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="093dd-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="093dd-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="093dd-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="093dd-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="093dd-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="093dd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="093dd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="093dd-139">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="093dd-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="093dd-140">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="093dd-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="093dd-141">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="093dd-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




