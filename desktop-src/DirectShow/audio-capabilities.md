---
description: Funzionalità audio
ms.assetid: de96f6ee-b526-4ac2-93ac-a731f86ef5d5
title: Funzionalità audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2cf02927b69d807f400c4185a7d4ddbdd14322
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522529"
---
# <a name="audio-capabilities"></a>Funzionalità audio

Per le funzionalità audio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) restituisce una matrice di coppie di strutture di [**\_ \_ tipo multimediale am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e di [**\_ \_ configurazione \_ del flusso audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) . Come per i video, è possibile usarlo per esporre tutti i tipi di funzionalità audio sul pin, ad esempio la velocità dei dati e se supporta mono o stereo.

Per esempi correlati ai video relativi a GetStreamCaps, vedere [funzionalità video](video-capabilities.md).

Si supponga di supportare il formato Wave Pulse Code Modulation (PCM), come rappresentato dalla struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , a frequenze di campionamento di 11.025, 22.050 e 44.100 campioni al secondo, tutti a 8 o a 16 bit mono o stereo. In questo caso, sono disponibili due coppie di strutture. La prima coppia avrebbe una struttura di funzionalità per i **\_ \_ \_ tappi di configurazione del flusso audio** che indica il supporto di un minimo di 11.025 a un massimo di 22.050 campioni al secondo con una granularità di 11.025 campioni al secondo (la granularità è la differenza tra i valori supportati); un valore minimo a 8 bit per un numero massimo di bit a 16 bit per campione con una granularità di 8 bit per campione e un massimo di un canale minimo e un massimo di due canali. Il tipo di supporto della prima coppia sarà il formato PCM predefinito in tale intervallo, forse 22 kilohertz (kHz), stereo a 16 bit. La seconda coppia sarebbe una funzionalità che mostra 44.100 per i campioni minimo e massimo al secondo; bit a 8 bit (minimo) e a 16 bit (massimo) per campione, con una granularità di 8 bit per campione; e il valore massimo a un canale minimo e a due canali. Il tipo di supporto sarà il formato 44 kHz predefinito, ad esempio stereo a 16 bit 44 kHz.

Se si supportano formati Wave non PCM, il tipo di supporto restituito da questo metodo consente di visualizzare i formati non PCM supportati (con una frequenza di campionamento predefinita, velocità in bit e canali) e la struttura delle funzionalità associata a tale tipo di supporto può descrivere le altre frequenze di campionamento, velocità in bit e canali supportati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esposizione dei formati di acquisizione e compressione](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
