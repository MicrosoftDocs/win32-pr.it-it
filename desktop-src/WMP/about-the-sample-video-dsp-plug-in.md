---
title: Informazioni sul plug-in DSP video di esempio
description: Informazioni sul plug-in DSP video di esempio
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Windows Media Player plug-in, esempi
- plug-in, esempi
- plug-in di elaborazione del segnale digitale, esempi
- plug-in DSP, esempi
- Windows Media Player plug-in, DSP video
- plug-in, DSP video
- plug-in di elaborazione dei segnali digitali, esempi di video
- plug-in DSP, esempi video
- esempi, plug-in DSP
- plug-in video DSP,esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb771bb87ffb53cf46022fc17ee2588e7cdac0b6b2c821f98fe6cf86799434c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470251"
---
# <a name="about-the-sample-video-dsp-plug-in"></a>Informazioni sul plug-in DSP video di esempio

Il plug-in DSP video di esempio fornisce una semplice implementazione di elaborazione che ridimensiona la saturazione dei colori del video in base a un fattore fornito dall'utente nella pagina delle proprietà. Il plug-in accetta valori compresi tra zero e 1. Il valore predefinito è 1. Il valore 1 non ha alcun effetto sull'immagine video. altri fattori di scala desaturano il colore dell'immagine. Ad esempio, un valore pari a 0,5 comporta una saturazione del colore del 50%. Il valore zero restituisce un video in scala di grigi.

Il plug-in DSP video di esempio funziona con i formati video seguenti:

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

[**Compilazione di un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




