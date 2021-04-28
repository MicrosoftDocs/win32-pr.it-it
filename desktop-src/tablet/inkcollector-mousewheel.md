---
description: "Evento InkCollector.MouseWheel: si verifica quando la rotellina del mouse si sposta mentre l'oggetto InkCollector o InkOverlay ha lo stato attivo."
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Evento InkCollector.MouseWheel (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851a017af4bb71917c88e2194db86eec64218771
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110139"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="7bf77-103">Evento InkCollector.MouseWheel</span><span class="sxs-lookup"><span data-stu-id="7bf77-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="7bf77-104">Si verifica quando la rotellina del mouse si sposta mentre [**l'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="7bf77-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bf77-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7bf77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bf77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf77-107">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="7bf77-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="7bf77-109">*MAIUSC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="7bf77-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="7bf77-111">*Delta* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-112">Conteggio con segno del numero di deviazioni ruotate dalla rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="7bf77-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="7bf77-113">Un dentello corrisponde a uno scatto della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="7bf77-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="7bf77-114">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-115">Coordinata x, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="7bf77-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7bf77-116">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-117">Coordinata y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="7bf77-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="7bf77-118">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf77-119">**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="7bf77-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="7bf77-120">Il valore predefinito è **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="7bf77-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf77-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bf77-121">Return value</span></span>

<span data-ttu-id="7bf77-122">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7bf77-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf77-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7bf77-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bf77-124">Le proprietà *pX* e *pY* sono in pixel e non le unità HIMETRIC associate allo spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="7bf77-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="7bf77-125">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione non inconsapevole e questo tipo di applicazione comprende solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="7bf77-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="7bf77-126">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseWheel.</span><span class="sxs-lookup"><span data-stu-id="7bf77-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bf77-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bf77-127">Requirements</span></span>



| <span data-ttu-id="7bf77-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bf77-128">Requirement</span></span> | <span data-ttu-id="7bf77-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7bf77-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf77-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bf77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7bf77-131">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="7bf77-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7bf77-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bf77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7bf77-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7bf77-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7bf77-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7bf77-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bf77-135"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="7bf77-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7bf77-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="7bf77-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="7bf77-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bf77-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7bf77-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bf77-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf77-139">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="7bf77-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="7bf77-140">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="7bf77-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="7bf77-141">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="7bf77-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




