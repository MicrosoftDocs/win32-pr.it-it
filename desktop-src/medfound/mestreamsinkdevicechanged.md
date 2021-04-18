---
description: Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307994"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="37f17-103">Evento MEStreamSinkDeviceChanged</span><span class="sxs-lookup"><span data-stu-id="37f17-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="37f17-104">Generato dai sink di flusso del renderer video avanzato (EVR) se il dispositivo video viene modificato.</span><span class="sxs-lookup"><span data-stu-id="37f17-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="37f17-105">Ad esempio, EVR genera questo evento quando riceve un evento di [**\_ \_ modifica della visualizzazione EC**](../directshow/ec-display-changed.md) .</span><span class="sxs-lookup"><span data-stu-id="37f17-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="37f17-106">La pipeline Media Foundation risponde a questo evento inviando nuovamente tutte le richieste di esempio non riuscite durante la modifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37f17-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="37f17-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="37f17-107">Event values</span></span>

<span data-ttu-id="37f17-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="37f17-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="37f17-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="37f17-109">VARTYPE</span></span>              | <span data-ttu-id="37f17-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37f17-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="37f17-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="37f17-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="37f17-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="37f17-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="37f17-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37f17-113">Requirements</span></span>



| <span data-ttu-id="37f17-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37f17-114">Requirement</span></span> | <span data-ttu-id="37f17-115">Valore</span><span class="sxs-lookup"><span data-stu-id="37f17-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37f17-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37f17-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37f17-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="37f17-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37f17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37f17-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37f17-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37f17-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="37f17-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37f17-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37f17-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37f17-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37f17-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37f17-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="37f17-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="37f17-124">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="37f17-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
