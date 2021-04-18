---
description: Generato da un componente della pipeline quando vengono modificati i criteri di output per il flusso. Questo evento si applica solo ai contenuti protetti.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309627"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="16624-104">Evento MEPolicyChanged</span><span class="sxs-lookup"><span data-stu-id="16624-104">MEPolicyChanged event</span></span>

<span data-ttu-id="16624-105">Generato da un componente della pipeline quando vengono modificati i criteri di output per il flusso.</span><span class="sxs-lookup"><span data-stu-id="16624-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="16624-106">Questo evento si applica solo ai contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="16624-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="16624-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="16624-107">Event values</span></span>

<span data-ttu-id="16624-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="16624-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="16624-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="16624-109">VARTYPE</span></span>                | <span data-ttu-id="16624-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16624-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16624-111">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="16624-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="16624-112">Puntatore all'interfaccia [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) del nuovo criterio per il flusso.</span><span class="sxs-lookup"><span data-stu-id="16624-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="16624-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="16624-113">Remarks</span></span>

<span data-ttu-id="16624-114">Tutti gli output attendibili devono gestire questo evento.</span><span class="sxs-lookup"><span data-stu-id="16624-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="16624-115">Le trasformazioni Media Foundation (MFTs) ricevono questo evento tramite il metodo [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="16624-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="16624-116">I sink di supporto ricevono questo evento tramite il metodo [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="16624-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="16624-117">L'output attendibile deve applicare il nuovo criterio o restituire il codice di errore MF \_ E \_ criteri non \_ supportati.</span><span class="sxs-lookup"><span data-stu-id="16624-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="16624-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16624-118">Requirements</span></span>



| <span data-ttu-id="16624-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="16624-119">Requirement</span></span> | <span data-ttu-id="16624-120">Valore</span><span class="sxs-lookup"><span data-stu-id="16624-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16624-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16624-121">Minimum supported client</span></span><br/> | <span data-ttu-id="16624-122">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="16624-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="16624-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16624-123">Minimum supported server</span></span><br/> | <span data-ttu-id="16624-124">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="16624-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="16624-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16624-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16624-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16624-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16624-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16624-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16624-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16624-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




