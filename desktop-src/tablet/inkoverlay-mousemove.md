---
description: "Evento InkOverlay.MouseMove: si verifica quando il puntatore del mouse viene spostato sull'oggetto InkCollector o InkOverlay."
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay.MouseMove (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8290a11b00dcf97b3f3d8568ebe9890f715454
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116909"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="9faab-103">Evento InkOverlay.MouseMove</span><span class="sxs-lookup"><span data-stu-id="9faab-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="9faab-104">Si verifica quando il puntatore del mouse viene spostato [**sull'oggetto InkCollector**](inkcollector-class.md) [**o InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="9faab-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9faab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9faab-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="9faab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9faab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9faab-107">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9faab-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9faab-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="9faab-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="9faab-109">*MAIUSC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9faab-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9faab-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="9faab-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="9faab-111">*pX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9faab-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9faab-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9faab-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9faab-113">*pY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9faab-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9faab-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="9faab-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9faab-115">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9faab-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9faab-116">Indica se l'evento deve essere annullato per il controllo padre.</span><span class="sxs-lookup"><span data-stu-id="9faab-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="9faab-117">Il valore predefinito è **FALSE,** che specifica che l'evento non deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="9faab-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9faab-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9faab-118">Return value</span></span>

<span data-ttu-id="9faab-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9faab-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9faab-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9faab-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9faab-121">Le proprietà *pX* e *pY* sono espresse in pixel e non nelle unità HIMETRIC associate allo spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="9faab-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="9faab-122">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione inconsapevole e questo tipo di applicazione comprende solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="9faab-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="9faab-123">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md) [**e MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="9faab-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="9faab-124">L'annullamento di alcuni di questi eventi può avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="9faab-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="9faab-125">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="9faab-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="9faab-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9faab-126">Requirements</span></span>



| <span data-ttu-id="9faab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9faab-127">Requirement</span></span> | <span data-ttu-id="9faab-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9faab-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9faab-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9faab-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9faab-130">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9faab-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9faab-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9faab-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9faab-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9faab-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9faab-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9faab-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9faab-134"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9faab-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9faab-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="9faab-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="9faab-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9faab-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9faab-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9faab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9faab-138">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="9faab-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9faab-139">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="9faab-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="9faab-140">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="9faab-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




