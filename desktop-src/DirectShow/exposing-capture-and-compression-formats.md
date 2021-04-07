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
# <a name="exposing-capture-and-compression-formats"></a>Esposizione dei formati di acquisizione e compressione

Questo articolo descrive come restituire formati di acquisizione e compressione usando il metodo [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Questo metodo può ottenere altre informazioni sui tipi di supporto accettati rispetto al modo tradizionale di enumerare i tipi di supporto di un PIN, quindi deve essere in genere usato. **GetStreamCaps** può restituire informazioni sui tipi di formati consentiti per audio o video. Questo articolo fornisce inoltre un codice di esempio che illustra come riconnettere il pin di input di un filtro di trasformazione per assicurarsi che il filtro possa produrre un determinato output.

Il metodo **GetStreamCaps** restituisce una matrice di coppie di strutture di tipi e funzionalità di supporti. Il tipo di supporto è una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) e le funzionalità sono rappresentate da una struttura di [**Caps di \_ configurazione del flusso \_ \_ audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) o da una struttura di [**Caps di \_ configurazione del flusso \_ \_ video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . La prima sezione di questo articolo presenta un esempio di video e il secondo presenta un esempio di audio.

Questo articolo contiene gli argomenti seguenti:

-   [Funzionalità video](video-capabilities.md)
-   [Funzionalità audio](audio-capabilities.md)
-   [Riconnessione dell'input per garantire tipi di output specifici](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



