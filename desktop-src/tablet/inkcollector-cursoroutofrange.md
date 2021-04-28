---
description: "Evento InkCollector.CursorOutOfRange: si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tablet."
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: Evento InkCollector.CursorOutOfRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e14e674d5cb7c3da7f2a1e684a0e916e637106e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110279"
---
# <a name="inkcollectorcursoroutofrange-event"></a><span data-ttu-id="9eb70-103">Evento InkCollector.CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="9eb70-103">InkCollector.CursorOutOfRange event</span></span>

<span data-ttu-id="9eb70-104">Si verifica quando il cursore esce dall'intervallo di rilevamento fisico (prossimità) del contesto della tablet.</span><span class="sxs-lookup"><span data-stu-id="9eb70-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb70-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9eb70-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="9eb70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9eb70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb70-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb70-108">Oggetto [**interfaccia IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorOutOfRange.**</span><span class="sxs-lookup"><span data-stu-id="9eb70-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb70-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9eb70-109">Return value</span></span>

<span data-ttu-id="9eb70-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9eb70-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb70-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9eb70-111">Remarks</span></span>

<span data-ttu-id="9eb70-112">Questo metodo di evento è definito nelle interfacce di solo invio \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents (interfacce dispatch) con ID \_ DISPID ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="9eb70-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="9eb70-113">**L'evento CursorOutOfRange** viene generato anche in modalità di selezione o cancellazione, non solo in modalità input penna.</span><span class="sxs-lookup"><span data-stu-id="9eb70-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="9eb70-114">A questo scopo, è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="9eb70-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="9eb70-115">Il vantaggio di questo requisito è una maggiore libertà di innovazione sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9eb70-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb70-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9eb70-116">Requirements</span></span>



| <span data-ttu-id="9eb70-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb70-117">Requirement</span></span> | <span data-ttu-id="9eb70-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9eb70-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb70-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb70-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb70-120">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="9eb70-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9eb70-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9eb70-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb70-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9eb70-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9eb70-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9eb70-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eb70-124"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="9eb70-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9eb70-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9eb70-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="9eb70-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb70-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9eb70-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9eb70-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb70-128">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="9eb70-128">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="9eb70-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="9eb70-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="9eb70-130">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="9eb70-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




