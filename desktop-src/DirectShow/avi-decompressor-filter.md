---
description: Filtro Decompressore AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro Decompressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746922"
---
# <a name="avi-decompressor-filter"></a>Filtro Decompressore AVI

Il filtro del decompressore AVI consente ai codec di Gestione compressione video di aggiungere un grafico a filtro. Non è necessario che l'applicazione aggiunga il filtro al grafico di filtro; Quando necessario, viene eseguito il pull automatico dal gestore del grafico dei filtri.

Quando il gestore del grafo del filtro compila un grafico per eseguire il rendering di un file AVI, verifica FOURCC nell'intestazione AVI del file per determinare se il flusso video è compresso. In tal caso, il gestore del grafico di filtro aggiunge il decompressore AVI, che quindi Cerca nel registro di sistema un decompressore installato in grado di gestire il file.

> [!Note]  
> I decompressori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.

 

Sul suo pin upstream, il decompressore AVI si connette in genere al [separatore AVI](avi-splitter-filter.md). Sul pin di output si connette in genere al [renderer video](video-renderer-filter.md) o al [filtro Mux AVI](avi-mux-filter.md).



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Tipi di supporti pin di input                    | Tipo principale: MEDIATYPE \_ VideoSubtype: deve corrispondere al codice FourCC per il tipo di compressione. Per altre informazioni, vedere [codici FourCC](fourcc-codes.md).<br/> Tipo di formato: FORMAT \_ videoinfo<br/> |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Tipi di supporti pin di output                   | MEDIATYPE \_ video, MEDIASUBTYPE \_ null, Format \_ videoinfo                                                                                                                                                            |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| CLSID filtro                             | \_AVIDEC CLSID                                                                                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                  |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                         |
| [Merito](merit.md)                       | VALORE \_ normale                                                                                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




