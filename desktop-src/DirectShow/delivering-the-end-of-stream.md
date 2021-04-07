---
description: Distribuzione della fine del flusso
ms.assetid: 23afdb2e-93b0-4a74-94bd-e38eb82a5995
title: Distribuzione della fine del flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bd80d186bd62e6360fa1600f4ba970281315aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876086"
---
# <a name="delivering-the-end-of-stream"></a>Distribuzione della fine del flusso

Quando il pin di input riceve una notifica di fine flusso, propaga la chiamata downstream. Anche tutti i filtri downstream che ricevono i dati da questo pin di input devono ottenere la notifica di fine del flusso. Anche in questo caso, eseguire il blocco di flusso e non il blocco del filtro. Se il filtro contiene dati in sospeso non ancora recapitati, il filtro deve recapitarlo adesso, prima di inviare la notifica di fine flusso. Non deve inviare dati dopo la fine del flusso.


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



Il metodo [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) chiama [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) sul pin di input downstream.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread e sezioni critiche](threads-and-critical-sections.md)
</dt> </dl>

 

 



