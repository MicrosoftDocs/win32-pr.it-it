---
description: È stata raggiunta la fine di un segmento.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327830"
---
# <a name="ec_end_of_segment"></a><span data-ttu-id="5762b-103">\_fine \_ del \_ segmento EC</span><span class="sxs-lookup"><span data-stu-id="5762b-103">EC\_END\_OF\_SEGMENT</span></span>

<span data-ttu-id="5762b-104">È stata raggiunta la fine di un segmento.</span><span class="sxs-lookup"><span data-stu-id="5762b-104">The end of a segment was reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="5762b-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="5762b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5762b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="5762b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="5762b-107">(**const** **Reference \_ Time** \* ) puntatore a un valore di **\_ ora di riferimento** che specifica il tempo di flusso accumulato dopo l'avvio del segmento, in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="5762b-107">(**const** **REFERENCE\_TIME**\*) Pointer to a **REFERENCE\_TIME** value that specifies the accumulated stream time since the start of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="5762b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="5762b-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="5762b-109">(**DWORD**) Numero di segmento (in base zero).</span><span class="sxs-lookup"><span data-stu-id="5762b-109">(**DWORD**) Segment number (zero-based).</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="5762b-110">Azione predefinita</span><span class="sxs-lookup"><span data-stu-id="5762b-110">Default Action</span></span>

<span data-ttu-id="5762b-111">Il gestore del grafico del filtro controlla il numero di eventi **\_ \_ della fine del \_ segmento EC** rispetto al numero di eventi [**\_ \_ avviati del segmento EC**](ec-segment-started.md) .</span><span class="sxs-lookup"><span data-stu-id="5762b-111">The filter graph manager checks the number of **EC\_END\_OF\_SEGMENT** events against the number of [**EC\_SEGMENT\_STARTED**](ec-segment-started.md) events.</span></span> <span data-ttu-id="5762b-112">Se corrispondono, l'evento della **\_ fine \_ del \_ segmento EC** viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5762b-112">If they match, it forwards the **EC\_END\_OF\_SEGMENT** event to the application.</span></span> <span data-ttu-id="5762b-113">Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.</span><span class="sxs-lookup"><span data-stu-id="5762b-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="5762b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5762b-114">Remarks</span></span>

<span data-ttu-id="5762b-115">Questo codice di evento supporta il loop senza problemi.</span><span class="sxs-lookup"><span data-stu-id="5762b-115">This event code supports seamless looping.</span></span> <span data-ttu-id="5762b-116">Quando una chiamata al metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) include il flag del \_ \_ segmento di ricerca am, il filtro di origine invia questo codice evento anziché [**chiamare Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span><span class="sxs-lookup"><span data-stu-id="5762b-116">When a call to the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method includes the AM\_SEEKING\_Segment flag, the source filter sends this event code instead of calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).</span></span>

## <a name="requirements"></a><span data-ttu-id="5762b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5762b-117">Requirements</span></span>



| <span data-ttu-id="5762b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5762b-118">Requirement</span></span> | <span data-ttu-id="5762b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5762b-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5762b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5762b-120">Header</span></span><br/> | <dl> <span data-ttu-id="5762b-121"><dt>Dshow. h</dt></span><span class="sxs-lookup"><span data-stu-id="5762b-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5762b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5762b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5762b-123">Codici di notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="5762b-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="5762b-124">Notifica degli eventi in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5762b-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




