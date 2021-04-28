---
description: "Evento InkPicture.Stroke: si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet."
ms.assetid: 2829b65a-6120-402e-91e3-5587d1f456f9
title: Evento InkPicture.Stroke (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b181c8dc46348c76bd9c2d015d4a97c1f6911ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113699"
---
# <a name="inkpicturestroke-event"></a><span data-ttu-id="ec246-103">InkPicture.Stroke - evento</span><span class="sxs-lookup"><span data-stu-id="ec246-103">InkPicture.Stroke event</span></span>

<span data-ttu-id="ec246-104">Si verifica quando l'utente disegna un nuovo tratto su qualsiasi tablet.</span><span class="sxs-lookup"><span data-stu-id="ec246-104">Occurs when the user draws a new stroke on any tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec246-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec246-105">Syntax</span></span>


```C++
void Stroke(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in, out] VARIANT_BOOL   *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ec246-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec246-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec246-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ec246-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec246-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento Stroke.**</span><span class="sxs-lookup"><span data-stu-id="ec246-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Stroke** event.</span></span>

</dd> <dt>

<span data-ttu-id="ec246-109">*Tratto* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ec246-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec246-110">Oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) raccolto.</span><span class="sxs-lookup"><span data-stu-id="ec246-110">The collected [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="ec246-111">*Annulla* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ec246-111">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec246-112">**VARIANT \_ TRUE** per annullare la raccolta del tratto. in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="ec246-112">**VARIANT\_TRUE** to cancel the collection of the stroke; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec246-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec246-113">Return value</span></span>

<span data-ttu-id="ec246-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ec246-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec246-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec246-115">Remarks</span></span>

<span data-ttu-id="ec246-116">Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID DISPID \_ ICEStroke.</span><span class="sxs-lookup"><span data-stu-id="ec246-116">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEStroke.</span></span>

<span data-ttu-id="ec246-117">**L'evento Stroke** si verifica in modalità di selezione o cancellazione, non solo quando si inserisce l'input penna.</span><span class="sxs-lookup"><span data-stu-id="ec246-117">The **Stroke** event occurs when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="ec246-118">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="ec246-118">This requires that you monitor the editing mode (which you are responsible for setting) and are aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ec246-119">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ec246-119">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

> [!Note]  
> <span data-ttu-id="ec246-120">**L'evento Stroke** si verifica quando l'utente termina di disegnare un tratto, non quando viene aggiunto un tratto alla [raccolta InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec246-120">The **Stroke** event occurs when the user finishes drawing a stroke, not when a stroke is added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span> <span data-ttu-id="ec246-121">Quando l'utente inizia a disegnare un tratto per la prima volta, viene aggiunto immediatamente alla raccolta InkStrokes. Tuttavia, **l'evento Stroke** non si verifica fino al completamento del tratto.</span><span class="sxs-lookup"><span data-stu-id="ec246-121">When the user first starts to draw a stroke, it is added immediately to the InkStrokes collection; however, the **Stroke** event does not occur until the stroke is complete.</span></span> <span data-ttu-id="ec246-122">Di conseguenza, i tratti possono esistere nella raccolta InkStrokes che il gestore dell'evento **Stroke** non ha visto.</span><span class="sxs-lookup"><span data-stu-id="ec246-122">Therefore, strokes can exist in the InkStrokes collection that the **Stroke** event handler has not seen.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ec246-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec246-123">Requirements</span></span>



| <span data-ttu-id="ec246-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec246-124">Requirement</span></span> | <span data-ttu-id="ec246-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ec246-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec246-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec246-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec246-127">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="ec246-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ec246-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec246-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec246-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ec246-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ec246-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec246-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec246-131"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="ec246-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ec246-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec246-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="ec246-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec246-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ec246-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec246-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec246-135">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="ec246-135">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="ec246-136">[**Controllo InkPicture dell'evento \[ StrokesAdded\]**](inkpicture-strokesadded.md)</span><span class="sxs-lookup"><span data-stu-id="ec246-136">[**StrokesAdded Event \[InkPicture Control\]**](inkpicture-strokesadded.md)</span></span>
</dt> <dt>

<span data-ttu-id="ec246-137">[**Controllo InkPicture dell'evento \[ StrokesDeleted\]**](inkpicture-strokesdeleted.md)</span><span class="sxs-lookup"><span data-stu-id="ec246-137">[**StrokesDeleted Event \[InkPicture Control\]**](inkpicture-strokesdeleted.md)</span></span>
</dt> <dt>

[<span data-ttu-id="ec246-138">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="ec246-138">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="ec246-139">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="ec246-139">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

