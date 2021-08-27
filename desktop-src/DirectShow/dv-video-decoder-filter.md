---
description: Filtro del decodificatore video DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro del decodificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12131aa09f8e3f7dbef56504ad55410af11ffcbe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466048"
---
# <a name="dv-video-decoder-filter"></a>Filtro del decodificatore video DV

Questo filtro decodifica un flusso video digitale (DV) in un video non compresso.




| | | Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | | Tipi di supporti pin di input | <ul><li>MEDIATYPE_Video</li><li>MEDIASUBTYPE_dvsd</li><li>FORMAT_VideoInfo, FORMAT_DvInfo</li></ul> | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | <strong>Tipo principale:</strong>MEDIATYPE_Video<strong>sottotipi</strong>:<br /><ul><li>MEDIASUBTYPE_YUY2</li><li>MEDIASUBTYPE_UYVY</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li><li>MEDIASUBTYPE_ARGB32</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_Y41P</li></ul><strong>Tipi di formato:</strong><br /> Format_VideoInfo, Format_VideoInfo2<br /> | | Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare clsID | CLSID_DVVideoCodec | | Pagina delle proprietà CLSID | CLSID_DVDecPropertiesPage | | File eseguibili | qdv.dll | | <a href="merit.md">|</a> MERIT_NORMAL | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Usare [**l'interfaccia IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) per impostare la risoluzione di decodifica su full, half size, quarter size o one-eighth size.

**Interlacciamento:** le versioni precedenti del decodificatore eseguano sempre il dinterlace del video. A data di DirectX 9.0, il decodificatore video DV può mantenere l'interlacciamento. In questo modo il video interlacciato può essere dinterlacciato dal renderer di combinazione di video per migliorare la qualità del rendering. Per usare questa funzionalità, il filtro downstream deve supportare i formati [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) indicati da tale valore Format VideoInfo2 nel membro formattype della struttura \_ [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)  Con l'output a risoluzione completa, i flag di deinterlacciamento (**dwInterlace**) nella struttura **VIDEOINFOHEADER2** vengono impostati su , a indicare i campi `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` interlacciati. A metà risoluzione o inferiore, **dwInterlace è** impostato su zero, a indicare fotogrammi progressivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




