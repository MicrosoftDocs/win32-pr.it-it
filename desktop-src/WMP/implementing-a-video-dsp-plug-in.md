---
title: Implementazione di un plug-in DSP video
description: Implementazione di un plug-in DSP video
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player plug-in, DSP video
- plug-in, DSP video
- plug-in di elaborazione del segnale digitale, implementazione di codice
- plug-in DSP, implementazione di codice
- plug-in di elaborazione del segnale digitale, modifica del codice di esempio
- plug-in DSP, modifica del codice di esempio
- plug-in per l'elaborazione di segnali digitali, implementazione di video
- Plug-in DSP, implementazione video
- plug-in DSP video, implementazione di codice
- plug-in DSP video, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4afdbabd36167c11ef7c1c57aeccb475605f9365c550c572422af3440d760ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135704"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementazione di un plug-in DSP video

Le schede video del computer supportano un set di formati video. I codec video digitali supportano anche un set di formati video. Quando si tenta di riprodurre un file video specifico, Windows Media Player scegliere un formato da usare per il rendering. Il lettore tenta di trovare la corrispondenza migliore tra i formati supportati dal codec video e i formati supportati dalla scheda di visualizzazione video, ovvero quella che produce la massima qualità.

Per creare un plug-in DSP Windows Media Player che elabora i video, è prima di tutto necessario decidere quali formati video si desidera elaborare. Il plug-in DSP video di esempio funziona con i formati video seguenti:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

I formati che si sceglie di elaborare sono a scelta dell'utente. È possibile rimuovere i formati dal plug-in di esempio in modo che non siano più supportati ed è possibile aggiungere codice per elaborare altri formati.

Le sezioni seguenti forniscono informazioni aggiuntive da conoscere prima di creare un plug-in DSP video personalizzato per Windows Media Player:

-   [Negoziazione del formato video nel plug-in DSP video di esempio](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput nel plug-in DSP video di esempio](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Elaborazione del video](processing-the-video.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




