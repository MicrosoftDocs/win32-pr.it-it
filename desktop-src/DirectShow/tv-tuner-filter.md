---
description: Filtro di siner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro di siner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101dfcce4877570a2072d9e4c116466223e56889fb5e66de3e6ef0ec24afad6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015519"
---
# <a name="tv-tuner-filter"></a>Filtro di siner TV

Il filtro Tv Tuner (Tuner TV) seleziona un canale di trasmissione o cavo analogico da visualizzare. Il singolo flusso di output è un percorso hardware per video di baseband analogico. Questo output dovrebbe connettersi al filtro Analog Video Crossbar. I pin di input includono un input per il cavo e un input dell'antenna.



| Etichetta | Valore |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject**, [**IKsPropertySet**](ikspropertyset.md) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                   |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                   |
| Tipi di supporti pin di output                   | Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                      |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| CLSID del filtro                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID pagina delle proprietà                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| File eseguibile                               | Kstvtune.ax                                                                                                                                                                       |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                                               |
| [Categoria filtro](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



