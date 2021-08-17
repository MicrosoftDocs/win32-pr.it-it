---
description: Funzionalità audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Funzionalità audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd12f3e151a73c2a297d10fec4233ac0e931e11d8bf16e1068f6335c781ed6da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824231"
---
# <a name="audio-capabilities"></a>Funzionalità audio

Per le funzionalità audio, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) restituisce una matrice di coppie di strutture [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) e [**AUDIO STREAM CONFIG \_ \_ \_ CAPS.**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) Come per i video, è possibile usarlo per esporre tutti i tipi di funzionalità audio sul pin, ad esempio la velocità dei dati e se supporta mono o stereo.

Per esempi correlati a video relativi a GetStreamCaps, vedere [Funzionalità video.](video-capabilities.md)

Si supponga di supportare il formato d'onda PCM (Pulse Code Modulation), come rappresentato dalla struttura [**WAVEFORMATEX,**](/previous-versions/dd757713(v=vs.85)) a frequenze di campionamento di 11.025, 22.050 e 44.100 campioni al secondo, il tutto con mono o stereo a 8 o 16 bit. In questo caso, si offrono due coppie di strutture. La prima coppia avrebbe una struttura di funzionalità DI CONFIGURAZIONE FLUSSO AUDIO che indica che sono supportati da un minimo di 11.025 a un massimo di 22.050 campioni al secondo con una granularità di 11.025 campioni al secondo (la granularità è la differenza tra i valori supportati); da un minimo di 8 bit a un numero massimo di bit a 16 bit per campione con una granularità di 8 bit per campione; e minimo di un canale e massimo di due canali. **\_ \_ \_** Il tipo di supporto della prima coppia sarebbe il formato PCM predefinito in tale intervallo, ad esempio 22 kilohertz (kHz), stereo a 16 bit. La seconda coppia è una funzionalità che mostra 44.100 campioni minimi e massimi al secondo. Bit a 8 bit (minimo) e 16 bit (massimo) per campione, con una granularità di 8 bit per campione; e minimo di un canale e massimo di due canali. Il tipo di supporto è il formato predefinito a 44 kHz, ad esempio stereo a 44 kHz a 16 bit.

Se si supportano formati d'onda non PCM, il tipo di supporto restituito da questo metodo può mostrare quali formati non PCM sono supportati (con una frequenza di campionamento, una velocità in bit e canali predefiniti) e la struttura delle funzionalità che accompagna tale tipo di supporto può descrivere quali altre frequenze di campionamento, velocità in bit e canali supportati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esposizione di formati di acquisizione e compressione](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
