---
description: Generato da un componente della pipeline quando la configurazione cambia per uno degli schemi di protezione dell'output. Questo evento si applica solo ai contenuti protetti.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753183"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="0aab3-104">Evento MEContentProtectionMessage</span><span class="sxs-lookup"><span data-stu-id="0aab3-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="0aab3-105">Generato da un componente della pipeline quando la configurazione cambia per uno degli schemi di protezione dell'output.</span><span class="sxs-lookup"><span data-stu-id="0aab3-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="0aab3-106">Questo evento si applica solo ai contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="0aab3-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="0aab3-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="0aab3-107">Event values</span></span>

<span data-ttu-id="0aab3-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="0aab3-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0aab3-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0aab3-109">VARTYPE</span></span>              | <span data-ttu-id="0aab3-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aab3-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0aab3-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="0aab3-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0aab3-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0aab3-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0aab3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0aab3-113">Remarks</span></span>

<span data-ttu-id="0aab3-114">Tutti gli output attendibili devono gestire questo evento.</span><span class="sxs-lookup"><span data-stu-id="0aab3-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="0aab3-115">Le trasformazioni Media Foundation (MFTs) ricevono questo evento tramite il metodo [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="0aab3-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="0aab3-116">I sink di supporto ricevono questo evento tramite il metodo [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="0aab3-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="0aab3-117">L'output attendibile deve applicare le modifiche ai criteri o restituire il codice di errore MF \_ E \_ criteri non \_ supportati.</span><span class="sxs-lookup"><span data-stu-id="0aab3-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="0aab3-118">I dati e gli attributi dell'evento dipendono dal sistema di protezione del contenuto in uso.</span><span class="sxs-lookup"><span data-stu-id="0aab3-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aab3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aab3-119">Requirements</span></span>



| <span data-ttu-id="0aab3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aab3-120">Requirement</span></span> | <span data-ttu-id="0aab3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0aab3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aab3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aab3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0aab3-123">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0aab3-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="0aab3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aab3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0aab3-125">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="0aab3-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="0aab3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aab3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aab3-127"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0aab3-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aab3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aab3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aab3-129">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0aab3-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




