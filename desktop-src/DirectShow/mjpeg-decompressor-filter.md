---
description: Filtro decompressore MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro decompressore MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f0587abe77d1f76df043a37bc8e54db91d65d81e00b0a2677268b6d61bc782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684941"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro decompressore MJPEG

Questo filtro decodifica un flusso video da MOTION JPEG a un video non compresso. Alcune videocamere digitali producono un flusso video JPEG in movimento.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                               |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                         |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Questo filtro è compatibile con il video JPEG in movimento che usa il codice FOURCC 'MJPG'. Non è in grado di decodificare altre varietà di jpeg di movimento. Per queste operazioni, è necessario usare un filtro decodificatore di terze parti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



