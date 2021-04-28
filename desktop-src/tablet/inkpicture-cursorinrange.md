---
description: "Evento InkPicture.CursorInRange: si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet."
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: Evento InkPicture.CursorInRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05d703022e8d97df0d8d74a73e20af3d91b8531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086579"
---
# <a name="inkpicturecursorinrange-event"></a><span data-ttu-id="b3507-103">Evento InkPicture.CursorInRange</span><span class="sxs-lookup"><span data-stu-id="b3507-103">InkPicture.CursorInRange event</span></span>

<span data-ttu-id="b3507-104">Si verifica quando un cursore entra nell'intervallo di rilevamento fisico (prossimità) del contesto del tablet.</span><span class="sxs-lookup"><span data-stu-id="b3507-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3507-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3507-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="b3507-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3507-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b3507-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3507-108">Oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato **l'evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="b3507-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="b3507-109">*NewCursor* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b3507-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3507-110">**VARIANT \_ TRUE** se questa è la prima volta che l'agente di raccolta input penna viene contattato con [**l'oggetto IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorInRange.** in caso contrario, **VARIANT \_ FALSE.**</span><span class="sxs-lookup"><span data-stu-id="b3507-110">**VARIANT\_TRUE** if this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3507-111">*ButtonsState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b3507-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3507-112">Stato dei pulsanti per il cursore che ha generato **l'evento CursorInRange.**</span><span class="sxs-lookup"><span data-stu-id="b3507-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="b3507-113">Per altre informazioni sulla struttura VARIANT, vedere [Uso della libreria COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="b3507-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3507-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3507-114">Return value</span></span>

<span data-ttu-id="b3507-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b3507-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3507-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3507-116">Remarks</span></span>

<span data-ttu-id="b3507-117">Questo metodo di evento è definito nell'interfaccia di solo invio **\_ IInkCollectorEvents,** **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ ICECursorInRange DISPID.</span><span class="sxs-lookup"><span data-stu-id="b3507-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="b3507-118">**L'evento CursorInRange** viene generato anche in modalità selezione o cancellazione, non solo in modalità input penna.</span><span class="sxs-lookup"><span data-stu-id="b3507-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="b3507-119">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="b3507-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="b3507-120">Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="b3507-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3507-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3507-121">Requirements</span></span>



| <span data-ttu-id="b3507-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3507-122">Requirement</span></span> | <span data-ttu-id="b3507-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b3507-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3507-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3507-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b3507-125">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="b3507-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b3507-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3507-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b3507-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3507-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b3507-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3507-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3507-129"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="b3507-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b3507-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3507-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3507-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3507-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b3507-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3507-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3507-133">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="b3507-133">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b3507-134">**Evento CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="b3507-134">**CursorOutOfRange Event**</span></span>](inkpicture-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="b3507-135">**Enumerazione InkCursorButtonState**</span><span class="sxs-lookup"><span data-stu-id="b3507-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="b3507-136">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="b3507-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




