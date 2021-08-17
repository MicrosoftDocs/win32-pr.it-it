---
description: Filtro decodificatore video DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro decodificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f00d63c92da4c16697d7cc9ff173f4c50e822a10da429a586f8eaa688e9eb96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820683"
---
# <a name="dv-video-decoder-filter"></a>Filtro decodificatore video DV

Questo filtro decodifica un flusso video digitale (DV) in un video non compresso.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec,</strong></a> <strong>IPersistStream,</strong> <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td><ul>
<li>MEDIATYPE_Video</li>
<li>MEDIASUBTYPE_dvsd</li>
<li>FORMAT_VideoInfo, FORMAT_DvInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td><strong>Tipo principale:</strong>MEDIATYPE_Video<strong>sottotipi:</strong><br/>
<ul>
<li>MEDIASUBTYPE_YUY2</li>
<li>MEDIASUBTYPE_UYVY</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
<li>MEDIASUBTYPE_ARGB32</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_Y41P</li>
</ul>
<strong>Tipi di formato</strong>:<br/> Format_VideoInfo, Format_VideoInfo2<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtro CLSID</td>
<td>CLSID_DVVideoCodec</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>CLSID_DVDecPropertiesPage</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_NORMAL</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Usare [**l'interfaccia IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) per impostare la risoluzione di decodifica su full, half size, quarter size o one-eighth size.

**Interlacciamento:** le versioni precedenti del decodificatore del video vengono sempre delnterlace. A data di DirectX 9.0, il decodificatore video DV può mantenere l'interlacciamento. In questo modo il video interlacciato può essere deinterlaced dal renderer di mixaggio video (VMR), per migliorare la qualità del rendering. Per usare questa funzionalità, il filtro downstream deve supportare i formati [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) indicati da tale valore Format VideoInfo2 nel membro formattype della struttura \_ [**AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)  Nell'output con risoluzione completa, i flag di dinterlazione (**dwInterlace**) nella struttura **VIDEOINFOHEADER2** sono impostati su , a indicare i campi `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` interlacciati. A metà risoluzione o inferiore, **dwInterlace** è impostato su zero, a indicare fotogrammi progressivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




