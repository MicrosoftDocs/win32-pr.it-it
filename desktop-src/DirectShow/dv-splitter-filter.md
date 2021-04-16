---
description: Filtro Splitter DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro Splitter DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ada4f18a107f8e1b07571f3907aed5ddf50f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520554"
---
# <a name="dv-splitter-filter"></a>Filtro Splitter DV

Questo filtro suddivide un flusso di video digitali (DV) con interfoliazione nei flussi audio e video dei componenti.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipi di supporti pin di input                    | MEDIATYPE con \_ interfoliazione, MEDIASUBTYPE \_ DVSD, formato \_ DvInfo                                                                                         |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | **Video**: \_ video di MEDIATYPE, formato \_ DvInfo<br/> **Audio**: MEDIATYPE \_ audio, MEDIASUBTYPE \_ PCM, Format \_ WAVEFORMATEX<br/>             |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_DVSPLITTER CLSID                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | qdv.dll                                                                                                                                            |
| [Merito](merit.md)                       | VALORE \_ normale                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="remarks"></a>Commenti

I frame DV contengono audio e video nello stesso frame. Il filtro Splitter DV estrae i dati audio e li recapita come uno o due flussi audio, dai pin di output audio. Il frame DV originale viene recapitato dal pin di output del video, come fotogramma video. Il tipo di supporto nel fotogramma video è stato modificato da MEDIATYPE \_ con interfoliazione in MEDIATYPE \_ video, ma in caso contrario i dati non vengono modificati. Il tipo di supporto viene modificato per segnalare che i dati audio nel frame devono essere ignorati. Il separatore DV non imposta un tempo di supporto nei relativi esempi di output; Se si sta scrivendo un filtro downstream che richiede i tempi dei supporti, è possibile derivare le ore dal conteggio dei frame.

Solo un pin di output alla volta espone le interfacce [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .

Il filtro Splitter DV può accettare modifiche al formato dinamico nel flusso audio. Tuttavia, se il filtro [Mux AVI](avi-mux-filter.md) è downstream, rifiuterà la modifica del formato. In tal caso, la barra di divisione DV smette di produrre un flusso audio. Questa limitazione influiscono solo sull'acquisizione di file di tipo 2. Per i file di tipo 1, il flusso Interleaved non viene suddiviso nella prima posizione. Per la versione di anteprima, non è presente alcun filtro Mux AVI a valle.

Se l'origine DV è una fotocamera Live, in genere non è necessario modificare il formato audio. Tuttavia, il formato potrebbe cambiare se si trasmette da un nastro VTR che contiene diverse origini eterogenee.

Ogni frame DV contiene metadati, oltre ai dati audio e video. Questi metadati possono variare da frame a frame. Le applicazioni possono analizzare i metadati esaminando gli esempi di input o di output del video. Tuttavia, DirectShow non fornisce alcun supporto diretto per l'analisi dei metadati DV. Per ulteriori informazioni, consultare IEC 61834-4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




