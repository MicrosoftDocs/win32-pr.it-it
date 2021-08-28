---
description: Filtro del convertitore di spazi colori
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro del convertitore di spazi colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0a519772a6d38971654cb92a895fcd95f5ecc8
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987064"
---
# <a name="color-space-converter-filter"></a>Filtro del convertitore di spazi colori

Questo filtro di trasformazione esegue la conversione da un tipo di colore RGB a un altro tipo RGB, ad esempio da un colore RGB a 24 bit a 8 bit. Poiché questo tipo di conversione viene in genere gestito in modo più efficiente all'interno di un decompressore video, l'uso principale di Color Space Converter è quando l'origine del flusso è costituita da fotogrammi RGB non compressi.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipi di supporti pin di input | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Sono validi i sottotipi seguenti:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | MEDIATYPE_Video, FORMAT_VideoInfo.<br /> Sono validi i sottotipi seguenti:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtro CLSID | CLSID_Colour | 
| CLSID della pagina delle proprietà | Nessuna pagina delle proprietà. | 
| File eseguibile | quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




