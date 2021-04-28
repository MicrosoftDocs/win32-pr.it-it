---
description: 'Evento InkCollector.CursorButtonDown: si verifica quando la classe InkCollector rileva un pulsante del cursore verso il basso.'
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector.CursorButtonDown (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110329"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="4197f-103">Evento InkCollector.CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="4197f-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="4197f-104">Si verifica quando [**la classe InkCollector**](inkcollector-class.md) rileva un pulsante del cursore verso il basso.</span><span class="sxs-lookup"><span data-stu-id="4197f-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="4197f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4197f-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="4197f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4197f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4197f-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4197f-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4197f-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorButtonDown.**</span><span class="sxs-lookup"><span data-stu-id="4197f-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="4197f-109">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4197f-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4197f-110">Pulsante premuto.</span><span class="sxs-lookup"><span data-stu-id="4197f-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4197f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4197f-111">Return value</span></span>

<span data-ttu-id="4197f-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4197f-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4197f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4197f-113">Remarks</span></span>

<span data-ttu-id="4197f-114">Un pulsante su una punta della penna è verso il basso quando l'utente abbassa la penna al digitalizzatore e inizia a tracciare un tratto.</span><span class="sxs-lookup"><span data-stu-id="4197f-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="4197f-115">Un pulsante su un barile è in giù quando viene premuto il pulsante.</span><span class="sxs-lookup"><span data-stu-id="4197f-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="4197f-116">Quando si preme il pulsante destro del mouse, si ricevono effettivamente due **eventi CursorButtonDown:** uno per il pulsante destro premuto e uno per il pulsante sinistro premuto.</span><span class="sxs-lookup"><span data-stu-id="4197f-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="4197f-117">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID DISPID \_ ICECursorButtonDown.</span><span class="sxs-lookup"><span data-stu-id="4197f-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="4197f-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4197f-118">Requirements</span></span>



| <span data-ttu-id="4197f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4197f-119">Requirement</span></span> | <span data-ttu-id="4197f-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4197f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4197f-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4197f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4197f-122">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="4197f-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4197f-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4197f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4197f-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4197f-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4197f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4197f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4197f-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="4197f-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4197f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4197f-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4197f-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4197f-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4197f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4197f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4197f-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="4197f-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="4197f-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="4197f-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="4197f-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="4197f-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="4197f-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="4197f-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="4197f-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="4197f-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




