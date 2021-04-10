---
description: Si verifica quando viene riconosciuto un movimento dell'applicazione.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. Gesture (inchiostrata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232098"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="3d635-103">Evento InkEdit. Gesture</span><span class="sxs-lookup"><span data-stu-id="3d635-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="3d635-104">Si verifica quando viene riconosciuto un movimento dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d635-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d635-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d635-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3d635-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d635-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d635-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d635-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d635-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) utilizzato per creare questo movimento.</span><span class="sxs-lookup"><span data-stu-id="3d635-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="3d635-109">*Tratti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d635-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d635-110">Raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che contiene gli oggetti [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che compongono questo movimento.</span><span class="sxs-lookup"><span data-stu-id="3d635-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="3d635-111">*Movimenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d635-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d635-112">Matrice di oggetti [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , in ordine di confidenza.</span><span class="sxs-lookup"><span data-stu-id="3d635-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="3d635-113">Per ulteriori informazioni sulla struttura VARIANT, vedere [utilizzo della libreria com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3d635-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d635-114">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="3d635-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d635-115">Indica se la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che costituisce questo movimento deve essere annullata, in modo da non cancellare l'input penna e generare l'evento [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="3d635-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d635-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d635-116">Return value</span></span>

<span data-ttu-id="3d635-117">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3d635-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d635-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3d635-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d635-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d635-119">Remarks</span></span>

<span data-ttu-id="3d635-120">Questo metodo di evento è definito nell'interfaccia **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="3d635-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="3d635-121">L'interfaccia **\_ IInkEditEvents** implementa l'interfaccia IDispatch con un identificatore di DISPID \_ IeeGesture.</span><span class="sxs-lookup"><span data-stu-id="3d635-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="3d635-122">Un evento di **movimento** viene generato solo se [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) per l'oggetto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) è il primo oggetto **IInkStrokeDisp** dopo l'ultima chiamata al metodo [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) o l'ultima generazione del timeout di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="3d635-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="3d635-123">Se l'evento di **movimento** viene annullato, viene generato l'evento [**Stroke**](inkedit-stroke.md) per la raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) che ha generato l'evento di **movimento** .</span><span class="sxs-lookup"><span data-stu-id="3d635-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="3d635-124">Affinché questo evento si verifichi, il controllo [InkEdit](inkedit-control-reference.md) deve sottoscrivere un set di movimenti dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3d635-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="3d635-125">Per impostare l'interesse del controllo InkEdit in un set di movimenti, chiamare il metodo [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .</span><span class="sxs-lookup"><span data-stu-id="3d635-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="3d635-126">Per un elenco dei movimenti dell'applicazione, vedere il tipo di enumerazione [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="3d635-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="3d635-127">Il controllo [InkEdit](inkedit-control-reference.md) non riconosce più movimenti del tratto.</span><span class="sxs-lookup"><span data-stu-id="3d635-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="3d635-128">Il controllo [InkEdit](inkedit-control-reference.md) sottoscrive i movimenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d635-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="3d635-129">Movimento</span><span class="sxs-lookup"><span data-stu-id="3d635-129">Gesture</span></span>                              | <span data-ttu-id="3d635-130">Azione</span><span class="sxs-lookup"><span data-stu-id="3d635-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="3d635-131">In basso a sinistra, in basso a sinistra-lungo</span><span class="sxs-lookup"><span data-stu-id="3d635-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="3d635-132">Immettere</span><span class="sxs-lookup"><span data-stu-id="3d635-132">Enter</span></span><br/>     |
| <span data-ttu-id="3d635-133">Destra</span><span class="sxs-lookup"><span data-stu-id="3d635-133">Right</span></span><br/>                     | <span data-ttu-id="3d635-134">Space</span><span class="sxs-lookup"><span data-stu-id="3d635-134">Space</span></span><br/>     |
| <span data-ttu-id="3d635-135">Sinistra</span><span class="sxs-lookup"><span data-stu-id="3d635-135">Left</span></span><br/>                      | <span data-ttu-id="3d635-136">Backspace</span><span class="sxs-lookup"><span data-stu-id="3d635-136">Backspace</span></span><br/> |
| <span data-ttu-id="3d635-137">Up-right, up-right-Long</span><span class="sxs-lookup"><span data-stu-id="3d635-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="3d635-138">Scheda</span><span class="sxs-lookup"><span data-stu-id="3d635-138">Tab</span></span><br/>       |



 

<span data-ttu-id="3d635-139">Per modificare l'azione predefinita per un movimento:</span><span class="sxs-lookup"><span data-stu-id="3d635-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="3d635-140">Aggiungere gestori eventi per gli eventi **movimento** e [**tratto**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="3d635-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="3d635-141">Nel gestore eventi **movimento** annullare l'evento di **movimento** per il movimento ed eseguire l'azione alternativa per il movimento.</span><span class="sxs-lookup"><span data-stu-id="3d635-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="3d635-142">Nel gestore dell'evento [**Stroke**](inkedit-stroke.md) annullare l'evento **Stroke** per l'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) che ha generato l'evento di **movimento** annullato.</span><span class="sxs-lookup"><span data-stu-id="3d635-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d635-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d635-143">Requirements</span></span>



| <span data-ttu-id="3d635-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d635-144">Requirement</span></span> | <span data-ttu-id="3d635-145">Valore</span><span class="sxs-lookup"><span data-stu-id="3d635-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d635-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d635-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3d635-147">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3d635-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3d635-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d635-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3d635-149">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d635-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3d635-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d635-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d635-151"><dt>Inchiostrato. h (richiede anche il \_ . c)</dt></span><span class="sxs-lookup"><span data-stu-id="3d635-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3d635-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d635-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="3d635-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d635-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3d635-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d635-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d635-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="3d635-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="3d635-156">**Enumerazione InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="3d635-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="3d635-157">[**Metodo SetGestureStatus ( \[ controllo InkEdit)\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="3d635-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="3d635-158">**Proprietà RecoTimeout**</span><span class="sxs-lookup"><span data-stu-id="3d635-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="3d635-159">[**\[Controllo InkEdit evento Stroke\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="3d635-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="3d635-160">Uso di movimenti</span><span class="sxs-lookup"><span data-stu-id="3d635-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

