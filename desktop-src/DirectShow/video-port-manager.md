---
description: Gestione porte video
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Gestione porte video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4f030e6be9035432207dc608a775a0e1d30b09
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909199"
---
# <a name="video-port-manager"></a>Gestione porte video

Il filtro Video Port Manager (VPM) consente al filtro del renderer di combinazione video 7 (VMR-7) di funzionare con dispositivi di acquisizione video o decodificatori hardware che usano una porta video. Una porta video è una connessione hardware diretta al chip grafico. Consente di trasferire i video direttamente nel chip grafico senza passare attraverso il bus di sistema.

> [!Note]  
> Gestione porte video non è compatibile con VMR-9, perché VMR-9 non supporta le porte video.

 



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVideo o MEDIASUBTYPE \_ VPVBI, FORMAT \_ None                                                                                                                                         |
| Interfacce pin di input                     | [**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Video, FORMAT \_ VideoInfo2                                                                                                                                                                                 |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| CLSID del filtro                             | CLSID \_ VideoPortManager                                                                                                                                                                                              |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                                                                                        |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Gestione porte video combina la funzionalità della porta video del filtro [del mixer](overlay-mixer-filter.md) di sovrapposizione e la funzionalità dell'allocatore di superficie [VBI.](vbi-surface-allocator.md) Il VPM alloca le porte e le superfici video e sincronizza l'acquisizione dati dalla porta video. Consente l'acquisizione basata su porta video indipendente dal rendering. Se si desidera visualizzare l'anteprima, il VPM si coordina con VMR-7 per visualizzare i dati delle porte video acquisite. Quando nel sistema è presente una porta video, il filtro di acquisizione richiede buffer aggiuntivi per estrarre dati VBI dal flusso video. Questi buffer vengono forniti dal modulo di gestione delle applicazioni virtuali. Dopo aver estratto i dati VBI, il filtro di acquisizione lo recapita su un segnaposto separato ai filtri, ad esempio il decodificatore CC. La figura seguente mostra il VPM e le relative connessioni in un grafo di filtro.

![Segmento del grafico del filtro di Gestione porte video](images/vpm.png)

DVD Graph Builder aggiunge automaticamente il VPM al grafico dei filtri quando viene rilevata una porta video nel sistema. Dopo l'aggiunta al grafo, il modulo di gestione video usa un oggetto DirectDraw fornito dal renderer di combinazione video per allocare due o tre superfici. Queste superfici ricevono i fotogrammi digitalizzati dal filtro di acquisizione upstream. In risposta alle notifiche degli eventi in modalità utente inviate quando i dati sono presenti in superficie, il VPM esegue un blit automatico su una superficie offscreen fornita dal VMR.

Il fatto che il VPM usi più superfici per i buffer di input significa che richiede più VRAM rispetto all'implementazione della porta video DirectShow precedente. Il blit aggiuntivo dal VPM al VMR-7 richiede ulteriore larghezza di banda della memoria video. Poiché il capovolgimento automatico dell'hardware non viene più usato, esiste un potenziale teorico per i fotogrammi eliminati, ma l'evidenza empirica suggerisce che questo non si verifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[**Interfaccia IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



