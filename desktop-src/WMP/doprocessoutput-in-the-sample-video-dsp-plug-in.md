---
title: DoProcessOutput nel plug-in DSP video di esempio
description: DoProcessOutput nel plug-in DSP video di esempio
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Windows Media Player plug-in, DSP video
- plug-in, DSP video
- plug-in di elaborazione del segnale digitale,DoProcessOutput
- plug-in DSP,DoProcessOutput
- plug-in DSP video,DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b031ecddc4f7a1e4a83d4f8a7d8db3b975957789d7f887bf8b12438407624205
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680601"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a>DoProcessOutput nel plug-in DSP video di esempio

Poiché un plug-in DSP video supporta in genere diversi formati video, è utile separare il codice di implementazione dell'elaborazione in una funzione separata per ogni formato. Ciò significa che l'implementazione **di DoProcessOutput per** i plug-in DSP video è relativamente semplice.

L'implementazione nel plug-in di esempio verifica innanzitutto se l'utente ha abilitato il plug-in. Se il plug-in è disabilitato, il codice copia i dati forniti nel buffer di input nel buffer di output senza modificarlo, come illustrato nel codice seguente:


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



Se il plug-in è abilitato, il codice esegue semplicemente  una serie di controlli sul membro del sottotipo del tipo di supporto di input per determinare il formato video corrente. Quando viene trovata una corrispondenza, il codice chiama la funzione di elaborazione appropriata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP video**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




