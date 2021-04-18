---
title: Informazioni sul plug-in DSP video di esempio
description: Informazioni sul plug-in DSP video di esempio
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Plug-in di Windows Media Player, esempi
- plug-in, esempi
- plug-in di elaborazione dei segnali digitali, esempi
- Plug-in DSP, esempi
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, esempi video
- Plug-in DSP, esempi video
- esempi, plug-in DSP
- plug-in di video DSP, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297825"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>Informazioni sul plug-in DSP video di esempio

Il plug-in video DSP di esempio fornisce una semplice implementazione di elaborazione che consente di ridimensionare la saturazione dei colori del video in base a un fattore fornito dall'utente nella pagina delle proprietà. Il plug-in accetta valori compresi tra 0 e 1. Il valore predefinito è 1. Il valore 1 non ha alcun effetto sull'immagine video; altri fattori di scala desaturano il colore dell'immagine. Ad esempio, un valore di 0,5 comporterà una saturazione di colore del 50%. Il valore zero restituisce il video in scala di grigi.

Il plug-in video DSP di esempio funziona con i formati video seguenti:

-   NV12
-   YV12
-   YUY2
-   UYVY
-   RGB32
-   RGB24
-   RGB555
-   RGB565

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




