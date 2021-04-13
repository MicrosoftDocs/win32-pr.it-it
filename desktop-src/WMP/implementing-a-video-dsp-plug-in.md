---
title: Implementazione di un plug-in video DSP
description: Implementazione di un plug-in video DSP
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in di elaborazione dei segnali digitali, implementazione del codice
- Plug-in DSP, implementazione del codice
- plug-in di elaborazione dei segnali digitali, modifica del codice di esempio
- Plug-in DSP, modifica del codice di esempio
- plug-in per l'elaborazione di segnali digitali, implementazione video
- Plug-in DSP, implementazione video
- plug-in di video DSP, implementazione del codice
- plug-in di video DSP, modifica del codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330436"
---
# <a name="implementing-a-video-dsp-plug-in"></a>Implementazione di un plug-in video DSP

Gli adapter per la visualizzazione video del computer supportano un set di formati video. I codec video digitali supportano anche un set di formati video. Quando si tenta di riprodurre un file video specifico, Windows Media Player deve scegliere un formato da usare per il rendering. Il lettore tenta di trovare la migliore corrispondenza tra i formati supportati dal codec video e i formati supportati dalla scheda video video, ovvero quello che produce la qualità più elevata.

Per creare un plug-in di Windows Media Player DSP che elabora il video, è necessario innanzitutto decidere quali formati video si desidera vengano elaborati dal plug-in. Il plug-in video DSP di esempio funziona con i formati video seguenti:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

I formati scelti per l'elaborazione dipende dall'utente. È possibile rimuovere i formati dal plug-in di esempio in modo che non siano più supportati ed è possibile aggiungere codice per elaborare formati aggiuntivi.

Le sezioni seguenti forniscono informazioni aggiuntive che è necessario tenere presente prima di creare il plug-in video DSP per Windows Media Player:

-   [Negoziazione del formato video nel plug-in DSP video di esempio](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [DoProcessOutput nel plug-in di video DSP di esempio](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [Elaborazione del video](processing-the-video.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice DSP**](implementing-your-dsp-code.md)
</dt> </dl>

 

 




