---
description: Filtro codificatore video DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro codificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c89574ab257467e16b566fe899a5ab32384e48e
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986794"
---
# <a name="dv-video-encoder-filter"></a>Filtro codificatore video DV

Questo filtro codifica un flusso video non compresso in video digitale (DV). Fornisce un'interfaccia personalizzata, [**IDVEnc,**](/windows/desktop/api/Strmif/nn-strmif-idvenc)per l'impostazione della risoluzione e del formato di codifica.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong> | 
| Tipi di supporti pin di input | <ul><li>Tipo principale: MEDIATYPE_VideoThe seguenti sottotipi validi:<br /><ul><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB555</li></ul></li><li>Tipo di formato: FORMAT_VideoInfo</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | <ul><li>Tipo principale: MEDIATYPE_Video</li><li>Sottotipo: MEDIASUBTYPE_dvsd</li><li>Tipo di formato: FORMAT_VideoInfo</li></ul> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID del filtro | CLSID_DVVideoEnc | 
| CLSID pagina delle proprietà | CLSID_DVEncPropertiesPage | 
| File eseguibile | qdv.dll | 
| <a href="merit.md">Merito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_VideoCompressorCategory | 




 

## <a name="remarks"></a>Commenti

Per i video a 16 bit (MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565), l'input deve essere di 720 x 480 pixel per NTSC o di 720 x 576 pixel per l'elenco di accesso alla pubblicazione. Per i video a 24 bit, non sono presenti vincoli di dimensione sull'input.

L'output è sempre 720 x 480 per NTSC o 720 x 576 per l'elenco di accesso alla pubblicazione. Il video a 24 bit viene ridimensionato in base a queste dimensioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




