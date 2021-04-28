---
description: 'Evento InkOverlay.CursorButtonDown: si verifica quando la classe InkCollector rileva un pulsante del cursore verso il basso.'
ms.assetid: 993b84a3-a5ac-4b00-bfb4-26ca1c9727c6
title: Evento InkOverlay.CursorButtonDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcae13afb67be0312959939e0793d89d99c841ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117079"
---
# <a name="inkoverlaycursorbuttondown-event"></a><span data-ttu-id="2d873-103">Evento InkOverlay.CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="2d873-103">InkOverlay.CursorButtonDown event</span></span>

<span data-ttu-id="2d873-104">Si verifica quando [**la classe InkCollector**](inkcollector-class.md) rileva un pulsante del cursore verso il basso.</span><span class="sxs-lookup"><span data-stu-id="2d873-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d873-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d873-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="2d873-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d873-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d873-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d873-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento CursorButtonDown.**](inkcollector-cursorbuttondown.md)</span><span class="sxs-lookup"><span data-stu-id="2d873-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonDown**](inkcollector-cursorbuttondown.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="2d873-109">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2d873-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d873-110">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="2d873-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d873-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d873-111">Return value</span></span>

<span data-ttu-id="2d873-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2d873-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d873-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d873-113">Remarks</span></span>

<span data-ttu-id="2d873-114">Un pulsante su una punta della penna è verso il basso quando l'utente abbassa la penna al digitalizzatore e inizia a tracciare un tratto.</span><span class="sxs-lookup"><span data-stu-id="2d873-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="2d873-115">Un pulsante su un barile è in giù quando viene premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="2d873-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="2d873-116">Quando si preme il pulsante destro del mouse, si ricevono effettivamente due [**eventi CursorButtonDown:**](inkcollector-cursorbuttondown.md) uno per il pulsante destro premuto e uno per il pulsante sinistro premuto.</span><span class="sxs-lookup"><span data-stu-id="2d873-116">When you press the right mouse button, you actually receive two [**CursorButtonDown**](inkcollector-cursorbuttondown.md) events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="2d873-117">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="2d873-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d873-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d873-118">Requirements</span></span>



| <span data-ttu-id="2d873-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d873-119">Requirement</span></span> | <span data-ttu-id="2d873-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2d873-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d873-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d873-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2d873-122">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="2d873-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2d873-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d873-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2d873-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2d873-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="2d873-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d873-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d873-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="2d873-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2d873-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d873-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d873-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d873-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="2d873-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d873-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d873-130">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="2d873-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="2d873-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="2d873-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="2d873-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="2d873-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="2d873-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="2d873-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="2d873-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="2d873-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




