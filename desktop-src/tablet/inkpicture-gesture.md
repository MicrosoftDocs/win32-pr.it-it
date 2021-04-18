---
description: Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94581369554b4aef16530c9ddc8b3fd1a31ad861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316830"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="d5085-103">Evento InkPicture. Gesture</span><span class="sxs-lookup"><span data-stu-id="d5085-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="d5085-104">Si verifica quando viene riconosciuto un *movimento* specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5085-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5085-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5085-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d5085-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5085-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5085-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5085-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5085-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento di **movimento** .</span><span class="sxs-lookup"><span data-stu-id="d5085-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="d5085-109">*Tratti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5085-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5085-110">Raccolta [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) restituita dal riconoscimento come movimento.</span><span class="sxs-lookup"><span data-stu-id="d5085-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="d5085-111">*Movimenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5085-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5085-112">Matrice di oggetti [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , in ordine di confidenza, dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="d5085-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="d5085-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="d5085-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5085-114">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d5085-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5085-115">**Variante \_ TRUE** se l'evento deve essere annullato, ad esempio non cancellare l'input penna e generare l'evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="d5085-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="d5085-116">In caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d5085-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5085-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5085-117">Return value</span></span>

<span data-ttu-id="d5085-118">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d5085-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5085-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5085-119">Remarks</span></span>

<span data-ttu-id="d5085-120">Questo metodo di evento è definito nelle interfacce **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** dispatch (dispinterfaces) con ID DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="d5085-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="d5085-121">Quando la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) è impostata su [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), il timeout tra il momento in cui un utente aggiunge un movimento e quando si verifica l'evento di **movimento** è un valore fisso che non può essere modificato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="d5085-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="d5085-122">Il riconoscimento del movimento è più veloce in modalità **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="d5085-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="d5085-123">Per evitare la raccolta di input penna in modalità [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="d5085-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="d5085-124">Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) su [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="d5085-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="d5085-125">Eliminare il tratto nell'evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="d5085-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="d5085-126">Elaborare il movimento nell'evento di **movimento** .</span><span class="sxs-lookup"><span data-stu-id="d5085-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="d5085-127">Per impedire il flusso di input penna durante la gestualità, impostare la proprietà [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) su **false**.</span><span class="sxs-lookup"><span data-stu-id="d5085-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="d5085-128">Oltre a quando si inserisce l'input penna, l'evento di **movimento** viene attivato in modalità selezione o cancellazione.</span><span class="sxs-lookup"><span data-stu-id="d5085-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="d5085-129">L'utente è responsabile del rilevamento della modalità di modifica e deve tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="d5085-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="d5085-130">Per riconoscere i movimenti, è necessario utilizzare un oggetto o un controllo in grado di raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="d5085-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="d5085-131">I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5085-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="d5085-132">Per questo evento, è necessario che l'oggetto o il controllo siano interessati a un set di movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d5085-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="d5085-133">Per impostare gli oggetti o i controlli interessati da un set di movimenti, chiamare il metodo [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) dell'oggetto o del controllo.</span><span class="sxs-lookup"><span data-stu-id="d5085-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="d5085-134">Per un elenco di movimenti specifici dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="d5085-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5085-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5085-135">Requirements</span></span>



| <span data-ttu-id="d5085-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5085-136">Requirement</span></span> | <span data-ttu-id="d5085-137">Valore</span><span class="sxs-lookup"><span data-stu-id="d5085-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5085-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5085-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d5085-139">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d5085-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d5085-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5085-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d5085-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d5085-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d5085-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5085-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5085-143"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d5085-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d5085-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5085-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5085-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5085-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d5085-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5085-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5085-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d5085-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d5085-148">**Enumerazione InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="d5085-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="d5085-149">**Metodo SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="d5085-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="d5085-150">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="d5085-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

