---
description: Filtro decompressore MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro decompressore MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910019"
---
# <a name="mjpeg-decompressor-filter"></a>Filtro decompressore MJPEG

Questo filtro decodifica un flusso video da MOTION JPEG a un video non compresso. Alcune videocamere digitali producono un flusso video JPEG in movimento.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                               |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ MjpegDec                                                                                                                                    |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                         |
| [Merito](merit.md)                       | MERIT \_ NORMAL                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Commenti

Questo filtro è compatibile con il video JPEG di movimento che usa il codice FOURCC 'MJPG'. Non può decodificare altri tipi di movimento JPEG. Per queste operazioni, è necessario usare un filtro decodificatore di terze parti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



