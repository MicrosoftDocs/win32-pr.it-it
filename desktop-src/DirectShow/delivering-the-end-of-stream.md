---
description: Distribuzione della fine del flusso
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Distribuzione della fine del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebae0fe3238f32f630c0a2ecd0787f6bd9b75a9aed6342e202f187d3fe8dac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831351"
---
# <a name="delivering-the-end-of-stream"></a>Distribuzione della fine del flusso

Quando il pin di input riceve una notifica di fine flusso, propaga la chiamata a valle. Anche tutti i filtri downstream che ricevono dati da questo pin di input devono ricevere la notifica di fine flusso. Anche in questo caso, prendere il blocco di streaming e non il blocco del filtro. Se il filtro contiene dati in sospeso che non sono stati ancora recapitati, il filtro deve recapitarlo ora, prima di inviare la notifica di fine flusso. Non deve inviare dati dopo la fine del flusso.


```C++
HRESULT CMyInputPin::EndOfStream()
{
    CAutoLock lock_it(&m_csReceive);

    /* If the pin has not delivered all of the data in the stream 
       (based on what it received previously), do so now.  */

    // Propagate EndOfStream call downstream, via your output pin(s).
    for (each output pin)
    {    
        hr = pOutputPin->DeliverEndOfStream();
    }
    return S_OK;
}
```



Il [**metodo CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) chiama [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 



