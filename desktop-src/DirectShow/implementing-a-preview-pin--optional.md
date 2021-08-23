---
description: Questo argomento descrive come implementare un pin di anteprima in un filtro DirectShow capture.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementazione di un pin di anteprima (facoltativo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de47b86df70500c83c794fe1074dc927622d571e78ef6175b944702277da492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015559"
---
# <a name="implementing-a-preview-pin-optional"></a>Implementazione di un pin di anteprima (facoltativo)

Questo argomento descrive come implementare un pin di anteprima in un filtro DirectShow capture.

Se il filtro ha un pin di anteprima, il pin di anteprima deve inviare una copia dei dati recapitati dal pin di acquisizione. Solo l'invio di dati dal pin di anteprima quando si esegue questa operazione non causerà l'eliminazione dei frame da parte del pin di acquisizione. Il pin di acquisizione ha sempre la priorità rispetto al pin di anteprima.

Il pin di acquisizione e il pin di anteprima devono inviare dati con lo stesso formato. Pertanto, devono connettersi usando tipi di supporti identici. Se il pin di acquisizione si connette per primo, il pin di anteprima deve offrire lo stesso tipo di supporto e rifiutare qualsiasi altro tipo. Se il pin di anteprima si connette per primo e il pin di acquisizione si connette con un tipo di supporto diverso, il pin di anteprima deve riconnettersi usando il nuovo tipo di supporto. Se il filtro a valle dal pin di anteprima rifiuta il nuovo tipo, anche il pin di acquisizione deve rifiutare il tipo. Usare il [**metodo IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) per eseguire una query sul filtro a valle dal pin di anteprima e usare il metodo [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) per riconnettere il pin. Queste regole si applicano anche se Il Graph Manager riconnette il pin di acquisizione.

L'esempio seguente illustra una struttura di questo processo:


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

[Modalità di Connessione](how-filters-connect.md)
</dt> <dt>

[Scrittura di filtri di acquisizione](writing-capture-filters.md)
</dt> </dl>

 

 



