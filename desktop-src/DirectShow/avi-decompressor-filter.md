---
description: Filtro decompressore AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro decompressore AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910099"
---
# <a name="avi-decompressor-filter"></a>Filtro decompressore AVI

Il filtro AVI Decompressor consente ai codec VCM (Video Compression Manager) di unire un grafico dei filtri. L'applicazione non deve aggiungere il filtro al grafico dei filtri. viene estratto automaticamente da Filter Graph Manager quando necessario.

Quando Filter Graph Manager compila un grafo per eseguire il rendering di un file AVI, controlla FOURCC nell'intestazione AVI del file per determinare se il flusso video è compresso. In caso contrario, Filter Graph Manager aggiunge il decompressore AVI, che cerca nel Registro di sistema un decompressore installato in grado di gestire il file.

> [!Note]  
> I decompressori MPEG non vengono mai implementati come codec VCM, ma solo come filtri DirectShow nativi.

 

Sul pin upstream il decompressore AVI si connette in genere alla barra di divisione [AVI.](avi-splitter-filter.md) Nel pin di output si connette in genere al [renderer video o](video-renderer-filter.md) al filtro [Mux AVI.](avi-mux-filter.md)



| Label | Valore |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**Filtro IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| Tipi di supporti pin di input                    | Tipo principale: MEDIATYPE \_ VideoSubtype: deve corrispondere al codice FOURCC per il tipo di compressione. Per altre informazioni, vedere [FOURCC Codes](fourcc-codes.md).<br/> Tipo di formato: FORMAT \_ VideoInfo<br/> |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                             |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo                                                                                                                                                            |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                 |
| Filtro CLSID                             | CLSID \_ AVIDec                                                                                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                                                                                                                                  |
| File eseguibile                               | quartz.dll                                                                                                                                                                                                         |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                                                                                                                                                                      |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




