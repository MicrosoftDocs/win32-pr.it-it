---
description: Filtro VGA 16 Color Ditherer
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro VGA 16 Color Ditherer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908679"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtro VGA 16 Color Ditherer

Il filtro VGA 16 Color Ditherer esegue la conversione da un tipo di colore RGB a uno schermo a colori a 4 bit in modo che i flussi video AVI e MPEG possano essere visualizzati su monitor a 16 colori meno recenti. Questo filtro viene inserito nel grafico tra un filtro decompressore e un filtro del renderer video.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | Dithering CLSID \_                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | quartz.dll                                                                                                                                         |
| [Merito](merit.md)                       | PROBABILITÀ \_ IMPROBABILE                                                                                                                                    |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



