---
description: 'Generato dopo che il metodo IMFMediaSession:: SetValue viene completato in modo asincrono. La sessione multimediale genera questo evento dopo che la topologia è stata risolta in una topologia completa ed è stata accodata la topologia per la riproduzione.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967052"
---
# <a name="mesessiontopologyset-event"></a><span data-ttu-id="5cb24-104">Evento MESessionTopologySet</span><span class="sxs-lookup"><span data-stu-id="5cb24-104">MESessionTopologySet event</span></span>

<span data-ttu-id="5cb24-105">Generato dopo che il metodo [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) SetValue viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="5cb24-105">Raised after the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) method completes asynchronously.</span></span> <span data-ttu-id="5cb24-106">La sessione multimediale genera questo evento dopo che la topologia è stata risolta in una topologia completa ed è stata accodata la topologia per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="5cb24-106">The Media Session raises this event after it resolves the topology into a full topology and queues the topology for playback.</span></span>

## <a name="event-values"></a><span data-ttu-id="5cb24-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="5cb24-107">Event values</span></span>

<span data-ttu-id="5cb24-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="5cb24-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5cb24-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5cb24-109">VARTYPE</span></span>                | <span data-ttu-id="5cb24-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cb24-110">Description</span></span>                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb24-111">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="5cb24-111">VT\_EMPTY</span></span><br/>   | <span data-ttu-id="5cb24-112">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5cb24-112">No event data.</span></span><br/> <br/>                                                                    |
| <span data-ttu-id="5cb24-113">VT \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="5cb24-113">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="5cb24-114">Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia completa.</span><span class="sxs-lookup"><span data-stu-id="5cb24-114">Pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface of the full topology.</span></span><br/> <br/> |



## <a name="examples"></a><span data-ttu-id="5cb24-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="5cb24-115">Examples</span></span>

<span data-ttu-id="5cb24-116">Nell'esempio seguente viene recuperato il puntatore [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da un evento MESessionTopologySet.</span><span class="sxs-lookup"><span data-stu-id="5cb24-116">The following example retrieves the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) pointer from an MESessionTopologySet event.</span></span>


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5cb24-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cb24-117">Requirements</span></span>



| <span data-ttu-id="5cb24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cb24-118">Requirement</span></span> | <span data-ttu-id="5cb24-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5cb24-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb24-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb24-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5cb24-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cb24-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5cb24-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cb24-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5cb24-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cb24-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5cb24-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cb24-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cb24-125"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cb24-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cb24-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cb24-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cb24-127">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5cb24-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




