---
description: Filtro origine file (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro origine file (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125106"
---
# <a name="file-source-url-filter"></a>Filtro origine file (URL)

Il filtro origine file URL è un filtro di origine asincrono generico che funziona con qualsiasi file di origine che può essere identificato da un Uniform Resource Locator (URL) e il cui tipo di supporto principale è flusso. Sono inclusi i file AVI, MOV, MPEG e WAV. È necessario che il filtro downstream sia un parser, ad esempio il [separatore di flusso MPEG-1](mpeg-1-stream-splitter-filter.md), il [separatore AVI](avi-splitter-filter.md)o il [parser film QuickTime](quicktime-movie-parser-filter.md).



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)       |
| Tipi di supporti pin di input                    | Non applicabile                                                                                                                       |
| Interfacce pin di input                     | Non applicabile                                                                                                                       |
| Tipi di supporti pin di output                   | \_Flusso MEDIATYPE. Il sottotipo dipende dal formato multimediale. (MEDIASUBTYPE \_ NULL se il filtro non riconosce il formato.         |
| Interfacce del PIN di output                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID filtro                             | \_URLREADER CLSID                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                           |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                                                      |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                        |



 

## <a name="remarks"></a>Commenti

Questo filtro usa URLMon e supporta le tabelle codici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



