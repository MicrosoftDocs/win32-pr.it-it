---
description: Filtro renderer a schermo intero
ms.assetid: 59332096-bdfe-4208-b99a-1f434652f287
title: Filtro renderer a schermo intero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d580442887896f271b0f5b7fea5f7a33553f53f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303766"
---
# <a name="full-screen-renderer-filter"></a>Filtro renderer a schermo intero

Il filtro renderer a schermo intero fornisce il rendering video a schermo intero su hardware obsoleto. Le schede video più recenti possono allungare il video in modo sufficientemente efficiente che non è necessario il renderer a schermo intero. Pertanto, l'utilizzo di questo filtro è ora deprecato.

Non aggiungere manualmente questo filtro al grafico dei filtri. Se un'applicazione chiama [**IVideoWindow::p UT \_ FullScreenMode**](/windows/desktop/api/Control/nf-control-ivideowindow-put_fullscreenmode), Filter Graph Manager seleziona automaticamente il renderer video appropriato per la modalità schermo intero. La selezione è trasparente per l'applicazione. Con le schede video correnti, è improbabile che il gestore del grafo del filtro selezioni il renderer a schermo intero.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFullScreenVideoEx**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-ifullscreenvideoex), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                                                                     |
| Interfacce del PIN di output                    | Non applicabile                                                                                                                                                                                                                                     |
| CLSID filtro                             | \_MODEXRENDERER CLSID                                                                                                                                                                                                                               |
| CLSID della pagina delle proprietà                      | \_MODEXPROPERTIES CLSID                                                                                                                                                                                                                             |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                                                                                                                                                                    |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Il renderer a schermo intero supporta un set statico di modalità di visualizzazione. Tuttavia, la scheda video del sistema dell'utente potrebbe non supportare tutte le modalità. Per determinare se la scheda supporta una modalità particolare, chiamare il metodo [**IFullScreenVideoEx:: IsModeAvailable**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-ismodeavailable) . È anche possibile disabilitare una particolare modalità di visualizzazione a livello di programmazione, chiamando [**IFullScreenVideoEx:: Seenabled**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-setenabled). Il renderer a schermo intero supporta attualmente le modalità di visualizzazione visualizzate nella tabella seguente:



|      |       |        |           |
|------|-------|--------|-----------|
| Modalità | Larghezza | Altezza | Profondità bit |
| 0    | 320   | 200    | 16        |
| 1    | 320   | 200    | 8         |
| 2    | 320   | 240    | 16        |
| 3    | 320   | 240    | 8         |
| 4    | 640   | 400    | 16        |
| 5    | 640   | 400    | 8         |
| 6    | 640   | 480    | 16        |
| 7    | 640   | 480    | 8         |
| 8    | 800   | 600    | 16        |
| 9    | 800   | 600    | 8         |
| 10   | 1024  | 768    | 16        |
| 11   | 1024  | 768    | 8         |
| 12   | 1152  | 864    | 16        |
| 13   | 1152  | 864    | 8         |
| 14   | 1280  | 1024   | 16        |
| 15   | 1280  | 1024   | 8         |



 

(Tutte le modalità sono RGB). Questo elenco è tuttavia soggetto a modifiche. Usare il metodo [**IFullScreenVideoEx:: GetModeInfo**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getmodeinfo) per ottenere informazioni sulle modalità. Il renderer a schermo intero sceglie sempre la modalità di risoluzione più bassa disponibile, limitata da una proprietà denominata *fattore di ritaglio*, che determina la quantità di video a cui il renderer a schermo intero può ritagliare. Per ulteriori informazioni, vedere [**IFullScreenVideoEx:: GetClipFactor**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-ifullscreenvideoex-getclipfactor).

Quando l'applicazione esegue o sospende il grafico del filtro, il renderer a schermo intero passa alla modalità di visualizzazione scelta. Quando il grafico si interrompe, il renderer a schermo intero ripristina la modalità di visualizzazione originale.

Il renderer a schermo intero può funzionare solo come finestra attiva in primo piano. Se l'utente passa a un'altra applicazione, il renderer a schermo intero nasconde il video riducendo o nascondendo la finestra del video.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



