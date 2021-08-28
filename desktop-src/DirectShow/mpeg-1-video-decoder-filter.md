---
description: Filtro decodificatore video MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro decodificatore video MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf865d0e8cf45bcbde20a2d5b6f4035a4a17f970
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468228"
---
# <a name="mpeg-1-video-decoder-filter"></a>Filtro decodificatore video MPEG-1

Decodifica il video MPEG-1.




| | | Filtrare le interfacce | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Tipi di supporti pin di input | MEDIATYPE_Video, FORMAT_MPEGVideo<br /> Sono validi i sottotipi seguenti:<br /><ul><li><strong>MEDIASUBTYPE_MPEG1Packet</strong></li><li><strong>MEDIASUBTYPE_MPEG1Payload</strong></li></ul> | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin | |</strong></a> Tipi di supporti pin di output | Tipo principale: <strong>MEDIATYPE_Video</strong>,<br /> Tipo di formato: <strong>FORMAT_VideoInfo</strong> <strong>o FORMAT_VideoInfo2</strong><br /> Sottotipi:<br /><ul><li><strong>MEDIASUBTYPE_RGB24</strong></li><li><strong>MEDIASUBTYPE_RGB32</strong></li><li><strong>MEDIASUBTYPE_RGB8</strong></li><li><strong>MEDIASUBTYPE_RGB555</strong></li><li><strong>MEDIASUBTYPE_RGB565</strong></li><li><strong>MEDIASUBTYPE_UYVY</strong></li><li><strong>MEDIASUBTYPE_Y41P</strong></li><li><strong>MEDIASUBTYPE_YUY2</strong></li></ul> | | Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare i | CLSID <strong>CLSID_CMpegVideoCodec</strong> | | ClSID della pagina delle proprietà | <strong>CLSID_MpegVideoDecodePropertyPage</strong> | | File eseguibile | quartz.dll | | <a href="merit.md">Merito</a> | 0x40000001 | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Commenti

Questo filtro può decodificare in un oggetto DirectDraw Surface. Il filtro usa MMX se il computer supporta MMX.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




