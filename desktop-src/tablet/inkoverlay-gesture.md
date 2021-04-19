---
description: Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.
ms.assetid: 11b48fbc-0c93-4c3c-b218-258028822544
title: Evento InkOverlay. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3db800db2d1fca9ee1b00620c698a592ac2121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317949"
---
# <a name="inkoverlaygesture-event"></a><span data-ttu-id="44546-103">InkOverlay. Gesture (evento)</span><span class="sxs-lookup"><span data-stu-id="44546-103">InkOverlay.Gesture event</span></span>

<span data-ttu-id="44546-104">Si verifica quando viene riconosciuto un movimento specifico dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44546-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="44546-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44546-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="44546-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44546-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44546-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44546-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento di [**movimento**](inkcollector-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="44546-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Gesture**](inkcollector-gesture.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="44546-109">*Tratti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44546-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44546-110">Raccolta [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) restituita dal riconoscimento come movimento.</span><span class="sxs-lookup"><span data-stu-id="44546-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="44546-111">*Movimenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44546-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44546-112">Matrice di oggetti [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , in ordine di confidenza, dal riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="44546-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="44546-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="44546-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="44546-114">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="44546-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="44546-115">Indica se la raccolta di questo movimento deve essere annullata, ad esempio non cancellare l'input penna e generare l'evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="44546-115">Whether the collection of this gesture should be canceled, such as not to erase the ink and to fire the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44546-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44546-116">Return value</span></span>

<span data-ttu-id="44546-117">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="44546-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44546-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="44546-118">Remarks</span></span>

<span data-ttu-id="44546-119">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICEGesture.</span><span class="sxs-lookup"><span data-stu-id="44546-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="44546-120">Quando la proprietà [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) è impostata su [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), il timeout tra il momento in cui un utente aggiunge un movimento e quando si verifica l'evento di [**movimento**](inkcollector-gesture.md) è un valore fisso che non può essere modificato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="44546-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the [**Gesture**](inkcollector-gesture.md) event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="44546-121">Il riconoscimento del movimento è più veloce in modalità **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="44546-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="44546-122">Per evitare la raccolta di input penna in modalità [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="44546-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="44546-123">Impostare [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) su [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="44546-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="44546-124">Eliminare il tratto nell'evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="44546-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="44546-125">Elaborare il movimento nell'evento di [**movimento**](inkcollector-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="44546-125">Process the gesture in the [**Gesture**](inkcollector-gesture.md) event.</span></span>

<span data-ttu-id="44546-126">Per impedire il flusso di input penna durante la gestualità, impostare la proprietà [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) su **false**.</span><span class="sxs-lookup"><span data-stu-id="44546-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="44546-127">Oltre a quando si inserisce l'input penna, l'evento di [**movimento**](inkcollector-gesture.md) viene attivato in modalità selezione o cancellazione.</span><span class="sxs-lookup"><span data-stu-id="44546-127">In addition to when inserting ink, the [**Gesture**](inkcollector-gesture.md) event is fired when in select or erase mode.</span></span> <span data-ttu-id="44546-128">L'utente è responsabile del rilevamento della modalità di modifica e deve tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="44546-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="44546-129">Per riconoscere i movimenti, è necessario utilizzare un oggetto o un controllo in grado di raccogliere input penna.</span><span class="sxs-lookup"><span data-stu-id="44546-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="44546-130">I movimenti dell'applicazione sono definiti come movimenti supportati all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44546-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="44546-131">Per questo evento, è necessario che l'oggetto o il controllo siano interessati a un set di movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="44546-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="44546-132">Per impostare gli oggetti o i controlli interessati da un set di movimenti, chiamare il metodo [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) dell'oggetto o del controllo.</span><span class="sxs-lookup"><span data-stu-id="44546-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="44546-133">Per un elenco di movimenti specifici dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="44546-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="44546-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44546-134">Requirements</span></span>



| <span data-ttu-id="44546-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="44546-135">Requirement</span></span> | <span data-ttu-id="44546-136">Valore</span><span class="sxs-lookup"><span data-stu-id="44546-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44546-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44546-137">Minimum supported client</span></span><br/> | <span data-ttu-id="44546-138">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="44546-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="44546-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44546-139">Minimum supported server</span></span><br/> | <span data-ttu-id="44546-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="44546-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="44546-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44546-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="44546-142"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="44546-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="44546-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="44546-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="44546-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44546-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="44546-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44546-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44546-146">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="44546-146">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="44546-147">**Enumerazione InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="44546-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="44546-148">**Metodo SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="44546-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="44546-149">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="44546-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

