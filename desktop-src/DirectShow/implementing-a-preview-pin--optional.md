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
# <a name="implementing-a-preview-pin-optional"></a>Implementazione di un pin di anteprima (facoltativo)

In questo argomento viene descritto come implementare un pin di anteprima in un filtro di acquisizione DirectShow.

Se il filtro ha un pin di anteprima, il pin di anteprima deve inviare una copia dei dati recapitati dal pin di acquisizione. Inviare i dati dal pin di anteprima solo quando si esegue questa operazione non determina l'eliminazione dei frame dal pin di acquisizione. Il pin di acquisizione ha sempre la priorità sul pin di anteprima.

Il pin di acquisizione e il pin di anteprima devono inviare dati con lo stesso formato. Pertanto, devono connettersi utilizzando tipi di supporti identici. Se il pin di acquisizione si connette per primo, il pin di anteprima dovrebbe offrire lo stesso tipo di supporto e rifiutare altri tipi. Se il pin di anteprima si connette per primo e il pin di acquisizione si connette con un tipo di supporto diverso, il pin di anteprima dovrebbe riconnettersi usando il nuovo tipo di supporto. Se il filtro downstream dal pin di anteprima rifiuta il nuovo tipo, il pin di acquisizione deve rifiutare anche il tipo. Usare il metodo [**Ipin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) per eseguire una query sul filtro a valle dal pin di anteprima e usare il metodo [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) per riconnettere il PIN. Queste regole si applicano anche se il gestore del grafico dei filtri riconnette il pin di acquisizione.

Nell'esempio seguente viene illustrata una struttura di questo processo:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità di connessione dei filtri](how-filters-connect.md)
</dt> <dt>

[Scrittura dei filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



