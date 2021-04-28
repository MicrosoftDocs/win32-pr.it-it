---
description: 'InkPicture.Sysevento temGesture: si verifica quando viene riconosciuto un movimento di sistema.'
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.SystemGesture (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cde11b73b6b0d3861a79538a7f9ee19487b6384
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113689"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="26105-103">InkPicture.SystemGesture</span><span class="sxs-lookup"><span data-stu-id="26105-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="26105-104">Si verifica quando viene riconosciuto un movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="26105-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="26105-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26105-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="26105-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26105-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26105-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento SystemGesture.**</span><span class="sxs-lookup"><span data-stu-id="26105-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="26105-109">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26105-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-110">Valore del movimento di sistema.</span><span class="sxs-lookup"><span data-stu-id="26105-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="26105-111">*X* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26105-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-112">Coordinata x della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="26105-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="26105-113">*Y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26105-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-114">Coordinata y della posizione del movimento.</span><span class="sxs-lookup"><span data-stu-id="26105-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="26105-115">*Modificatore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26105-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-116">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26105-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26105-117">*Carattere* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26105-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-118">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26105-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26105-119">*CursorMode* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="26105-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26105-120">Valore che indica se [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) è in modalità normale o in modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="26105-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="26105-121">1 è per la modalità normale e 2 per la modalità gomma.</span><span class="sxs-lookup"><span data-stu-id="26105-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26105-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26105-122">Return value</span></span>

<span data-ttu-id="26105-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="26105-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26105-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="26105-124">Remarks</span></span>

<span data-ttu-id="26105-125">I movimenti di sistema forniscono informazioni [**sull'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) usato per creare il movimento.</span><span class="sxs-lookup"><span data-stu-id="26105-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="26105-126">Forniscono anche collegamenti a combinazioni di eventi del mouse e sono modi per rilevare gli eventi del mouse con un impatto minore sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="26105-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="26105-127">Ad esempio, anziché cercare una coppia di eventi [**MouseUp Event \[ InkPicture Control \]**](inkpicture-mouseup.md)MouseDown Event / [**\[ InkPicture Control \]**](inkpicture-mousedown.md) di eventi senza altri eventi del mouse che si verificano tra, è possibile cercare i movimenti di sistema Tap o RightTap.</span><span class="sxs-lookup"><span data-stu-id="26105-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="26105-128">Come altro esempio, invece di ascoltare gli eventi del controllo MouseDown Event [**\[ InkPicture \] Control**](inkpicture-mousedown.md)MouseMove Event InkPicture Control / [**\[ \]**](inkpicture-mousemove.md) e ricevere numerosi messaggi **mouseMove Event \[ InkPicture Control, \]** è possibile controllare i movimenti di sistema Drag o RightDrag purché non si sia interessati alle coordinate (x, y) di ogni posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="26105-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="26105-129">In questo modo è possibile ricevere un solo messaggio anziché numerosi messaggi di controllo **\[ InkPicture \]** dell'evento MouseMove.</span><span class="sxs-lookup"><span data-stu-id="26105-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="26105-130">Per un elenco di movimenti di sistema specifici, vedere il tipo di enumerazione [**InkSystemGesture.**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)</span><span class="sxs-lookup"><span data-stu-id="26105-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="26105-131">Per altre informazioni sui movimenti di sistema, vedere [Uso di movimenti e](using-gestures.md) input dei comandi nel Tablet [PC.](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26105-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="26105-132">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICESystemGesture DISPID.</span><span class="sxs-lookup"><span data-stu-id="26105-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="26105-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26105-133">Requirements</span></span>



| <span data-ttu-id="26105-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="26105-134">Requirement</span></span> | <span data-ttu-id="26105-135">Valore</span><span class="sxs-lookup"><span data-stu-id="26105-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26105-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26105-136">Minimum supported client</span></span><br/> | <span data-ttu-id="26105-137">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="26105-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="26105-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26105-138">Minimum supported server</span></span><br/> | <span data-ttu-id="26105-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="26105-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="26105-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26105-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="26105-141"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="26105-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="26105-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="26105-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="26105-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26105-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="26105-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26105-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26105-145">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="26105-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="26105-146">**Enumerazione InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="26105-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="26105-147">Uso dei movimenti</span><span class="sxs-lookup"><span data-stu-id="26105-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

