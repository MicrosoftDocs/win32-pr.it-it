---
description: Filtro siner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro siner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909029"
---
# <a name="tv-tuner-filter"></a>Filtro siner TV

Il filtro Siner TV seleziona una trasmissione o un canale via cavo analogico da visualizzare. Il flusso di output singolo è un percorso hardware per video con banda di base analogica. Questo output deve connettersi al filtro crossbar video analogico. I pin di input includono un input per il cavo e un input dell'antenna.



| Label | Valore |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMTVTuner,**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) **ISpecifyPropertyPages,** **IPersistPropertyBag,** **IKsObject,** [**IKsPropertySet**](ikspropertyset.md) |
| Tipi di supporti pin di input                    | Non applicabile.                                                                                                                                                                   |
| Interfacce pin di input                     | Non applicabile.                                                                                                                                                                   |
| Tipi di supporti pin di output                   | Video: MEDIATYPE \_ AnalogVideo, KSDATAFORMAT \_ SUBTYPE \_ NONE Audio: MEDIATYPE \_ AnalogAudio, MEDIASUBTYPE \_ NULL                                                                      |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| Filtro CLSID                             | CLSID \_ TVTunerFilter                                                                                                                                                              |
| CLSID della pagina delle proprietà                      | CLSID \_ TVTunerFilterPropertyPage                                                                                                                                                  |
| File eseguibile                               | Kstvtune.ax                                                                                                                                                                       |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                                               |
| [Categoria filtro](filter-categories.md) | AM \_ KSCATEGORY \_ TVTUNER                                                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



