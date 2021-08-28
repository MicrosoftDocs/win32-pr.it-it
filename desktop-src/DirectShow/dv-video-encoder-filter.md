---
description: Filtro codificatore video DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro codificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e14928c937313d056549a348bd255f251354c0ab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482637"
---
# <a name="dv-video-encoder-filter"></a>Filtro codificatore video DV

Questo filtro codifica un flusso video non compresso in video digitale (DV). Fornisce un'interfaccia personalizzata, [**IDVEnc,**](/windows/desktop/api/Strmif/nn-strmif-idvenc)per l'impostazione della risoluzione e del formato di codifica.




| | | Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | | Tipi di supporti pin di input | <ul><li>Tipo principale: MEDIATYPE_VideoThe seguenti sottotipi validi:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Tipo di formato: FORMAT_VideoInfo</li></ul> | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | <ul><li>Tipo principale: MEDIATYPE_Video</li><li>Sottotipo: MEDIASUBTYPE_dvsd</li><li>Tipo di formato: FORMAT_VideoInfo</li></ul> | | Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare l'| CLSID CLSID_DVVideoEnc | | Pagina delle proprietà CLSID | CLSID_DVEncPropertiesPage | | File eseguibili | qdv.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Commenti

Per i video a 16 bit (MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565), l'input deve essere di 720 x 480 pixel per NTSC o di 720 x 576 pixel per l'elenco di accesso alla pubblicazione. Per i video a 24 bit, non sono presenti vincoli di dimensione sull'input.

L'output è sempre 720 x 480 per NTSC o 720 x 576 per l'elenco di accesso alla pubblicazione. Il video a 24 bit viene ridimensionato in base a queste dimensioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




