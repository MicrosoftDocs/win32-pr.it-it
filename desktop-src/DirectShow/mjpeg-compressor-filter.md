---
description: Filtro compressione MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro compressione MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304220"
---
# <a name="mjpeg-compressor-filter"></a>Filtro compressione MJPEG

Questo filtro comprime un flusso video non compresso, usando la compressione JPEG di movimento.



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipi di supporti pin di input                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | \_Video di MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfacce del PIN di output                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_MJPGENC CLSID                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_VIDEOCOMPRESSORCATEGORY CLSID                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questo filtro codifica usando il sottotipo di supporto MEDIASUBTYPE \_ MJPG, che corrisponde al codice FourCC ' MJPG '.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



