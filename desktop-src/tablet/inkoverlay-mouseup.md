---
description: "Evento InkOverlay.MouseUp: si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene rilasciato un pulsante del mouse."
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Evento InkOverlay.MouseUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402083aa677b134ea469980227a482ac5546da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086809"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="80e78-103">Evento InkOverlay.MouseUp</span><span class="sxs-lookup"><span data-stu-id="80e78-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="80e78-104">Si verifica quando il puntatore del mouse si trova [**sull'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene rilasciato un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="80e78-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e78-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80e78-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="80e78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80e78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e78-107">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80e78-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e78-108">Pulsante del mouse rilasciato.</span><span class="sxs-lookup"><span data-stu-id="80e78-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="80e78-109">*MAIUSC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80e78-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e78-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="80e78-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="80e78-111">*pX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80e78-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e78-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="80e78-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="80e78-113">*pY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="80e78-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e78-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="80e78-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="80e78-115">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="80e78-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e78-116">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="80e78-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="80e78-117">Il valore predefinito è **FALSE,** che specifica che l'evento non deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="80e78-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e78-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80e78-118">Return value</span></span>

<span data-ttu-id="80e78-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="80e78-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80e78-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="80e78-120">Remarks</span></span>

<span data-ttu-id="80e78-121">Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="80e78-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="80e78-122">Le proprietà *pX* e *pY* sono espresse in pixel e non nelle unità HIMETRIC associate allo spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="80e78-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="80e78-123">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione inconsapevole e questo tipo di applicazione comprende solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="80e78-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="80e78-124">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md) [**e MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="80e78-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="80e78-125">L'annullamento di alcuni di questi eventi può avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="80e78-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="80e78-126">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseUp.</span><span class="sxs-lookup"><span data-stu-id="80e78-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e78-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80e78-127">Requirements</span></span>



| <span data-ttu-id="80e78-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e78-128">Requirement</span></span> | <span data-ttu-id="80e78-129">Valore</span><span class="sxs-lookup"><span data-stu-id="80e78-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e78-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e78-130">Minimum supported client</span></span><br/> | <span data-ttu-id="80e78-131">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="80e78-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="80e78-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80e78-132">Minimum supported server</span></span><br/> | <span data-ttu-id="80e78-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="80e78-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="80e78-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80e78-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e78-135"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="80e78-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="80e78-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="80e78-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="80e78-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e78-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="80e78-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80e78-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e78-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="80e78-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="80e78-140">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="80e78-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="80e78-141">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="80e78-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




