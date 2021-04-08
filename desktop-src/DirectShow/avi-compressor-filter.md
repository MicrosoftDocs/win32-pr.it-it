---
description: Filtro compressore AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro compressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875946"
---
# <a name="avi-compressor-filter"></a>Filtro compressore AVI

Il filtro del compressore AVI consente ai codec di Gestione compressione video di aggiungere un grafico a filtro. Ogni codec viene visualizzato come un'istanza separata del filtro. Non è possibile creare direttamente questo filtro con CoCreateInstance. È invece necessario utilizzare l'enumeratore di dispositivo di sistema. Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).

Il pin di input del filtro si connette ai filtri che restituiscono dati video non compressi, ad esempio i filtri di acquisizione video o il [filtro separatore AVI](avi-splitter-filter.md). Il pin di output del filtro in genere si connette a un filtro MUX, ad esempio il [filtro Mux AVI](avi-mux-filter.md).

Se il codec supporta una finestra di dialogo di configurazione VFW obsoleta o una finestra di dialogo informazioni su, un'applicazione può visualizzarla usando l'interfaccia [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .

> [!Note]  
> I compressatori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipi di supporti pin di input                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                                                                                                                                                               |
| Interfacce del PIN di output                    | [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | Non applicabile                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                  |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_VIDEOCOMPRESSORCATEGORY CLSID                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



