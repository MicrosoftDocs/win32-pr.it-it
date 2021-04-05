---
description: Generato da un sink del flusso dopo la chiamata del metodo IMFStreamSink::P laceMarker.
ms.assetid: 40f68352-86e5-4864-9ca0-f30998857fef
title: Evento MEStreamSinkMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 071d6e5b25873739c176d1c808929c26e1e338bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754295"
---
# <a name="mestreamsinkmarker-event"></a><span data-ttu-id="ac745-103">Evento MEStreamSinkMarker</span><span class="sxs-lookup"><span data-stu-id="ac745-103">MEStreamSinkMarker event</span></span>

<span data-ttu-id="ac745-104">Generato da un sink del flusso dopo la chiamata del metodo [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="ac745-104">Raised by a stream sink after the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="ac745-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="ac745-105">Event values</span></span>

<span data-ttu-id="ac745-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="ac745-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ac745-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ac745-107">VARTYPE</span></span>            | <span data-ttu-id="ac745-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac745-108">Description</span></span>                                                                                                                                                                                           |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac745-109">>qualsiasi</span><span class="sxs-lookup"><span data-stu-id="ac745-109">>Any</span></span><br/> | <span data-ttu-id="ac745-110">Il valore dell'evento è una copia di **PROPVARIANT** che il chiamante ha specificato nel parametro *pvarContextValue* del metodo del [**segnaposto**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="ac745-110">The event value is a copy of the **PROPVARIANT** that the caller specified in the *pvarContextValue* parameter of the [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="ac745-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac745-111">Requirements</span></span>



| <span data-ttu-id="ac745-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac745-112">Requirement</span></span> | <span data-ttu-id="ac745-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ac745-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac745-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac745-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ac745-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac745-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac745-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac745-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ac745-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac745-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac745-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac745-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac745-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac745-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac745-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac745-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac745-121">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac745-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="ac745-122">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="ac745-122">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




