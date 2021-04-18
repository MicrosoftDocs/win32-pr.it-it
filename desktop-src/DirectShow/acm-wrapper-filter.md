---
description: Filtro wrapper ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro wrapper ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da0c1283ac6d4980f51d40001b38c719f5e31c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304271"
---
# <a name="acm-wrapper-filter"></a>Filtro wrapper ACM

Il filtro del wrapper ACM consente ai codec ACM (Audio Compression Manager) di aggiungere un grafico a filtro. Può fungere da filtro di decompressione o come filtro di compressione.

Come filtro di decompressione, il wrapper ACM viene visualizzato nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory) e ha un merito del \_ normale merito. Il tipo di supporto di connessione al pin di input determina il codec utilizzato dal filtro. In genere, l'applicazione non deve aggiungere il filtro al grafico di filtro; Quando necessario, viene eseguito il pull automatico dal gestore del grafico dei filtri. La decompressione è solo l'audio PCM.

Come filtro di compressione, il wrapper ACM viene visualizzato nella categoria "comprimer audio" (CLSID \_ AudioCompressorCategory) ed è caratterizzato da un \_ merito \_ non \_ utilizzato. Ogni codec viene visualizzato come un'istanza separata. Per la compressione non è possibile creare direttamente il filtro con CoCreateInstance. È invece necessario utilizzare l'enumeratore di dispositivo di sistema. Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, IPersist, IPersistPropertyBag</td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx. qualsiasi combinazione dei seguenti elementi è possibile:<br/>
<ul>
<li>Campioni al secondo (kHz): 44,1, 22,05, 11,025 o 8,0.</li>
<li>Canali: stereo o mono.</li>
<li>BITS per campione: 8 o 16.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
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

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




