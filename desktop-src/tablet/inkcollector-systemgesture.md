---
description: 'InkCollector.Sysevento temGesture: si verifica quando viene riconosciuto un movimento di sistema.'
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.SystemGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f753807d8aaaf03c2de2fd9810ef1e044bcbe05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110052"
---
# <a name="inkcollectorsystemgesture-event"></a><span data-ttu-id="263ed-103">InkCollector.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="263ed-103">InkCollector.SystemGesture event</span></span>

<span data-ttu-id="263ed-104">Si verifica quando viene riconosciuto un movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="263ed-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="263ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="263ed-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="263ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="263ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="263ed-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="263ed-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento SystemGesture.**</span><span class="sxs-lookup"><span data-stu-id="263ed-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="263ed-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-110">Valore del movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="263ed-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="263ed-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-112">Coordinata x della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="263ed-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="263ed-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-114">Coordinata y della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="263ed-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-115">*Modificatore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="263ed-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="263ed-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-117">*Carattere* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="263ed-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="263ed-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="263ed-119">*CursorMode* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="263ed-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="263ed-120">Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="263ed-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="263ed-121">1 è per la modalità normale e 2 per la modalità di cancellazione.</span><span class="sxs-lookup"><span data-stu-id="263ed-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="263ed-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="263ed-122">Return value</span></span>

<span data-ttu-id="263ed-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="263ed-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="263ed-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="263ed-124">Remarks</span></span>

<span data-ttu-id="263ed-125">I movimenti di sistema sono utili perché forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento.</span><span class="sxs-lookup"><span data-stu-id="263ed-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="263ed-126">Forniscono inoltre collegamenti a combinazioni di eventi del mouse e sono modi "più economici" per rilevare gli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="263ed-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="263ed-127">Ad esempio, anziché cercare una coppia di eventi [**MouseUp Event**](inkcollector-mouseup.md)MouseDown Event senza altri eventi del mouse che si verificano tra di loro, è possibile cercare i movimenti di sistema Tap o  /  [](inkcollector-mousedown.md) **RightTap.** [](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="263ed-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="263ed-128">Come altro esempio, invece di ascoltare gli eventi evento [](inkcollector-mousedown.md)  /  [**MouseMove**](inkcollector-mousemove.md) dell'evento MouseDown e ricevere numerosi messaggi di evento **MouseMove,** è possibile controllare i movimenti di sistema [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag** purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="263ed-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="263ed-129">In questo modo è possibile ricevere un solo messaggio anziché numerosi **messaggi di evento MouseMove.**</span><span class="sxs-lookup"><span data-stu-id="263ed-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="263ed-130">Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="263ed-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="263ed-131">Per altre informazioni sui movimenti di sistema, vedere [Uso di movimenti e](using-gestures.md) input dei comandi nel Tablet [PC.](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="263ed-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="263ed-132">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="263ed-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="263ed-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="263ed-133">Requirements</span></span>



| <span data-ttu-id="263ed-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="263ed-134">Requirement</span></span> | <span data-ttu-id="263ed-135">Valore</span><span class="sxs-lookup"><span data-stu-id="263ed-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="263ed-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="263ed-136">Minimum supported client</span></span><br/> | <span data-ttu-id="263ed-137">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="263ed-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="263ed-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="263ed-138">Minimum supported server</span></span><br/> | <span data-ttu-id="263ed-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="263ed-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="263ed-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="263ed-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="263ed-141"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="263ed-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="263ed-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="263ed-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="263ed-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="263ed-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="263ed-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="263ed-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263ed-145">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="263ed-145">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="263ed-146">**Enumerazione InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="263ed-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="263ed-147">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="263ed-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="263ed-148">Uso dei movimenti</span><span class="sxs-lookup"><span data-stu-id="263ed-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="263ed-149">Input penna, input penna e riconoscimento</span><span class="sxs-lookup"><span data-stu-id="263ed-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="263ed-150">[Input dei comandi nel Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="263ed-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

