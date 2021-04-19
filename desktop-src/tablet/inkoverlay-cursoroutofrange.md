---
description: Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.
ms.assetid: c696b2a9-dc47-4b73-a556-9bb222f5bf59
title: Evento InkOverlay. CursorOutOfRange (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1510013d24bf092a08ba7d57b54c0f94bf7c2dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317950"
---
# <a name="inkoverlaycursoroutofrange-event"></a><span data-ttu-id="906ce-103">Evento InkOverlay. CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="906ce-103">InkOverlay.CursorOutOfRange event</span></span>

<span data-ttu-id="906ce-104">Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tavoletta.</span><span class="sxs-lookup"><span data-stu-id="906ce-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="906ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="906ce-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="906ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="906ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="906ce-107">*Cursore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="906ce-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="906ce-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) .</span><span class="sxs-lookup"><span data-stu-id="906ce-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="906ce-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="906ce-109">Return value</span></span>

<span data-ttu-id="906ce-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="906ce-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="906ce-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="906ce-111">Remarks</span></span>

<span data-ttu-id="906ce-112">Questo metodo di evento è definito nelle \_ interfacce IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents dispatch (DISPINTERFACES) con ID DISPID \_ ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="906ce-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="906ce-113">L'evento [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) viene generato anche in modalità selezione o cancellazione, non solo in modalità input penna.</span><span class="sxs-lookup"><span data-stu-id="906ce-113">The [**CursorOutOfRange**](inkcollector-cursoroutofrange.md) event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="906ce-114">A tale scopo, è necessario monitorare la modalità di modifica (che è responsabile dell'impostazione) e tenere presente la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="906ce-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="906ce-115">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma grazie a una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="906ce-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="906ce-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="906ce-116">Requirements</span></span>



| <span data-ttu-id="906ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="906ce-117">Requirement</span></span> | <span data-ttu-id="906ce-118">Valore</span><span class="sxs-lookup"><span data-stu-id="906ce-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="906ce-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="906ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="906ce-120">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="906ce-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="906ce-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="906ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="906ce-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="906ce-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="906ce-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="906ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="906ce-124"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="906ce-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="906ce-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="906ce-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="906ce-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="906ce-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="906ce-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="906ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="906ce-128">**InkOverlay (classe)**</span><span class="sxs-lookup"><span data-stu-id="906ce-128">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="906ce-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="906ce-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="906ce-130">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="906ce-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




