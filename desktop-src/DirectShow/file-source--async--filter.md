---
description: Filtro di origine file (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro di origine file (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481645"
---
# <a name="file-source-async-filter"></a>Filtro di origine file (Async)

Il filtro origine file asincrono apre e legge i file locali di molti formati dati diversi e passa i dati a un filtro del parser.

Per scaricare i file multimediali dal Web tramite HTTP, usare il filtro di [origine file (URL)](file-source--url--filter.md) . Per leggere i file ASF, usare il filtro [WM ASF Reader](wm-asf-reader-filter.md) .



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Tipi di supporti pin di input                    | Non applicabile                                                                                                                       |
| Interfacce pin di input                     | Non applicabile                                                                                                                       |
| Tipi di supporti pin di output                   | **MEDIATYPE \_ Flusso**. Il sottotipo dipende dal formato multimediale. (**MEDIASUBTYPE \_ null** se il filtro non riconosce il formato). |
| Interfacce del PIN di output                    | [**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID filtro                             | **\_ASYNCREADER CLSID**                                                                                                               |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                           |
| [Merito](merit.md)                       | **VALORE \_ improbabile**                                                                                                                  |
| [Categoria filtro](filter-categories.md) | **\_LEGACYAMFILTERCATEGORY CLSID**                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



