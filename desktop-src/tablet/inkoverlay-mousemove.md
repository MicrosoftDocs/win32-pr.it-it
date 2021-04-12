---
description: Si verifica quando il puntatore del mouse viene spostato sull'oggetto InkCollector o InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ddefd5f3b3f75b03488f74bdbd4aee222a89d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233554"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="78550-103">InkOverlay. MouseMove (evento)</span><span class="sxs-lookup"><span data-stu-id="78550-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="78550-104">Si verifica quando il puntatore del mouse viene spostato sull'oggetto [**InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="78550-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="78550-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78550-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="78550-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="78550-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78550-107">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78550-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78550-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="78550-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="78550-109">*Sposta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78550-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78550-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="78550-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="78550-111">*px* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78550-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78550-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="78550-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="78550-113">*py* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78550-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78550-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="78550-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="78550-115">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="78550-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="78550-116">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="78550-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="78550-117">Il valore predefinito è **false**, che specifica che l'evento non deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="78550-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78550-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78550-118">Return value</span></span>

<span data-ttu-id="78550-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="78550-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78550-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="78550-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="78550-121">Le proprietà *px* e *py* sono in pixel e non le unità HIMETRIC associate allo spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="78550-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="78550-122">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione basata su penna e questo tipo di applicazione riconosce solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="78550-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="78550-123">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="78550-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="78550-124">L'annullamento di alcuni di questi eventi potrebbe avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="78550-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="78550-125">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="78550-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="78550-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78550-126">Requirements</span></span>



| <span data-ttu-id="78550-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="78550-127">Requirement</span></span> | <span data-ttu-id="78550-128">Valore</span><span class="sxs-lookup"><span data-stu-id="78550-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78550-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78550-129">Minimum supported client</span></span><br/> | <span data-ttu-id="78550-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="78550-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="78550-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78550-131">Minimum supported server</span></span><br/> | <span data-ttu-id="78550-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78550-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="78550-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78550-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="78550-134"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78550-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78550-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="78550-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="78550-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78550-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="78550-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78550-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78550-138">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="78550-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="78550-139">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="78550-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="78550-140">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="78550-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




