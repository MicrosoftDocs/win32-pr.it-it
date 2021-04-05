---
description: Gestione porta video
ms.assetid: d70558a5-9820-432a-b4f3-ccf7bb2a34d5
title: Gestione porta video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ca884ff009584ef2904387d872733ddf8d53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883081"
---
# <a name="video-port-manager"></a>Gestione porta video

Il filtro di gestione porta video (VPM) consente al filtro renderer video mixing 7 (VMR-7) di funzionare con i dispositivi di acquisizione video o i decodificatori hardware che usano una porta video. Una porta video è una connessione hardware diretta al chip grafico. Consente il trasferimento dei video direttamente al chip grafico senza passare sul bus di sistema.

> [!Note]  
> Il gestore della porta video non è compatibile con VMR-9 perché VMR-9 non supporta le porte video.

 



|                                          |                                                                                                                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMVideoDecimationProperties**](/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IKsPropertySet**](ikspropertyset.md), [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop), [**IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ VPVIDEO o MEDIASUBTYPE \_ VPVBI, formato \_ None                                                                                                                                         |
| Interfacce pin di input                     | [**IKsPin**](ikspin.md), [**IKsPropertySet**](ikspropertyset.md), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Tipi di supporti pin di output                   | \_Video MEDIATYPE, formato \_ VideoInfo2                                                                                                                                                                                 |
| Interfacce del PIN di output                    | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                     |
| CLSID filtro                             | \_VIDEOPORTMANAGER CLSID                                                                                                                                                                                              |
| [Merito](merit.md)                       | VALORE \_ normale                                                                                                                                                                                                        |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Video Port Manager combina le funzionalità della porta video del filtro per il [mixer overlay](overlay-mixer-filter.md) e la funzionalità dell' [allocatore della superficie VBI](vbi-surface-allocator.md). Il VPM alloca le porte e le superfici video e sincronizza l'acquisizione dei dati dalla porta video. Consente l'acquisizione basata su porta video indipendente dal rendering. Se si desidera visualizzare l'anteprima, VPM coordina con VMR-7 per visualizzare i dati acquisiti della porta video. Quando nel sistema è presente una porta video, il filtro di acquisizione richiede buffer aggiuntivi per estrarre i dati VBI dal flusso video. Questi buffer sono forniti da VPM. Una volta che il filtro di acquisizione ha estratto i dati VBI, lo recapita su un pin separato ai filtri, ad esempio il decodificatore CC. Nella figura seguente vengono illustrati VPM e le relative connessioni in un grafico di filtro.

![segmento del grafico filtro di gestione porte video](images/vpm.png)

Il generatore di DVD Graph aggiunge automaticamente il VPM al grafico di filtro quando viene rilevata una porta video nel sistema. Una volta aggiunto al grafico, VPM utilizza un oggetto DirectDraw fornito dal renderer di combinazione video per allocare due o tre superfici. Queste superfici ricevono i frame digitalizzati dal filtro di acquisizione upstream. In risposta alle notifiche degli eventi in modalità utente inviate quando i dati sono presenti nell'area, VPM esegue una blit automatica a una superficie Offscreen fornita da VMR.

Il fatto che VPM usi più superfici per i buffer di input significa che richiede più VRAM rispetto all'implementazione precedente della porta video DirectShow. Il blit aggiuntivo da VPM a VMR-7 richiede larghezza di banda di memoria video aggiuntiva. Poiché il capovolgimento automatico dell'hardware non viene più usato, esiste un potenziale teorico per i frame eliminati, ma l'evidenza empirica suggerisce che questa situazione non si verifica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[**Interfaccia IVPManager**](/windows/desktop/api/Strmif/nn-strmif-ivpmanager)
</dt> </dl>

 

 



