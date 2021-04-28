---
description: "Evento InkCollector.CursorButtonUp: si verifica quando InkCollector rileva un pulsante del cursore verso l'alto."
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Evento InkCollector.CursorButtonUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936b050c64d07a6957039278f0455bc71d77dbdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110309"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="14b25-103">Evento InkCollector.CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="14b25-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="14b25-104">Si verifica quando [**InkCollector rileva**](inkcollector-class.md) un pulsante del cursore verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="14b25-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b25-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14b25-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="14b25-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14b25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b25-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="14b25-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b25-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorButtonUp.**</span><span class="sxs-lookup"><span data-stu-id="14b25-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="14b25-109">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="14b25-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14b25-110">Pulsante rilasciato.</span><span class="sxs-lookup"><span data-stu-id="14b25-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b25-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b25-111">Return value</span></span>

<span data-ttu-id="14b25-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="14b25-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14b25-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b25-113">Remarks</span></span>

<span data-ttu-id="14b25-114">Un pulsante sulla punta di una penna è in alto quando l'utente completa un tratto e solleva la penna dal digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="14b25-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="14b25-115">Quando il pulsante non è premuto, è disponibile un pulsante su una freccia verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="14b25-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="14b25-116">Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi **CursorButtonUp:** uno per il pulsante destro verso l'alto e uno per il pulsante sinistro in alto.</span><span class="sxs-lookup"><span data-stu-id="14b25-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="14b25-117">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="14b25-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b25-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b25-118">Requirements</span></span>



| <span data-ttu-id="14b25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b25-119">Requirement</span></span> | <span data-ttu-id="14b25-120">Valore</span><span class="sxs-lookup"><span data-stu-id="14b25-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b25-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14b25-122">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="14b25-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="14b25-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14b25-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="14b25-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="14b25-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14b25-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b25-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="14b25-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="14b25-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="14b25-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="14b25-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14b25-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="14b25-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b25-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="14b25-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="14b25-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="14b25-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="14b25-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="14b25-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="14b25-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="14b25-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="14b25-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="14b25-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




