---
description: 'Evento InkCollector.CursorDown: si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.'
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Evento InkCollector.CursorDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110299"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="40244-103">Evento InkCollector.CursorDown</span><span class="sxs-lookup"><span data-stu-id="40244-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="40244-104">Si verifica quando la punta del cursore contatta la superficie del tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="40244-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="40244-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40244-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="40244-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40244-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40244-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="40244-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40244-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="40244-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="40244-109">*Tratto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="40244-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40244-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) avviato quando [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ha causato l'evento **CursorDown.**</span><span class="sxs-lookup"><span data-stu-id="40244-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40244-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40244-111">Return value</span></span>

<span data-ttu-id="40244-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="40244-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40244-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="40244-113">Remarks</span></span>

<span data-ttu-id="40244-114">Questo metodo di evento è definito in \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="40244-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="40244-115">Le \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e IInkPictureEvents implementano l'interfaccia IDispatch con un identificatore \_ DISPID [](/windows/win32/api/oaidl/nn-oaidl-idispatch) \_ ICECursorDown.</span><span class="sxs-lookup"><span data-stu-id="40244-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="40244-116">Usare questo evento con attenzione perché potrebbe influire negativamente sulle prestazioni dell'input penna se viene eseguita una quantità troppo grande di codice nei gestori eventi.</span><span class="sxs-lookup"><span data-stu-id="40244-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="40244-117">Per migliorare le prestazioni dell'input penna in tempo reale, nascondere o visualizzare il cursore del mouse nei gestori [**eventi MouseDown**](inkcollector-mousedown.md) e [**MouseUp.**](inkcollector-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="40244-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="40244-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40244-118">Requirements</span></span>



| <span data-ttu-id="40244-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="40244-119">Requirement</span></span> | <span data-ttu-id="40244-120">Valore</span><span class="sxs-lookup"><span data-stu-id="40244-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40244-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40244-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40244-122">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="40244-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="40244-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40244-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40244-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40244-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="40244-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40244-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="40244-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="40244-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="40244-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="40244-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="40244-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40244-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="40244-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40244-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40244-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="40244-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="40244-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="40244-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="40244-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="40244-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="40244-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="40244-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="40244-134">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="40244-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

