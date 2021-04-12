---
description: Si verifica quando l'oggetto InkCollector rileva un pulsante del cursore.
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8315f2cf87589bb24e5fb3c6ac6fd7128df426e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348676"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="3c1bb-103">Evento InkOverlay. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="3c1bb-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="3c1bb-104">Si verifica quando l'oggetto [**InkCollector**](inkcollector-class.md) rileva un pulsante del cursore.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c1bb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c1bb-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="3c1bb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c1bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1bb-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1bb-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**CursorButtonUp**](inkcollector-cursorbuttonup.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1bb-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="3c1bb-109">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c1bb-110">Pulsante rilasciato.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1bb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c1bb-111">Return value</span></span>

<span data-ttu-id="3c1bb-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1bb-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c1bb-113">Remarks</span></span>

<span data-ttu-id="3c1bb-114">Quando l'utente completa un tratto e solleva la penna dal digitalizzatore, viene applicato un pulsante su una penna.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="3c1bb-115">Quando il pulsante non è premuto, viene attivato un pulsante su un barino.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="3c1bb-116">Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi [**CursorButtonUp**](inkcollector-cursorbuttonup.md) , uno per il pulsante destro e uno per il pulsante sinistro.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="3c1bb-117">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="3c1bb-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1bb-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c1bb-118">Requirements</span></span>



| <span data-ttu-id="3c1bb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1bb-119">Requirement</span></span> | <span data-ttu-id="3c1bb-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3c1bb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c1bb-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c1bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1bb-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3c1bb-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3c1bb-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c1bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1bb-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3c1bb-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3c1bb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c1bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c1bb-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c1bb-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c1bb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c1bb-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c1bb-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c1bb-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3c1bb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c1bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1bb-130">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="3c1bb-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="3c1bb-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="3c1bb-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="3c1bb-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="3c1bb-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




