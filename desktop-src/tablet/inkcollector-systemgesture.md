---
description: Si verifica quando viene riconosciuto un movimento del sistema.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: Evento InkCollector.SystemGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525945"
---
# <a name="inkcollectorsystemgesture-event"></a><span data-ttu-id="9ed39-103">Evento temGesture InkCollector.Sys</span><span class="sxs-lookup"><span data-stu-id="9ed39-103">InkCollector.SystemGesture event</span></span>

<span data-ttu-id="9ed39-104">Si verifica quando viene riconosciuto un movimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ed39-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed39-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ed39-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9ed39-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ed39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ed39-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="9ed39-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-110">Valore del movimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="9ed39-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-112">Coordinata x della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="9ed39-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-114">Coordinata y della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="9ed39-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-115">*Modificatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9ed39-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-117">*Carattere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="9ed39-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="9ed39-119">*CursorMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ed39-120">Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="9ed39-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="9ed39-121">1 è per la modalità normale e 2 sono per la modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="9ed39-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ed39-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ed39-122">Return value</span></span>

<span data-ttu-id="9ed39-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9ed39-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed39-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ed39-124">Remarks</span></span>

<span data-ttu-id="9ed39-125">I movimenti di sistema sono utili perché forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento.</span><span class="sxs-lookup"><span data-stu-id="9ed39-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="9ed39-126">Forniscono anche collegamenti alle combinazioni di eventi del mouse e sono metodi "più economici" per rilevare gli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="9ed39-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="9ed39-127">Ad esempio, invece di cercare una [](inkcollector-mouseup.md)  /  coppia di eventi di evento [**MouseDown**](inkcollector-mousedown.md) di un evento MouseUp senza che si verifichino altri eventi del mouse, è possibile cercare i movimenti del sistema [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightTap** .</span><span class="sxs-lookup"><span data-stu-id="9ed39-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="9ed39-128">Come altro esempio, anziché ascoltare gli eventi dell'evento MouseMove di [**evento MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) e ottenere numerosi messaggi di **evento MouseMove** , è possibile osservare i movimenti del sistema di [**trascinamento**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) o **RightDrag se** , purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="9ed39-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="9ed39-129">In questo modo è possibile ricevere un solo messaggio anziché molti messaggi di **evento MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="9ed39-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="9ed39-130">Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="9ed39-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="9ed39-131">Per ulteriori informazioni sui movimenti di sistema, vedere [utilizzo di movimenti](using-gestures.md) e [input del comando sul Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ed39-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="9ed39-132">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="9ed39-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ed39-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ed39-133">Requirements</span></span>



| <span data-ttu-id="9ed39-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ed39-134">Requirement</span></span> | <span data-ttu-id="9ed39-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9ed39-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ed39-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ed39-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9ed39-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9ed39-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9ed39-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ed39-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9ed39-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9ed39-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9ed39-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ed39-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ed39-141"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9ed39-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9ed39-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ed39-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ed39-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ed39-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9ed39-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ed39-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed39-145">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="9ed39-145">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="9ed39-146">**Enumerazione InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="9ed39-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="9ed39-147">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="9ed39-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="9ed39-148">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="9ed39-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="9ed39-149">Input penna, input penna e riconoscimento</span><span class="sxs-lookup"><span data-stu-id="9ed39-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="9ed39-150">[Input del comando sul Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9ed39-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

