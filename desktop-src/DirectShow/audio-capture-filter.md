---
description: Filtro acquisizione audio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtro acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73da50653a4a159d30a6ca1b83ebc1f37a6de42c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747258"
---
# <a name="audio-capture-filter"></a>Filtro acquisizione audio

Il filtro di acquisizione audio rappresenta un dispositivo di acquisizione audio. Include un pin di output di acquisizione e diversi pin di input (uno per ogni tipo di input sulla scheda, ad esempio line in, MIC, CD e MIDI).

Questo filtro può funzionare con più di un dispositivo hardware, quindi la chiamata a CoCreateInstance per la creazione del filtro non funziona. Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md). L'enumeratore del dispositivo di sistema restituisce un moniker univoco per ogni dispositivo. Il nome descrittivo del moniker corrisponde al nome del dispositivo. Si tratta del nome visualizzato in GraphEdit. Per altre informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).



|                                          |                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IAMResourceControl**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Tipi di supporti pin di input                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                         |
| Interfacce pin di input                     | [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer), [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Tipi di supporti pin di output                   | MEDIATYPE \_ audio, MEDIASUBTYPE \_ null                                                                                                                                                                                                                                                               |
| Interfacce del PIN di output                    | [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation), [**IAMPushSource**](/windows/desktop/api/Strmif/nn-strmif-iampushsource), [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IKsPropertySet**](ikspropertyset.md), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | Non applicabile                                                                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | \_AUDIOINPUTMIXERPROPERTIES CLSID                                                                                                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_AUDIOINPUTDEVICECATEGORY CLSID                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

I pin di input rappresentano le connessioni hardware fisiche e non sono mai connessi ad altri filtri in DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



