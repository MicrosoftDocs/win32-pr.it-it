---
description: "Evento InkOverlay.CursorInRange: si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tablet."
ms.assetid: 11327fef-1f5e-407a-812b-48f427af291e
title: Evento InkOverlay.CursorInRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1b48cba731720072aae88aa59b80c569a4aa07b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086839"
---
# <a name="inkoverlaycursorinrange-event"></a><span data-ttu-id="9f504-103">Evento InkOverlay.CursorInRange</span><span class="sxs-lookup"><span data-stu-id="9f504-103">InkOverlay.CursorInRange event</span></span>

<span data-ttu-id="9f504-104">Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto della tablet.</span><span class="sxs-lookup"><span data-stu-id="9f504-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f504-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f504-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="9f504-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f504-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f504-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9f504-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f504-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato [**l'evento CursorInRange.**](inkcollector-cursorinrange.md)</span><span class="sxs-lookup"><span data-stu-id="9f504-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="9f504-109">*NewCursor* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9f504-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f504-110">Indica se è la prima volta che l'agente di raccolta input penna viene contattato con [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**CursorInRange.**](inkcollector-cursorinrange.md)</span><span class="sxs-lookup"><span data-stu-id="9f504-110">Whether this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="9f504-111">*ButtonsState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9f504-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f504-112">Stato dei pulsanti per il cursore che ha generato [**l'evento CursorInRange.**](inkcollector-cursorinrange.md)</span><span class="sxs-lookup"><span data-stu-id="9f504-112">The state of the buttons for the cursor that generated the [**CursorInRange**](inkcollector-cursorinrange.md) event.</span></span>

<span data-ttu-id="9f504-113">Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM.](using-the-com-library.md)</span><span class="sxs-lookup"><span data-stu-id="9f504-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f504-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f504-114">Return value</span></span>

<span data-ttu-id="9f504-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9f504-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f504-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f504-116">Remarks</span></span>

<span data-ttu-id="9f504-117">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorInRange.</span><span class="sxs-lookup"><span data-stu-id="9f504-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="9f504-118">[**L'evento CursorInRange**](inkcollector-cursorinrange.md) viene generato anche in modalità di selezione o cancellazione, non solo in modalità input penna.</span><span class="sxs-lookup"><span data-stu-id="9f504-118">The [**CursorInRange**](inkcollector-cursorinrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="9f504-119">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="9f504-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="9f504-120">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9f504-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f504-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f504-121">Requirements</span></span>



| <span data-ttu-id="9f504-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f504-122">Requirement</span></span> | <span data-ttu-id="9f504-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9f504-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f504-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f504-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9f504-125">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9f504-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9f504-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f504-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9f504-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9f504-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9f504-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f504-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f504-129"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f504-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f504-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f504-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f504-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f504-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9f504-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f504-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f504-133">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="9f504-133">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="9f504-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="9f504-134">**CursorOutOfRange Event**</span></span>](inkcollector-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="9f504-135">**Enumerazione InkCursorButtonState**</span><span class="sxs-lookup"><span data-stu-id="9f504-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="9f504-136">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="9f504-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




