---
description: Filtro origine file (asincrono)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro origine file (asincrono)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909699"
---
# <a name="file-source-async-filter"></a>Filtro origine file (asincrono)

Il filtro Origine file asincrona apre e legge i file locali di molti formati di dati diversi e passa i dati a un filtro del parser.

Per scaricare file multimediali dal Web tramite HTTP, usare il filtro [Origine file (URL).](file-source--url--filter.md) Per leggere i file ASF, usare il filtro [Lettore ASF WM.](wm-asf-reader-filter.md)



| Label | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)                                                   |
| Tipi di supporti pin di input                    | Non applicabile                                                                                                                       |
| Interfacce pin di input                     | Non applicabile                                                                                                                       |
| Tipi di supporti pin di output                   | **MEDIATYPE \_ Flusso**. Il sottotipo dipende dal formato multimediale. (**MEDIASUBTYPE \_ NULL** se il filtro non riconosce il formato). |
| Interfacce pin di output                    | [**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) |
| CLSID del filtro                             | **CLSID \_ AsyncReader**                                                                                                               |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                     |
| File eseguibile                               | quartz.dll                                                                                                                           |
| [Merito](merit.md)                       | **MERITO \_ IMPROBABILE**                                                                                                                  |
| [Categoria filtro](filter-categories.md) | **CLSID \_ LegacyAmFilterCategory**                                                                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



