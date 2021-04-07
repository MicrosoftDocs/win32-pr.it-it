---
description: Esposizione dei formati di acquisizione e compressione
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Esposizione dei formati di acquisizione e compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02051d9e68b3ad919b96dca53b674305787b3186
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747639"
---
# <a name="exposing-capture-and-compression-formats"></a><span data-ttu-id="bbe59-103">Esposizione dei formati di acquisizione e compressione</span><span class="sxs-lookup"><span data-stu-id="bbe59-103">Exposing Capture and Compression Formats</span></span>

<span data-ttu-id="bbe59-104">Questo articolo descrive come restituire formati di acquisizione e compressione usando il metodo [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) .</span><span class="sxs-lookup"><span data-stu-id="bbe59-104">This article describes how to return capture and compression formats by using the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="bbe59-105">Questo metodo può ottenere altre informazioni sui tipi di supporto accettati rispetto al modo tradizionale di enumerare i tipi di supporto di un PIN, quindi deve essere in genere usato.</span><span class="sxs-lookup"><span data-stu-id="bbe59-105">This method can get more information about accepted media types than the traditional way of enumerating a pin's media types, so it should typically be used instead.</span></span> <span data-ttu-id="bbe59-106">**GetStreamCaps** può restituire informazioni sui tipi di formati consentiti per audio o video.</span><span class="sxs-lookup"><span data-stu-id="bbe59-106">**GetStreamCaps** can return information about the kinds of formats allowed for audio or video.</span></span> <span data-ttu-id="bbe59-107">Questo articolo fornisce inoltre un codice di esempio che illustra come riconnettere il pin di input di un filtro di trasformazione per assicurarsi che il filtro possa produrre un determinato output.</span><span class="sxs-lookup"><span data-stu-id="bbe59-107">Additionally, this article provides some sample code that demonstrates how to reconnect the input pin of a transform filter to ensure your filter can produce a particular output.</span></span>

<span data-ttu-id="bbe59-108">Il metodo **GetStreamCaps** restituisce una matrice di coppie di strutture di tipi e funzionalità di supporti.</span><span class="sxs-lookup"><span data-stu-id="bbe59-108">The **GetStreamCaps** method returns an array of pairs of media type and capabilities structures.</span></span> <span data-ttu-id="bbe59-109">Il tipo di supporto è una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e le funzionalità sono rappresentate da una struttura di [**Caps di \_ configurazione del flusso \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) o da una struttura di [**Caps di \_ configurazione del flusso \_ \_ video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) .</span><span class="sxs-lookup"><span data-stu-id="bbe59-109">The media type is an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure and the capabilities are represented either by an [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure or a [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure.</span></span> <span data-ttu-id="bbe59-110">La prima sezione di questo articolo presenta un esempio di video e il secondo presenta un esempio di audio.</span><span class="sxs-lookup"><span data-stu-id="bbe59-110">The first section in this article presents a video example and the second presents an audio example.</span></span>

<span data-ttu-id="bbe59-111">Questo articolo contiene gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbe59-111">This article contains the following topics:</span></span>

-   [<span data-ttu-id="bbe59-112">Funzionalità video</span><span class="sxs-lookup"><span data-stu-id="bbe59-112">Video Capabilities</span></span>](video-capabilities.md)
-   [<span data-ttu-id="bbe59-113">Funzionalità audio</span><span class="sxs-lookup"><span data-stu-id="bbe59-113">Audio Capabilities</span></span>](audio-capabilities.md)
-   [<span data-ttu-id="bbe59-114">Riconnessione dell'input per garantire tipi di output specifici</span><span class="sxs-lookup"><span data-stu-id="bbe59-114">Reconnecting Your Input to Ensure Specific Output Types</span></span>](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a><span data-ttu-id="bbe59-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbe59-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe59-116">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="bbe59-116">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



