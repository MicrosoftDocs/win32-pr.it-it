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
# <a name="audio-capabilities"></a><span data-ttu-id="7648b-103">Funzionalità audio</span><span class="sxs-lookup"><span data-stu-id="7648b-103">Audio Capabilities</span></span>

<span data-ttu-id="7648b-104">Per le funzionalità audio, [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) restituisce una matrice di coppie di strutture di [**\_ \_ tipo multimediale am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e di [**\_ \_ configurazione \_ del flusso audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="7648b-104">For audio capabilities, [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns an array of pairs of [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) and [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structures.</span></span> <span data-ttu-id="7648b-105">Come per i video, è possibile usarlo per esporre tutti i tipi di funzionalità audio sul pin, ad esempio la velocità dei dati e se supporta mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="7648b-105">As with video, you can use this to expose all kinds of audio capabilities on the pin, such as data rate and whether it supports mono or stereo.</span></span>

<span data-ttu-id="7648b-106">Per esempi correlati ai video relativi a GetStreamCaps, vedere [funzionalità video](video-capabilities.md).</span><span class="sxs-lookup"><span data-stu-id="7648b-106">For video-related examples relating to GetStreamCaps, see [Video Capabilities](video-capabilities.md).</span></span>

<span data-ttu-id="7648b-107">Si supponga di supportare il formato Wave Pulse Code Modulation (PCM), come rappresentato dalla struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , a frequenze di campionamento di 11.025, 22.050 e 44.100 campioni al secondo, tutti a 8 o a 16 bit mono o stereo.</span><span class="sxs-lookup"><span data-stu-id="7648b-107">Suppose you support pulse code modulation (PCM) wave format (as represented by the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure) at sampling rates of 11,025, 22,050, and 44,100 samples per second, all at 8- or 16-bit mono or stereo.</span></span> <span data-ttu-id="7648b-108">In questo caso, sono disponibili due coppie di strutture.</span><span class="sxs-lookup"><span data-stu-id="7648b-108">In this case, you would offer two pairs of structures.</span></span> <span data-ttu-id="7648b-109">La prima coppia avrebbe una struttura di funzionalità per i **\_ \_ \_ tappi di configurazione del flusso audio** che indica il supporto di un minimo di 11.025 a un massimo di 22.050 campioni al secondo con una granularità di 11.025 campioni al secondo (la granularità è la differenza tra i valori supportati); un valore minimo a 8 bit per un numero massimo di bit a 16 bit per campione con una granularità di 8 bit per campione e un massimo di un canale minimo e un massimo di due canali.</span><span class="sxs-lookup"><span data-stu-id="7648b-109">The first pair would have an **AUDIO\_STREAM\_CONFIG\_CAPS** capability structure saying you support a minimum of 11,025 to a maximum of 22,050 samples per second with a granularity of 11,025 samples per second (granularity is the difference between supported values); an 8-bit minimum to a 16-bit maximum bits per sample with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="7648b-110">Il tipo di supporto della prima coppia sarà il formato PCM predefinito in tale intervallo, forse 22 kilohertz (kHz), stereo a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="7648b-110">The first pair's media type would be your default PCM format in that range, perhaps 22 kilohertz (kHz), 16-bit stereo.</span></span> <span data-ttu-id="7648b-111">La seconda coppia sarebbe una funzionalità che mostra 44.100 per i campioni minimo e massimo al secondo; bit a 8 bit (minimo) e a 16 bit (massimo) per campione, con una granularità di 8 bit per campione; e il valore massimo a un canale minimo e a due canali.</span><span class="sxs-lookup"><span data-stu-id="7648b-111">Your second pair would be a capability showing 44,100 for both minimum and maximum samples per second; 8-bit (minimum) and 16-bit (maximum) bits per sample, with a granularity of 8 bits per sample; and one-channel minimum and two-channel maximum.</span></span> <span data-ttu-id="7648b-112">Il tipo di supporto sarà il formato 44 kHz predefinito, ad esempio stereo a 16 bit 44 kHz.</span><span class="sxs-lookup"><span data-stu-id="7648b-112">The media type would be your default 44 kHz format, perhaps 44 kHz 16-bit stereo.</span></span>

<span data-ttu-id="7648b-113">Se si supportano formati Wave non PCM, il tipo di supporto restituito da questo metodo consente di visualizzare i formati non PCM supportati (con una frequenza di campionamento predefinita, velocità in bit e canali) e la struttura delle funzionalità associata a tale tipo di supporto può descrivere le altre frequenze di campionamento, velocità in bit e canali supportati.</span><span class="sxs-lookup"><span data-stu-id="7648b-113">If you support non-PCM wave formats, the media type returned by this method can show which non-PCM formats you support (with a default sample rate, bit rate, and channels) and the capabilities structure accompanying that media type can describe which other sample rates, bit rates, and channels you support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7648b-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7648b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7648b-115">Esposizione dei formati di acquisizione e compressione</span><span class="sxs-lookup"><span data-stu-id="7648b-115">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
</dt> </dl>

 

 
