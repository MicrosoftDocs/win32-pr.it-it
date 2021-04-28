---
description: "Evento InkCollector.MouseMove: si verifica quando il puntatore del mouse viene spostato sull'oggetto InkCollector o InkOverlay."
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector.MouseMove (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110159"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="c54bb-103">Evento InkCollector.MouseMove</span><span class="sxs-lookup"><span data-stu-id="c54bb-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="c54bb-104">Si verifica quando il puntatore del mouse viene spostato [**sull'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay.**](inkoverlay-class.md)</span><span class="sxs-lookup"><span data-stu-id="c54bb-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c54bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c54bb-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="c54bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c54bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c54bb-107">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54bb-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="c54bb-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="c54bb-109">*MAIUSC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54bb-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="c54bb-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="c54bb-111">*pX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54bb-112">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="c54bb-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c54bb-113">*pY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c54bb-114">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="c54bb-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="c54bb-115">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c54bb-116">**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="c54bb-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c54bb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c54bb-117">Return value</span></span>

<span data-ttu-id="c54bb-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c54bb-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c54bb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c54bb-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c54bb-120">Le proprietà *pX* e *pY* sono in pixel e non le unità HIMETRIC associate allo spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="c54bb-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="c54bb-121">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione non inconsapevole e questo tipo di applicazione comprende solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="c54bb-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="c54bb-122">Alcuni controlli si basano su una relazione specifica tra [**gli eventi MouseDown**](inkcollector-mousedown.md), **MouseMove** [**e MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="c54bb-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="c54bb-123">L'annullamento di alcuni di questi eventi può avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="c54bb-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="c54bb-124">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseMove.</span><span class="sxs-lookup"><span data-stu-id="c54bb-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="c54bb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c54bb-125">Requirements</span></span>



| <span data-ttu-id="c54bb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c54bb-126">Requirement</span></span> | <span data-ttu-id="c54bb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c54bb-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c54bb-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c54bb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c54bb-129">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="c54bb-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c54bb-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c54bb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c54bb-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c54bb-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c54bb-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c54bb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c54bb-133"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="c54bb-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c54bb-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="c54bb-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c54bb-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c54bb-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c54bb-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c54bb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c54bb-137">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="c54bb-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="c54bb-138">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="c54bb-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="c54bb-139">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="c54bb-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




