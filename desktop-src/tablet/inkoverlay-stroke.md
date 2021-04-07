---
description: Si verifica quando l'utente disegna un nuovo tratto su un tablet.
ms.assetid: 315155ec-0de1-4052-ae7c-51bc3127fbbf
title: Evento InkOverlay. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6db3bdbe996830596a8e25cebf6f05b94638894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759530"
---
# <a name="inkoverlaystroke-event"></a><span data-ttu-id="80174-103">InkOverlay. Stroke (evento)</span><span class="sxs-lookup"><span data-stu-id="80174-103">InkOverlay.Stroke event</span></span>

<span data-ttu-id="80174-104">Si verifica quando l'utente disegna un nuovo tratto su un tablet.</span><span class="sxs-lookup"><span data-stu-id="80174-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="80174-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80174-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="80174-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80174-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80174-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80174-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**Stroke**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="80174-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**Stroke**](inkcollector-stroke.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="80174-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80174-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80174-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.</span><span class="sxs-lookup"><span data-stu-id="80174-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="80174-111">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="80174-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="80174-112">Specifica se l'evento deve essere annullato.</span><span class="sxs-lookup"><span data-stu-id="80174-112">Specifies whether the event should be canceled.</span></span> <span data-ttu-id="80174-113">Se **true**, la raccolta del tratto viene annullata.</span><span class="sxs-lookup"><span data-stu-id="80174-113">If **TRUE**, the collection of the stroke is canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80174-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80174-114">Return value</span></span>

<span data-ttu-id="80174-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="80174-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80174-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="80174-116">Remarks</span></span>

<span data-ttu-id="80174-117">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="80174-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="80174-118">L'evento [**Stroke**](inkcollector-stroke.md) viene generato in modalità Select o Erase, non solo quando si inserisce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="80174-118">The [**Stroke**](inkcollector-stroke.md) event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="80174-119">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="80174-119">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="80174-120">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="80174-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="80174-121">L'evento [**Stroke**](inkcollector-stroke.md) viene generato quando l'utente completa il disegno di un tratto, non quando un tratto viene aggiunto alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="80174-121">The [**Stroke**](inkcollector-stroke.md) event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="80174-122">Quando l'utente inizia per la prima volta a disegnare un tratto, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, l'evento **Stroke** non viene attivato fino al completamento del tratto.</span><span class="sxs-lookup"><span data-stu-id="80174-122">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="80174-123">Di conseguenza, i tratti possono esistere nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha rilevato.</span><span class="sxs-lookup"><span data-stu-id="80174-123">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80174-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80174-124">Requirements</span></span>



| <span data-ttu-id="80174-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80174-125">Requirement</span></span> | <span data-ttu-id="80174-126">Valore</span><span class="sxs-lookup"><span data-stu-id="80174-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80174-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80174-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80174-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="80174-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="80174-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80174-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80174-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="80174-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="80174-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80174-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="80174-132"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="80174-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="80174-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="80174-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="80174-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80174-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="80174-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80174-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80174-136">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="80174-136">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="80174-137">[**\[Raccolta InkStrokes evento StrokesAdded\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="80174-137">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="80174-138">[**Classe InkOverlay dell'evento StrokesDeleted \[\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="80174-138">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="80174-139">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="80174-139">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="80174-140">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="80174-140">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

