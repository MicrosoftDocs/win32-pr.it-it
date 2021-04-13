---
description: Filtro sintonizzatore TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro sintonizzatore TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348556"
---
# <a name="tv-tuner-filter"></a>Filtro sintonizzatore TV

Il filtro del sintonizzatore TV seleziona un canale di trasmissione o trasmissione analogo da visualizzare. Il flusso di output singolo è un percorso hardware per il video di Baseband analogico. Questo output deve connettersi al filtro per la traversa video analogo. I pin di input includono un input per il cavo e un input di antenna.



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**Impossibile IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                   |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                   |
| Tipi di supporti pin di output                   | Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SubType \_ None audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ null                                                                      |
| Interfacce del PIN di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| CLSID filtro                             | \_TVTUNERFILTER CLSID                                                                                                                                                              |
| CLSID della pagina delle proprietà                      | \_TVTUNERFILTERPROPERTYPAGE CLSID                                                                                                                                                  |
| File eseguibile                               | KSTVTune.ax                                                                                                                                                                       |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                               |
| [Categoria filtro](filter-categories.md) | \_TVTUNER KSCATEGORY \_                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



