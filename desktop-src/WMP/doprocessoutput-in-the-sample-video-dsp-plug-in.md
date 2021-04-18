---
title: DoProcessOutput nel plug-in di video DSP di esempio
description: DoProcessOutput nel plug-in di video DSP di esempio
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, DoProcessOutput
- Plug-in DSP, DoProcessOutput
- plug-in DSP video, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297877"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput nel plug-in di video DSP di esempio

Poiché un plug-in video DSP supporta in genere diversi formati video, è opportuno separare il codice di implementazione dell'elaborazione in una funzione separata per ogni formato. Ciò significa che l'implementazione di **DoProcessOutput** per i plug-in di video DSP è relativamente semplice.

L'implementazione nel plug-in di esempio verifica innanzitutto se l'utente ha abilitato il plug-in. Se il plug-in è disabilitato, il codice copia i dati forniti nel buffer di input nel buffer di output senza modificarli, come illustrato nel codice seguente:


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



Se il plug-in è abilitato, il codice esegue semplicemente una serie di controlli sul membro del **sottotipo** di Media Type di input per determinare il formato video corrente. Quando viene trovata una corrispondenza, il codice chiama la funzione di elaborazione appropriata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in video DSP**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




