---
description: "Evento InkOverlay.CursorButtonUp: si verifica quando InkCollector rileva un pulsante del cursore verso l'alto."
ms.assetid: ce7205f7-727c-4acf-a727-4dbb3cc42441
title: Evento InkOverlay.CursorButtonUp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f22590362c6eb9a987da94bf3adb4e99943c12cd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086849"
---
# <a name="inkoverlaycursorbuttonup-event"></a><span data-ttu-id="8fbdf-103">Evento InkOverlay.CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="8fbdf-103">InkOverlay.CursorButtonUp event</span></span>

<span data-ttu-id="8fbdf-104">Si verifica quando [**InkCollector rileva**](inkcollector-class.md) un pulsante del cursore verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbdf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fbdf-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="8fbdf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fbdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbdf-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8fbdf-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbdf-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**CursorButtonUp.**](inkcollector-cursorbuttonup.md)</span><span class="sxs-lookup"><span data-stu-id="8fbdf-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorButtonUp**](inkcollector-cursorbuttonup.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="8fbdf-109">*Pulsante* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8fbdf-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbdf-110">Pulsante rilasciato.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbdf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fbdf-111">Return value</span></span>

<span data-ttu-id="8fbdf-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fbdf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fbdf-113">Remarks</span></span>

<span data-ttu-id="8fbdf-114">Un pulsante sulla punta di una penna è in alto quando l'utente completa un tratto e solleva la penna dal digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="8fbdf-115">Quando il pulsante non è premuto, è disponibile un pulsante su una freccia verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="8fbdf-116">Quando si rilascia il pulsante destro del mouse, si ricevono effettivamente due eventi [**CursorButtonUp:**](inkcollector-cursorbuttonup.md) uno per il pulsante destro verso l'alto e uno per il pulsante sinistro in alto.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-116">When you release the right mouse button, you actually receive two [**CursorButtonUp**](inkcollector-cursorbuttonup.md) events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="8fbdf-117">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorButtonUp.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fbdf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fbdf-118">Requirements</span></span>



| <span data-ttu-id="8fbdf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fbdf-119">Requirement</span></span> | <span data-ttu-id="8fbdf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8fbdf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbdf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fbdf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbdf-122">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="8fbdf-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8fbdf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8fbdf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbdf-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8fbdf-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8fbdf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fbdf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbdf-126"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="8fbdf-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8fbdf-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fbdf-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fbdf-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fbdf-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8fbdf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fbdf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbdf-130">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="8fbdf-130">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="8fbdf-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="8fbdf-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8fbdf-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="8fbdf-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="8fbdf-133">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="8fbdf-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="8fbdf-134">**Interfaccia IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="8fbdf-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




