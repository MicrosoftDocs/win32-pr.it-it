---
description: Si verifica quando viene riconosciuto un movimento del sistema.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: Evento InkPicture.SystemGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318712"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="0ff52-103">Evento temGesture InkPicture.Sys</span><span class="sxs-lookup"><span data-stu-id="0ff52-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="0ff52-104">Si verifica quando viene riconosciuto un movimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="0ff52-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ff52-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0ff52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ff52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff52-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="0ff52-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-110">Valore del movimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="0ff52-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-112">Coordinata x della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="0ff52-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-114">Coordinata y della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="0ff52-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-115">*Modificatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0ff52-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-117">*Carattere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="0ff52-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0ff52-119">*CursorMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff52-120">Valore che indica se l'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="0ff52-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="0ff52-121">1 è per la modalità normale e 2 sono per la modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="0ff52-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff52-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ff52-122">Return value</span></span>

<span data-ttu-id="0ff52-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0ff52-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff52-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ff52-124">Remarks</span></span>

<span data-ttu-id="0ff52-125">I movimenti di sistema forniscono informazioni sull'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento.</span><span class="sxs-lookup"><span data-stu-id="0ff52-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="0ff52-126">Forniscono anche collegamenti alle combinazioni di eventi del mouse e sono modi per rilevare gli eventi del mouse con minore effetto sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0ff52-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="0ff52-127">Ad esempio, invece di cercare una coppia di eventi del controllo InkPicture del controllo InkPicture per un evento [**MouseUp \[ \]**](inkpicture-mouseup.md) / [**\[ \]**](inkpicture-mousedown.md) , è possibile cercare i movimenti del sistema Tap o RightTap.</span><span class="sxs-lookup"><span data-stu-id="0ff52-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="0ff52-128">Come altro esempio, anziché [**\[ \]**](inkpicture-mousedown.md)ascoltare gli / [**\[ \]**](inkpicture-mousemove.md) **\[ eventi del controllo InkPicture degli eventi di MouseDown e ricevere numerosi messaggi di controllo InkPicture evento MouseMove, è possibile osservare i movimenti del sistema di trascinamento o RightDrag se, purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse. \]**</span><span class="sxs-lookup"><span data-stu-id="0ff52-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="0ff52-129">In questo modo è possibile ricevere un solo messaggio anziché numerosi messaggi di **\[ \] controllo InkPicture dell'evento MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="0ff52-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="0ff52-130">Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="0ff52-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="0ff52-131">Per ulteriori informazioni sui movimenti di sistema, vedere [utilizzo di movimenti](using-gestures.md) e [input del comando sul Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0ff52-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="0ff52-132">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICESystemGesture.</span><span class="sxs-lookup"><span data-stu-id="0ff52-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff52-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ff52-133">Requirements</span></span>



| <span data-ttu-id="0ff52-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ff52-134">Requirement</span></span> | <span data-ttu-id="0ff52-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0ff52-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff52-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ff52-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff52-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0ff52-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0ff52-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ff52-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff52-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ff52-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0ff52-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ff52-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ff52-141"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0ff52-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0ff52-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ff52-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ff52-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ff52-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0ff52-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ff52-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff52-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0ff52-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0ff52-146">**Enumerazione InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="0ff52-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="0ff52-147">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="0ff52-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

