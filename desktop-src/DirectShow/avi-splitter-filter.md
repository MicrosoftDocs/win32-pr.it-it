---
description: Filtro separatore AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro separatore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909659"
---
# <a name="avi-splitter-filter"></a>Filtro separatore AVI

Il filtro del separatore AVI viene usato per la riproduzione di file AVI. Accetta i dati in formato AVI e suddivide i dati nei flussi costitutivi per un'ulteriore elaborazione e/o rendering.



| Label | Valore |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Tipi di supporti pin di input                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi                                                                                                                                |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Tipi di supporti pin di output                   | In **genere MEDIATYPE \_ Video** o **MEDIATYPE \_ Audio.** Il tipo esatto dipende dal contenuto del file, dal fatto che il file sia compresso e dal codec usato. |
| Interfacce pin di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| CLSID del filtro                             | CLSID \_ AviSplitter                                                                                                                                                  |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                                          |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                                       |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo filtro è in genere connesso al filtro [Origine file asincrona](file-source--async--filter.md) sul relativo pin di input. Può connettersi a qualsiasi filtro il cui pin di output supporta [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e offre il tipo di supporto corretto al pin di input del filtro AVI Splitter.

I pin di output sullo splitter AVI supportano il metodo IPropertyBag::Read per la lettura delle proprietà dai singoli flussi. Attualmente è definita la proprietà seguente.



| Proprietà | Descrizione                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Restituisce il nome del flusso, tratto dal `'strn'` blocco nel file AVI. Se questo blocco è assente, il metodo Read restituisce E \_ INVALIDARG. |



 

Il metodo IPropertyBag::Write restituisce E \_ FAIL. Il [filtro Mux AVI](avi-mux-filter.md) supporta IPropertyBag::Write per salvare le proprietà del flusso in un file AVI.

Lo strumento di suddivisione AVI non consente ai filtri downstream di usare il proprio allocatore.

La durata dell'interfoliazione nel file determina la quantità di memoria allocata dal separatore AVI per elaborarlo. Un file interfoliato in blocchi di un secondo richiederà molto più memoria per l'elaborazione rispetto a un file la cui durata dell'interfoliazione è impostata su uno o due fotogrammi. Nei computer moderni non si tratta in genere di un problema, a meno che non si esercitino più istanze dello splitter AVI contemporaneamente.

### <a name="seeking"></a>riercare

Se il file contiene un flusso video, lo splitter AVI supporta la ricerca in base al numero di fotogramma. Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore TIME FORMAT **\_ \_ FRAME**.

Se il file contiene un flusso audio, la barra di divisione AVI supporta la ricerca in base al numero di esempio. Per abilitare la ricerca basata sul campione, chiamare [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in Filter Graph Manager con il **valore TIME FORMAT \_ \_ SAMPLE.**

In entrambi i casi, il pin di output per tale flusso deve essere connesso a un filtro renderer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



