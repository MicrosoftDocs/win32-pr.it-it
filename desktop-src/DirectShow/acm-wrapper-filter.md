---
description: Filtro wrapper ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro wrapper ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aaa56d955fe9cf1966e17c657fbf741b4bb8694a7f18b501b148b0383ea19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664080"
---
# <a name="acm-wrapper-filter"></a>Filtro wrapper ACM

Il filtro Wrapper ACM consente ai codec ACM (Audio Compression Manager) di unire un grafico filtri. Può fungere da filtro di decompressione o da filtro di compressione.

Come filtro di decompressione, il wrapper ACM viene visualizzato nella categoria "filtri DirectShow" (CLSID LegacyAmFilterCategory) e ha un merito di \_ MERIT \_ NORMAL. Il tipo di supporto di connessione sul pin di input determina il codec utilizzato dal filtro. In genere, l'applicazione non deve aggiungere il filtro al grafico dei filtri. viene estratto automaticamente da Filter Graph Manager quando necessario. La decompressione è solo per l'audio PCM.

Come filtro di compressione, il wrapper ACM viene visualizzato nella categoria "Audio Compressions" (CLSID AudioCompressorCategory) e ha un merito di \_ MERIT \_ DO NOT \_ \_ USE. Ogni codec viene visualizzato come istanza separata. Per la compressione, non è possibile creare direttamente il filtro con CoCreateInstance. È invece necessario usare l'enumeratore del dispositivo di sistema. Per altre informazioni, vedere [Uso dell'enumeratore del dispositivo di sistema](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Qualsiasi combinazione di quanto segue è possibile:<br/>
<ul>
<li>Esempi al secondo (kHz): 44.1, 22.05, 11.025 o 8.0.</li>
<li>Canali: stereo o mono.</li>
<li>Bit per campione: 8 o 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtro CLSID</td>
<td>CLSID_ACMWrapper</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà.</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_NORMAL o MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




