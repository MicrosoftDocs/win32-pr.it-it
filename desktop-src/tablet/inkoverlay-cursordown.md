---
description: Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.
ms.assetid: 753aa733-8d62-4983-b76d-d58844b79c35
title: Evento InkOverlay. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea0bd76d8836ae31c6e17877ddc4870dafaaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313936"
---
# <a name="inkoverlaycursordown-event"></a><span data-ttu-id="452a0-103">Evento InkOverlay. CursorDown</span><span class="sxs-lookup"><span data-stu-id="452a0-103">InkOverlay.CursorDown event</span></span>

<span data-ttu-id="452a0-104">Si verifica quando il suggerimento del cursore Contatta la superficie del Tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="452a0-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="452a0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="452a0-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="452a0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="452a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452a0-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="452a0-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="452a0-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**CursorDown**](inkcollector-cursordown.md) .</span><span class="sxs-lookup"><span data-stu-id="452a0-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorDown**](inkcollector-cursordown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="452a0-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="452a0-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="452a0-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che è stato avviato quando l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'attivazione dell'evento [**CursorDown**](inkcollector-cursordown.md) .</span><span class="sxs-lookup"><span data-stu-id="452a0-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the [**CursorDown**](inkcollector-cursordown.md) event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452a0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="452a0-111">Return value</span></span>

<span data-ttu-id="452a0-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="452a0-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="452a0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="452a0-113">Remarks</span></span>

<span data-ttu-id="452a0-114">Questo metodo di evento è definito in \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="452a0-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="452a0-115">le \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents implementano l'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) con un identificatore di DISPID \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="452a0-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="452a0-116">Utilizzare attentamente questo evento perché potrebbe avere un effetto negativo sulle prestazioni dell'input penna se nei gestori eventi viene eseguita una quantità eccessiva di codice.</span><span class="sxs-lookup"><span data-stu-id="452a0-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="452a0-117">Per migliorare le prestazioni in tempo reale dell'input penna, nascondere o mostrare il cursore del mouse nei gestori eventi [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="452a0-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="452a0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="452a0-118">Requirements</span></span>



| <span data-ttu-id="452a0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="452a0-119">Requirement</span></span> | <span data-ttu-id="452a0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="452a0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="452a0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452a0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="452a0-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="452a0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="452a0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="452a0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="452a0-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="452a0-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="452a0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="452a0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="452a0-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="452a0-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="452a0-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="452a0-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="452a0-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="452a0-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="452a0-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="452a0-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452a0-130">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="452a0-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="452a0-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="452a0-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="452a0-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="452a0-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="452a0-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="452a0-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="452a0-134">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="452a0-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

