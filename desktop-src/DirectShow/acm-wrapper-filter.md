---
description: Filtro wrapper ACM
ms.assetid: f3cd8e90-8949-482a-8ada-47711f6c935f
title: Filtro wrapper ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3897f5345d9d974c16193f922e173a4e0237ece9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468578"
---
# <a name="acm-wrapper-filter"></a>Filtro wrapper ACM

Il filtro Wrapper ACM consente ai codec ACM (Audio Compression Manager) di unire un grafico filtri. Può fungere da filtro di decompressione o da filtro di compressione.

Come filtro di decompressione, il wrapper ACM viene visualizzato nella categoria "filtri DirectShow" (CLSID LegacyAmFilterCategory) e ha un merito di \_ MERIT \_ NORMAL. Il tipo di supporto di connessione sul pin di input determina il codec utilizzato dal filtro. In genere, l'applicazione non deve aggiungere il filtro al grafico dei filtri. viene estratto automaticamente da Filter Graph Manager quando necessario. La decompressione è solo per l'audio PCM.

Come filtro di compressione, il wrapper ACM viene visualizzato nella categoria "Audio Compressions" (CLSID AudioCompressorCategory) e ha un merito di \_ MERIT \_ DO NOT \_ \_ USE. Ogni codec viene visualizzato come istanza separata. Per la compressione, non è possibile creare direttamente il filtro con CoCreateInstance. È invece necessario usare l'enumeratore del dispositivo di sistema. Per altre informazioni, vedere [Uso dell'enumeratore del dispositivo di sistema](using-the-system-device-enumerator.md).




| | | Filtrare le interfacce | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a>IPersist, IPersistPropertyBag | | Tipi di supporti pin di input | MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx | | Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipi di supporti pin di output | MEDIATYPE_Audio, MEDIASUBTYPE_PCM, FORMAT_WaveFormatEx.Qualsiasi combinazione di quanto segue è possibile:<br /><ul><li>Esempi al secondo (kHz): 44.1, 22.05, 11.025 o 8.0.</li><li>Canali: stereo o mono.</li><li>Bit per campione: 8 o 16.</li></ul> | | Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig"><strong>IAMStreamConfig,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare i | CLSID CLSID_ACMWrapper | | ClSID della pagina delle proprietà | Nessuna pagina delle proprietà. | | File eseguibile | Quartz.dll | | <a href="merit.md">Merito</a> | MERIT_NORMAL o MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory o CLSID_AudioCompressorCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




