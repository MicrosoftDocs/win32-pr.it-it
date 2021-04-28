---
description: "Evento InkOverlay.MouseDown: si verifica quando il puntatore del mouse si trova sull'oggetto InkCollector o InkOverlay e viene premuto un pulsante del mouse."
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay.MouseDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1e4bff715a6585ee607de766c809579f527aa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086819"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="83740-103">Evento InkOverlay.MouseDown</span><span class="sxs-lookup"><span data-stu-id="83740-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="83740-104">Si verifica quando il puntatore del mouse si trova [**sull'oggetto InkCollector**](inkcollector-class.md) o [**InkOverlay**](inkoverlay-class.md) e viene premuto un pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="83740-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="83740-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83740-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="83740-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="83740-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83740-107">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83740-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83740-108">Pulsante del mouse premuto.</span><span class="sxs-lookup"><span data-stu-id="83740-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="83740-109">*MAIUSC* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83740-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83740-110">Stato del tasto MAIUSC.</span><span class="sxs-lookup"><span data-stu-id="83740-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="83740-111">*pX* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83740-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83740-112">Coordinata X, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="83740-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="83740-113">*pY* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="83740-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83740-114">Coordinata Y, in pixel, di un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="83740-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="83740-115">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83740-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83740-116">**VARIANT \_ TRUE** per annullare l'evento per il controllo padre. in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="83740-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="83740-117">Il valore predefinito è **VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="83740-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83740-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83740-118">Return value</span></span>

<span data-ttu-id="83740-119">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="83740-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83740-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="83740-120">Remarks</span></span>

<span data-ttu-id="83740-121">Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="83740-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="83740-122">Le proprietà pX e pY sono espresse in pixel e non nelle unità HIMETRIC associate allo spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="83740-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="83740-123">Questo è dovuto al fatto che questo evento sostituisce l'evento del mouse correlato di un'applicazione inconsapevole e questo tipo di applicazione comprende solo i pixel.</span><span class="sxs-lookup"><span data-stu-id="83740-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="83740-124">Alcuni controlli si basano su una relazione specifica tra gli eventi [**MouseDown,**](inkcollector-mousedown.md) [**MouseMove**](inkcollector-mousemove.md) [**e MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="83740-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="83740-125">L'annullamento di alcuni di questi eventi può avere risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="83740-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="83740-126">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID IPEMouseDown.</span><span class="sxs-lookup"><span data-stu-id="83740-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="83740-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83740-127">Requirements</span></span>



| <span data-ttu-id="83740-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="83740-128">Requirement</span></span> | <span data-ttu-id="83740-129">Valore</span><span class="sxs-lookup"><span data-stu-id="83740-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83740-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83740-130">Minimum supported client</span></span><br/> | <span data-ttu-id="83740-131">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="83740-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="83740-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83740-132">Minimum supported server</span></span><br/> | <span data-ttu-id="83740-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="83740-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="83740-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83740-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="83740-135"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="83740-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="83740-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="83740-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="83740-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83740-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="83740-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83740-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83740-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="83740-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="83740-140">**Enumerazione InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="83740-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="83740-141">**Enumerazione InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="83740-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="83740-142">**Evento MouseUp**</span><span class="sxs-lookup"><span data-stu-id="83740-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




