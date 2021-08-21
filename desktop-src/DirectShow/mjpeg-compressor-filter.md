---
description: Filtro del compressione MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro del compressione MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7891a85aa32b0ec7572a8c3be08f216c75f8655a7782261a675521aa952bf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791391"
---
# <a name="mjpeg-compressor-filter"></a>Filtro del compressione MJPEG

Questo filtro comprime un flusso video non compresso usando la compressione JPEG del movimento.



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**                                                                                                                                                                                             |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MJPG                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ MJPGEnc                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                                                                   |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                                                         |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="remarks"></a>Commenti

Questo filtro codifica usando il sottotipo multimediale MEDIASUBTYPE MJPG, che corrisponde al codice \_ FOURCC 'MJPG'.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



