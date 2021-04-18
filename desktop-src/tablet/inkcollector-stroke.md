---
description: Si verifica quando l'utente disegna un nuovo tratto su un tablet.
ms.assetid: eaa89dfe-6141-4205-845b-634321130e26
title: Evento InkCollector. Stroke (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e75ee7f3e8129fdab52e62178fe4b8a322807fc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306053"
---
# <a name="inkcollectorstroke-event"></a><span data-ttu-id="18f1e-103">Evento InkCollector. Stroke</span><span class="sxs-lookup"><span data-stu-id="18f1e-103">InkCollector.Stroke event</span></span>

<span data-ttu-id="18f1e-104">Si verifica quando l'utente disegna un nuovo tratto su un tablet.</span><span class="sxs-lookup"><span data-stu-id="18f1e-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="18f1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18f1e-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="18f1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="18f1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18f1e-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="18f1e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="18f1e-109">*Tratto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.</span><span class="sxs-lookup"><span data-stu-id="18f1e-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="18f1e-111">*Annulla* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18f1e-112">**Variante \_ TRUE** per annullare l'evento; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="18f1e-112">**VARIANT\_TRUE** to cancel the event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18f1e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18f1e-113">Return value</span></span>

<span data-ttu-id="18f1e-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18f1e-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18f1e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="18f1e-115">Remarks</span></span>

<span data-ttu-id="18f1e-116">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="18f1e-116">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="18f1e-117">L'evento **Stroke** viene generato in modalità Select o Erase, non solo quando si inserisce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="18f1e-117">The **Stroke** event is fired when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="18f1e-118">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="18f1e-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="18f1e-119">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="18f1e-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="18f1e-120">L'evento **Stroke** viene generato quando l'utente completa il disegno di un tratto, non quando un tratto viene aggiunto alla raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="18f1e-120">The **Stroke** event fires when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="18f1e-121">Quando l'utente inizia per la prima volta a disegnare un tratto, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, l'evento **Stroke** non viene attivato fino al completamento del tratto.</span><span class="sxs-lookup"><span data-stu-id="18f1e-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not fire until the stroke is complete.</span></span> <span data-ttu-id="18f1e-122">Di conseguenza, i tratti possono esistere nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha rilevato.</span><span class="sxs-lookup"><span data-stu-id="18f1e-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18f1e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18f1e-123">Requirements</span></span>



| <span data-ttu-id="18f1e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="18f1e-124">Requirement</span></span> | <span data-ttu-id="18f1e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="18f1e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18f1e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18f1e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18f1e-127">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="18f1e-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="18f1e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18f1e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18f1e-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="18f1e-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="18f1e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18f1e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="18f1e-131"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="18f1e-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="18f1e-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="18f1e-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="18f1e-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f1e-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="18f1e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18f1e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18f1e-135">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="18f1e-135">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

<span data-ttu-id="18f1e-136">[**\[Raccolta InkStrokes evento StrokesAdded\]**](inkstrokes-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="18f1e-136">[**StrokesAdded Event \[InkStrokes Collection\]**](inkstrokes-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="18f1e-137">[**Classe InkOverlay dell'evento StrokesDeleted \[\]**](inkoverlay-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="18f1e-137">[**StrokesDeleted Event \[InkOverlay Class\]**](inkoverlay-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="18f1e-138">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="18f1e-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="18f1e-139">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="18f1e-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

