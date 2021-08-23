---
description: Esposizione di formati di acquisizione e compressione
ms.assetid: f7466cfe-b13e-4ee9-82f9-0528ed97bf99
title: Esposizione di formati di acquisizione e compressione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80821ade82b894a7c3e2752528ffdd72bc2223a4616b629f7e2b236461b31e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685741"
---
# <a name="exposing-capture-and-compression-formats"></a>Esposizione di formati di acquisizione e compressione

Questo articolo descrive come restituire i formati di acquisizione e compressione usando il [**metodo IAMStreamConfig::GetStreamCaps.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) Questo metodo può ottenere più informazioni sui tipi di supporti accettati rispetto al metodo tradizionale di enumerazione dei tipi di supporti di un pin, pertanto in genere deve essere usato. **GetStreamCaps può** restituire informazioni sui tipi di formati consentiti per audio o video. Questo articolo include anche codice di esempio che illustra come riconnettere il pin di input di un filtro di trasformazione per garantire che il filtro possa produrre un output specifico.

Il **metodo GetStreamCaps** restituisce una matrice di coppie di strutture di tipo di supporto e funzionalità. Il tipo di supporto è una [**struttura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) e le funzionalità sono rappresentate da una struttura [**AUDIO STREAM CONFIG \_ \_ \_ CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) o da una [**struttura VIDEO STREAM CONFIG \_ \_ \_ CAPS.**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) La prima sezione di questo articolo presenta un esempio video e la seconda presenta un esempio audio.

Questo articolo contiene gli argomenti seguenti:

-   [Funzionalità video](video-capabilities.md)
-   [Funzionalità audio](audio-capabilities.md)
-   [Riconnessione dell'input per garantire tipi di output specifici](reconnecting-your-input-to-ensure-specific-output-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



