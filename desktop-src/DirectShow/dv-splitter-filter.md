---
description: Filtro separatore DV
ms.assetid: 099d1cc7-f0c5-4c50-a1d5-f2defde7e104
title: Filtro separatore DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 323593fd5b55fdbd65cb05e83d1097d0d764c94c30141125dcc1cc6fc5ed60d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820673"
---
# <a name="dv-splitter-filter"></a>Filtro separatore DV

Questo filtro suddivide un flusso video digitale interleaved (DV) nei flussi video e audio dei relativi componenti.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                                                                             |
| Tipi di supporti pin di input                    | MEDIATYPE \_ Interleaved, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                                         |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | **Video:** MEDIATYPE \_ Video, FORMAT \_ DvInfo<br/> **Audio:** MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx<br/>             |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ DVSplitter                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | qdv.dll                                                                                                                                            |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Commenti

I fotogrammi DV contengono audio e video nello stesso fotogramma. Il filtro DV Splitter estrae i dati audio e lo recapita come uno o due flussi audio dai pin di output audio. Il fotogramma DV originale viene recapitato dal pin di output video, come fotogramma video. Il tipo di supporto nel fotogramma video è stato modificato da MEDIATYPE \_ Interleaved a MEDIATYPE Video, ma in caso contrario i dati \_ non vengono modificati. Il tipo di supporto viene modificato per segnalare che i dati audio nel frame devono essere ignorati. Lo splitter DV non imposta un'ora multimediale nei relativi esempi di output. se si scrive un filtro downstream che richiede i tempi dei supporti, è possibile derivare gli orari dal numero di fotogrammi.

Un solo pin di output alla volta espone le [**interfacce IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)

Il filtro DV Splitter può accettare modifiche di formato dinamico nel flusso audio. Tuttavia, se il [filtro Mux AVI](avi-mux-filter.md) è downstream, la modifica del formato verrà rifiutata. In questo caso, lo splitter DV interrompe la produzione di un flusso audio. Questa limitazione influisce solo sull'acquisizione di file di tipo 2. Per i file di tipo 1, il flusso interleaved non viene suddiviso in primo luogo. Per l'anteprima, non è disponibile alcun filtro Mux AVI downstream.

Se l'origine DV è una fotocamera live, in genere non è necessario modificare il formato audio. Tuttavia, il formato potrebbe cambiare se si trasmette da un nastro VTR che contiene diverse origini eterogenee.

Ogni fotogramma DV contiene metadati, oltre ai dati audio e video. Questi metadati possono cambiare da frame a frame. Le applicazioni possono analizzare i metadati esaminando gli esempi di input o gli esempi di output video. Tuttavia, DirectShow non fornisce alcun supporto diretto per l'analisi dei metadati DV. Per altre informazioni, vedere IEC 61834-4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




