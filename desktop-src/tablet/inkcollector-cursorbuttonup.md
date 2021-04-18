---
description: Si verifica quando l'oggetto InkCollector rileva un pulsante del cursore.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Evento InkCollector. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306055"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="30527-103">Evento InkCollector. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="30527-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="30527-104">Si verifica quando l'oggetto [**InkCollector**](inkcollector-class.md) rileva un pulsante del cursore.</span><span class="sxs-lookup"><span data-stu-id="30527-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="30527-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30527-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="30527-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30527-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30527-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30527-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30527-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="30527-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="30527-109">*Pulsante* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30527-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30527-110">Pulsante rilasciato.</span><span class="sxs-lookup"><span data-stu-id="30527-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30527-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30527-111">Return value</span></span>

<span data-ttu-id="30527-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="30527-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30527-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="30527-113">Remarks</span></span>

<span data-ttu-id="30527-114">Quando l'utente completa un tratto e solleva la penna dal digitalizzatore, viene applicato un pulsante su una penna.</span><span class="sxs-lookup"><span data-stu-id="30527-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="30527-115">Quando il pulsante non è premuto, viene attivato un pulsante su un barino.</span><span class="sxs-lookup"><span data-stu-id="30527-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="30527-116">Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi **CursorButtonUp** , uno per il pulsante destro e uno per il pulsante sinistro.</span><span class="sxs-lookup"><span data-stu-id="30527-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="30527-117">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="30527-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="30527-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30527-118">Requirements</span></span>



| <span data-ttu-id="30527-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="30527-119">Requirement</span></span> | <span data-ttu-id="30527-120">Valore</span><span class="sxs-lookup"><span data-stu-id="30527-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30527-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30527-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30527-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="30527-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="30527-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30527-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30527-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="30527-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="30527-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30527-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="30527-126"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30527-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30527-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="30527-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="30527-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30527-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="30527-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30527-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30527-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="30527-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="30527-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="30527-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="30527-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="30527-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="30527-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="30527-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="30527-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="30527-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




