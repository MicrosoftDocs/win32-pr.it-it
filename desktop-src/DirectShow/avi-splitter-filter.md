---
description: Filtro separatore AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro separatore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125319"
---
# <a name="avi-splitter-filter"></a>Filtro separatore AVI

Il filtro separatore AVI viene usato per la riproduzione di file AVI. Accetta i dati in formato AVI e li suddivide nei flussi costitutivi per un'ulteriore elaborazione e/o rendering.



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Tipi di supporti pin di input                    | \_Flusso MEDIATYPE, MEDIASUBTYPE \_ AVI                                                                                                                                |
| Interfacce pin di input                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Tipi di supporti pin di output                   | In genere **MEDIATYPE \_ video** o **\_ audio MEDIATYPE**. Il tipo esatto dipende dal contenuto del file, dal fatto che il file sia compresso e da quale codec è stato usato. |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| CLSID filtro                             | \_AVISPLITTER CLSID                                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                                          |
| [Merito](merit.md)                       | VALORE \_ normale                                                                                                                                                       |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo filtro viene in genere connesso al filtro di [origine file asincrono](file-source--async--filter.md) sul pin di input. Può connettersi a qualsiasi filtro il cui pin di output supporti [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) e offre il tipo di supporto corretto al pin di input del filtro Splitter AVI.

I pin di output nella barra di divisione AVI supportano il metodo IPropertyBag:: Read per la lettura delle proprietà dai singoli flussi. Attualmente, viene definita la proprietà seguente.



| Proprietà | Descrizione                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Restituisce il nome del flusso, tratto dal `'strn'` blocco nel file AVI. Se questo blocco è assente, il metodo Read restituisce E \_ INVALIDARG. |



 

Il metodo IPropertyBag:: Write restituisce E ha \_ esito negativo. Il filtro [Mux AVI](avi-mux-filter.md) supporta IPropertyBag:: Write per salvare le proprietà del flusso in un file AVI.

Il separatore AVI non consente ai filtri downstream di usare il proprio allocatore.

La durata dell'interfoliazione nel file determina la quantità di memoria allocata dal separatore AVI per elaborarla. Un file con interfoliazione in blocchi di un secondo richiede una quantità maggiore di memoria per l'elaborazione rispetto a un file la cui durata di interfoliazione è impostata su uno o due frame. Nei computer moderni, questo non è in genere un problema a meno che non vengano eseguite contemporaneamente più istanze del separatore AVI.

### <a name="seeking"></a>La ricerca

Se il file contiene un flusso video, il separatore AVI supporta la ricerca in base al numero di frame. Per abilitare la ricerca basata su frame, chiamare [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in [Filter Graph Manager](filter-graph-manager.md) con il valore **\_ format time format \_ frame**.

Se il file contiene un flusso audio, il separatore AVI supporta la ricerca in base al numero di campione. Per abilitare la ricerca basata su campione, chiamare [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) in Filter Graph Manager con l' **esempio valore \_ time \_ Format**.

In entrambi i casi, il pin di output per quel flusso deve essere connesso a un filtro renderer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



