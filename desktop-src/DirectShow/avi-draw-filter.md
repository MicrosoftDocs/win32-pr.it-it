---
description: Filtro di disegno AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro di disegno AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003336a68bdc1591e6e9a3f8af139f4bf27ddc4d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471277"
---
# <a name="avi-draw-filter"></a>Filtro di disegno AVI

Il filtro AVI Draw viene estratto automaticamente in un grafico di riproduzione anziché nel [decompressore AVI](avi-decompressor-filter.md) quando il video viene restituito a un monitor tv NTSC esterno.




| | | Filtrare le interfacce | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipi di supporti pin di input | Tipo principale: MEDIATYPE_VideoSubtypes:<br /><ul><li>MEDIASUBTYPE_MJPG</li><li>MEDIASUBTYPE_TVMJ</li><li>MEDIASUBTYPE_WAKE</li><li>MEDIASUBTYPE_CFCC</li><li>MEDIASUBTYPE_IJPG</li><li>MEDIASUBTYPE_Plum</li><li>MEDIASUBTYPE_DVCS</li><li>MEDIASUBTYPE_DVSD</li><li>MEDIASUBTYPE_MDVF</li><li>Tipo di formato: FORMAT_VideoInfo</li></ul> | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | MEDIATYPE_Video, MEDIASUBTYPE_NULL | | Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare i | CLSID CLSID_AVIDraw | | ClSID della pagina delle proprietà | Nessuna pagina delle proprietà. | | File eseguibile | quartz.dll | | <a href="merit.md">Merito</a> | MERIT_NORMAL + 100 | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Poiché il filtro AVI Draw e il filtro di acquisizione [VFW](vfw-capture-filter.md) si connettono entrambi allo stesso hardware, non possono essere nello stesso grafico dei filtri.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




