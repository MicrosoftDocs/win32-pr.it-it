---
description: Filtro renderer audio (WaveOut)
ms.assetid: a3f2776b-974b-4886-82a3-38e00b607a07
title: Filtro renderer audio (WaveOut)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef79acb21221c1a0b91efc2da67773534fe54ca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470158"
---
# <a name="audio-renderer-waveout-filter"></a>Filtro renderer audio (WaveOut)

Questo filtro usa l'API waveOut \* per eseguire il rendering dell'audio della forma d'onda. Tuttavia, il [filtro renderer DirectSound](directsound-renderer-filter.md) offre la stessa funzionalità usando DirectSound. Per impostazione predefinita, Filter Graph Manager usa il renderer DirectSound anziché questo filtro. Il mixaggio audio è disabilitato nel renderer audio waveOut, quindi se è necessario combinare più flussi audio durante la riproduzione, usare il renderer DirectSound.

Questo filtro non controlla il sottotipo del flusso audio. La [**struttura WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) passata nel formato contiene le informazioni necessarie per la connessione.

Questo filtro supporta un intervallo di frequenze di campionamento che dipende dal driver audio.




| | | Filtrare le interfacce | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats"><strong>IAMAudioRendererStats</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamclockslave"><strong>IAMClockSlave</strong></a></li><li><a href="/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound"><strong>IAMDirectSound</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol"><strong>IAMResourceControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-ibasicaudio"><strong>IBasicAudio</strong></a></li><li><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></li><li>IPersistPropertyBag</li><li>Ipersiststream</li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></li></ul> | | Tipi di supporti pin di input | <strong>MEDIATYPE_Audio</strong> | | Interfacce pin di input | <ul><li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li><li><a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></li></ul> | | Tipi di supporti pin di output | Non applicabile. | | Interfacce pin di output | Non applicabile. | | Filtrare i | CLSID <strong>CLSID_AudioRender</strong> | | ClSID della pagina delle proprietà | <strong>CLSID_AudioProperties</strong>, <strong>CLSID_AudioRendererAdvancedProperties</strong> | | File eseguibile | quartz.dll | | <a href="merit.md">Merito</a>  |  <strong>MERIT_DO_NOT_USE</strong> | | <a href="filter-categories.md">Categoria filtro</a>  |  <strong>CLSID_AudioRendererCategory</strong> | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 
