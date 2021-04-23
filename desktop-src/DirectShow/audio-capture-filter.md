---
description: Filtro di acquisizione audio
ms.assetid: f76d5c82-33b2-4579-9420-8f97eca53ede
title: Filtro acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a630452565fafad3c4a4420154efd8fe6b282f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910209"
---
# <a name="audio-capture-filter"></a>Filtro acquisizione audio

Il filtro Acquisizione audio rappresenta un dispositivo di acquisizione audio. Ha un pin di output di acquisizione e diversi pin di input (uno per ogni tipo di input nella scheda, ad esempio Line In, Mic, CD e MIDI).

Questo filtro può funzionare con più di un dispositivo hardware, pertanto la chiamata a CoCreateInstance per creare il filtro non funziona. Usare invece [l'enumeratore del dispositivo di sistema](system-device-enumerator.md). L'enumeratore del dispositivo di sistema restituisce un moniker univoco per ogni dispositivo. Il nome descrittivo del moniker corrisponde al nome del dispositivo. Questo è il nome visualizzato in GraphEdit. Per altre informazioni, vedere [Enumerazione di dispositivi e filtri.](enumerating-devices-and-filters.md)



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IAMResourceControl,**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                               |
| Tipi di supporti pin di input                    | MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                         |
| Interfacce pin di input                     | [**IAMAudioInputMixer,**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                           |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Audio, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IAMBufferNegotiation,**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation) [**IAMPushSource,**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMStreamControl,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) [**IKsPropertySet,**](ikspropertyset.md) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID del filtro                             | Non applicabile                                                                                                                                                                                                                                                                                     |
| CLSID pagina delle proprietà                      | CLSID \_ AudioInputMixerProperties                                                                                                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ AudioInputDeviceCategory                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Commenti

I pin di input rappresentano le connessioni hardware fisiche e non sono mai connessi ad altri filtri in DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 



