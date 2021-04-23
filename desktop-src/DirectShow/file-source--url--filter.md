---
description: Filtro origine file (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro origine file (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909239"
---
# <a name="file-source-url-filter"></a>Filtro origine file (URL)

Il filtro origine file URL è un filtro di origine asincrono generico che funziona con qualsiasi file di origine che può essere identificato da un Uniform Resource Locator (URL) e il cui tipo di elemento multimediale principale è stream. Sono inclusi i file AVI, MOV, MPEG e WAV. Richiede che il filtro downstream sia un parser, ad esempio [mpeg-1 stream splitter,](mpeg-1-stream-splitter-filter.md) [AVI Splitter](avi-splitter-filter.md)o [QuickTime Movie Parser.](quicktime-movie-parser-filter.md)



| Label | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipi di supporti pin di input                    | Non applicabile                                                                                                                       |
| Interfacce pin di input                     | Non applicabile                                                                                                                       |
| Tipi di supporti pin di output                   | Flusso \_ MEDIATYPE. Il sottotipo dipende dal formato multimediale. (MEDIASUBTYPE \_ NULL se il filtro non riconosce il formato.         |
| Interfacce pin di output                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID del filtro                             | CLSID \_ URLReader                                                                                                                     |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ IMPROBABILE                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                        |



 

## <a name="remarks"></a>Commenti

Questo filtro usa URLMon e supporta le code pages.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



