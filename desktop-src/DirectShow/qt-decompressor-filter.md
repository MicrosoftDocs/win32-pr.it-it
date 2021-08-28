---
description: Filtro decompressore QT
ms.assetid: d013075f-deab-40ef-8438-4fb09820da3e
title: Filtro decompressore QT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cedb26acdcfabb3c0be4aeb2cbf306b654f9570
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983650"
---
# <a name="qt-decompressor-filter"></a>Filtro decompressore QT

Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.

Il filtro decompressore QT decomprime apple® QuickTime® 2.0 video. Questo formato viene in genere usato nei file QuickTime meno recenti.




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipi di supporti pin di input | MEDIATYPE_Video, FORMAT_VideoInfo<br /> Sono validi i sottotipi seguenti:<br /><ul><li>MEDIASUBTYPE_QTRpza</li><li>MEDIASUBTYPE_QTSmc</li><li>MEDIASUBTYPE_QTRle</li><li>MEDIASUBTYPE_QTJpeg</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Filtro CLSID | CLSID_QTDec | 
| CLSID della pagina delle proprietà | Nessuna pagina delle proprietà. | 
| File eseguibile | quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_NORMAL | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




