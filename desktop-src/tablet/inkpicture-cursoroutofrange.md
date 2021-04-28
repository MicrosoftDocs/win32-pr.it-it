---
description: "Evento InkPicture.CursorOutOfRange: si verifica quando il cursore lascia l'intervallo di rilevamento fisico (prossimità) del contesto del tablet."
ms.assetid: 0c71a4ad-3c09-4134-b0e7-82f29e8913ed
title: Evento InkPicture.CursorOutOfRange (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d80584eafb7f1e5222316507f08bd73efb12fae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086569"
---
# <a name="inkpicturecursoroutofrange-event"></a><span data-ttu-id="ab22e-103">Evento InkPicture.CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="ab22e-103">InkPicture.CursorOutOfRange event</span></span>

<span data-ttu-id="ab22e-104">Si verifica quando il cursore lascia l'intervallo di rilevamento fisico (prossimità) del contesto del tablet.</span><span class="sxs-lookup"><span data-stu-id="ab22e-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab22e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab22e-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="ab22e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab22e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab22e-107">*Cursore* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ab22e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab22e-108">Oggetto [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) che ha generato l'evento **CursorOutOfRange.**</span><span class="sxs-lookup"><span data-stu-id="ab22e-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab22e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab22e-109">Return value</span></span>

<span data-ttu-id="ab22e-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ab22e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab22e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab22e-111">Remarks</span></span>

<span data-ttu-id="ab22e-112">Questo metodo di evento è definito nelle interfacce di solo invio **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (interfacce dispatch) con ID \_ DISPID ICECursorOutOfRange.</span><span class="sxs-lookup"><span data-stu-id="ab22e-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="ab22e-113">**L'evento CursorOutOfRange** viene generato anche in modalità di selezione o cancellazione, non solo in modalità input penna.</span><span class="sxs-lookup"><span data-stu-id="ab22e-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="ab22e-114">A questo scopo è necessario monitorare la modalità di modifica (che si è responsabili dell'impostazione) e conoscere la modalità prima di interpretare l'evento.</span><span class="sxs-lookup"><span data-stu-id="ab22e-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="ab22e-115">Il vantaggio di questo requisito è una maggiore libertà di innovare sulla piattaforma attraverso una maggiore consapevolezza degli eventi della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="ab22e-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab22e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab22e-116">Requirements</span></span>



| <span data-ttu-id="ab22e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab22e-117">Requirement</span></span> | <span data-ttu-id="ab22e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ab22e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab22e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab22e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab22e-120">Solo app desktop di Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="ab22e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ab22e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab22e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab22e-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab22e-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ab22e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab22e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab22e-124"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="ab22e-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ab22e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab22e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab22e-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab22e-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ab22e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab22e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab22e-128">Inkpicture</span><span class="sxs-lookup"><span data-stu-id="ab22e-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ab22e-129">**Evento CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="ab22e-129">**CursorInRange Event**</span></span>](inkpicture-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="ab22e-130">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="ab22e-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




