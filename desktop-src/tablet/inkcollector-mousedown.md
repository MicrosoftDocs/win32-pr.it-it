---
description: Si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene premuto un pulsante del mouse.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: Evento InkCollector. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760801fb5c578ddbdd67b15a4201c21c4981b097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525272"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="69e7e-103">Evento InkCollector. MouseDown</span><span class="sxs-lookup"><span data-stu-id="69e7e-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="69e7e-104">Si verifica quando il puntatore del mouse si trova sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene premuto un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="69e7e-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="69e7e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69e7e-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="69e7e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69e7e-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7e-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="69e7e-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="69e7e-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7e-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="69e7e-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="69e7e-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7e-112">Coordinata X, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="69e7e-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="69e7e-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7e-114">Coordinata Y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="69e7e-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="69e7e-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="69e7e-116">**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="69e7e-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69e7e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69e7e-117">Return value</span></span>

<span data-ttu-id="69e7e-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="69e7e-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="69e7e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="69e7e-119">Remarks</span></span>

<span data-ttu-id="69e7e-120">Per migliorare le prestazioni in tempo reale dell'input penna, nascondere o mostrare il cursore del mouse nei gestori eventi **MouseDown** e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="69e7e-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="69e7e-121">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="69e7e-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="69e7e-122">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="69e7e-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="69e7e-123">Alcuni controlli si basano su una relazione specifica tra gli eventi **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="69e7e-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="69e7e-124">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="69e7e-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="69e7e-125">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="69e7e-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="69e7e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69e7e-126">Requirements</span></span>



| <span data-ttu-id="69e7e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="69e7e-127">Requirement</span></span> | <span data-ttu-id="69e7e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="69e7e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69e7e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69e7e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="69e7e-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69e7e-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="69e7e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69e7e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="69e7e-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="69e7e-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="69e7e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69e7e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="69e7e-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="69e7e-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69e7e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="69e7e-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="69e7e-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69e7e-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="69e7e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69e7e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69e7e-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="69e7e-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="69e7e-139">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="69e7e-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="69e7e-140">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="69e7e-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="69e7e-141">**Evento MouseUp**</span><span class="sxs-lookup"><span data-stu-id="69e7e-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




