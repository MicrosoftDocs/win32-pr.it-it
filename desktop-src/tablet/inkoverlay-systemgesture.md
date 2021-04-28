---
description: 'InkOverlay.Sysevento temGesture: si verifica quando viene riconosciuto un movimento di sistema.'
ms.assetid: 6f82b234-2088-4207-a6b4-6c6919623d6a
title: InkOverlay.SystemGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3498d6b5fa779f6a15866ac93d53be8348f3d1a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086669"
---
# <a name="inkoverlaysystemgesture-event"></a><span data-ttu-id="062f3-103">InkOverlay.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="062f3-103">InkOverlay.SystemGesture event</span></span>

<span data-ttu-id="062f3-104">Si verifica quando viene riconosciuto un movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="062f3-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="062f3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="062f3-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="062f3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="062f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062f3-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="062f3-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento SystemGesture.**](inkcollector-systemgesture.md)</span><span class="sxs-lookup"><span data-stu-id="062f3-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**SystemGesture**](inkcollector-systemgesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="062f3-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-110">Valore del movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="062f3-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="062f3-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-112">Coordinata x della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="062f3-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="062f3-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-114">Coordinata y della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="062f3-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-115">*Modificatore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="062f3-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="062f3-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-117">*Carattere* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="062f3-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="062f3-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="062f3-119">*CursorMode* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="062f3-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="062f3-120">Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="062f3-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="062f3-121">1 è per la modalità normale e 2 per la modalità di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="062f3-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="062f3-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="062f3-122">Return value</span></span>

<span data-ttu-id="062f3-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="062f3-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="062f3-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="062f3-124">Remarks</span></span>

<span data-ttu-id="062f3-125">I movimenti di sistema sono utili perché forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento.</span><span class="sxs-lookup"><span data-stu-id="062f3-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="062f3-126">Forniscono inoltre collegamenti a combinazioni di eventi del mouse e sono modi "più economici" per rilevare gli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="062f3-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="062f3-127">Ad esempio, anziché cercare una coppia di eventi [**MouseUp Event**](inkcollector-mouseup.md)MouseDown Event senza altri eventi del mouse che si verificano tra di loro, è possibile cercare i movimenti di sistema Tap o  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="062f3-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="062f3-128">Come altro esempio, invece di ascoltare gli eventi evento [](inkcollector-mousedown.md)  /  [**MouseMove**](inkcollector-mousemove.md) dell'evento MouseDown e ricevere numerosi messaggi di evento **MouseMove,** è possibile controllare i movimenti di sistema [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag** purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="062f3-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="062f3-129">In questo modo è possibile ricevere un solo messaggio anziché numerosi **messaggi di evento MouseMove.**</span><span class="sxs-lookup"><span data-stu-id="062f3-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="062f3-130">Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="062f3-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="062f3-131">Per altre informazioni sui movimenti di sistema, vedere [Uso di movimenti e](using-gestures.md) input dei comandi nel Tablet [PC.](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="062f3-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="062f3-132">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ ICESystemGesture DISPID.</span><span class="sxs-lookup"><span data-stu-id="062f3-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="062f3-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="062f3-133">Requirements</span></span>



| <span data-ttu-id="062f3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="062f3-134">Requirement</span></span> | <span data-ttu-id="062f3-135">Valore</span><span class="sxs-lookup"><span data-stu-id="062f3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062f3-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="062f3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="062f3-137">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="062f3-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="062f3-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="062f3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="062f3-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="062f3-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="062f3-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="062f3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="062f3-141"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="062f3-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="062f3-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="062f3-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="062f3-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="062f3-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="062f3-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="062f3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062f3-145">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="062f3-145">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="062f3-146">**Enumerazione InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="062f3-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="062f3-147">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="062f3-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="062f3-148">Uso dei movimenti</span><span class="sxs-lookup"><span data-stu-id="062f3-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="062f3-149">Input penna, input penna e riconoscimento</span><span class="sxs-lookup"><span data-stu-id="062f3-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="062f3-150">[Input dei comandi nel Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="062f3-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

