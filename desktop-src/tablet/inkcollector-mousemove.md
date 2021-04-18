---
description: Si verifica quando il puntatore del mouse viene spostato sull'oggetto InkCollector o InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306735"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="4b56a-103">Evento InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="4b56a-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="4b56a-104">Si verifica quando il puntatore del mouse viene spostato sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="4b56a-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b56a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b56a-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="4b56a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b56a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b56a-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b56a-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="4b56a-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="4b56a-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b56a-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="4b56a-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="4b56a-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b56a-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="4b56a-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="4b56a-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b56a-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="4b56a-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="4b56a-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b56a-116">**Variante \_ TRUE** per annullare l'evento per il controllo padre; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="4b56a-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b56a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b56a-117">Return value</span></span>

<span data-ttu-id="4b56a-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4b56a-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b56a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b56a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4b56a-120">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="4b56a-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="4b56a-121">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="4b56a-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b56a-122">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkcollector-mousedown.md), **MouseMove** e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="4b56a-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="4b56a-123">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="4b56a-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="4b56a-124">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="4b56a-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b56a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b56a-125">Requirements</span></span>



| <span data-ttu-id="4b56a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b56a-126">Requirement</span></span> | <span data-ttu-id="4b56a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4b56a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b56a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b56a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4b56a-129">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4b56a-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4b56a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b56a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4b56a-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4b56a-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4b56a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b56a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b56a-133"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4b56a-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4b56a-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b56a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b56a-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b56a-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4b56a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b56a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b56a-137">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="4b56a-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="4b56a-138">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="4b56a-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="4b56a-139">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="4b56a-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




