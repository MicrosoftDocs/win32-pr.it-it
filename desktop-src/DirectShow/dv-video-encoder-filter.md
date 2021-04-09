---
description: Filtro codificatore video DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro codificatore video DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965514"
---
# <a name="dv-video-encoder-filter"></a>Filtro codificatore video DV

Questo filtro codifica un flusso video non compresso in video digitale (DV). Fornisce un'interfaccia personalizzata, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), per l'impostazione della risoluzione e del formato della codifica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td><ul>
<li>Tipo principale: MEDIATYPE_VideoThe sottotipi seguenti sono validi:<br/>
<ul>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB555</li>
</ul></li>
<li>Tipo formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td><ul>
<li>Tipo principale: MEDIATYPE_Video</li>
<li>Sottotipo: MEDIASUBTYPE_dvsd</li>
<li>Tipo formato: FORMAT_VideoInfo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_DVVideoEnc</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>CLSID_DVEncPropertiesPage</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>qdv.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_VideoCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Per video a 16 bit (MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565), l'input deve essere 720 x 480 pixel per NTSC o 720 x 576 pixel per PAL. Per il video a 24 bit, non sono presenti vincoli di dimensione per l'input.

L'output è sempre 720 x 480 per NTSC o 720 x 576 per PAL; il video a 24 bit viene ridimensionato per adattarsi a queste dimensioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 




