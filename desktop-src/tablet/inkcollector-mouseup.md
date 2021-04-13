---
description: Si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene rilasciato un pulsante del mouse.
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: Evento InkCollector. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f217cf6f5eeff930c1746d1a5ceac180686942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484372"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="2c8fb-103">Evento InkCollector. MouseUp</span><span class="sxs-lookup"><span data-stu-id="2c8fb-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="2c8fb-104">Si verifica quando il puntatore del mouse si trova sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene rilasciato un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c8fb-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="2c8fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c8fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8fb-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-108">Pulsante del mouse rilasciato.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="2c8fb-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="2c8fb-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2c8fb-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="2c8fb-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-116">**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8fb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c8fb-117">Return value</span></span>

<span data-ttu-id="2c8fb-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8fb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c8fb-119">Remarks</span></span>

<span data-ttu-id="2c8fb-120">Per migliorare le prestazioni in tempo reale dell'input penna, nascondere o mostrare il cursore del mouse nei gestori eventi [**MouseDown**](inkcollector-mousedown.md) e **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="2c8fb-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="2c8fb-121">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="2c8fb-122">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c8fb-123">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="2c8fb-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="2c8fb-124">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="2c8fb-125">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseUp.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c8fb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c8fb-126">Requirements</span></span>



| <span data-ttu-id="2c8fb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c8fb-127">Requirement</span></span> | <span data-ttu-id="2c8fb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2c8fb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8fb-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c8fb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8fb-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2c8fb-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c8fb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8fb-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2c8fb-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2c8fb-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c8fb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8fb-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2c8fb-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2c8fb-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c8fb-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c8fb-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8fb-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2c8fb-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c8fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8fb-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="2c8fb-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="2c8fb-139">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="2c8fb-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="2c8fb-140">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="2c8fb-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




