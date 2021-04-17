---
description: Riconnessione dell'input per garantire tipi di output specifici
ms.assetid: c83d002e-59bf-4d03-9917-e39ceab9a4ce
title: Riconnessione dell'input per garantire tipi di output specifici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d74d6914989231542ddfea9f97e93ce860d34eb4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401157"
---
# <a name="reconnecting-your-input-to-ensure-specific-output-types"></a><span data-ttu-id="31559-103">Riconnessione dell'input per garantire tipi di output specifici</span><span class="sxs-lookup"><span data-stu-id="31559-103">Reconnecting Your Input to Ensure Specific Output Types</span></span>

<span data-ttu-id="31559-104">I filtri implementano il metodo [**IAMStreamConfig:: Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) per impostare il formato audio o video prima che i pin del filtro siano connessi.</span><span class="sxs-lookup"><span data-stu-id="31559-104">Filters implement the [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method to set the audio or video format before the filter's pins are connected.</span></span> <span data-ttu-id="31559-105">Se il pin di output è già connesso ed è possibile specificare un nuovo tipo, riconnettere il PIN, ma solo se l'altro filtro può accettare il nuovo tipo.</span><span class="sxs-lookup"><span data-stu-id="31559-105">If your output pin is already connected and you can provide a new type, then reconnect your pin, but only if the other filter can accept the new type.</span></span> <span data-ttu-id="31559-106">Se l'altro filtro non è in grado di accettare il tipo di supporto, non riuscire a eseguire la chiamata a **Seformatt** e lasciare solo la connessione.</span><span class="sxs-lookup"><span data-stu-id="31559-106">If the other filter cannot accept the media type, fail the call to **SetFormat** and leave your connection alone.</span></span>

<span data-ttu-id="31559-107">Un filtro di trasformazione non può avere tipi di output preferiti, a meno che il pin di input non sia connesso.</span><span class="sxs-lookup"><span data-stu-id="31559-107">A transform filter may not have any preferred output types unless their input pin is connected.</span></span> <span data-ttu-id="31559-108">In tal caso, i metodi **Seformatt** e [**IAMStreamConfig:: GETSTREAMCAPS**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) devono restituire VFW \_ e \_ non \_ connessi fino a quando il pin di input non è connesso.</span><span class="sxs-lookup"><span data-stu-id="31559-108">In that case, the **SetFormat** and [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) methods should return VFW\_E\_NOT\_CONNECTED until the input pin is connected.</span></span> <span data-ttu-id="31559-109">In caso contrario, questi metodi possono funzionare come di consueto.</span><span class="sxs-lookup"><span data-stu-id="31559-109">Otherwise, these methods can function as usual.</span></span>

<span data-ttu-id="31559-110">In alcuni casi è utile riconnettere i pin quando si offre un formato in una connessione stabilita.</span><span class="sxs-lookup"><span data-stu-id="31559-110">In certain cases it is useful to reconnect pins when you are offering a format on an established connection.</span></span> <span data-ttu-id="31559-111">Si supponga, ad esempio, che un filtro possa comprimere video RGB a 24 bit nel formato X e che sia in grado di comprimere il video RGB a 8 bit nel formato Y. Il pin di output può eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="31559-111">For example, suppose that a filter can compress 24-bit RGB video into format X, and that it can compress 8-bit RGB video into format Y. The output pin can do either of the following:</span></span>

-   <span data-ttu-id="31559-112">Offrire sempre entrambe le opzioni X e Y in **GetStreamCaps** e accettare sempre le opzioni x e y in **seformatt**.</span><span class="sxs-lookup"><span data-stu-id="31559-112">Always offer both X and Y in **GetStreamCaps**, and always accept both X and Y in **SetFormat**.</span></span>
-   <span data-ttu-id="31559-113">Offrire e accettare solo il formato X se il tipo di input è RGB a 24 bit.</span><span class="sxs-lookup"><span data-stu-id="31559-113">Offer and accept just format X if the input type is 24-bit RGB.</span></span> <span data-ttu-id="31559-114">Offrire e accettare solo il formato Y se il tipo di input è RGB a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="31559-114">Offer and accept just format Y if the input type 8-bit RGB.</span></span> <span data-ttu-id="31559-115">Interrompere entrambi i metodi se il pin di input non è connesso.</span><span class="sxs-lookup"><span data-stu-id="31559-115">Fail both methods if the input pin is not connected.</span></span>

<span data-ttu-id="31559-116">In entrambi i casi, sarà necessario un codice di riconnessione simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="31559-116">In either case, you will need some reconnecting code that looks like this:</span></span>


```C++
HRESULT MyOutputPin::CheckMediaType(const CMediaType *pmtOut)
{
    // Fail if the input pin is not connected.
    if (!m_pFilter->m_pInput->IsConnected()) {
        return VFW_E_NOT_CONNECTED;
    }

    // (Not shown: Reject any media types that you know in advance your 
    // filter cannot use. Check the major type and subtype GUIDs.)

    // (Not shown: If SetFormat was previously called, check whether
    // pmtOut exactly matches the format that was specified in SetFormat.
    // Return S_OK if they match, or VFW_E_INVALIDMEDIATYPE otherwise.)
   
    // Now do the normal check for this media type.
    HRESULT hr;
    hr = m_pFilter->CheckTransform(
        &m_pFilter->m_pInput->CurrentMediaType(),  // The input type.
        pmtOut  // The proposed output type.
    );
    if (hr == S_OK)
    {
        // This format is compatible with the current input type.
        return S_OK;
    }
 
    // This format is not compatible with the current input type. 
    // Maybe we can reconnect the input pin with a new input type.
    
    // Enumerate the upstream filter's preferred output types, and 
    // see if one of them will work.
    CMediaType *pmtEnum;
    BOOL fFound = FALSE;
    IEnumMediaTypes *pEnum;
    hr = m_pFilter->m_pInput->GetConnected()->EnumMediaTypes(&pEnum);
    if (hr != S_OK)
    {
        return E_FAIL;
    }
    while (hr = pEnum->Next(1, (AM_MEDIA_TYPE **)&pmtEnum, NULL), hr == S_OK)
    {
        // Check this input type against the proposed output type.
        hr = m_pFilter->CheckTransform(pmtEnum, pmtOut);
        if (hr != S_OK) 
        {
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }

        // This input type is a possible candidate. But, we have to make
        // sure that the upstream filter can switch to this type. 
        hr = m_pFilter->m_pInput->GetConnected()->QueryAccept(pmtEnum);
        if (hr != S_OK) 
        {
            // The upstream filter will not switch to this type.
            DeleteMediaType(pmtEnum);
            continue; // Try the next one.
        }
        fFound = TRUE;
        DeleteMediaType(pmtEnum);
        break;
    }
    pEnum->Release();

    if (fFound)
    {
        // This output type is OK, but if we are asked to use it, we will
        // need to reconnect our input pin. (See SetFormat, below.)
        return S_OK;
    }
    else
    {
        return VFW_E_INVALIDMEDIATYPE;
    }
}

HRESULT MyOutputPin::SetFormat(AM_MEDIA_TYPE *pmt)
{
    CheckPointer(pmt, E_POINTER);
    HRESULT hr;

    // Hold the filter state lock, to make sure that streaming isn't 
    // in the middle of starting or stopping:
    CAutoLock cObjectLock(&m_pFilter->m_csFilter);

    // Cannot set the format unless the filter is stopped.
    if (m_pFilter->m_State != State_Stopped)
    {
        return VFW_E_NOT_STOPPED;
    }

    // The set of possible output formats depends on the input format,
    // so if the input pin is not connected, return a failure code.
    if (!m_pFilter->m_pInput->IsConnected())
    {
        return VFW_E_NOT_CONNECTED;
    }

    // If the pin is already using this format, there's nothing to do.
    if (IsConnected() && CurrentMediaType() == *pmt)
    {
        return S_OK;
    }

    // See if this media type is acceptable.
    if ((hr = CheckMediaType((CMediaType *)pmt)) != S_OK) 
    {
        return hr;
    }

    // If we're connected to a downstream filter, we have to make
    // sure that the downstream filter accepts this media type.
    if (IsConnected()) 
    {
        hr = GetConnected()->QueryAccept(pmt);
        if (hr != S_OK)
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }

    // Now make a note that from now on, this is the only format allowed,
    // and refuse anything but this in the CheckMediaType code above.

    // Changing the format means reconnecting if necessary.
    if (IsConnected())
    {
        m_pFilter->m_pGraph->Reconnect(this);
    }

    return NOERROR;
}


// Override CTransformFilter::SetMediaType to reconnect the input pin. 
// This method is called immediately after the media type is set on a pin.
HRESULT MyFilter::SetMediaType(
    PIN_DIRECTION direction, 
    const CMediaType *pmt
)
{
    HRESULT hr;
    if (direction == PINDIR_OUTPUT) 
    {
        // Before we set the output type, we might need to reconnect 
        // the input pin with a new type.
        if (m_pInput && m_pInput->IsConnected()) 
        {
            // Check if the current input type is compatible.
            hr = CheckTransform(
                    &m_pInput->CurrentMediaType(),
                    &m_pOutput->CurrentMediaType());
            if (SUCCEEDED(hr))
            {
                return S_OK;
            }
            // Otherwise, we need to reconnect the input pin.
            // Note: The CheckMediaType method has already called 
            // QueryAccept on the upstream filter. 
            hr = m_pGraph->Reconnect(m_pInput);
            return hr;
        }
    }
    return S_OK;
}
```



 

 



