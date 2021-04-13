---
title: Informazioni sul plug-in audio DSP di esempio
description: Informazioni sul plug-in audio DSP di esempio
ms.assetid: e60b055b-77e6-470e-91f6-9882827cf238
keywords:
- Plug-in di Windows Media Player, esempi
- plug-in, esempi
- plug-in di elaborazione dei segnali digitali, esempi
- Plug-in DSP, esempi
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, esempi di audio
- Plug-in DSP, esempi di audio
- esempi, plug-in DSP
- plug-in audio DSP, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0edc3a5860c0c52837bfece16d2e709bf16d836d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330111"
---
# <a name="about-the-sample-audio-dsp-plug-in"></a>Informazioni sul plug-in audio DSP di esempio

Il plug-in audio DSP di esempio fornisce una semplice implementazione di elaborazione che ridimensiona l'ampiezza dell'audio in base a un fattore fornito dall'utente nella pagina delle proprietà. Il plug-in accetta valori compresi tra 0 e 1. Il valore predefinito è 1. Il valore 1 non ha alcun effetto sul suono; altri fattori di scala sono moltiplicatori per gli esempi audio. Ad esempio, un valore di 0,5 comporterebbe una riduzione di 6 decibel nel volume. Il valore zero restituisce il silenzio.

Il plug-in audio DSP di esempio funziona con audio stereo o mono PCM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un plug-in DSP**](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




