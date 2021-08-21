---
description: Filtro AVI per il compressore
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro AVI per il compressore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa074f5ad4a72fe1e1a32f45baa4888a526b1a0532a562c2fadb7753ea71e0aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159273"
---
# <a name="avi-compressor-filter"></a>Filtro AVI per il compressore

Il filtro AVI Compression Manager consente ai codec VCM (Video Compression Manager) di unirsi a un grafo di filtro. Ogni codec viene visualizzato come istanza separata del filtro. Non è possibile creare direttamente questo filtro con CoCreateInstance. È invece necessario usare l'enumeratore del dispositivo di sistema. Per altre informazioni, vedere [Uso dell'enumeratore del dispositivo di sistema](using-the-system-device-enumerator.md).

Il pin di input del filtro si connette ai filtri che generano dati video non compressi, ad esempio filtri di acquisizione video o filtro [AVI Splitter.](avi-splitter-filter.md) Il pin di output del filtro si connette in genere a un filtro MUX, ad esempio il filtro [Mux AVI.](avi-mux-filter.md)

Se il codec supporta una finestra di dialogo di configurazione VFW di vecchio stile o la finestra di dialogo Informazioni su, un'applicazione può visualizzarla usando [**l'interfaccia IAMVfwCompressDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)

> [!Note]  
> I codec MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.

 



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMVfwCompressDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | Non applicabile                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                  |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



