---
description: 'Evento InkOverlay.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: Evento InkOverlay.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ed26c672aadc9fa19f6a6426fed7339752448d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117059"
---
# <a name="inkoverlaycursordown-event"></a><span data-ttu-id="49cf0-103">Evento InkOverlay.CursorDown</span><span class="sxs-lookup"><span data-stu-id="49cf0-103">InkOverlay.CursorDown event</span></span>

<span data-ttu-id="49cf0-104">Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="49cf0-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="49cf0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49cf0-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="49cf0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49cf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49cf0-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="49cf0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf0-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento CursorDown.**](inkcollector-cursordown.md)</span><span class="sxs-lookup"><span data-stu-id="49cf0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorDown**](inkcollector-cursordown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="49cf0-109">*Tratto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="49cf0-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49cf0-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento [**CursorDown.**](inkcollector-cursordown.md)</span><span class="sxs-lookup"><span data-stu-id="49cf0-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the [**CursorDown**](inkcollector-cursordown.md) event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49cf0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49cf0-111">Return value</span></span>

<span data-ttu-id="49cf0-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="49cf0-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49cf0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="49cf0-113">Remarks</span></span>

<span data-ttu-id="49cf0-114">Questo metodo di evento è definito in \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="49cf0-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="49cf0-115">Le interfacce \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents implementano [**l'interfaccia IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="49cf0-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="49cf0-116">Usare questo evento con attenzione perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="49cf0-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="49cf0-117">Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="49cf0-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cf0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49cf0-118">Requirements</span></span>



| <span data-ttu-id="49cf0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="49cf0-119">Requirement</span></span> | <span data-ttu-id="49cf0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="49cf0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49cf0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49cf0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="49cf0-122">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="49cf0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="49cf0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49cf0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="49cf0-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="49cf0-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="49cf0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49cf0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cf0-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="49cf0-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="49cf0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="49cf0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="49cf0-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49cf0-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="49cf0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49cf0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cf0-130">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="49cf0-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="49cf0-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="49cf0-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="49cf0-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="49cf0-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="49cf0-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="49cf0-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="49cf0-134">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="49cf0-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

