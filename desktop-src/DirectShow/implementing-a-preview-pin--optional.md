---
description: In questo argomento viene descritto come implementare un pin di anteprima in un filtro di acquisizione DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementazione di un pin di anteprima (facoltativo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1e09d070be2aa154428cb8684ff1c405fac959
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401269"
---
# <a name="implementing-a-preview-pin-optional"></a><span data-ttu-id="6bd41-103">Implementazione di un pin di anteprima (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6bd41-103">Implementing a Preview Pin (Optional)</span></span>

<span data-ttu-id="6bd41-104">In questo argomento viene descritto come implementare un pin di anteprima in un filtro di acquisizione DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6bd41-104">This topic describes how to implement a preview pin on a DirectShow capture filter.</span></span>

<span data-ttu-id="6bd41-105">Se il filtro ha un pin di anteprima, il pin di anteprima deve inviare una copia dei dati recapitati dal pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6bd41-105">If your filter has a preview pin, the preview pin must send a copy of the data delivered by the capture pin.</span></span> <span data-ttu-id="6bd41-106">Inviare i dati dal pin di anteprima solo quando si esegue questa operazione non determina l'eliminazione dei frame dal pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6bd41-106">Only send data from the preview pin when doing so will not cause the capture pin to drop frames.</span></span> <span data-ttu-id="6bd41-107">Il pin di acquisizione ha sempre la priorità sul pin di anteprima.</span><span class="sxs-lookup"><span data-stu-id="6bd41-107">The capture pin always has priority over the preview pin.</span></span>

<span data-ttu-id="6bd41-108">Il pin di acquisizione e il pin di anteprima devono inviare dati con lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="6bd41-108">The capture pin and the preview pin must send data with the same format.</span></span> <span data-ttu-id="6bd41-109">Pertanto, devono connettersi utilizzando tipi di supporti identici.</span><span class="sxs-lookup"><span data-stu-id="6bd41-109">Therefore, they must connect using identical media types.</span></span> <span data-ttu-id="6bd41-110">Se il pin di acquisizione si connette per primo, il pin di anteprima dovrebbe offrire lo stesso tipo di supporto e rifiutare altri tipi.</span><span class="sxs-lookup"><span data-stu-id="6bd41-110">If the capture pin connects first, the preview pin should offer the same media type, and reject any others types.</span></span> <span data-ttu-id="6bd41-111">Se il pin di anteprima si connette per primo e il pin di acquisizione si connette con un tipo di supporto diverso, il pin di anteprima dovrebbe riconnettersi usando il nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6bd41-111">If the preview pin connects first, and the capture pin connects with a different media type, the preview pin should reconnect using the new media type.</span></span> <span data-ttu-id="6bd41-112">Se il filtro downstream dal pin di anteprima rifiuta il nuovo tipo, il pin di acquisizione deve rifiutare anche il tipo.</span><span class="sxs-lookup"><span data-stu-id="6bd41-112">If the filter downstream from the preview pin rejects the new type, the capture pin should also reject the type.</span></span> <span data-ttu-id="6bd41-113">Usare il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) per eseguire una query sul filtro a valle dal pin di anteprima e usare il metodo [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) per riconnettere il PIN.</span><span class="sxs-lookup"><span data-stu-id="6bd41-113">Use the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method to query the filter downstream from the preview pin, and use the [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) method to reconnect the pin.</span></span> <span data-ttu-id="6bd41-114">Queste regole si applicano anche se il gestore del grafico dei filtri riconnette il pin di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6bd41-114">These rules also apply if the Filter Graph Manager reconnects the capture pin.</span></span>

<span data-ttu-id="6bd41-115">Nell'esempio seguente viene illustrata una struttura di questo processo:</span><span class="sxs-lookup"><span data-stu-id="6bd41-115">The following example shows an outline of this process:</span></span>


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a><span data-ttu-id="6bd41-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6bd41-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bd41-117">Modalità di connessione dei filtri</span><span class="sxs-lookup"><span data-stu-id="6bd41-117">How Filters Connect</span></span>](how-filters-connect.md)
</dt> <dt>

[<span data-ttu-id="6bd41-118">Scrittura dei filtri di acquisizione</span><span class="sxs-lookup"><span data-stu-id="6bd41-118">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



