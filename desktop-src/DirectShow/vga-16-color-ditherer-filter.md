---
description: Filtro del sequelo di colore VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro del sequelo di colore VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057827"
---
# <a name="vga-16-color-ditherer-filter"></a>Filtro del sequelo di colore VGA 16

Il filtro di tipo VGA a 16 colori viene convertito da un tipo di colore RGB a una visualizzazione a colori a 4 bit, in modo che i flussi video AVI e MPEG possano essere visualizzati nei monitoraggi a 16 colori precedenti. Questo filtro viene inserito nel grafico tra un filtro decompressore e un filtro renderer video.



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | \_Video di MEDIATYPE, MEDIASUBTYPE \_ RGB8                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | \_Video di MEDIATYPE, MEDIASUBTYPE \_ RGB4                                                                                                               |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_Dithering CLSID                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                  |
| File eseguibile                               | quartz.dll                                                                                                                                         |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                                                                    |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



