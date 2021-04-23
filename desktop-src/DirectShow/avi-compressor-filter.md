---
description: Filtro AVI Filter
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro AVI Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909469"
---
# <a name="avi-compressor-filter"></a>Filtro AVI Filter

Il filtro AVI Ntfs consente ai codec VCM (Video Compression Manager) di unirsi a un grafico di filtro. Ogni codec viene visualizzato come un'istanza separata del filtro. Non è possibile creare direttamente questo filtro con CoCreateInstance. È invece necessario usare l'enumeratore del dispositivo di sistema. Per altre informazioni, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).

Il pin di input del filtro si connette ai filtri che generano dati video non compressi, ad esempio i filtri di acquisizione video o il filtro [AVI Splitter.](avi-splitter-filter.md) Il pin di output del filtro si connette in genere a un filtro MUX, ad esempio il filtro [Mux AVI.](avi-mux-filter.md)

Se il codec supporta una finestra di dialogo di configurazione VFW o una finestra di dialogo Informazioni su, un'applicazione può visualizzarlo usando [**l'interfaccia IAMVfwCompressDialogs.**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)

> [!Note]  
> I file MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.

 



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMVfwCompressDialogs,**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)IPersistPropertyBag, ISpecifyPropertyPages                                                                                                             |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                             |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                                                                               |
| Interfacce pin di output                    | [**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | Non applicabile                                                                                                                                                                                                                                     |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                                                  |
| File eseguibile                               | qcap.dll                                                                                                                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ VideoCompressorCategory                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



